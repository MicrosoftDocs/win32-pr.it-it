---
description: Evento di modifica del catalogo Winsock per un'operazione di rimozione di un provider di servizi a più livelli (LSP).
ms.assetid: 86FF17F7-8CCF-4A03-899F-42BFACDF3F54
title: Evento WINSOCK_WS2HELP_LSP_REMOVE
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WINSOCK_WS2HELP_LSP_REMOVE
api_type:
- NA
api_location: ''
ms.openlocfilehash: 597cd2f8cfc3bb7727301e64af53671bafbd9469
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106315751"
---
# <a name="winsock_ws2help_lsp_remove-event"></a><span data-ttu-id="d15d5-103">\_Evento di \_ rimozione LSP ws2help \_ di Winsock</span><span class="sxs-lookup"><span data-stu-id="d15d5-103">WINSOCK\_WS2HELP\_LSP\_REMOVE event</span></span>

> [!Note]  
> <span data-ttu-id="d15d5-104">I provider di servizi sovrapposti sono deprecati.</span><span class="sxs-lookup"><span data-stu-id="d15d5-104">Layered Service Providers are deprecated.</span></span> <span data-ttu-id="d15d5-105">A partire da Windows 8 e Windows Server 2012, usare la [piattaforma filtro Windows](../fwp/windows-filtering-platform-start-page.md).</span><span class="sxs-lookup"><span data-stu-id="d15d5-105">Starting with Windows 8 and Windows Server 2012, use [Windows Filtering Platform](../fwp/windows-filtering-platform-start-page.md).</span></span>

 

<span data-ttu-id="d15d5-106">L'evento di rimozione di **Winsock \_ ws2help \_ LSP \_** è un evento di modifica del catalogo Winsock per un'operazione di rimozione di un provider di servizi a più livelli.</span><span class="sxs-lookup"><span data-stu-id="d15d5-106">The **WINSOCK\_WS2HELP\_LSP\_REMOVE** event is a Winsock catalog change event for a layered service provider (LSP) removal operation.</span></span>


```C++
const EVENT_DESCRIPTOR WINSOCK_WS2HELP_LSP_REMOVE = {0x2, 0x0, 0x10, 0x0, 0x0, 0x0, 0x8000000000000000};
```



## <a name="parameters"></a><span data-ttu-id="d15d5-107">Parametri</span><span class="sxs-lookup"><span data-stu-id="d15d5-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d15d5-108">*Nome LSP*</span><span class="sxs-lookup"><span data-stu-id="d15d5-108">*LSP Name*</span></span> 
</dt> <dd>

<span data-ttu-id="d15d5-109">Nome dell'oggetto LSP ottenuto dal membro **szProtocol** della struttura di [**\_ informazioni WSAPROTOCOL**](/windows/win32/api/winsock2/ns-winsock2-wsaprotocol_infoa) per l'oggetto LSP da rimuovere.</span><span class="sxs-lookup"><span data-stu-id="d15d5-109">The name of the LSP as obtained from the **szProtocol** member of the [**WSAPROTOCOL\_INFO**](/windows/win32/api/winsock2/ns-winsock2-wsaprotocol_infoa) structure for the LSP being removed.</span></span>

</dd> <dt>

<span data-ttu-id="d15d5-110">*Catalogo*</span><span class="sxs-lookup"><span data-stu-id="d15d5-110">*Catalog*</span></span> 
</dt> <dd>

<span data-ttu-id="d15d5-111">Il catalogo Winsock (32 bit o 64 bit) in cui viene rimosso lo LSP.</span><span class="sxs-lookup"><span data-stu-id="d15d5-111">The Winsock catalog (32-bit or 64-bit) where the LSP is being removed.</span></span> <span data-ttu-id="d15d5-112">Si tratta di un valore intero che può essere 32 o 64.</span><span class="sxs-lookup"><span data-stu-id="d15d5-112">This is an integer value that is either 32 or 64.</span></span>

</dd> <dt>

<span data-ttu-id="d15d5-113">*Programma di installazione*</span><span class="sxs-lookup"><span data-stu-id="d15d5-113">*Installer*</span></span> 
</dt> <dd>

<span data-ttu-id="d15d5-114">Il nome file del modulo dell'applicazione che effettua la chiamata di rimozione LSP.</span><span class="sxs-lookup"><span data-stu-id="d15d5-114">The module filename of the application making the LSP remove call.</span></span>

</dd> <dt>

<span data-ttu-id="d15d5-115">*GUID*</span><span class="sxs-lookup"><span data-stu-id="d15d5-115">*GUID*</span></span> 
</dt> <dd>

<span data-ttu-id="d15d5-116">Valore GUID del provider di trasporto Winsock da cui viene rimosso lo LSP.</span><span class="sxs-lookup"><span data-stu-id="d15d5-116">The GUID value of the Winsock transport provider that the LSP is being removed from.</span></span>

</dd> <dt>

<span data-ttu-id="d15d5-117">*Categoria*</span><span class="sxs-lookup"><span data-stu-id="d15d5-117">*Category*</span></span> 
</dt> <dd>

<span data-ttu-id="d15d5-118">Membro **dwCatalogEntryId** della struttura di [**\_ informazioni di WSAPROTOCOL**](/windows/win32/api/winsock2/ns-winsock2-wsaprotocol_infoa) per l'oggetto LSP da rimuovere.</span><span class="sxs-lookup"><span data-stu-id="d15d5-118">The **dwCatalogEntryId** member of the [**WSAPROTOCOL\_INFO**](/windows/win32/api/winsock2/ns-winsock2-wsaprotocol_infoa) structure for the LSP being removed.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="d15d5-119">Commenti</span><span class="sxs-lookup"><span data-stu-id="d15d5-119">Remarks</span></span>

<span data-ttu-id="d15d5-120">L'evento di rimozione di **Winsock \_ ws2help \_ LSP \_** viene tracciato per un'operazione di rimozione di LSP quando viene rimossa una voce di protocollo dal catalogo Winsock.</span><span class="sxs-lookup"><span data-stu-id="d15d5-120">The **WINSOCK\_WS2HELP\_LSP\_REMOVE** event is traced for an LSP removal operation when a protocol entry is removed from the Winsock catalog.</span></span>

## <a name="requirements"></a><span data-ttu-id="d15d5-121">Requisiti</span><span class="sxs-lookup"><span data-stu-id="d15d5-121">Requirements</span></span>



| <span data-ttu-id="d15d5-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="d15d5-122">Requirement</span></span> | <span data-ttu-id="d15d5-123">Valore</span><span class="sxs-lookup"><span data-stu-id="d15d5-123">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="d15d5-124">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="d15d5-124">Minimum supported client</span></span><br/> | <span data-ttu-id="d15d5-125">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="d15d5-125">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="d15d5-126">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="d15d5-126">Minimum supported server</span></span><br/> | <span data-ttu-id="d15d5-127">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="d15d5-127">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="d15d5-128">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="d15d5-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d15d5-129">Controllo della traccia Winsock</span><span class="sxs-lookup"><span data-stu-id="d15d5-129">Control of Winsock Tracing</span></span>](control-of-winsock-tracing.md)
</dt> <dt>

[<span data-ttu-id="d15d5-130">Traccia Winsock</span><span class="sxs-lookup"><span data-stu-id="d15d5-130">Winsock Tracing</span></span>](winsock-tracing.md)
</dt> <dt>

[<span data-ttu-id="d15d5-131">Livelli di traccia Winsock</span><span class="sxs-lookup"><span data-stu-id="d15d5-131">Winsock Tracing Levels</span></span>](winsock-tracing-levels.md)
</dt> <dt>

[<span data-ttu-id="d15d5-132">Dettagli della traccia delle modifiche del catalogo Winsock</span><span class="sxs-lookup"><span data-stu-id="d15d5-132">Winsock Catalog Change Tracing Details</span></span>](winsock-layered-service-provider-tracing-event-details.md)
</dt> </dl>

 

 
