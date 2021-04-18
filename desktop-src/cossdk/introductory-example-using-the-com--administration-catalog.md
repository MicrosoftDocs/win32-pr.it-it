---
description: Esempio introduttivo di utilizzo del catalogo di amministrazione COM+
ms.assetid: e9ce25aa-4fb1-4357-9f4e-5bf649e29447
title: Esempio introduttivo di utilizzo del catalogo di amministrazione COM+
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: db24f3985538b7189534c9fef3ef279ed240e3a1
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106305218"
---
# <a name="introductory-example-using-the-com-administration-catalog"></a><span data-ttu-id="e006f-103">Esempio introduttivo di utilizzo del catalogo di amministrazione COM+</span><span class="sxs-lookup"><span data-stu-id="e006f-103">Introductory Example Using the COM+ Administration Catalog</span></span>

<span data-ttu-id="e006f-104">Quando si usa il catalogo di amministrazione COM+ a livello di codice, in genere si eseguono i passaggi generali seguenti (non specificati in un ordine rigoroso):</span><span class="sxs-lookup"><span data-stu-id="e006f-104">When programmatically using the COM+ Administration catalog, you typically carry out the following general steps (not given in a strict order here):</span></span>

-   <span data-ttu-id="e006f-105">Aprire una sessione di con il catalogo COM+ nel computer locale.</span><span class="sxs-lookup"><span data-stu-id="e006f-105">Open a session with the COM+ catalog on the local machine.</span></span> <span data-ttu-id="e006f-106">Facoltativamente, connettersi al catalogo COM+ in un computer remoto.</span><span class="sxs-lookup"><span data-stu-id="e006f-106">Optionally, connect to the COM+ catalog on a remote machine.</span></span>
-   <span data-ttu-id="e006f-107">Eseguire azioni quali l'avvio o l'arresto di servizi, ovvero azioni che non riguardano una particolare applicazione COM+.</span><span class="sxs-lookup"><span data-stu-id="e006f-107">Perform actions such as starting or stopping services—actions that don't pertain to a particular COM+ application.</span></span>
-   <span data-ttu-id="e006f-108">Eseguire azioni quali l'installazione o l'esportazione di applicazioni COM+ o l'installazione di componenti in applicazioni, ovvero azioni che riguardano la lettura o la scrittura su file.</span><span class="sxs-lookup"><span data-stu-id="e006f-108">Perform actions such as installing or exporting COM+ applications, or installing components into applications—actions that pertain to reading from or writing to files.</span></span>
-   <span data-ttu-id="e006f-109">Aggiungere nuovi elementi alle raccolte, ad esempio creando una nuova applicazione COM+ aggiungendo un nuovo elemento alla raccolta "Applications".</span><span class="sxs-lookup"><span data-stu-id="e006f-109">Add new items to collections, such as creating a new COM+ application by adding a new item to the "Applications" collection.</span></span>
-   <span data-ttu-id="e006f-110">Imposta o ottiene le proprietà di un elemento in una raccolta.</span><span class="sxs-lookup"><span data-stu-id="e006f-110">Set or get properties on an item in a collection.</span></span>
-   <span data-ttu-id="e006f-111">Salvare o rimuovere le modifiche in sospeso nel catalogo.</span><span class="sxs-lookup"><span data-stu-id="e006f-111">Save or discard pending changes to the catalog.</span></span>
-   <span data-ttu-id="e006f-112">Gestire gli eventuali errori che potrebbero verificarsi.</span><span class="sxs-lookup"><span data-stu-id="e006f-112">Handle any errors that might occur.</span></span>

<span data-ttu-id="e006f-113">Per visualizzare l'aspetto di questi passaggi quando si usano gli oggetti COMAdmin, viene fornito un esempio di Visual Basic Microsoft.</span><span class="sxs-lookup"><span data-stu-id="e006f-113">To show what these steps look like when you use the COMAdmin objects, a Microsoft Visual Basic example is provided below.</span></span> <span data-ttu-id="e006f-114">Vengono brevemente illustrati alcuni dei passaggi tipici descritti in precedenza, ad esempio l'individuazione di raccolte, l'enumerazione di una raccolta per recuperare un elemento e l'impostazione delle proprietà di tale elemento.</span><span class="sxs-lookup"><span data-stu-id="e006f-114">It briefly illustrates some of the typical steps described above, such as locating collections, enumerating through a collection to retrieve an item, and setting properties on that item.</span></span>

<span data-ttu-id="e006f-115">Nell'esempio seguente vengono eseguite le azioni seguenti:</span><span class="sxs-lookup"><span data-stu-id="e006f-115">In the example below you will perform the following actions:</span></span>

1.  <span data-ttu-id="e006f-116">Creare una nuova applicazione COM+, "MyHomeZoo".</span><span class="sxs-lookup"><span data-stu-id="e006f-116">Create a new COM+ application, "MyHomeZoo".</span></span>
2.  <span data-ttu-id="e006f-117">Installare alcuni componenti, cat e Dog, nell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="e006f-117">Install some components, Cat and Dog, into the application.</span></span> <span data-ttu-id="e006f-118">Entrambi i componenti sono contenuti in una singola DLL che deve esistere già: MyZoo.dll.</span><span class="sxs-lookup"><span data-stu-id="e006f-118">Both components are contained in a single DLL that must already exist: MyZoo.dll.</span></span>
3.  <span data-ttu-id="e006f-119">Configurare la sicurezza basata sui ruoli per l'applicazione definendo due ruoli: ZooKeeper e AllergicToCats.</span><span class="sxs-lookup"><span data-stu-id="e006f-119">Configure role-based security for the application by defining two roles: ZooKeeper and AllergicToCats.</span></span>
4.  <span data-ttu-id="e006f-120">Assegnare il ruolo ZooKeeper per l'accesso all'intera applicazione.</span><span class="sxs-lookup"><span data-stu-id="e006f-120">Assign the ZooKeeper role access to the entire application.</span></span>
5.  <span data-ttu-id="e006f-121">Assegnare il ruolo AllergicToCats accesso solo al componente Dog.</span><span class="sxs-lookup"><span data-stu-id="e006f-121">Assign the AllergicToCats role access to only the Dog component.</span></span>
6.  <span data-ttu-id="e006f-122">Attivare le proprietà di sicurezza in modo che il controllo dei ruoli venga applicato per l'applicazione.</span><span class="sxs-lookup"><span data-stu-id="e006f-122">Turn on security properties so that role checking will be enforced for the application.</span></span>
7.  <span data-ttu-id="e006f-123">Esportare l'applicazione MyHomeZoo in un file in modo che possa essere installata in altri computer.</span><span class="sxs-lookup"><span data-stu-id="e006f-123">Export the MyHomeZoo application to a file so that it can be installed on other computers.</span></span>

<span data-ttu-id="e006f-124">Per usare questo esempio da Visual Basic, aggiungere un riferimento alla libreria dei tipi di amministrazione COM+.</span><span class="sxs-lookup"><span data-stu-id="e006f-124">To use this example from Visual Basic, add a reference to the COM+ Admin Type Library.</span></span>


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



## <a name="related-topics"></a><span data-ttu-id="e006f-125">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="e006f-125">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e006f-126">Operazioni di amministrazione COM+ all'interno delle transazioni</span><span class="sxs-lookup"><span data-stu-id="e006f-126">COM+ Administration Operations Within Transactions</span></span>](com--administration-operations-within-transactions.md)
</dt> <dt>

[<span data-ttu-id="e006f-127">Gestione degli errori di amministrazione COM+</span><span class="sxs-lookup"><span data-stu-id="e006f-127">Handling COM+ Administration Errors</span></span>](handling-com--administration-errors.md)
</dt> <dt>

[<span data-ttu-id="e006f-128">Panoramica degli oggetti COMAdmin</span><span class="sxs-lookup"><span data-stu-id="e006f-128">Overview of the COMAdmin Objects</span></span>](overview-of-the-comadmin-objects.md)
</dt> <dt>

[<span data-ttu-id="e006f-129">Recupero di raccolte nel catalogo COM+</span><span class="sxs-lookup"><span data-stu-id="e006f-129">Retrieving Collections on the COM+ Catalog</span></span>](retrieving-collections-on-the-com--catalog.md)
</dt> <dt>

[<span data-ttu-id="e006f-130">Impostazione delle proprietà e salvataggio delle modifiche nel catalogo COM+</span><span class="sxs-lookup"><span data-stu-id="e006f-130">Setting Properties and Saving Changes to the COM+ Catalog</span></span>](setting-properties-and-saving-changes-to-the-com--catalog.md)
</dt> </dl>

 

 



