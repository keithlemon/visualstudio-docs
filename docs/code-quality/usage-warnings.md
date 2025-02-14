---
title: Usage Warnings
ms.date: 11/04/2016
ms.topic: reference
f1_keywords:
  - "vs.codeanalysis.usagerules"
helpviewer_keywords:
  - "warnings, usage"
  - "managed code analysis warnings, usage warnings"
  - "usage warnings"
ms.assetid: fe7dc2a3-289d-4bf7-a1e4-0947a81287c4
author: gewarren
ms.author: gewarren
manager: jillfra
ms.workload:
  - "multiple"
---
# Usage Warnings

Usage warnings support proper usage of .NET.

## In This Section

|Rule|Description|
|----------|-----------------|
|[CA1801: Review unused parameters](../code-quality/ca1801-review-unused-parameters.md)|A method signature includes a parameter that is not used in the method body.|
|[CA1806: Do not ignore method results](../code-quality/ca1806-do-not-ignore-method-results.md)|A new object is created but never used; or a method that creates and returns a new string is called and the new string is never used; or a COM or P/Invoke method returns an HRESULT or error code that is never used.|
|[CA1816: Call GC.SuppressFinalize correctly](../code-quality/ca1816-call-gc-suppressfinalize-correctly.md)|A method that is an implementation of Dispose does not call GC.SuppressFinalize; or a method that is not an implementation of Dispose calls GC.SuppressFinalize; or a method calls GC.SuppressFinalize and passes something other than this (Me in Visual Basic).|
|[CA2200: Rethrow to preserve stack details](../code-quality/ca2200-rethrow-to-preserve-stack-details.md)|An exception is rethrown and the exception is explicitly specified in the throw statement. If an exception is rethrown by specifying the exception in the throw statement, the list of method calls between the original method that threw the exception and the current method is lost.|
|[CA2201: Do not raise reserved exception types](../code-quality/ca2201-do-not-raise-reserved-exception-types.md)|This makes the original error hard to detect and debug.|
|[CA2202: Do not dispose objects multiple times](../code-quality/ca2202-do-not-dispose-objects-multiple-times.md)|A method implementation contains code paths that could cause multiple calls to System.IDisposable.Dispose or a Dispose equivalent (such as a Close() method on some types) on the same object.|
|[CA2204: Literals should be spelled correctly](../code-quality/ca2204-literals-should-be-spelled-correctly.md)|A literal string in a method body contains one or more words that are not recognized by the Microsoft spelling checker library.|
|[CA2205: Use managed equivalents of Win32 API](../code-quality/ca2205-use-managed-equivalents-of-win32-api.md)|A platform invoke method is defined and a .NET method with the equivalent functionality is available.|
|[CA2207: Initialize value type static fields inline](../code-quality/ca2207-initialize-value-type-static-fields-inline.md)|A value type declares an explicit static constructor. To fix a violation of this rule, initialize all static data when it is declared and remove the static constructor.|
|[CA2208: Instantiate argument exceptions correctly](../code-quality/ca2208-instantiate-argument-exceptions-correctly.md)|A call is made to the default (parameterless) constructor of an exception type that is or derives from ArgumentException, or an incorrect string argument is passed to a parameterized constructor of an exception type that is or derives from ArgumentException.|
|[CA2211: Non-constant fields should not be visible](../code-quality/ca2211-non-constant-fields-should-not-be-visible.md)|Static fields that are not constants or read-only are not thread-safe. Access to such a field must be carefully controlled and requires advanced programming techniques for synchronizing access to the class object.|
|[CA2212: Do not mark serviced components with WebMethod](../code-quality/ca2212-do-not-mark-serviced-components-with-webmethod.md)|A method in a type that inherits from System.EnterpriseServices.ServicedComponent is marked with System.Web.Services.WebMethodAttribute. Because WebMethodAttribute and a ServicedComponent method have conflicting behavior and requirements for context and transaction flow, the behavior of the method will be incorrect in some scenarios.|
|[CA2213: Disposable fields should be disposed](../code-quality/ca2213-disposable-fields-should-be-disposed.md)|A type that implements System.IDisposable declares fields that are of types that also implement IDisposable. The Dispose method of the field is not called by the Dispose method of the declaring type.|
|[CA2214: Do not call overridable methods in constructors](../code-quality/ca2214-do-not-call-overridable-methods-in-constructors.md)|When a constructor calls a virtual method, it is possible that the constructor for the instance that invokes the method has not executed.|
|[CA2215: Dispose methods should call base class dispose](../code-quality/ca2215-dispose-methods-should-call-base-class-dispose.md)|If a type inherits from a disposable type, it must call the Dispose method of the base type from its own Dispose method.|
|[CA2216: Disposable types should declare finalizer](../code-quality/ca2216-disposable-types-should-declare-finalizer.md)|A type that implements System.IDisposable, and has fields that suggest the use of unmanaged resources, does not implement a finalizer as described by Object.Finalize.|
|[CA2217: Do not mark enums with FlagsAttribute](../code-quality/ca2217-do-not-mark-enums-with-flagsattribute.md)|An externally visible enumeration is marked with FlagsAttribute, and it has one or more values that are not powers of two or a combination of the other defined values on the enumeration.|
|[CA2218: Override GetHashCode on overriding Equals](../code-quality/ca2218-override-gethashcode-on-overriding-equals.md)|GetHashCode returns a value, based on the current instance, that is suited for hashing algorithms and data structures such as a hash table. Two objects that are the same type and are equal must return the same hash code.|
|[CA2219: Do not raise exceptions in exception clauses](../code-quality/ca2219-do-not-raise-exceptions-in-exception-clauses.md)|When an exception is raised in a finally or fault clause, the new exception hides the active exception. When an exception is raised in a filter clause, the run time silently catches the exception. This makes the original error hard to detect and debug.|
|[CA2220: Finalizers should call base class finalizer](../code-quality/ca2220-finalizers-should-call-base-class-finalizer.md)|Finalization must be propagated through the inheritance hierarchy. To guarantee this, types must call their base class Finalize method in their own Finalize method.|
|[CA2221: Finalizers should be protected](../code-quality/ca2221-finalizers-should-be-protected.md)|Finalizers must use the family access modifier.|
|[CA2222: Do not decrease inherited member visibility](../code-quality/ca2222-do-not-decrease-inherited-member-visibility.md)|Don't change the access modifier for inherited members. Changing an inherited member to private does not prevent callers from accessing the base class implementation of the method.|
|[CA2223: Members should differ by more than return type](../code-quality/ca2223-members-should-differ-by-more-than-return-type.md)|Although the common language runtime allows the use of return types to differentiate between otherwise identical members, this feature is not in the Common Language Specification, nor is it a common feature of .NET programming languages.|
|[CA2224: Override equals on overloading operator equals](../code-quality/ca2224-override-equals-on-overloading-operator-equals.md)|A public type implements the equality operator, but does not override Object.Equals.|
|[CA2225: Operator overloads have named alternates](../code-quality/ca2225-operator-overloads-have-named-alternates.md)|An operator overload was detected, and the expected named alternative method was not found. The named alternative member provides access to the same functionality as the operator, and is provided for developers who program in languages that do not support overloaded operators.|
|[CA2226: Operators should have symmetrical overloads](../code-quality/ca2226-operators-should-have-symmetrical-overloads.md)|A type implements the equality or inequality operator, and does not implement the opposite operator.|
|[CA2227: Collection properties should be read only](../code-quality/ca2227-collection-properties-should-be-read-only.md)|A writable collection property allows a user to replace the collection with a different collection. A read-only property stops the collection from being replaced but still allows the individual members to be set.|
|[CA2228: Do not ship unreleased resource formats](../code-quality/ca2228-do-not-ship-unreleased-resource-formats.md)|Resource files that were built by using pre-release versions of the .NET Framework might not be usable by supported versions of the .NET Framework.|
|[CA2229: Implement serialization constructors](../code-quality/ca2229-implement-serialization-constructors.md)|To fix a violation of this rule, implement the serialization constructor. For a sealed class, make the constructor private; otherwise, make it protected.|
|[CA2230: Use params for variable arguments](../code-quality/ca2230-use-params-for-variable-arguments.md)|A public or protected type contains a public or protected method that uses the VarArgs calling convention instead of the params keyword.|
|[CA2231: Overload operator equals on overriding ValueType.Equals](../code-quality/ca2231-overload-operator-equals-on-overriding-valuetype-equals.md)|A value type overrides `Object.Equals` but does not implement the equality operator.|
|[CA2232: Mark Windows Forms entry points with STAThread](../code-quality/ca2232-mark-windows-forms-entry-points-with-stathread.md)|STAThreadAttribute indicates that the COM threading model for the application is a single-threaded apartment. This attribute must be present on the entry point of any application that uses Windows Forms; if it is omitted, the Windows components might not work correctly.|
|[CA2233: Operations should not overflow](../code-quality/ca2233-operations-should-not-overflow.md)|Arithmetic operations should not be performed without first validating the operands, to make sure that the result of the operation is not outside the range of possible values for the data types involved.|
|[CA2234: Pass System.Uri objects instead of strings](../code-quality/ca2234-pass-system-uri-objects-instead-of-strings.md)|A call is made to a method that has a string parameter whose name contains "uri", "URI", "urn", "URN", "url", or "URL".  The declaring type of the method contains a corresponding method overload that has a System.Uri parameter.|
|[CA2235: Mark all non-serializable fields](../code-quality/ca2235-mark-all-non-serializable-fields.md)|An instance field of a type that is not serializable is declared in a type that is serializable.|
|[CA2236: Call base class methods on ISerializable types](../code-quality/ca2236-call-base-class-methods-on-iserializable-types.md)|To fix a violation of this rule, call the base type GetObjectData method or serialization constructor from the corresponding derived type method or constructor.|
|[CA2237: Mark ISerializable types with SerializableAttribute](../code-quality/ca2237-mark-iserializable-types-with-serializableattribute.md)|To be recognized by the common language runtime as serializable, types must be marked with the SerializableAttribute attribute even if the type uses a custom serialization routine through implementation of the ISerializable interface.|
|[CA2238: Implement serialization methods correctly](../code-quality/ca2238-implement-serialization-methods-correctly.md)|A method that handles a serialization event does not have the correct signature, return type, or visibility.|
|[CA2239: Provide deserialization methods for optional fields](../code-quality/ca2239-provide-deserialization-methods-for-optional-fields.md)|A type has a field that is marked with the System.Runtime.Serialization.OptionalFieldAttribute attribute, and the type does not provide de-serialization event handling methods.|
|[CA2240: Implement ISerializable correctly](../code-quality/ca2240-implement-iserializable-correctly.md)|To fix a violation of this rule, make the GetObjectData method visible and overridable, and make sure that all instance fields are included in the serialization process or explicitly marked with the NonSerializedAttribute attribute.|
|[CA2241: Provide correct arguments to formatting methods](../code-quality/ca2241-provide-correct-arguments-to-formatting-methods.md)|The format argument passed to System.String.Format does not contain a format item that corresponds to each object argument, or vice versa.|
|[CA2242: Test for NaN correctly](../code-quality/ca2242-test-for-nan-correctly.md)|This expression tests a value against Single.Nan or Double.Nan. Use Single.IsNan(Single) or Double.IsNan(Double) to test the value.|
|[CA2243: Attribute string literals should parse correctly](../code-quality/ca2243-attribute-string-literals-should-parse-correctly.md)|An attribute's string literal parameter does not parse correctly for a URL, a GUID, or a version.|