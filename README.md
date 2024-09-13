Inheritance and Access Specifiers
This C++ program showcases the concept of inheritance along with the use of access specifiers (private, protected, and public) in class design. The program defines a base class called Base that contains members with different access levels: private, protected, and public. Three derived classes—Derived_Private, Derived_Protected, and Derived_Public—are used to inherit from Base using private, protected, and public inheritance, respectively.

Compilation Errors
The program deliberately tries to access private and protected members of the Base class from its derived classes, leading to compilation errors. The errors are as follows:

error: 'int Base::secret' is private – This error arises when trying to access the private member secret from a derived class.

Explanation: Private members cannot be accessed by derived classes, no matter the type of inheritance.
error: 'int Base::protect' is protected – This error occurs when the derived class attempts to access the protected member protect using private inheritance.

Explanation: Protected members are not accessible through private inheritance.
error: 'int Base::access' is public but inaccessible due to private inheritance – This error happens when the public member access is accessed from Derived_Private due to private inheritance.

Explanation: Public members become inaccessible when inherited privately.
Explanation
Private members (secret) are not accessible from derived classes, regardless of the inheritance type.
Protected members (protect) can only be accessed by derived classes through protected or public inheritance, not private inheritance.
Public members (access) are accessible through public inheritance, but not via private inheritance.
