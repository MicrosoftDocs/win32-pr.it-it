---
title: Codice di esempio per l'enumerazione degli utenti in un server membro
description: Questo argomento include esempi di codice che enumerano gli utenti in un server membro.
ms.assetid: a856281a-7f84-44d0-9123-b27fda56e0ea
ms.tgt_platform: multiple
keywords:
- Esempi di Active Directory Active Directory, enumerazione degli utenti in un server membro
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7b066e92ced26c58ef932025f4e818d87a907b30
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103955145"
---
# <a name="example-code-for-enumerating-users-on-a-member-server"></a><span data-ttu-id="a898a-104">Codice di esempio per l'enumerazione degli utenti in un server membro</span><span class="sxs-lookup"><span data-stu-id="a898a-104">Example Code for Enumerating Users on a Member Server</span></span>

<span data-ttu-id="a898a-105">L'esempio di codice seguente Visual Basic enumera tutti gli utenti in un server membro o in Windows 2000 Professional.</span><span class="sxs-lookup"><span data-stu-id="a898a-105">The following Visual Basic code example enumerates all users on a member server or Windows 2000 Professional.</span></span>


```VB
Const ADS_SECURE_AUTHENTICATION = 1

'   ListObjectsWithWinNtProvider()
'
'   Uses the WinNT provider to list child objects based on a filter.
'
'   Parameters:
'
'   pwszComputer - Contains the computer to list the objects for.
'   pwszClass - Contains the object class name to filter for.
'   pwszUsername - Contains the user name to be used for 
'                  authentication.
'   pwszPassword - Contains the password to be used for 
'                  authentication.
'
Public Sub ListObjectsWithWinNtProvider(Computer As String, _
                                        Class As String, _
                                        Username As String, _
                                        Password As String)
    Dim BindingString As String
    Dim oComputer As IADsContainer
    Dim oObject As IADs
    Dim oNSP As IADsOpenDSObject
    
    ' Build the binding string.
    BindingString = "WinNT://" + Computer + ",computer"
    
    ' Bind to the computer.
    If Username = "" Then
        Set oComputer = GetObject(BindingString)
    Else
        Set oNSP = GetObject("WinNT:")
        Set oComputer = oNSP.OpenDSObject(BindingString, _
            Username, _
            Password, _
            ADS_SECURE_AUTHENTICATION)
    End If
    
    ' Add the class to the Filter property of the 
    ' IADsContainer object.
    oComputer.Filter = Array(Class)
    
    For Each oObject In oComputer
        Debug.Print ""
        Debug.Print "Name:" + oObject.Name
        Debug.Print "ADsPath:" + oObject.ADsPath
        Debug.Print "-----------------------------------------"
    Next
End Sub
```



<span data-ttu-id="a898a-106">Nell'esempio di codice C++ riportato di seguito vengono enumerati tutti gli oggetti di una classe specificata, ad esempio un utente, e vengono visualizzati i membri contenuti in ogni oggetto in un server membro o Windows 2000 Professional.</span><span class="sxs-lookup"><span data-stu-id="a898a-106">The following C++ code example enumerates all objects of a specified class, such as a user, and displays the members contained in each object on a member server or Windows 2000 Professional.</span></span>


```C++
/********************************************************************

    ListObjectsWithWinNtProvider()

    Uses the WinNT provider to list children based on a filter. 
    Returns S_OK if successful.
 
    Parameters:

    pwszComputer - Contains the computer for which to 
                   list the objects.
    pwszClass - Contains the object class name to filter for.
    pwszUsername - Contains the user name to be used for 
                   authentication.
    pwszPassword - Contains the password to be used for 
                   authentication.
 
*********************************************************************/

HRESULT ListObjectsWithWinNtProvider(
    LPCWSTR pwszComputer, 
    LPCWSTR pwszClass, 
    LPCWSTR pwszUsername, 
    LPCWSTR pwszPassword)
{
    HRESULT hr;
 
    IADsContainer * pIADsCont = NULL;
 
    // Build the binding string.
    CComBSTR sbstrBindingString;
    sbstrBindingString = "WinNT://";
    sbstrBindingString += pwszComputer;
    sbstrBindingString += ",computer";
    
    // Bind to the container.
    hr = ADsOpenObject( sbstrBindingString,
                        pwszUsername, 
                        pwszPassword, 
                        ADS_SECURE_AUTHENTICATION,
                        IID_IADsContainer, 
                        (void**) &pIADsCont);

    if (SUCCEEDED(hr))
    {
        VARIANT vFilter;
        VariantInit(&vFilter);
        LPWSTR rgpwszFilter[] = {(LPWSTR)pwszClass};
 
        // Build a Variant of array type, using the filter passed.
        hr = ADsBuildVarArrayStr(rgpwszFilter, 1, &vFilter);
        if (SUCCEEDED(hr))
        {
            // Set the filter for the results of the enumeration.
            hr = pIADsCont->put_Filter(vFilter);
            if (SUCCEEDED(hr))
            {
                IEnumVARIANT *pEnumVariant = NULL;
 
                // Build an enumerator interface. This is used 
                // to enumerate the objects contained in 
                // the IADsContainer.
                hr = ADsBuildEnumerator(pIADsCont, &pEnumVariant);

                if(SUCCEEDED(hr))
                {
                    VARIANT Variant;
                    ULONG ulElementsFetched;

                    // Loop through and print the data.
                    while(SUCCEEDED(ADsEnumerateNext(pEnumVariant, 
                                                     1,
                                                     &Variant, 
                                                     &ulElementsFetched))
                          && (ulElementsFetched > 0))
                    {
                        if(VT_DISPATCH == Variant.vt)
                        {
                            IADs *pIADs= NULL;

                            // Query the variant IDispatch *
                            // for the IADs interface
                            hr = Variant.pdispVal->QueryInterface(IID_IADs,
                                                                  (VOID**)&pIADs);
     
                            if (SUCCEEDED(hr))
                            {
                                // Print the object data.
                                CComBSTR sbstrResult;
                                hr = pIADs->get_Name(&sbstrResult); 
                                if(SUCCEEDED(hr))
                                {
                                    wprintf(L"Name : %s\n", 
                                            sbstrResult);
                                }

                                hr = pIADs->get_ADsPath(&sbstrResult); 
                                if(SUCCEEDED(hr))
                                {
                                    wprintf(L"ADsPath : %s\n", 
                                            sbstrResult);
                                }
     
                                wprintf(L"-------------------\n\n");
                                
                                pIADs->Release();
                            }
                        }
                    
                        VariantClear(&Variant);
                    }
                    
                    pEnumVariant->Release();
                }

            }
        }
        VariantClear(&vFilter);
    }
 
    return hr;
}
```



 

 




