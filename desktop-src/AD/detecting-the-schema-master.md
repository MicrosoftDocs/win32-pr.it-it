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
# <a name="detecting-the-schema-master"></a><span data-ttu-id="419c8-104">Rilevamento del master schema</span><span class="sxs-lookup"><span data-stu-id="419c8-104">Detecting the Schema Master</span></span>

<span data-ttu-id="419c8-105">Active Directory Domain Services dispone di un sistema di aggiornamento multimaster; ogni controller di dominio include una copia scrivibile della directory.</span><span class="sxs-lookup"><span data-stu-id="419c8-105">Active Directory Domain Services have a multi-master update system; every domain controller holds a writable copy of the directory.</span></span> <span data-ttu-id="419c8-106">Gli aggiornamenti dello schema vengono propagati a tutti i domini appartenenti allo stesso albero o alla stessa foresta.</span><span class="sxs-lookup"><span data-stu-id="419c8-106">Schema updates are propagated to all domains that belong to the same tree or forest.</span></span> <span data-ttu-id="419c8-107">Poiché è difficile riconciliare gli aggiornamenti in conflitto allo schema, gli aggiornamenti dello schema possono essere eseguiti solo in un singolo server.</span><span class="sxs-lookup"><span data-stu-id="419c8-107">Because it is difficult to reconcile conflicting updates to the schema, schema updates can only be performed at a single server.</span></span> <span data-ttu-id="419c8-108">Il server con il diritto di eseguire gli aggiornamenti può cambiare, ma un solo server avrà tale diritto in un determinato momento.</span><span class="sxs-lookup"><span data-stu-id="419c8-108">The server with the right to perform updates can change, but only one server will have that right at any given time.</span></span> <span data-ttu-id="419c8-109">Questo server è denominato master schema.</span><span class="sxs-lookup"><span data-stu-id="419c8-109">This server is called the schema master.</span></span> <span data-ttu-id="419c8-110">Il primo controller di dominio installato in un'organizzazione è, per impostazione predefinita, il master schema.</span><span class="sxs-lookup"><span data-stu-id="419c8-110">The first DC installed in an enterprise is, by default, the schema master.</span></span>

<span data-ttu-id="419c8-111">Le modifiche dello schema possono essere apportate solo a livello di master schema.</span><span class="sxs-lookup"><span data-stu-id="419c8-111">Schema changes can only be made at the schema master level.</span></span> <span data-ttu-id="419c8-112">Per rilevare quale controller di dominio è il master schema, seguire questa procedura.</span><span class="sxs-lookup"><span data-stu-id="419c8-112">To detect which DC is the schema master, perform the following steps.</span></span>

<span data-ttu-id="419c8-113">**Rilevamento del master schema del controller di dominio**</span><span class="sxs-lookup"><span data-stu-id="419c8-113">**Detecting the DC Schema Master**</span></span>

1.  <span data-ttu-id="419c8-114">Leggere l'attributo **fSMORoleOwner** del contenitore dello schema in qualsiasi controller di dominio.</span><span class="sxs-lookup"><span data-stu-id="419c8-114">Read the **fsmoRoleOwner** attribute of the schema container on any DC.</span></span> <span data-ttu-id="419c8-115">L'attributo **fSMORoleOwner** restituisce il nome distinto (DN) dell'oggetto **NTDSDSA** per il master schema.</span><span class="sxs-lookup"><span data-stu-id="419c8-115">The **fsmoRoleOwner** attribute returns the distinguished name (DN) of the **nTDSDSA** object for the schema master.</span></span>
2.  <span data-ttu-id="419c8-116">Eseguire l'associazione all'oggetto **NTDSDSA** di cui è stato appena recuperato il DN.</span><span class="sxs-lookup"><span data-stu-id="419c8-116">Bind to the **nTDSDSA** object whose DN you just retrieved.</span></span> <span data-ttu-id="419c8-117">L'elemento padre di questo oggetto è l'oggetto server per il controller di dominio che contiene il master schema.</span><span class="sxs-lookup"><span data-stu-id="419c8-117">The parent of this object is the server object for the DC containing the schema master.</span></span>
3.  <span data-ttu-id="419c8-118">Ottiene il ADsPath per l'elemento padre dell'oggetto **NTDSDSA** .</span><span class="sxs-lookup"><span data-stu-id="419c8-118">Get the ADsPath for the parent of the **nTDSDSA** object.</span></span> <span data-ttu-id="419c8-119">L'elemento padre è un oggetto server.</span><span class="sxs-lookup"><span data-stu-id="419c8-119">The parent is a server object.</span></span>
4.  <span data-ttu-id="419c8-120">Eseguire l'associazione all'oggetto server.</span><span class="sxs-lookup"><span data-stu-id="419c8-120">Bind to the server object.</span></span>
5.  <span data-ttu-id="419c8-121">Ottiene l'attributo **dNSHostName** dell'oggetto server.</span><span class="sxs-lookup"><span data-stu-id="419c8-121">Get the **dNSHostName** attribute of the server object.</span></span> <span data-ttu-id="419c8-122">Si tratta del nome DNS del controller di dominio che contiene il master schema.</span><span class="sxs-lookup"><span data-stu-id="419c8-122">This is the DNS name of the DC that contains the schema master.</span></span>
6.  <span data-ttu-id="419c8-123">Specificare il nome DNS del master schema come server e il DN come DN del contenitore dello schema da associare al master schema.</span><span class="sxs-lookup"><span data-stu-id="419c8-123">Specify the DNS name of the schema master as the server and the DN as the DN of the schema container to bind to the schema master.</span></span> <span data-ttu-id="419c8-124">Se ad esempio il server è "dc1.fabrikam.com" e il DN del contenitore dello schema è "CN = schema, CN = Configuration, DC = Fabrikam, DC = com", ADsPath sarà il seguente.</span><span class="sxs-lookup"><span data-stu-id="419c8-124">For example, if the server was "dc1.fabrikam.com" and the schema container DN was "cn=schema,cn=configuration,dc=fabrikam,dc=com", the ADsPath would be as follows.</span></span>
    ```C++
    LDAP://dc1.fabrikam.com/cn=schema,cn=configuration,dc=fabrikam,dc=com
    ```

    

<span data-ttu-id="419c8-125">È consigliabile trovare il master schema e associarlo per apportare modifiche allo schema.</span><span class="sxs-lookup"><span data-stu-id="419c8-125">It is recommended that you find the schema master and bind to it to make schema changes.</span></span> <span data-ttu-id="419c8-126">Tuttavia, è possibile spostare il master schema in un altro server.</span><span class="sxs-lookup"><span data-stu-id="419c8-126">However, you can move the schema master to another server.</span></span>

<span data-ttu-id="419c8-127">Per creare un altro server come master schema, un utente con privilegi idonei può:</span><span class="sxs-lookup"><span data-stu-id="419c8-127">To make another server the schema master, a suitably privileged user can:</span></span>

-   <span data-ttu-id="419c8-128">Utilizzare lo snap-in MMC Gestione schema.</span><span class="sxs-lookup"><span data-stu-id="419c8-128">Use the Schema Manager MMC snap-in.</span></span>
    > [!Note]
    > <span data-ttu-id="419c8-129">Lo snap-in MMC dello schema di Active Directory deve essere registrato manualmente.</span><span class="sxs-lookup"><span data-stu-id="419c8-129">The Active Directory Schema MMC snap-in must be registered manually.</span></span> <span data-ttu-id="419c8-130">Per registrare lo snap-in dello schema, è necessario eseguire il comando seguente dal prompt dei comandi nella directory Windows system32.</span><span class="sxs-lookup"><span data-stu-id="419c8-130">To register the Schema snap-in, you must run the following command from the command prompt in the Windows System32 directory.</span></span>
    >
    > <span data-ttu-id="419c8-131">**regsvr32.exe schmmgmt.dll**</span><span class="sxs-lookup"><span data-stu-id="419c8-131">**regsvr32.exe schmmgmt.dll**</span></span>

     

-   <span data-ttu-id="419c8-132">Utilizzare l'utilità da riga di comando NTDSUTIL.</span><span class="sxs-lookup"><span data-stu-id="419c8-132">Use the NTDSUTIL command-line utility.</span></span>
-   <span data-ttu-id="419c8-133">Usare un'applicazione di terze parti (un'applicazione che rilascia la scrittura LDAP appropriata).</span><span class="sxs-lookup"><span data-stu-id="419c8-133">Use a third-party application (an application that issues the appropriate LDAP write).</span></span>

<span data-ttu-id="419c8-134">Per diventare il master schema a livello di codice, un'applicazione in esecuzione nel contesto di un utente con privilegi idonei può emettere una scrittura LDAP dell'attributo operativo **becomeSchemaMaster** in RootDSE su tale controller di dominio.</span><span class="sxs-lookup"><span data-stu-id="419c8-134">To become the schema master programmatically, an application running in the context of a suitably privileged user can issue an LDAP write of the operational attribute **becomeSchemaMaster** to the rootDSE on that DC.</span></span> <span data-ttu-id="419c8-135">In questo modo viene avviato un trasferimento atomico del master schema dal titolare corrente al controller di dominio locale.</span><span class="sxs-lookup"><span data-stu-id="419c8-135">This initiates an atomic transfer of the schema master right from the current holder to the local DC.</span></span>

<span data-ttu-id="419c8-136">Nell'esempio di codice seguente viene trovato il master schema.</span><span class="sxs-lookup"><span data-stu-id="419c8-136">The following code example finds the schema master.</span></span> <span data-ttu-id="419c8-137">La funzione seguente viene associata al contenitore dello schema nel computer che corrisponde al master schema.</span><span class="sxs-lookup"><span data-stu-id="419c8-137">The following function binds to the schema container on the computer that is the schema master.</span></span>


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



<span data-ttu-id="419c8-138">Nell'esempio di codice seguente viene visualizzato il nome DNS per il computer che corrisponde al master schema.</span><span class="sxs-lookup"><span data-stu-id="419c8-138">The following code example displays the DNS name for the computer that is the schema master.</span></span>


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



 

 




