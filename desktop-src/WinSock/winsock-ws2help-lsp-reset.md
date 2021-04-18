---
description: Evento di modifica del catalogo Winsock per un'operazione di reimpostazione del catalogo Winsock.
ms.assetid: BE8DC0DB-0F96-4015-87F5-ECF25AE164AA
title: Evento WINSOCK_WS2HELP_LSP_RESET
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WINSOCK_WS2HELP_LSP_RESET
api_type:
- NA
api_location: ''
ms.openlocfilehash: 219eb85dec0cdda77ca8741ae42df1f63d1a7dbc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106315750"
---
# <a name="winsock_ws2help_lsp_reset-event"></a><span data-ttu-id="d047b-103">\_Evento di \_ reimpostazione di Winsock ws2help LSP \_</span><span class="sxs-lookup"><span data-stu-id="d047b-103">WINSOCK\_WS2HELP\_LSP\_RESET event</span></span>

> [!Note]  
> <span data-ttu-id="d047b-104">I provider di servizi sovrapposti sono deprecati.</span><span class="sxs-lookup"><span data-stu-id="d047b-104">Layered Service Providers are deprecated.</span></span> <span data-ttu-id="d047b-105">A partire da Windows 8 e Windows Server 2012, usare la [piattaforma filtro Windows](../fwp/windows-filtering-platform-start-page.md).</span><span class="sxs-lookup"><span data-stu-id="d047b-105">Starting with Windows 8 and Windows Server 2012, use [Windows Filtering Platform](../fwp/windows-filtering-platform-start-page.md).</span></span>

 

<span data-ttu-id="d047b-106">L'evento di **\_ \_ \_ reimpostazione di Winsock ws2help LSP** è un evento di modifica del catalogo Winsock per un'operazione di reimpostazione del catalogo Winsock.</span><span class="sxs-lookup"><span data-stu-id="d047b-106">The **WINSOCK\_WS2HELP\_LSP\_RESET** event is a Winsock catalog change event for a Winsock catalog reset operation.</span></span>


```C++
const EVENT_DESCRIPTOR WINSOCK_WS2HELP_LSP_RESET = {0x4, 0x0, 0x10, 0x0, 0x0, 0x0, 0x8000000000000000};
```



## <a name="parameters"></a><span data-ttu-id="d047b-107">Parametri</span><span class="sxs-lookup"><span data-stu-id="d047b-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d047b-108">*Catalogo*</span><span class="sxs-lookup"><span data-stu-id="d047b-108">*Catalog*</span></span> 
</dt> <dd>

<span data-ttu-id="d047b-109">Il catalogo Winsock (32 bit o 64 bit) che viene reimpostato.</span><span class="sxs-lookup"><span data-stu-id="d047b-109">The Winsock catalog (32-bit or 64-bit) that is being reset.</span></span> <span data-ttu-id="d047b-110">Si tratta di un valore intero che può essere 32 o 64.</span><span class="sxs-lookup"><span data-stu-id="d047b-110">This is an integer value that is either 32 or 64.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="d047b-111">Commenti</span><span class="sxs-lookup"><span data-stu-id="d047b-111">Remarks</span></span>

<span data-ttu-id="d047b-112">L'evento di **\_ \_ \_ reimpostazione di Winsock ws2help LSP** viene tracciato per un'operazione LSP (Layered Service Provider) Winsock quando viene reimpostato il catalogo Winsock.</span><span class="sxs-lookup"><span data-stu-id="d047b-112">The **WINSOCK\_WS2HELP\_LSP\_RESET** event is traced for an Winsock Layered Service Provider (LSP) operation when the Winsock catalog is reset.</span></span>

## <a name="requirements"></a><span data-ttu-id="d047b-113">Requisiti</span><span class="sxs-lookup"><span data-stu-id="d047b-113">Requirements</span></span>



| <span data-ttu-id="d047b-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="d047b-114">Requirement</span></span> | <span data-ttu-id="d047b-115">Valore</span><span class="sxs-lookup"><span data-stu-id="d047b-115">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="d047b-116">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="d047b-116">Minimum supported client</span></span><br/> | <span data-ttu-id="d047b-117">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="d047b-117">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="d047b-118">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="d047b-118">Minimum supported server</span></span><br/> | <span data-ttu-id="d047b-119">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="d047b-119">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="d047b-120">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="d047b-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d047b-121">Controllo della traccia Winsock</span><span class="sxs-lookup"><span data-stu-id="d047b-121">Control of Winsock Tracing</span></span>](control-of-winsock-tracing.md)
</dt> <dt>

[<span data-ttu-id="d047b-122">Traccia Winsock</span><span class="sxs-lookup"><span data-stu-id="d047b-122">Winsock Tracing</span></span>](winsock-tracing.md)
</dt> <dt>

[<span data-ttu-id="d047b-123">Livelli di traccia Winsock</span><span class="sxs-lookup"><span data-stu-id="d047b-123">Winsock Tracing Levels</span></span>](winsock-tracing-levels.md)
</dt> <dt>

[<span data-ttu-id="d047b-124">Dettagli della traccia delle modifiche del catalogo Winsock</span><span class="sxs-lookup"><span data-stu-id="d047b-124">Winsock Catalog Change Tracing Details</span></span>](winsock-layered-service-provider-tracing-event-details.md)
</dt> </dl>

 

 
