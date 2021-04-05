---
title: Interfaccia ITfContextRenderingMarkup
description: L'interfaccia ITfContextRenderingMarkup viene implementata da TSF Manager e utilizzata dalle applicazioni. Questa interfaccia può essere recuperata usando IQueryInterface dall'oggetto ITfContext. Questa interfaccia consente all'applicazione di enumerare le informazioni di rendering.
ms.assetid: 733d2db2-f9e9-4b78-af13-adc03825bf2b
keywords:
- Framework servizi di testo interfaccia ITfContextRenderingMarkup
- Framework dei servizi di testo dell'interfaccia ITfContextRenderingMarkup, descritto
topic_type:
- apiref
api_name:
- ITfContextRenderingMarkup
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 1b71e977665a4b3a6e817ef782ee558064e0986a
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "103872694"
---
# <a name="itfcontextrenderingmarkup-interface"></a><span data-ttu-id="87e47-107">Interfaccia ITfContextRenderingMarkup</span><span class="sxs-lookup"><span data-stu-id="87e47-107">ITfContextRenderingMarkup interface</span></span>

<span data-ttu-id="87e47-108">L'interfaccia **ITfContextRenderingMarkup** viene implementata da TSF Manager e utilizzata dalle applicazioni.</span><span class="sxs-lookup"><span data-stu-id="87e47-108">The **ITfContextRenderingMarkup** interface is implemented by TSF manager and used by applications.</span></span> <span data-ttu-id="87e47-109">Questa interfaccia può essere recuperata usando IQueryInterface dall'oggetto [ITfContext](/windows/desktop/api/Msctf/nn-msctf-itfcontext) .</span><span class="sxs-lookup"><span data-stu-id="87e47-109">This interface can be retrieved using IQueryInterface from [ITfContext](/windows/desktop/api/Msctf/nn-msctf-itfcontext) object.</span></span> <span data-ttu-id="87e47-110">Questa interfaccia consente all'applicazione di enumerare le informazioni di rendering.</span><span class="sxs-lookup"><span data-stu-id="87e47-110">This interface helps the application enumerate rendering information.</span></span>



| <span data-ttu-id="87e47-111">Metodi ITfContextRenderingMarkup</span><span class="sxs-lookup"><span data-stu-id="87e47-111">ITfContextRenderingMarkup methods</span></span>                                                | <span data-ttu-id="87e47-112">Descrizione</span><span class="sxs-lookup"><span data-stu-id="87e47-112">Description</span></span>                                                           |
|----------------------------------------------------------------------------------|-----------------------------------------------------------------------|
| [<span data-ttu-id="87e47-113">GetRenderingMarkup</span><span class="sxs-lookup"><span data-stu-id="87e47-113">GetRenderingMarkup</span></span>](itfcontextrenderingmarkup-getrenderingmarkup.md)           | <span data-ttu-id="87e47-114">Recupera un enumeratore dei markup di rendering per l'intervallo specificato.</span><span class="sxs-lookup"><span data-stu-id="87e47-114">Retrieves an enumerator of the rendering markups for the given range.</span></span> |
| [<span data-ttu-id="87e47-115">FindNextRenderingMarkup</span><span class="sxs-lookup"><span data-stu-id="87e47-115">FindNextRenderingMarkup</span></span>](itfcontextrenderingmarkup-findnextrenderingmarkup.md) | <span data-ttu-id="87e47-116">Questa funzione non è implementata.</span><span class="sxs-lookup"><span data-stu-id="87e47-116">This function is not implemented.</span></span> <span data-ttu-id="87e47-117">Restituisce sempre E \_ NOTIMPL.</span><span class="sxs-lookup"><span data-stu-id="87e47-117">It always returns E\_NOTIMPL.</span></span>       |



 

## <a name="members"></a><span data-ttu-id="87e47-118">Membri</span><span class="sxs-lookup"><span data-stu-id="87e47-118">Members</span></span>

<span data-ttu-id="87e47-119">L'interfaccia **ITfContextRenderingMarkup** eredita dall'interfaccia [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) ma non dispone di membri aggiuntivi.</span><span class="sxs-lookup"><span data-stu-id="87e47-119">The **ITfContextRenderingMarkup** interface inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface but does not have additional members.</span></span>

## <a name="remarks"></a><span data-ttu-id="87e47-120">Commenti</span><span class="sxs-lookup"><span data-stu-id="87e47-120">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="87e47-121">Questa interfaccia non è attualmente presente nei file di intestazione pubblici.</span><span class="sxs-lookup"><span data-stu-id="87e47-121">This interface is not currently in the public header files.</span></span> <span data-ttu-id="87e47-122">Per usare questa API, è necessario compilare MIDL per il [prototipo](prototypes.md).</span><span class="sxs-lookup"><span data-stu-id="87e47-122">To use this API, you must MIDL-compile the [prototype](prototypes.md).</span></span>

 

 

 