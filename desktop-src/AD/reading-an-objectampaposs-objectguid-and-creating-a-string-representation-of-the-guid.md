---
title: Lettura di objectGUID di un oggetto e creazione di una rappresentazione di stringa del GUID
description: Usare il metodo IADs Get \_ GUID per recuperare il formato stringa associabile di objectGUID di un oggetto directory.
ms.assetid: 4f7f0e9d-3e06-47c9-83ce-cabed8692c15
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 77bf9c346585e8604968c3f708dfdc62ee8d248f
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/17/2020
ms.locfileid: "103724455"
---
# <a name="reading-an-objects-objectguid-and-creating-a-string-representation-of-the-guid"></a><span data-ttu-id="e5e0b-103">Lettura di objectGUID di un oggetto e creazione di una rappresentazione di stringa del GUID</span><span class="sxs-lookup"><span data-stu-id="e5e0b-103">Reading an Object's objectGUID and Creating a String Representation of the GUID</span></span>

<span data-ttu-id="e5e0b-104">La proprietà **objectGUID** di ogni oggetto nel Active Directory Domain Services viene archiviata nella directory come stringa di ottetto.</span><span class="sxs-lookup"><span data-stu-id="e5e0b-104">The **objectGUID** property of each object in Active Directory Domain Services is stored in the directory as an octet string.</span></span> <span data-ttu-id="e5e0b-105">Una stringa di ottetto è una matrice di caratteri a un byte.</span><span class="sxs-lookup"><span data-stu-id="e5e0b-105">An octet string is an array of one-byte characters.</span></span> <span data-ttu-id="e5e0b-106">Usare il metodo [**IADs:: Get \_ GUID**](/windows/desktop/ADSI/iads-property-methods) per recuperare il formato stringa associabile di **objectGUID** di un oggetto directory.</span><span class="sxs-lookup"><span data-stu-id="e5e0b-106">Use the [**IADs::get\_GUID**](/windows/desktop/ADSI/iads-property-methods) method to retrieve the bindable string form of a directory object's **objectGUID**.</span></span>

<span data-ttu-id="e5e0b-107">Negli esempi di codice seguenti viene illustrata una funzione che legge l'attributo **objectGUID** e restituisce una rappresentazione di stringa del GUID utilizzato per l'associazione all'oggetto.</span><span class="sxs-lookup"><span data-stu-id="e5e0b-107">The following code examples show a function that reads the **objectGUID** attribute and returns a string representation of the GUID used to bind to the object.</span></span>

-   [<span data-ttu-id="e5e0b-108">Esempio di Visual Basic</span><span class="sxs-lookup"><span data-stu-id="e5e0b-108">Visual Basic Example</span></span>](#visual-basic-example)
-   [<span data-ttu-id="e5e0b-109">Esempio di C++</span><span class="sxs-lookup"><span data-stu-id="e5e0b-109">C++ Example</span></span>](#c-example)

## <a name="visual-basic-example"></a><span data-ttu-id="e5e0b-110">Esempio di Visual Basic</span><span class="sxs-lookup"><span data-stu-id="e5e0b-110">Visual Basic Example</span></span>


```VB
Dim sADsPathObject As String
Dim sObjectGUID As String
Dim sBindByGuidStr As String
 
Dim IADsObject As IADs
Dim IADsObject2 As IADs
On Error Resume Next
 
' Query the user for an ADsPath to start.
sADsPathObject = InputBox("This code binds to a directory object by ADsPath, retrieves the GUID, then rebinds by GUID." & vbCrLf & vbCrLf & "Specify the ADsPath of the object to bind to :")
 
If sADsPathObject = "" Then
    GoTo CleanUp
End If
 
MsgBox "Binding to " & sADsPathObject
 
' Bind to initial object.
Set IADsObject = GetObject(sADsPathObject)
 
If (Err.Number <> 0) Then
   MsgBox Err.Number & " on GetObject method"
   GoTo CleanUp
End If
 
' Save the GUID of the object.
sObjectGUID = IADsObject.Guid
 
MsgBox "The GUID for " & vbCrLf & vbCrLf & sADsPathObject & vbCrLf & vbCrLf & " is " & vbCrLf & vbCrLf & sObjectGUID
 
' Release the initial object.
Set IADsObject = Nothing
 
' Build a string for Binding to the object by GUID.
sBindByGuidStr = "LDAP://<GUID=" & sObjectGUID & ">"

MsgBox sBindByGuidStr
 
' Bind BACK to the Same object using the GUID.
Set IADsObject = GetObject(sBindByGuidStr)
 
If (Err.Number <> 0) Then
   MsgBox Err.Number & " on GetObject method "
   GoTo CleanUp
End If
 
MsgBox "Successfully RE bound to " & sADsPathObject & vbCrLf & vbCrLf & " using the path:" & vbCrLf & vbCrLf & sBindByGuidStr
 
' Release bind by GUID Object.
CleanUp:
   Set IADsObject = Nothing

```



## <a name="c-example"></a><span data-ttu-id="e5e0b-111">Esempio C++</span><span class="sxs-lookup"><span data-stu-id="e5e0b-111">C++ Example</span></span>


```C++
#define UNICODE
#include <ole2.h>
#include <stdio.h>
#include <activeds.h>

#define PATH_SIZE 1024

void wmain(int argc, wchar_t *argv[])
{
    // Initialize COM.
    CoInitialize(0);
     
    WCHAR wszADsPathObject[PATH_SIZE + 1];
    HRESULT hr;
    IADs *pIADsObject = NULL;
    IADs *pIADsObjectByGuid = NULL;
     
    // If no ADsPath was specified on the command line, query the user for a ADsPath to start.
    if(!argv[1])
    {
        _putws(L"This code binds to a directory object by ADsPath, retrieves the GUID,\n"
            L" then rebinds by GUID. \n\nEnter the ADsPath of the object to bind to :\n");
        fgetws(wszADsPathObject, PATH_SIZE, stdin);
    }
    else
    {
        wcsncpy_s(wszADsPathObject, argv[1], PATH_SIZE - 1);
        wszADsPathObject[PATH_SIZE] = 0;
    }
     
    if (!wszADsPathObject[0])
    {
        return;
    }
     
    wprintf(L"\nBinding to %s\n", wszADsPathObject);
     
    // Bind to initial object.
    hr = ADsGetObject(wszADsPathObject, IID_IADs, (void**)&pIADsObject);
    if (SUCCEEDED(hr))
    {
        BSTR bstrGuid = NULL;
        hr = pIADsObject->get_GUID(&bstrGuid); 
        
        if (SUCCEEDED(hr))
        {
            LPWSTR wszFormat = L"LDAP://<GUID=%s>";
            LPWSTR pwszBindByGuidStr; 

            wprintf(L"\n The GUID for\n\n%s\n\nis\n\n%s\n", wszADsPathObject, bstrGuid);
     
            // Build a string for Binding to the object by GUID.
            pwszBindByGuidStr = new WCHAR[wcslen(wszFormat) + wcslen(bstrGuid) + 1];
            if(pwszBindByGuidStr)
            {
                swprintf_s(pwszBindByGuidStr, wszFormat, bstrGuid);
         
                // Bind BACK to the Same object using the GUID.
                hr = ADsGetObject(pwszBindByGuidStr, IID_IADs, (void**)&pIADsObjectByGuid);
                 
                if (SUCCEEDED(hr))
                {
                    wprintf(L"\nSuccessfully re-bound to\n\n%s\n\nUsing the path:\n\n%s\n", 
                        wszADsPathObject, pwszBindByGuidStr);
         
                    // Release bind by GUID Object.
                    pIADsObjectByGuid->Release();
                    pIADsObjectByGuid = NULL;
                }

                delete pwszBindByGuidStr;
            }
            else
            {
                hr = E_OUTOFMEMORY;
            }
     
            SysFreeString(bstrGuid);
        }
     
        pIADsObject->Release();
        pIADsObject = NULL;
    }
     
    if (FAILED(hr))
    {
        wprintf(L"Failed");
    }
}
```



 

 