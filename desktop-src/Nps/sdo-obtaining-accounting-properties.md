---
title: Recupero delle proprietà di contabilità
description: L'oggetto contabilità è uno degli oggetti nella raccolta di gestori di richieste.
ms.assetid: eb5c8606-d3f0-4c33-9035-7b7b1369cb0d
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9911397c1de3521ccb5a275405416d8b88c1fa6f
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104399304"
---
# <a name="obtaining-accounting-properties"></a><span data-ttu-id="6e9ea-103">Recupero delle proprietà di contabilità</span><span class="sxs-lookup"><span data-stu-id="6e9ea-103">Obtaining Accounting Properties</span></span>

> [!Note]  
> <span data-ttu-id="6e9ea-104">Il servizio di autenticazione Internet (IAS) è stato rinominato server dei criteri di rete (NPS) a partire da Windows Server 2008.</span><span class="sxs-lookup"><span data-stu-id="6e9ea-104">Internet Authentication Service (IAS) was renamed Network Policy Server (NPS) starting with Windows Server 2008.</span></span> <span data-ttu-id="6e9ea-105">Il contenuto di questo argomento si applica sia a IAS che a NPS.</span><span class="sxs-lookup"><span data-stu-id="6e9ea-105">The content of this topic applies to both IAS and NPS.</span></span> <span data-ttu-id="6e9ea-106">In tutto il testo, NPS viene utilizzato per fare riferimento a tutte le versioni del servizio, incluse le versioni originariamente indicate come IAS.</span><span class="sxs-lookup"><span data-stu-id="6e9ea-106">Throughout the text, NPS is used to refer to all versions of the service, including the versions originally referred to as IAS.</span></span>

 

<span data-ttu-id="6e9ea-107">L'oggetto contabilità è uno degli oggetti nella raccolta di gestori di richieste.</span><span class="sxs-lookup"><span data-stu-id="6e9ea-107">The accounting object is one of the objects in the Request Handlers collection.</span></span> <span data-ttu-id="6e9ea-108">Il valore di enumerazione per la raccolta di gestori di richieste è la **proprietà \_ IAS \_ REQUESTHANDLERS \_ Collection**.</span><span class="sxs-lookup"><span data-stu-id="6e9ea-108">The enumeration value for the request handlers collection is **PROPERTY\_IAS\_REQUESTHANDLERS\_COLLECTION**.</span></span> <span data-ttu-id="6e9ea-109">Il nome del gestore per l'oggetto contabilità è "contabilità Microsoft".</span><span class="sxs-lookup"><span data-stu-id="6e9ea-109">The name of the handler for the accounting object is "Microsoft Accounting".</span></span>

<span data-ttu-id="6e9ea-110">Il codice Visual Basic seguente accede alle proprietà disponibili dal gestore dell'oggetto contabilità.</span><span class="sxs-lookup"><span data-stu-id="6e9ea-110">The following Visual Basic code accesses the properties available from the accounting object handler.</span></span>


```VB
Set sdoRequestHandler = sdoCollRequestHandlers.Item("Microsoft Accounting")
vtTemp = sdoRequestHandler.GetProperty(PROPERTY_ACCOUNTING_LOG_ACCOUNTING)
vtTemp = sdoRequestHandler.GetProperty(PROPERTY_ACCOUNTING_LOG_ACCOUNTING_INTERIM)
vtTemp = sdoRequestHandler.GetProperty(PROPERTY_ACCOUNTING_LOG_AUTHENTICATION)
vtTemp = sdoRequestHandler.GetProperty(PROPERTY_ACCOUNTING_LOG_FILE_DIRECTORY)
vtTemp = sdoRequestHandler.GetProperty(PROPERTY_ACCOUNTING_LOG_IAS1_FORMAT)
vtTemp = sdoRequestHandler.GetProperty(PROPERTY_ACCOUNTING_LOG_OPEN_NEW_FREQUENCY)
vtTemp = sdoRequestHandler.GetProperty(PROPERTY_ACCOUNTING_LOG_OPEN_NEW_SIZE)
```



<span data-ttu-id="6e9ea-111">Per accedere alle proprietà di contabilità con C++, ottenere prima la raccolta di gestori di richieste.</span><span class="sxs-lookup"><span data-stu-id="6e9ea-111">To access the accounting properties using C++, first obtain the request handlers collection.</span></span> <span data-ttu-id="6e9ea-112">Il [recupero di una raccolta](/windows/desktop/Nps/sdo-retrieving-a-collection) contiene codice C++ che illustra come ottenere una raccolta.</span><span class="sxs-lookup"><span data-stu-id="6e9ea-112">The [Retrieving a Collection](/windows/desktop/Nps/sdo-retrieving-a-collection) contains C++ code that demonstrates how to obtain a collection.</span></span> <span data-ttu-id="6e9ea-113">Il valore di enumerazione per la raccolta di gestori di richieste è la **proprietà \_ IAS \_ REQUESTHANDLERS \_ Collection**.</span><span class="sxs-lookup"><span data-stu-id="6e9ea-113">The enumeration value for the request handlers collection is **PROPERTY\_IAS\_REQUESTHANDLERS\_COLLECTION**.</span></span> <span data-ttu-id="6e9ea-114">I valori corrispondenti alle varie raccolte NPS vengono enumerati dal tipo di enumerazione [**IASPROPERTIES**](/windows/desktop/api/sdoias/ne-sdoias-iasproperties) .</span><span class="sxs-lookup"><span data-stu-id="6e9ea-114">(The values corresponding to the various NPS collections are enumerated by the [**IASPROPERTIES**](/windows/desktop/api/sdoias/ne-sdoias-iasproperties) enumeration type.)</span></span>

<span data-ttu-id="6e9ea-115">La raccolta di gestori di richieste contiene un oggetto denominato "Microsoft Accounting".</span><span class="sxs-lookup"><span data-stu-id="6e9ea-115">The request handlers collection contains an object named "Microsoft Accounting".</span></span> <span data-ttu-id="6e9ea-116">Recuperare questo oggetto dalla raccolta.</span><span class="sxs-lookup"><span data-stu-id="6e9ea-116">Retrieve this object from the collection.</span></span> <span data-ttu-id="6e9ea-117">La sezione [recupero di un oggetto da una raccolta](/windows/desktop/Nps/sdo-retrieving-an-object-from-a-collection) contiene codice C++ che illustra come ottenere un oggetto da una raccolta.</span><span class="sxs-lookup"><span data-stu-id="6e9ea-117">The section [Retrieving an Object from a Collection](/windows/desktop/Nps/sdo-retrieving-an-object-from-a-collection) contains C++ code that demonstrates how to obtain an object from a collection.</span></span>

<span data-ttu-id="6e9ea-118">Una volta ottenuto l'oggetto Accounting Microsoft, ottenere un'interfaccia [**ISdo**](/windows/desktop/api/sdoias/nn-sdoias-isdo) per l'oggetto usando [**IUnknown:: QueryInterface**](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)).</span><span class="sxs-lookup"><span data-stu-id="6e9ea-118">Once you have the Microsoft Accounting object, obtain an [**ISdo**](/windows/desktop/api/sdoias/nn-sdoias-isdo) interface for the object using [**IUnknown::QueryInterface**](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)).</span></span> <span data-ttu-id="6e9ea-119">La sezione [recupero di un SDO utente](/windows/desktop/Nps/sdo-retrieving-a-user-sdo) contiene codice C++ che illustra come ottenere un'interfaccia **ISdo** per un oggetto.</span><span class="sxs-lookup"><span data-stu-id="6e9ea-119">The section [Retrieving a User SDO](/windows/desktop/Nps/sdo-retrieving-a-user-sdo) contains C++ code that demonstrates how obtain an **ISdo** interface for an object.</span></span> <span data-ttu-id="6e9ea-120">È quindi possibile usare il metodo [**ISdo:: GetProperty**](/windows/desktop/api/sdoias/nf-sdoias-isdo-getproperty) per ottenere i valori delle proprietà per l'oggetto Accounting Microsoft.</span><span class="sxs-lookup"><span data-stu-id="6e9ea-120">You can then use the [**ISdo::GetProperty**](/windows/desktop/api/sdoias/nf-sdoias-isdo-getproperty) method to obtain property values for the Microsoft Accounting object.</span></span>

## <a name="related-topics"></a><span data-ttu-id="6e9ea-121">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="6e9ea-121">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="6e9ea-122">Recupero di una raccolta</span><span class="sxs-lookup"><span data-stu-id="6e9ea-122">Retrieving a Collection</span></span>](/windows/desktop/Nps/sdo-retrieving-a-collection)
</dt> <dt>

[<span data-ttu-id="6e9ea-123">Recupero di un oggetto da una raccolta</span><span class="sxs-lookup"><span data-stu-id="6e9ea-123">Retrieving an Object from a Collection</span></span>](/windows/desktop/Nps/sdo-retrieving-an-object-from-a-collection)
</dt> <dt>

[<span data-ttu-id="6e9ea-124">Recupero di un utente SDO</span><span class="sxs-lookup"><span data-stu-id="6e9ea-124">Retrieving a User SDO</span></span>](/windows/desktop/Nps/sdo-retrieving-a-user-sdo)
</dt> <dt>

[<span data-ttu-id="6e9ea-125">**ISdo**</span><span class="sxs-lookup"><span data-stu-id="6e9ea-125">**ISdo**</span></span>](/windows/desktop/api/sdoias/nn-sdoias-isdo)
</dt> <dt>

<span data-ttu-id="6e9ea-126">[**IUnknown:: QueryInterface**](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q))</span><span class="sxs-lookup"><span data-stu-id="6e9ea-126">[**IUnknown::QueryInterface**](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q))</span></span>
</dt> <dt>

[<span data-ttu-id="6e9ea-127">**IASPROPERTIES**</span><span class="sxs-lookup"><span data-stu-id="6e9ea-127">**IASPROPERTIES**</span></span>](/windows/desktop/api/sdoias/ne-sdoias-iasproperties)
</dt> </dl>

 

 