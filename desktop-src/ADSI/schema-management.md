---
title: Gestione dello schema
description: Il componente provider di esempio ADSI definisce le classi dello schema \ 0034; unità organizzativa \ 0034; e \ 0034; Utente \ 0034; e gestisce queste classi dello schema nel modo seguente.
ms.assetid: c3e07846-a11e-46d4-9863-a89810896ad7
ms.tgt_platform: multiple
keywords:
- Gestione dello schema ADSI
- gestione dello schema ADSI
- gestione degli schemi ADSI
- schemi, gestione di ADSI
- gestione di uno schema ADSI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 99d398f8eb056498977f886e836c0f97c95f0b9b
ms.sourcegitcommit: b0ebdefc3dcd5c04bede94091833aa1015a2f95c
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/21/2020
ms.locfileid: "104560752"
---
# <a name="schema-management"></a><span data-ttu-id="44a2f-108">Gestione dello schema</span><span class="sxs-lookup"><span data-stu-id="44a2f-108">Schema Management</span></span>

<span data-ttu-id="44a2f-109">Il componente provider di esempio ADSI definisce le classi di schema "unità organizzativa" e "utente" e gestisce queste classi dello schema nel modo seguente.</span><span class="sxs-lookup"><span data-stu-id="44a2f-109">The ADSI example provider component defines the schema classes "Organizational Unit" and "User" and manages these schema classes in the following way.</span></span>

<span data-ttu-id="44a2f-110">La classe dello schema "unità organizzativa" è rappresentata da un oggetto contenitore ADs e può contenere altre "unità organizzative" e "utenti".</span><span class="sxs-lookup"><span data-stu-id="44a2f-110">The "Organizational Unit" schema class is represented by an ADs container object and can contain other "Organizational Units" and "Users".</span></span> <span data-ttu-id="44a2f-111">L'oggetto contenitore supporta le interfacce [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown), [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch), [**IADs**](/windows/desktop/api/Iads/nn-iads-iads)e [**IADsContainer**](/windows/desktop/api/Iads/nn-iads-iadscontainer).</span><span class="sxs-lookup"><span data-stu-id="44a2f-111">The container object supports the interfaces [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown), [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch), [**IADs**](/windows/desktop/api/Iads/nn-iads-iads), and [**IADsContainer**](/windows/desktop/api/Iads/nn-iads-iadscontainer).</span></span> <span data-ttu-id="44a2f-112">La classe dello schema "User" è rappresentata da un oggetto Active Directory generico e non contiene altri tipi di oggetti.</span><span class="sxs-lookup"><span data-stu-id="44a2f-112">The "User" schema class is represented by a generic Active Directory object and does not contain other types of objects.</span></span> <span data-ttu-id="44a2f-113">Nel componente provider di esempio, l'oggetto utente viene implementato come un oggetto Active Directory generico che supporta le interfacce **IUnknown**, **IDispatch** e **IADs**.</span><span class="sxs-lookup"><span data-stu-id="44a2f-113">In the example provider component, the User object is implemented as a generic Active Directory object that supports the interfaces **IUnknown**, **IDispatch**, and **IADs**.</span></span> <span data-ttu-id="44a2f-114">Tenere presente che l'oggetto utente, in questo caso, non supporta l'interfaccia [**IADsUser**](/windows/desktop/api/Iads/nn-iads-iadsuser) .</span><span class="sxs-lookup"><span data-stu-id="44a2f-114">Be aware that the User object, in this case, does not support the [**IADsUser**](/windows/desktop/api/Iads/nn-iads-iadsuser) interface.</span></span>

<span data-ttu-id="44a2f-115">Il componente provider di esempio deve implementare anche l'oggetto spazio dei nomi ADs, che supporta le interfacce [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown), [**IADs**](/windows/desktop/api/Iads/nn-iads-iads), [**IADsContainer**](/windows/desktop/api/Iads/nn-iads-iadscontainer), [**IADsOpenDSObject**](/windows/desktop/api/Iads/nn-iads-iadsopendsobject)e [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch).</span><span class="sxs-lookup"><span data-stu-id="44a2f-115">The example provider component must also implement the ADs namespace object, which supports the interfaces [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown), [**IADs**](/windows/desktop/api/Iads/nn-iads-iads), [**IADsContainer**](/windows/desktop/api/Iads/nn-iads-iadscontainer), [**IADsOpenDSObject**](/windows/desktop/api/Iads/nn-iads-iadsopendsobject), and [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch).</span></span>

<span data-ttu-id="44a2f-116">Nella figura seguente vengono illustrati i dettagli dello schema che rappresenta le due classi dello schema dei componenti del provider di esempio.</span><span class="sxs-lookup"><span data-stu-id="44a2f-116">The following figure shows the details of the schema that represents the two example provider component schema classes.</span></span>

![schema del componente provider di esempio ADSI](images/dssmsch.png)

<span data-ttu-id="44a2f-118">Tenere presente che nella figura precedente la classe dello schema "unità organizzativa" definisce tre proprietà: "Description", "headcounts" e "ID".</span><span class="sxs-lookup"><span data-stu-id="44a2f-118">Be aware that in the preceding figure the "Organizational Unit" schema class defines three properties: "Description," "Headcounts," and "ID."</span></span> <span data-ttu-id="44a2f-119">La classe dello schema "User" definisce quattro proprietà: "ID", "Name", "PhoneNumber" e "title".</span><span class="sxs-lookup"><span data-stu-id="44a2f-119">The "User" schema class defines four properties: "ID," "Name," "PhoneNumber," and "Title."</span></span> <span data-ttu-id="44a2f-120">La proprietà "ID" è condivisa da entrambe le classi di schema.</span><span class="sxs-lookup"><span data-stu-id="44a2f-120">The "ID" property is shared by both schema classes.</span></span> <span data-ttu-id="44a2f-121">Ogni proprietà è definita dall'oggetto sintassi "String" o "Integer".</span><span class="sxs-lookup"><span data-stu-id="44a2f-121">Each property is defined by either the "String" or the "Integer" syntax object.</span></span>

> [!Note]  
> <span data-ttu-id="44a2f-122">Gli oggetti sintassi non sono presenti nella prima versione del componente provider di esempio.</span><span class="sxs-lookup"><span data-stu-id="44a2f-122">Syntax objects are not present in the first release of the example provider component.</span></span> <span data-ttu-id="44a2f-123">Tuttavia, nella maggior parte delle implementazioni dello schema di Microsoft ADSI, gli oggetti sintassi sono inclusi nell'oggetto contenitore dello schema, così come gli oggetti classe e proprietà dello schema.</span><span class="sxs-lookup"><span data-stu-id="44a2f-123">However, in most Microsoft ADSI schema implementations, the syntax objects are included in the schema container object, just as the schema class and property objects are.</span></span> <span data-ttu-id="44a2f-124">Per questo motivo, vengono visualizzati qui.</span><span class="sxs-lookup"><span data-stu-id="44a2f-124">For this reason, they are shown here.</span></span>

 

<span data-ttu-id="44a2f-125">Questo componente del provider rende accessibili i dati dello schema all'applicazione client ADSI sotto forma di oggetti della classe ADs, oggetti proprietà ADs e oggetti sintassi ADs, tutti all'interno di un oggetto contenitore di classi di schema, in modo che i dati dello schema possano essere recuperati in fase di esecuzione.</span><span class="sxs-lookup"><span data-stu-id="44a2f-125">This provider component makes schema data accessible to the ADSI client application in the form of ADs class objects, ADs property objects, and ADs syntax objects, all within a schema class container object, so that schema data can be retrieved at run time.</span></span>

<span data-ttu-id="44a2f-126">ADsPaths per gli oggetti contenitore della classe dello schema definiti per il componente provider di esempio sono "Sample://Seattle/schema" e "Sample://Toronto/schema".</span><span class="sxs-lookup"><span data-stu-id="44a2f-126">The ADsPaths for the schema class container objects defined for the example provider component are "Sample://Seattle/schema" and "Sample://Toronto/schema".</span></span> <span data-ttu-id="44a2f-127">In questo esempio, il contenuto degli schemi è identico.</span><span class="sxs-lookup"><span data-stu-id="44a2f-127">In this example, the contents of the schemas are identical.</span></span>

 

 