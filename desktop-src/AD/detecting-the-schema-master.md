---
title: Rilevamento del master schema
description: Active Directory Domain Services dispone di un sistema di aggiornamento multimaster; ogni controller di dominio include una copia scrivibile della directory.
ms.assetid: 8e096351-43f8-48ee-acb6-681d9e38e93c
ms.tgt_platform: multiple
keywords:
- Rilevamento dell'annuncio master dello schema
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6869853cba68d7155f2091e2fe4515116944a629
ms.sourcegitcommit: f730b85cc85448913e50a7f331e10b646ea7978b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/23/2019
ms.locfileid: "103857050"
---
# <a name="detecting-the-schema-master"></a>Rilevamento del master schema

Active Directory Domain Services dispone di un sistema di aggiornamento multimaster; ogni controller di dominio include una copia scrivibile della directory. Gli aggiornamenti dello schema vengono propagati a tutti i domini appartenenti allo stesso albero o alla stessa foresta. Poiché è difficile riconciliare gli aggiornamenti in conflitto allo schema, gli aggiornamenti dello schema possono essere eseguiti solo in un singolo server. Il server con il diritto di eseguire gli aggiornamenti può cambiare, ma un solo server avrà tale diritto in un determinato momento. Questo server è denominato master schema. Il primo controller di dominio installato in un'organizzazione è, per impostazione predefinita, il master schema.

Le modifiche dello schema possono essere apportate solo a livello di master schema. Per rilevare quale controller di dominio è il master schema, seguire questa procedura.

**Rilevamento del master schema del controller di dominio**

1.  Leggere l'attributo **fSMORoleOwner** del contenitore dello schema in qualsiasi controller di dominio. L'attributo **fSMORoleOwner** restituisce il nome distinto (DN) dell'oggetto **NTDSDSA** per il master schema.
2.  Eseguire l'associazione all'oggetto **NTDSDSA** di cui è stato appena recuperato il DN. L'elemento padre di questo oggetto è l'oggetto server per il controller di dominio che contiene il master schema.
3.  Ottiene il ADsPath per l'elemento padre dell'oggetto **NTDSDSA** . L'elemento padre è un oggetto server.
4.  Eseguire l'associazione all'oggetto server.
5.  Ottiene l'attributo **dNSHostName** dell'oggetto server. Si tratta del nome DNS del controller di dominio che contiene il master schema.
6.  Specificare il nome DNS del master schema come server e il DN come DN del contenitore dello schema da associare al master schema. Se ad esempio il server è "dc1.fabrikam.com" e il DN del contenitore dello schema è "CN = schema, CN = Configuration, DC = Fabrikam, DC = com", ADsPath sarà il seguente.
    ```C++
    LDAP://dc1.fabrikam.com/cn=schema,cn=configuration,dc=fabrikam,dc=com
    ```

    

È consigliabile trovare il master schema e associarlo per apportare modifiche allo schema. Tuttavia, è possibile spostare il master schema in un altro server.

Per creare un altro server come master schema, un utente con privilegi idonei può:

-   Utilizzare lo snap-in MMC Gestione schema.
    > [!Note]
    > Lo snap-in MMC dello schema di Active Directory deve essere registrato manualmente. Per registrare lo snap-in dello schema, è necessario eseguire il comando seguente dal prompt dei comandi nella directory Windows system32.
    >
    > **regsvr32.exe schmmgmt.dll**

     

-   Utilizzare l'utilità da riga di comando NTDSUTIL.
-   Usare un'applicazione di terze parti (un'applicazione che rilascia la scrittura LDAP appropriata).

Per diventare il master schema a livello di codice, un'applicazione in esecuzione nel contesto di un utente con privilegi idonei può emettere una scrittura LDAP dell'attributo operativo **becomeSchemaMaster** in RootDSE su tale controller di dominio. In questo modo viene avviato un trasferimento atomico del master schema dal titolare corrente al controller di dominio locale.

Nell'esempio di codice seguente viene trovato il master schema. La funzione seguente viene associata al contenitore dello schema nel computer che corrisponde al master schema.


```C++
HRESULT BindToSchemaMaster(IADsContainer **ppSchemaMaster)
{
HRESULT hr = E_FAIL;
// Get rootDSE and the schema container DN.
IADs *pObject = NULL;
IADs *pTempSchema = NULL;
IADs *pNTDS = NULL;
IADs *pServer = NULL;
BSTR bstrParent;
LPOLESTR szPath = new OLECHAR[MAX_PATH];
VARIANT var, varRole,varComputer;
hr = ADsOpenObject(L"LDAP://rootDSE",
         NULL,
         NULL,
         ADS_SECURE_AUTHENTICATION, // Use Secure Authentication.
         IID_IADs,
         (void**)&pObject);
if (hr == S_OK)
{
  hr = pObject->Get(CComBSTR("schemaNamingContext"), &var);
  if (hr == S_OK)
  {
    wcscpy_s(szPath,L"LDAP://");
    wcscat_s(szPath,var.bstrVal);
    hr = ADsOpenObject(szPath,
             NULL,
             NULL,
             ADS_SECURE_AUTHENTICATION, // Use Secure Authentication.
             IID_IADs,
             (void**)&pTempSchema);
 
    if (hr == S_OK)
    {
      /*
      Read the fsmoRoleOwner attribute to identify which server is 
      the schema master.
      */  
      hr = pTempSchema->Get(CComBSTR("fsmoRoleOwner"), &varRole);
      if (hr == S_OK)
      {
        // The fsmoRoleOwner attribute returns the nTDSDSA object.
        // The parent is the server object.
        // Bind to NTDSDSA object and get parent.
        wcscpy_s(szPath,L"LDAP://");
        wcscat_s(szPath,varRole.bstrVal);
        hr = ADsOpenObject(szPath,
             NULL,
             NULL,
             ADS_SECURE_AUTHENTICATION,
             IID_IADs,
             (void**)&pNTDS);
        if (hr == S_OK)
        {
          hr = pNTDS->get_Parent(&bstrParent);
          if (hr == S_OK)
          {
            /*
            Bind to server object and get the DNS name of 
            the server.
            */
            wcscpy_s(szPath,bstrParent);
            hr = ADsOpenObject(szPath,
               NULL,
               NULL,
               ADS_SECURE_AUTHENTICATION,
               IID_IADs,
               (void**)&pServer);
            if (hr == S_OK)
            {
              // Get the dns name of the server.
              hr = pServer->Get(CComBSTR("dNSHostName"), 
                  &varComputer);
              if (hr == S_OK)
              {
                    wcscpy_s(szPath,L"LDAP://");
                    wcscat_s(szPath,varComputer.bstrVal);
                    wcscat_s(szPath,L"/");
                    wcscat_s(szPath,var.bstrVal);
                    hr = ADsOpenObject(szPath,
                         NULL,
                         NULL,
                         ADS_SECURE_AUTHENTICATION,
                         IID_IADs,
                         (void**)ppSchemaMaster);
                    if (FAILED(hr))
                    {
                      if (*ppSchemaMaster)
                      {
                        (*ppSchemaMaster)->Release();
                        (*ppSchemaMaster) = NULL;
                      }
                    }
              }
              VariantClear(&varComputer);
            }
            if (pServer)
              pServer->Release();
          }
          SysFreeString(bstrParent);
        }
        if (pNTDS)
          pNTDS->Release();
      }
      VariantClear(&varRole);
    }
    if (pTempSchema)
      pTempSchema->Release();
  }
  VariantClear(&var);
}
if (pObject)
    pObject->Release();
 
return hr;
}
```



Nell'esempio di codice seguente viene visualizzato il nome DNS per il computer che corrisponde al master schema.


```VB
On Error Resume Next
 
'''''''''''''''''''
' Bind to the rootDSE
''''''''''''''''''''
sPrefix = "LDAP://"
Set root= GetObject(sPrefix & "rootDSE")
If (Err.Number <> 0) Then
   BailOnFailure Err.Number, "on GetObject method"
End If
 
'''''''''''''''''''
' Get the DN for the schema
''''''''''''''''''''
sSchema = root.Get("schemaNamingContext")
If (Err.Number <> 0) Then
   BailOnFailure Err.Number, "on Get method"
End If
 
'''''''''''''''''''
' Bind to the schema container
''''''''''''''''''''
Set Schema= GetObject(sPrefix & sSchema )
If (Err.Number <> 0) Then
   BailOnFailure Err.Number, "on GetObject method to bind to schema"
End If
''''''''''''''''''''
' Read the fsmoRoleOwner attribute to see which server is the 
' schema master.
''''''''''''''''''''
sMaster = Schema.Get("fsmoRoleOwner")
If (Err.Number <> 0) Then
   BailOnFailure Err.Number, "on IADs::Get method for fsmoRoleOwner"
End If
''''''''''''''''''''
' The fsmoRoleOwner attribute returns the nTDSDSA object.
' The parent is the server object.
' Bind to NTDSDSA object and get the parent object.
''''''''''''''''''''
Set NTDS = GetObject(sPrefix & sMaster)
If (Err.Number <> 0) Then
   BailOnFailure Err.Number, "on GetObject method for NTDS"
End If
sServer = NTDS.Parent
If (Err.Number <> 0) Then
   BailOnFailure Err.Number, "on IADs::get_Parent method"
End If
''''''''''''''''''''
' Bind to server object
' and get the reference to the computer object.
''''''''''''''''''''
Set Server = GetObject(sServer)
If (Err.Number <> 0) Then
   BailOnFailure Err.Number, "on GetObject method for " & sServer
End If
sComputer = Server.Get("dNSHostName")
''''''''''''''''''''
' Display the DNS name for the computer.
''''''''''''''''''''
strText = "Schema master has the following DNS name: "& sComputer
WScript.echo strText
 
 
 
''''''''''''''''''''
' Display subroutines
''''''''''''''''''''
 
Sub BailOnFailure(ErrNum, ErrText)
    strText = "Error 0x" & Hex(ErrNum) & " " & ErrText
    MsgBox strText, vbInformation, "ADSI Error"
    WScript.Quit
End Sub
```



 

 




