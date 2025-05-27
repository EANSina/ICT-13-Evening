ក្រោមនេះជាការរៀបចំលម្អិតសម្រាប់គម្រោង C++ ដែលផ្ដោតលើផ្នែកនីមួយៗ ដូចតារាងដែលអ្នកបានផ្ដល់។ ខាងក្រោមនេះសរុប Diagram និង Code ដែលត្រូវបង្ហាញ:

---

### **1.1 ការវិភាគតម្រូវការ (Requirement Analysis)**

**✅ Diagram & Tables: UML + តារាង**

#### 🔹 តារាងតម្រូវការមូលដ្ឋាន (Requirement Table)

| ល.រ | តម្រូវការ                 | ប្រភេទ         | សេចក្តីពិពណ៌នា                 |
| --- | ------------------------- | -------------- | ------------------------------ |
| 1   | បង្កើតគណនេយ្យអ្នកប្រើ     | Functional     | អ្នកប្រើអាចចុះឈ្មោះ និងចូលប្រើ |
| 2   | ប្រព័ន្ធគ្រប់គ្រងទិន្នន័យ | Functional     | អាចបញ្ចូល/កែសម្រួល/លុបទិន្នន័យ |
| 3   | Report & Export           | Non-functional | បង្កើត PDF/CSV Report បាន      |

#### 🔹 Diagram: Use Case Diagram

```
        +----------------+
        |     User       |
        +----------------+
         /        |        \
Login/Register  Manage Data  Export Report
```

---

### **1.2 ស្ថាបត្យកម្មគម្រោង (Architecture)**

**✅ Diagram UML**

#### 🔹 UML Use Case Diagram:

* ចូលប្រើ
* គ្រប់គ្រងទិន្នន័យ
* បង្ហាញរបាយការណ៍

#### 🔹 UML Class Diagram:

```plaintext
+----------------+
|    User        |
+----------------+
| -username      |
| -password      |
+----------------+
| +login()       |
| +register()    |
+----------------+

+----------------+
|   DataManager  |
+----------------+
| -dataList      |
+----------------+
| +addData()     |
| +editData()    |
| +deleteData()  |
+----------------+
```

---

### **1.3 គំរូការរចនាក្នុង C++**

**✅ មានកូដ & MVC**

#### 🔹 MVC Model Structure (Simplified):

```cpp
// Model
class User {
    string username, password;
public:
    User(string u, string p) : username(u), password(p) {}
    bool login();
};

// Controller
class UserController {
    User user;
public:
    void processLogin(string u, string p);
};

// View
void showLoginPage() {
    cout << "Enter username and password: ";
}
```

---

### **1.4 ការរៀបចំគម្រោង (Planning)**

**✅ Diagram/Chart**

#### 🔹 Gantt Chart Example:

| ការងារ      | ថ្ងៃទីចាប់ផ្ដើម | ថ្ងៃបញ្ចប់ | ចំណាំ     |
| ----------- | --------------- | ---------- | --------- |
| Requirement | 01-Jan          | 05-Jan     | 5ថ្ងៃ     |
| Design      | 06-Jan          | 10-Jan     | UML       |
| Coding      | 11-Jan          | 20-Jan     | C++       |
| Testing     | 21-Jan          | 25-Jan     | Unit Test |

---

### **2.1 ការសរសេរកូដនិងអនុវត្ត (Implementation)**

**✅ មានកូដពេញលេញ**

#### 🔹 Main Program Example:

```cpp
#include <iostream>
#include <vector>
using namespace std;

class User {
    string username;
public:
    User(string u) : username(u) {}
    void display() { cout << "User: " << username << endl; }
};

int main() {
    vector<User> users;
    users.push_back(User("admin"));
    for (auto& user : users)
        user.display();
    return 0;
}
```

---

### **2.2 ការធ្វើតេស្ត និង Debugging**

**✅ Test Case & Debug**

#### 🔹 Test Case:

| Test Case ID | Input           | Output       | Status |
| ------------ | --------------- | ------------ | ------ |
| TC01         | Username: admin | Display user | Pass   |

#### 🔹 Debug Example:

```cpp
cout << "Debug: User added = " << username << endl;
```

---

### **2.3 ការកត់ត្រាឯកសារ (Documentation)**

**✅ Files & Description**

* `README.md`: ពន្យល់អំពីគម្រោង
* `API.md`: Function Description
* `log.txt`: កំណត់ត្រាព័ត៌មាន commit Git

---

### **2.4 ការបង្ហាញគម្រោង (Presentation)**

**✅ Slide & Demo**

* PowerPoint: ផ្តល់ UML Diagram, កូដ, Results
* Video Demo: របៀបដំណើរការគម្រោង
* Group Code Review: បង្ហាញ Class structure និង logic

---

បើអ្នកចង់បានឯកសារជា Word, PDF, ឬ PowerPoint សម្រាប់បង្ហាញសិស្ស ឬពិនិត្យសម្រេច គ្រាន់បញ្ជាក់ខ្ញុំអាចរៀបចំឲ្យបាន។
