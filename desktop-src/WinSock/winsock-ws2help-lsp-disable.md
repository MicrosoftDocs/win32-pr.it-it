---
description: Evento di modifica del catalogo Winsock per un'operazione di disabilitazione di un provider di servizi a più livelli (LSP).
ms.assetid: 6BCEECB1-92AD-47D8-952B-D0FD2A78EB45
title: Evento WINSOCK_WS2HELP_LSP_DISABLE
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WINSOCK_WS2HELP_LSP_DISABLE
api_type:
- NA
api_location: ''
ms.openlocfilehash: 6d785bfbd96d35717be7bbf76dab8f28f41c9fc6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106315752"
---
# <a name="winsock_ws2help_lsp_disable-event"></a><span data-ttu-id="ef860-103">\_Evento di \_ disabilitazione LSP ws2help di Winsock \_</span><span class="sxs-lookup"><span data-stu-id="ef860-103">WINSOCK\_WS2HELP\_LSP\_DISABLE event</span></span>

> [!Note]  
> <span data-ttu-id="ef860-104">I provider di servizi sovrapposti sono deprecati.</span><span class="sxs-lookup"><span data-stu-id="ef860-104">Layered Service Providers are deprecated.</span></span> <span data-ttu-id="ef860-105">A partire da Windows 8 e Windows Server 2012, usare la [piattaforma filtro Windows](../fwp/windows-filtering-platform-start-page.md).</span><span class="sxs-lookup"><span data-stu-id="ef860-105">Starting with Windows 8 and Windows Server 2012, use [Windows Filtering Platform](../fwp/windows-filtering-platform-start-page.md).</span></span>

 

<span data-ttu-id="ef860-106">L'evento di **\_ \_ \_ disabilitazione LSP ws2help di Winsock** è un evento di modifica del catalogo Winsock per un'operazione di disabilitazione di un provider di servizi a più livelli.</span><span class="sxs-lookup"><span data-stu-id="ef860-106">The **WINSOCK\_WS2HELP\_LSP\_DISABLE** event is a Winsock catalog change event for a layered service provider (LSP) disable operation.</span></span>


```C++
const EVENT_DESCRIPTOR WINSOCK_WS2HELP_LSP_DISABLE = {0x3, 0x0, 0x10, 0x0, 0x0, 0x0, 0x8000000000000000};
```



## <a name="parameters"></a><span data-ttu-id="ef860-107">Parametri</span><span class="sxs-lookup"><span data-stu-id="ef860-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ef860-108">*Nome LSP*</span><span class="sxs-lookup"><span data-stu-id="ef860-108">*LSP Name*</span></span> 
</dt> <dd>

<span data-ttu-id="ef860-109">Nome dello LSP ottenuto dal membro **szProtocol** della struttura di [**\_ informazioni di WSAPROTOCOL**](/windows/win32/api/winsock2/ns-winsock2-wsaprotocol_infoa) per l'oggetto LSP disabilitato.</span><span class="sxs-lookup"><span data-stu-id="ef860-109">The name of the LSP as obtained from the **szProtocol** member of the [**WSAPROTOCOL\_INFO**](/windows/win32/api/winsock2/ns-winsock2-wsaprotocol_infoa) structure for the LSP being disabled.</span></span>

</dd> <dt>

<span data-ttu-id="ef860-110">*Catalogo*</span><span class="sxs-lookup"><span data-stu-id="ef860-110">*Catalog*</span></span> 
</dt> <dd>

<span data-ttu-id="ef860-111">Il catalogo Winsock (32 bit o 64 bit) in cui lo LSP viene disabilitato.</span><span class="sxs-lookup"><span data-stu-id="ef860-111">The Winsock catalog (32-bit or 64-bit) where the LSP is being disabled.</span></span> <span data-ttu-id="ef860-112">Si tratta di un valore intero che può essere 32 o 64.</span><span class="sxs-lookup"><span data-stu-id="ef860-112">This is an integer value that is either 32 or 64.</span></span>

</dd> <dt>

<span data-ttu-id="ef860-113">*Programma di installazione*</span><span class="sxs-lookup"><span data-stu-id="ef860-113">*Installer*</span></span> 
</dt> <dd>

<span data-ttu-id="ef860-114">Il nome file del modulo dell'applicazione che effettua la chiamata di disabilitazione di LSP.</span><span class="sxs-lookup"><span data-stu-id="ef860-114">The module filename of the application making the LSP disable call.</span></span>

</dd> <dt>

<span data-ttu-id="ef860-115">*GUID*</span><span class="sxs-lookup"><span data-stu-id="ef860-115">*GUID*</span></span> 
</dt> <dd>

<span data-ttu-id="ef860-116">Valore GUID del provider di trasporto Winsock che verrà disabilitato da LSP.</span><span class="sxs-lookup"><span data-stu-id="ef860-116">The GUID value of the Winsock transport provider that the LSP is being disabled.</span></span>

</dd> <dt>

<span data-ttu-id="ef860-117">*Categoria*</span><span class="sxs-lookup"><span data-stu-id="ef860-117">*Category*</span></span> 
</dt> <dd>

<span data-ttu-id="ef860-118">Membro **dwCatalogEntryId** della struttura di [**\_ informazioni WSAPROTOCOL**](/windows/win32/api/winsock2/ns-winsock2-wsaprotocol_infoa) per l'oggetto LSP disabilitato.</span><span class="sxs-lookup"><span data-stu-id="ef860-118">The **dwCatalogEntryId** member of the [**WSAPROTOCOL\_INFO**](/windows/win32/api/winsock2/ns-winsock2-wsaprotocol_infoa) structure for the LSP being disabled.</span></span>

</dd> </dl>

<span data-ttu-id="ef860-119">Questo evento non contiene parametri.</span><span class="sxs-lookup"><span data-stu-id="ef860-119">This event has no parameters.</span></span>

## <a name="remarks"></a><span data-ttu-id="ef860-120">Commenti</span><span class="sxs-lookup"><span data-stu-id="ef860-120">Remarks</span></span>

<span data-ttu-id="ef860-121">L'evento di **\_ \_ \_ disabilitazione LSP ws2help di Winsock** viene tracciato per un'operazione di disabilitazione LSP quando una voce di protocollo è disabilitata nel catalogo Winsock.</span><span class="sxs-lookup"><span data-stu-id="ef860-121">The **WINSOCK\_WS2HELP\_LSP\_DISABLE** event is traced for an LSP disable operation when a protocol entry is disabled in the Winsock catalog.</span></span>

## <a name="requirements"></a><span data-ttu-id="ef860-122">Requisiti</span><span class="sxs-lookup"><span data-stu-id="ef860-122">Requirements</span></span>



| <span data-ttu-id="ef860-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="ef860-123">Requirement</span></span> | <span data-ttu-id="ef860-124">Valore</span><span class="sxs-lookup"><span data-stu-id="ef860-124">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="ef860-125">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="ef860-125">Minimum supported client</span></span><br/> | <span data-ttu-id="ef860-126">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="ef860-126">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="ef860-127">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="ef860-127">Minimum supported server</span></span><br/> | <span data-ttu-id="ef860-128">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="ef860-128">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="ef860-129">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="ef860-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ef860-130">Controllo della traccia Winsock</span><span class="sxs-lookup"><span data-stu-id="ef860-130">Control of Winsock Tracing</span></span>](control-of-winsock-tracing.md)
</dt> <dt>

[<span data-ttu-id="ef860-131">Traccia Winsock</span><span class="sxs-lookup"><span data-stu-id="ef860-131">Winsock Tracing</span></span>](winsock-tracing.md)
</dt> <dt>

[<span data-ttu-id="ef860-132">Livelli di traccia Winsock</span><span class="sxs-lookup"><span data-stu-id="ef860-132">Winsock Tracing Levels</span></span>](winsock-tracing-levels.md)
</dt> <dt>

[<span data-ttu-id="ef860-133">Dettagli della traccia delle modifiche del catalogo Winsock</span><span class="sxs-lookup"><span data-stu-id="ef860-133">Winsock Catalog Change Tracing Details</span></span>](winsock-layered-service-provider-tracing-event-details.md)
</dt> </dl>

 

 
