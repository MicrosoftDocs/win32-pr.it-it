---
title: Rivisitazione di regole di aggregazione COM con estensioni ADSI
description: Di seguito viene riportata una breve panoramica delle regole di aggregazione COM e di estensione ADSI.
ms.assetid: 3efcdfcf-4965-4436-90b2-dc0f627c71b4
ms.tgt_platform: multiple
keywords:
- Estensioni ADSI, regole di aggregazione COM
- ADSI aggregazione COM
- Rivisitazione di regole di aggregazione COM con ADSI Extensions ADSI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3e9b3e3614c4adc225883f120f8fbf362df3e646
ms.sourcegitcommit: b0ebdefc3dcd5c04bede94091833aa1015a2f95c
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/21/2020
ms.locfileid: "103730258"
---
# <a name="revisiting-com-aggregation-rules-with-adsi-extensions"></a><span data-ttu-id="fab09-106">Rivisitazione di regole di aggregazione COM con estensioni ADSI</span><span class="sxs-lookup"><span data-stu-id="fab09-106">Revisiting COM Aggregation Rules with ADSI Extensions</span></span>

<span data-ttu-id="fab09-107">Di seguito viene riportata una breve panoramica delle regole di aggregazione COM e di estensione ADSI.</span><span class="sxs-lookup"><span data-stu-id="fab09-107">The following is a brief review of COM aggregation and ADSI extension rules.</span></span>

-   <span data-ttu-id="fab09-108">Il metodo **CreateInstance** restituisce un puntatore a un'interfaccia [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) , come indicato di seguito, che non delega alcuna chiamata di funzione a Aggregator.</span><span class="sxs-lookup"><span data-stu-id="fab09-108">The **CreateInstance** method returns a pointer to an [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) interface, as follows, that does not delegate any function calls to the aggregator.</span></span>

    <span data-ttu-id="fab09-109">Il metodo [**IUnknown:: QueryInterface**](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) restituisce i puntatori alle interfacce supportate ed errori per le interfacce che non supporta.</span><span class="sxs-lookup"><span data-stu-id="fab09-109">The [**IUnknown::QueryInterface**](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) method returns pointers to the interfaces that it supports, and errors for interfaces it does not support.</span></span>

    <span data-ttu-id="fab09-110">Il metodo [**IUnknown:: AddRef**](/windows/win32/api/unknwn/nf-unknwn-iunknown-addref) incrementa il conteggio dei riferimenti nell'oggetto di estensione aggregato.</span><span class="sxs-lookup"><span data-stu-id="fab09-110">The [**IUnknown::AddRef**](/windows/win32/api/unknwn/nf-unknwn-iunknown-addref) method increments the reference count on the aggregated extension object itself.</span></span>

    <span data-ttu-id="fab09-111">Il metodo [**IUnkown:: Release**](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) decrementa il conteggio dei riferimenti nell'oggetto estensione aggregato stesso e si elimina da solo quando il conteggio dei riferimenti è 0.</span><span class="sxs-lookup"><span data-stu-id="fab09-111">The [**IUnkown::Release**](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) method decrements the reference count on the aggregated extension object itself and destroys itself when the reference count is 0.</span></span>

-   <span data-ttu-id="fab09-112">L'oggetto estensione deve archiviare il puntatore [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) di aggregator, ad esempio m \_ pOuterUnknown, durante l'implementazione del metodo **CreateInstance** .</span><span class="sxs-lookup"><span data-stu-id="fab09-112">The extension object should store the [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) pointer of the aggregator, such as m\_pOuterUnknown, during the implementation of the **CreateInstance** method.</span></span>
-   <span data-ttu-id="fab09-113">Tutte le interfacce supportate dall'oggetto di estensione, incluso [**IADsExtension**](/windows/desktop/api/Iads/nn-iads-iadsextension), devono ereditare da [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown), che delega tutte le chiamate di funzione a Aggregator.</span><span class="sxs-lookup"><span data-stu-id="fab09-113">All interfaces that the extension object supports, including [**IADsExtension**](/windows/desktop/api/Iads/nn-iads-iadsextension), should inherit from [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown), which delegates all function calls back to the aggregator.</span></span>
    -   <span data-ttu-id="fab09-114">[**IUnknown:: QueryInterface**](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) chiama "m \_ POuterUnknown->QueryInterface"</span><span class="sxs-lookup"><span data-stu-id="fab09-114">[**IUnknown::QueryInterface**](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) calls "m\_pOuterUnknown->QueryInterface"</span></span>
    -   <span data-ttu-id="fab09-115">[**IUnknown:: AddRef**](/windows/win32/api/unknwn/nf-unknwn-iunknown-addref) chiama "m \_ POuterUnknown->AddRef"</span><span class="sxs-lookup"><span data-stu-id="fab09-115">[**IUnknown::AddRef**](/windows/win32/api/unknwn/nf-unknwn-iunknown-addref) calls "m\_pOuterUnknown->AddRef"</span></span>
    -   <span data-ttu-id="fab09-116">[**IUnkown:: Release**](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) chiama "m \_ POuterUnknown->Release"</span><span class="sxs-lookup"><span data-stu-id="fab09-116">[**IUnkown::Release**](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) calls "m\_pOuterUnknown->Release"</span></span>

<span data-ttu-id="fab09-117">I writer di estensione possono scegliere qualsiasi implementazione interna che preferiscono purché rispettino le regole di aggregazione COM standard.</span><span class="sxs-lookup"><span data-stu-id="fab09-117">Extension writers can choose any internal implementation they prefer as long as they obey standard COM aggregation rules.</span></span> <span data-ttu-id="fab09-118">Tenere presente che non è necessario che un oggetto estensione funzioni come oggetto autonomo.</span><span class="sxs-lookup"><span data-stu-id="fab09-118">Be aware that an extension object does not have to work as a standalone object.</span></span> <span data-ttu-id="fab09-119">Le estensioni sono progettate per funzionare come aggregati.</span><span class="sxs-lookup"><span data-stu-id="fab09-119">Extensions are designed to work as aggregates.</span></span> <span data-ttu-id="fab09-120">Tuttavia, un'estensione può essere scritta per funzionare sia come oggetto autonomo che come aggregato.</span><span class="sxs-lookup"><span data-stu-id="fab09-120">However, an extension can be written to work as both a standalone object and as an aggregate.</span></span>

<span data-ttu-id="fab09-121">Oltre al supporto di aggregazione COM standard, un oggetto estensione può supportare [**IADsExtension**](/windows/desktop/api/Iads/nn-iads-iadsextension) per funzionalità più avanzate.</span><span class="sxs-lookup"><span data-stu-id="fab09-121">In addition to standard COM aggregation support, an extension object may support [**IADsExtension**](/windows/desktop/api/Iads/nn-iads-iadsextension) for more advanced features.</span></span> <span data-ttu-id="fab09-122">Se l'associazione tardiva è supportata, l'estensione deve:</span><span class="sxs-lookup"><span data-stu-id="fab09-122">If late binding is supported, the extension should:</span></span>

-   <span data-ttu-id="fab09-123">Funzioni delegate per [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) di nuovo all'aggregatore.</span><span class="sxs-lookup"><span data-stu-id="fab09-123">Delegate functions for [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) back to the aggregator.</span></span>
-   <span data-ttu-id="fab09-124">Implementare l'interfaccia [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) in [**IADsExtension**](/windows/desktop/api/Iads/nn-iads-iadsextension).</span><span class="sxs-lookup"><span data-stu-id="fab09-124">Implement the [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) interface in [**IADsExtension**](/windows/desktop/api/Iads/nn-iads-iadsextension).</span></span>

 

 