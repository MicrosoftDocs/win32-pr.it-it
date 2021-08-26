---
description: Esempio introduttivo sull'uso del catalogo di amministrazione COM+
ms.assetid: e9ce25aa-4fb1-4357-9f4e-5bf649e29447
title: Esempio introduttivo sull'uso del catalogo di amministrazione COM+
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5bfd085cbe9a829a1248ddf36057c9d9f79de9d576236a2621b237063340cf95
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120070591"
---
# <a name="introductory-example-using-the-com-administration-catalog"></a>Esempio introduttivo sull'uso del catalogo di amministrazione COM+

Quando si usa il catalogo di amministrazione COM+ a livello di codice, in genere si ese verificano i passaggi generali seguenti (non indicati in un ordine rigoroso in questo caso):

-   Aprire una sessione con il catalogo COM+ nel computer locale. Facoltativamente, connettersi al catalogo COM+ in un computer remoto.
-   Eseguire azioni come l'avvio o l'arresto di servizi, ovvero azioni che non riguardano una determinata applicazione COM+.
-   Eseguire azioni come l'installazione o l'esportazione di applicazioni COM+ o l'installazione di componenti in applicazioni, azioni che riguardano la lettura o la scrittura in file.
-   Aggiungere nuovi elementi alle raccolte, ad esempio creare una nuova applicazione COM+ aggiungendo un nuovo elemento alla raccolta "Applicazioni".
-   Impostare o ottenere proprietà per un elemento di una raccolta.
-   Salvare o rimuovere le modifiche in sospeso nel catalogo.
-   Gestire eventuali errori che potrebbero verificarsi.

Per illustrare l'aspetto di questi passaggi quando si usano gli oggetti COMAdmin, di seguito viene fornito un esempio Visual Basic Microsoft. Illustra brevemente alcuni dei passaggi tipici descritti in precedenza, ad esempio l'individuazione di raccolte, l'enumerazione tramite una raccolta per recuperare un elemento e l'impostazione delle proprietà per tale elemento.

Nell'esempio seguente verranno eseguite le azioni seguenti:

1.  Creare una nuova applicazione COM+, "MyHomeZoo".
2.  Installare alcuni componenti, Cat e Dog, nell'applicazione. Entrambi i componenti sono contenuti in una singola DLL che deve esistere già: MyZoo.dll.
3.  Configurare la sicurezza basata sui ruoli per l'applicazione definendo due ruoli: ZooKeeper eKeeperToCats.
4.  Assegnare al ruolo ZooKeeper l'accesso all'intera applicazione.
5.  Assegnare l'accesso al ruolo DirtoCats solo al componente Dog.
6.  Attivare le proprietà di sicurezza in modo che il controllo dei ruoli verrà applicato per l'applicazione.
7.  Esportare l'applicazione MyHomeZoo in un file in modo che possa essere installata in altri computer.

Per usare questo esempio da Visual Basic, aggiungere un riferimento alla libreria dei tipi di amministrazione COM+.


```VB
Function SetupMyZoo() As Boolean  ' Return False if any errors occur.

    '  Initialize error handling for this function.
    SetupMyZoo = False 
    On Error GoTo My_Error_Handler

    '  Open a session with the catalog.
    '  Instantiate a COMAdminCatalog object. 
    Dim objCatalog As COMAdminCatalog
    Set objCatalog = CreateObject("COMAdmin.COMAdminCatalog")

    '  Create a new COM+ application.
    '  First get the "Applications" collection from the catalog.
    Dim objApplicationsColl As COMAdminCatalogCollection
    Set objApplicationsColl = objCatalog.GetCollection("Applications")

    '  Add a new item to this collection. 
    Dim objZooApp As COMAdminCatalogObject
    Set objZooApp = objApplicationsColl.Add

    '  The "Applications" collection determines the available properties.
    '  Set the "Name" property of the new application item. 
    objZooApp.Value("Name") = "MyHomeZoo"

    '  Set the "Description" property of the new application item. 
    objZooApp.Value("Description") = "My pets at home"

    '  Save changes made to the "Applications" collection. 
    objApplicationsColl.SaveChanges

    '  Install components into the application.
    '  Use the InstallComponent method on COMAdminCatalog. 
    '  In this case, the last two parameters are passed as empty strings.
    objCatalog.InstallComponent "MyHomeZoo","MyZoo.DLL","","" 

    '  Define the roles ZooKeeper and AllergicToCats 
    '  by adding them to the "Roles" collection related to MyHomeZoo. 
    '  First get the "Roles" collection related to MyHomeZoo.
    '  Use the GetCollection method on COMAdminCatalogCollection,
    '  passing in the name of the desired collection, "Roles", 
    '  and the Key property value of objZooApp.   
    '  The Key property uniquely identifies the object, serving
    '  here to distinguish the "Roles" collection related 
    '  to MyHomeZoo from that of any other application. 
    Dim objRolesColl As COMAdminCatalogCollection
    Set objRolesColl = objApplicationsColl.GetCollection("Roles", objZooApp.Key)

    '  Add new items to this "Roles" collection. 
    Dim objZooKeeperRole As COMAdminCatalogObject
    Dim objAllergicToCatsRole As COMAdminCatalogObject
    Set objZooKeeperRole = objRolesColl.Add
    Set objAllergicToCatsRole = objRolesColl.Add

    '  Set the "Name" for the new items.
    objZooKeeperRole.Value("Name") = "ZooKeeper" 
    objAllergicToCatsRole.Value("Name") = "AllergicToCats" 

    '  Save changes made to any items in this "Roles" collection. 
    objRolesColl.SaveChanges

    '  Assign the AllergicToCats role to the Dog component to 
    '  restrict its scope of access. (The ZooKeeper role, if assigned
    '  only at the application level, can access the whole application.)
    '  First get the "Components" collection related to MyHomeZoo.
    '  Use the GetCollection method on COMAdminCatalogCollection,
    '  passing in the name of the desired collection, "Components", and
    '  the Key property value of objZooApp. 
    Dim objZooComponentsColl As COMAdminCatalogCollection
    Set objZooComponentsColl = objApplicationsColl.GetCollection("Components", objZooApp.Key) 

    '  Find the Dog component item in this "Components" collection.
    '  First Populate the collection to read in data for all its items. 
    objZooComponentsColl.Populate

    '  Enumerate through the "Components" collection 
    '  until the Dog component item is located. 
    Dim objDog As COMAdminCatalogObject 
    For Each objDog in objZooComponentsColl
        If objDog.Name = "Dog" Then 
            Exit For
        End If
    Next 
    '  Set the role checking property at the component level for Dog.
        objDog.Value("ComponentAccessChecksEnabled") = True 

    '  Save these changes.
        objZooComponentsColl.SaveChanges
    '  Get the "RolesForComponent" collection related to the 
    '  Dog component, using the Key property of objDog. 
    Dim objRolesForDogColl As COMAdminCatalogCollection 
    Set objRolesForDogColl = objZooComponentsColl.GetCollection("RolesForComponent", objDog.Key) 

    '  Add a new item to this "RolesForComponent" collection. 
    Dim objCatSneezerRole As COMAdminCatalogObject
    Set objCatSneezerRole = objRolesForDogColl.Add

    '  Set the "Name" of the new item to be "AllergicToCats". 
    objCatSneezerRole.Value("Name") = "AllergicToCats" 

    '  Save changes made to this "RolesForComponent" collection. 
    objRolesForDogColl.SaveChanges

    '  Now set properties to enforce role-based security. 
    '  First set role-based security at the application level.
    objZooApp.Value("ApplicationAccessChecksEnabled") = True 
    objZooApp.Value("AccessChecksLevel") = COMAdminAccessChecksApplicationComponentLevel 

    '  Save these changes.
    objApplicationsColl.SaveChanges

    '  Finally, export the new configured MyHomeZoo application to an 
    '  MSI file, used to install the application on other machines.
    '  Use the ExportApplication method on COMAdminCatalogObject.
    objCatalog.ExportApplication "MyHomeZoo", "c:\Program Files\COM applications\MyHomeZoo.MSI", 4

    '  Exit the function gracefully.
    SetupMyZoo = True

My_Error_Handler:
    If Not SetupMyZoo Then
        MsgBox "Error # " & Err.Number & " (Hex: " & Hex(Err.Number) & ")" & vbNewLine & Err.Description
    End If
    objCatSneezerRole = Nothing
    objRolesForDogColl = Nothing
    objDog = Nothing
    objZooComponentsColl = Nothing
    objAllergicToCatsRole = Nothing
    objZooKeeperRole = Nothing
    objRolesColl = Nothing
    objZooApp = Nothing
    objApplicationsColl = Nothing
    objCatalog = Nothing
Exit Function
```



## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Operazioni di amministrazione COM+ all'interno delle transazioni](com--administration-operations-within-transactions.md)
</dt> <dt>

[Gestione degli errori di amministrazione COM+](handling-com--administration-errors.md)
</dt> <dt>

[Panoramica degli oggetti COMAdmin](overview-of-the-comadmin-objects.md)
</dt> <dt>

[Recupero di raccolte nel catalogo COM+](retrieving-collections-on-the-com--catalog.md)
</dt> <dt>

[Impostazione delle proprietà e salvataggio delle modifiche nel catalogo COM+](setting-properties-and-saving-changes-to-the-com--catalog.md)
</dt> </dl>

 

 



