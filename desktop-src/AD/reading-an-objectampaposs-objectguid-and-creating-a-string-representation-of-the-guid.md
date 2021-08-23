---
title: Lettura dell'objectGUID di un oggetto e creazione di una rappresentazione di stringa del GUID
description: Usare il metodo get GUID IADs per recuperare il formato stringa associabile \_ dell'objectGUID di un oggetto directory.
ms.assetid: 4f7f0e9d-3e06-47c9-83ce-cabed8692c15
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9872f16ddeee2e7a01e05be0d3c98aed5e66a9e6bce310565c001f831bd46e02
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119025329"
---
# <a name="reading-an-objects-objectguid-and-creating-a-string-representation-of-the-guid"></a>Lettura dell'objectGUID di un oggetto e creazione di una rappresentazione di stringa del GUID

La **proprietà objectGUID** di ogni oggetto in Active Directory Domain Services viene archiviata nella directory come stringa ottetto. Una stringa ottetto è una matrice di caratteri a un byte. Usare il [**metodo IADs::get \_ GUID**](/windows/desktop/ADSI/iads-property-methods) per recuperare il formato stringa associabile dell'objectGUID di un oggetto directory. 

Negli esempi di codice seguenti viene illustrata una funzione che legge l'attributo **objectGUID** e restituisce una rappresentazione di stringa del GUID usato per l'associazione all'oggetto .

-   [Visual Basic Esempio](#visual-basic-example)
-   [Esempio di C++](#c-example)

## <a name="visual-basic-example"></a>Visual Basic Esempio


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



## <a name="c-example"></a>Esempio C++


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



 

 