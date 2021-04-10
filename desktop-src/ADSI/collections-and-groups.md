---
title: Raccolte e gruppi
description: ADSI utilizza oggetti raccolta per rappresentare qualsiasi set arbitrario di elementi in un servizio directory che possono essere rappresentati utilizzando lo stesso tipo di dati.
ms.assetid: 03257cc9-f354-4e1c-8880-936a7acac3ef
ms.tgt_platform: multiple
keywords:
- ADSI ADSI, utilizzo, raccolte e gruppi
- ADSI Collections
- ADSI per gruppi
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a9f0f4d699d8dde0c3d70c7449dfe146212b2b30
ms.sourcegitcommit: b0ebdefc3dcd5c04bede94091833aa1015a2f95c
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/21/2020
ms.locfileid: "103963443"
---
# <a name="collections-and-groups"></a><span data-ttu-id="671ce-106">Raccolte e gruppi</span><span class="sxs-lookup"><span data-stu-id="671ce-106">Collections and Groups</span></span>

<span data-ttu-id="671ce-107">ADSI utilizza oggetti raccolta per rappresentare qualsiasi set arbitrario di elementi in un servizio directory che possono essere rappresentati utilizzando lo stesso tipo di dati.</span><span class="sxs-lookup"><span data-stu-id="671ce-107">ADSI uses collection objects to represent any arbitrary set of items in a directory service that can be represented using the same data type.</span></span> <span data-ttu-id="671ce-108">Gli oggetti della raccolta vengono definiti come un set di valori **Variant** , che rappresenta uno dei tipi di dati di automazione validi.</span><span class="sxs-lookup"><span data-stu-id="671ce-108">Collection objects are defined as a set of **VARIANT** values, representing any of the valid Automation data types.</span></span> <span data-ttu-id="671ce-109">Gli oggetti della raccolta possono rappresentare entrambe le informazioni persistenti, ad esempio elenchi di controllo di accesso e informazioni volatili, ad esempio i processi di stampa in una coda di stampa.</span><span class="sxs-lookup"><span data-stu-id="671ce-109">Collection objects can represent both persistent information such as access-control lists and volatile information such as print jobs in a print queue.</span></span>

<span data-ttu-id="671ce-110">La convenzione COM standard per elencare il contenuto di un oggetto raccolta (o contenitore) consiste nel creare un oggetto enumeratore che supporti [**IEnumVARIANT**](/windows/win32/api/oaidl/nn-oaidl-ienumvariant), che dispone di metodi per scorrere l'elenco di oggetti raccolta.</span><span class="sxs-lookup"><span data-stu-id="671ce-110">The standard COM convention for listing the contents of a collection (or container) object is to create an enumerator object that supports [**IEnumVARIANT**](/windows/win32/api/oaidl/nn-oaidl-ienumvariant), which has methods to step through the list of collection objects.</span></span> <span data-ttu-id="671ce-111">Le interfacce in ADSI che forniscono il metodo **get \_ \_ NewEnum** (si notino i due caratteri di sottolineatura) sono [**IADsContainer**](/windows/desktop/api/Iads/nn-iads-iadscontainer), [**IADsMembers**](/windows/desktop/api/Iads/nn-iads-iadsmembers) e [**IADsCollection**](/windows/desktop/api/Iads/nn-iads-iadscollection).</span><span class="sxs-lookup"><span data-stu-id="671ce-111">The interfaces in ADSI that supply the **get\_\_NewEnum** method (note the two underscores) are [**IADsContainer**](/windows/desktop/api/Iads/nn-iads-iadscontainer), [**IADsMembers**](/windows/desktop/api/Iads/nn-iads-iadsmembers) and [**IADsCollection**](/windows/desktop/api/Iads/nn-iads-iadscollection).</span></span> <span data-ttu-id="671ce-112">ADSI fornisce anche le funzioni di supporto [**ADsBuildEnumerator**](/windows/desktop/api/Adshlp/nf-adshlp-adsbuildenumerator) e [**ADsEnumerateNext**](/windows/desktop/api/Adshlp/nf-adshlp-adsenumeratenext) per i programmi C e C++ per semplificare l'enumerazione.</span><span class="sxs-lookup"><span data-stu-id="671ce-112">ADSI also supplies the helper functions [**ADsBuildEnumerator**](/windows/desktop/api/Adshlp/nf-adshlp-adsbuildenumerator) and [**ADsEnumerateNext**](/windows/desktop/api/Adshlp/nf-adshlp-adsenumeratenext) for C and C++ programs to simplify enumeration.</span></span> <span data-ttu-id="671ce-113">I client di automazione usano l'enumerazione in modo implicito quando chiamano **Next** in un ciclo **for** .</span><span class="sxs-lookup"><span data-stu-id="671ce-113">Automation clients use enumeration implicitly when they call **Next** in a **For** loop.</span></span>

<span data-ttu-id="671ce-114">I gruppi sono semplicemente raccolte di oggetti che supportano l'interfaccia [**IADsMembers**](/windows/desktop/api/Iads/nn-iads-iadsmembers) .</span><span class="sxs-lookup"><span data-stu-id="671ce-114">Groups are simply collections of objects supporting the [**IADsMembers**](/windows/desktop/api/Iads/nn-iads-iadsmembers) interface.</span></span>

 

 