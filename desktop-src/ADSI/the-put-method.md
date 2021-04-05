---
title: Metodo Put
description: Salva il valore di una proprietà per un oggetto Active Directory in base al nome nella cache delle proprietà.
ms.assetid: 8534ceba-5fcb-441f-9e76-3060319478af
ms.tgt_platform: multiple
keywords:
- Inserisci ADSI, informazioni
- ADSI ADSI, esempio di codice Visual Basic, uso del metodo Put
- Proprietà ADSI, salvataggio di un valore per una proprietà nella cache delle proprietà
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a64a5cba8056f8eac0125fc5b32fd66bdf988dae
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103855238"
---
# <a name="the-put-method"></a>Metodo Put

Il metodo [**IADs::P UT**](/windows/desktop/api/Iads/nf-iads-iads-put) Salva il valore di una proprietà per un oggetto Active Directory in base al nome nella cache delle proprietà. Usare [**IADs::P UTEX**](/windows/desktop/api/Iads/nf-iads-iads-putex) per salvare le proprietà multivalore nella cache delle proprietà o per rimuovere una proprietà da un oggetto. Questi valori non vengono salvati in modo permanente nel servizio directory sottostante fino a quando non viene chiamato [**IADs:: SetInfo**](/windows/desktop/api/Iads/nf-iads-iads-setinfo) .


```VB
Dim Namespace As IADsOpenDSObject
Dim User As IADsUser
Dim NewName As Variant
Dim sUserName As String
Dim sPassword As String

On Error GoTo CleanUp
 
Set Namespace = GetObject("LDAP:")

' Insert code to safely get the user name and password
 
Set User = Namespace.OpenDSObject("LDAP://MyMachine/CN=Administrator,CN=Users,DC=MyDomain,DC=Fabrikam,DC=COM", sUserName, sPassword, ADS_SECURE_AUTHENTICATION)
 
NewName = InputBox("Enter a new name:")
 
' Set using IADs::PutMethod
User.Put "FullName", NewName
User.SetInfo

Exit Sub

CleanUp:
    Set IADsOpenDSObject = Nothing
    Set IADsUser = Nothing

End Sub
```



Nell'esempio di codice seguente viene illustrato come utilizzare [**IADs::P UT**](/windows/desktop/api/Iads/nf-iads-iads-put) con un singolo valore:


```VB
Dim x As IADs
Dim sUserName As String
Dim sFull As String

On Error GoTo CleanUp

sUserName = InputBox("Enter your user name:")
 
Set x = GetObject("LDAP://CN="& sUserName &",CN=Users,DC=Fabrikam, DC=Com") 

sFull = InputBox ("Enter your full name:")
x.Put "name", sFull
 
' Commit to the directory.
x.SetInfo

Exit Sub

CleanUp:
    MsgBox ("An error has occurred. " & Err.Description)
    Set x = Nothing
```



Nell'esempio di codice seguente viene illustrato come utilizzare [**IADs::P UT**](/windows/desktop/api/Iads/nf-iads-iads-put) con più valori:


```VB
Dim x As IADs
Dim sFirst As String
Dim sLast As String
Dim sUsername As String

On Error GoTo CleanUp

sUsername = InputBox("User name:")
 
Set x = GetObject("LDAP://CN=" & sUsername & ", CN=Users,DC=Fabrikam, DC=Com")

sFirst = InputBox("Enter your first name:")
sLast = InputBox("Enter your last name:")
 
x.Put "givenName", sFirst
x.Put "sn", sLast
 
'Commit to the directory
x.SetInfo

Exit Sub

CleanUp:
    MsgBox ("An error has occurred. " & Err.Description)
    Set x = Nothing
```



Nell'esempio di codice seguente viene illustrato come utilizzare [**IADs::P UT**](/windows/desktop/api/Iads/nf-iads-iads-put) con valori multipli e singoli:


```C++
int main(int argc, char* argv[], LPWSTR pszADsPath)
{
   HRESULT hr;
   IADs *pADs=NULL;

   CoInitialize(NULL);

   hr = ADsGetObject(pszADsPath,
                     IID_IADs, 
                    (void**) &pADs );

   if (!SUCCEEDED(hr) )
   {
     return hr;
   }

   VARIANT var;
 
   // Using Put with a single value for the first name
   VariantInit(&var);
   V_BSTR(&var) = SysAllocString(L"Janet");
   V_VT(&var) = VT_BSTR;
   hr = pADs->Put( L"givenName", var );

   // Using Put with a single value for the last name
   VariantClear(&var);
   V_BSTR(&var) = SysAllocString(L"Johns");
   V_VT(&var) = VT_BSTR;
   hr = pADs->Put( L"sn", var ); 
   VariantClear(&var);

   // Using Put with multiple values for other telephones
   LPWSTR pszPhones[] = { L"425 844 1234", L"425 924 4321" };
   DWORD dwNumber = sizeof( pszPhones ) /sizeof(LPWSTR);

   hr = ADsBuildVarArrayStr( pszPhones, dwNumber, &var );
   hr = pADs->Put( L"otherTelephone", var ); 
   VariantClear(&var);

   hr = pADs->SetInfo();
   pADs->Release();

   if (!SUCCEEDED(hr) )
   {
     return hr;
   }

 CoUninitialize();
 return 0;
}
```



 

 




