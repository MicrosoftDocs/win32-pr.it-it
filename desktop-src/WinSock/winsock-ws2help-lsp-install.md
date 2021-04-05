---
description: Evento di modifica del catalogo Winsock per un'operazione di installazione di un provider di servizi a più livelli (LSP).
ms.assetid: 76A3D175-8CDC-486C-8341-D6314BCEC113
title: Evento WINSOCK_WS2HELP_LSP_INSTALL
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WINSOCK_WS2HELP_LSP_INSTALL
api_type:
- NA
api_location: ''
ms.openlocfilehash: 2d95a77f68bafd29fde3bbf34336d9b31d2a412e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103968056"
---
# <a name="winsock_ws2help_lsp_install-event"></a><span data-ttu-id="f9f8c-103">Evento di installazione di WINSOCK \_ ws2help \_ LSP \_</span><span class="sxs-lookup"><span data-stu-id="f9f8c-103">WINSOCK\_WS2HELP\_LSP\_INSTALL event</span></span>

> [!Note]  
> <span data-ttu-id="f9f8c-104">I provider di servizi sovrapposti sono deprecati.</span><span class="sxs-lookup"><span data-stu-id="f9f8c-104">Layered Service Providers are deprecated.</span></span> <span data-ttu-id="f9f8c-105">A partire da Windows 8 e Windows Server 2012, usare la [piattaforma filtro Windows](../fwp/windows-filtering-platform-start-page.md).</span><span class="sxs-lookup"><span data-stu-id="f9f8c-105">Starting with Windows 8 and Windows Server 2012, use [Windows Filtering Platform](../fwp/windows-filtering-platform-start-page.md).</span></span>

 

<span data-ttu-id="f9f8c-106">L'evento di **installazione di Winsock \_ ws2help \_ LSP \_** è un evento di modifica del catalogo Winsock per un'operazione di installazione di un provider di servizi a più livelli (LSP).</span><span class="sxs-lookup"><span data-stu-id="f9f8c-106">The **WINSOCK\_WS2HELP\_LSP\_INSTALL** event is a Winsock catalog change event for a layered service provider (LSP) installation operation.</span></span>


```C++
const EVENT_DESCRIPTOR WINSOCK_WS2HELP_LSP_INSTALL = {0x1, 0x0, 0x10, 0x0, 0x0, 0x0, 0x8000000000000000};
```



## <a name="parameters"></a><span data-ttu-id="f9f8c-107">Parametri</span><span class="sxs-lookup"><span data-stu-id="f9f8c-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f9f8c-108">*Nome LSP*</span><span class="sxs-lookup"><span data-stu-id="f9f8c-108">*LSP Name*</span></span> 
</dt> <dd>

<span data-ttu-id="f9f8c-109">Nome dello LSP ottenuto dal membro **szProtocol** della struttura di [**\_ informazioni di WSAPROTOCOL**](/windows/win32/api/winsock2/ns-winsock2-wsaprotocol_infoa) per l'oggetto LSP da installare.</span><span class="sxs-lookup"><span data-stu-id="f9f8c-109">The name of the LSP as obtained from the **szProtocol** member of the [**WSAPROTOCOL\_INFO**](/windows/win32/api/winsock2/ns-winsock2-wsaprotocol_infoa) structure for the LSP being installed.</span></span>

</dd> <dt>

<span data-ttu-id="f9f8c-110">*Catalogo*</span><span class="sxs-lookup"><span data-stu-id="f9f8c-110">*Catalog*</span></span> 
</dt> <dd>

<span data-ttu-id="f9f8c-111">Il catalogo Winsock (32 bit o 64 bit) in cui viene installato lo LSP.</span><span class="sxs-lookup"><span data-stu-id="f9f8c-111">The Winsock catalog (32-bit or 64-bit) where the LSP is being installed.</span></span> <span data-ttu-id="f9f8c-112">Si tratta di un valore intero che può essere 32 o 64.</span><span class="sxs-lookup"><span data-stu-id="f9f8c-112">This is an integer value that is either 32 or 64.</span></span>

</dd> <dt>

<span data-ttu-id="f9f8c-113">*Programma di installazione*</span><span class="sxs-lookup"><span data-stu-id="f9f8c-113">*Installer*</span></span> 
</dt> <dd>

<span data-ttu-id="f9f8c-114">Il nome file del modulo dell'applicazione che effettua la chiamata di installazione di LSP.</span><span class="sxs-lookup"><span data-stu-id="f9f8c-114">The module filename of the application making the LSP install call.</span></span>

</dd> <dt>

<span data-ttu-id="f9f8c-115">*GUID*</span><span class="sxs-lookup"><span data-stu-id="f9f8c-115">*GUID*</span></span> 
</dt> <dd>

<span data-ttu-id="f9f8c-116">Valore GUID del provider di trasporto Winsock in cui viene installato il LSP.</span><span class="sxs-lookup"><span data-stu-id="f9f8c-116">The GUID value of the Winsock transport provider that the LSP is being installed under.</span></span>

</dd> <dt>

<span data-ttu-id="f9f8c-117">*Categoria*</span><span class="sxs-lookup"><span data-stu-id="f9f8c-117">*Category*</span></span> 
</dt> <dd>

<span data-ttu-id="f9f8c-118">Membro **dwCatalogEntryId** della struttura di [**\_ informazioni di WSAPROTOCOL**](/windows/win32/api/winsock2/ns-winsock2-wsaprotocol_infoa) per l'oggetto LSP da installare.</span><span class="sxs-lookup"><span data-stu-id="f9f8c-118">The **dwCatalogEntryId** member of the [**WSAPROTOCOL\_INFO**](/windows/win32/api/winsock2/ns-winsock2-wsaprotocol_infoa) structure for the LSP being installed.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="f9f8c-119">Commenti</span><span class="sxs-lookup"><span data-stu-id="f9f8c-119">Remarks</span></span>

<span data-ttu-id="f9f8c-120">L'evento di **installazione di Winsock \_ ws2help \_ LSP \_** viene tracciato per un'operazione di installazione di LSP quando viene installata una voce di protocollo nel catalogo Winsock.</span><span class="sxs-lookup"><span data-stu-id="f9f8c-120">The **WINSOCK\_WS2HELP\_LSP\_INSTALL** event is traced for an LSP install operation when a protocol entry is installed into the Winsock catalog.</span></span>

## <a name="requirements"></a><span data-ttu-id="f9f8c-121">Requisiti</span><span class="sxs-lookup"><span data-stu-id="f9f8c-121">Requirements</span></span>



| <span data-ttu-id="f9f8c-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="f9f8c-122">Requirement</span></span> | <span data-ttu-id="f9f8c-123">Valore</span><span class="sxs-lookup"><span data-stu-id="f9f8c-123">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="f9f8c-124">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="f9f8c-124">Minimum supported client</span></span><br/> | <span data-ttu-id="f9f8c-125">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="f9f8c-125">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="f9f8c-126">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="f9f8c-126">Minimum supported server</span></span><br/> | <span data-ttu-id="f9f8c-127">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="f9f8c-127">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="f9f8c-128">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="f9f8c-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f9f8c-129">Controllo della traccia Winsock</span><span class="sxs-lookup"><span data-stu-id="f9f8c-129">Control of Winsock Tracing</span></span>](control-of-winsock-tracing.md)
</dt> <dt>

[<span data-ttu-id="f9f8c-130">Traccia Winsock</span><span class="sxs-lookup"><span data-stu-id="f9f8c-130">Winsock Tracing</span></span>](winsock-tracing.md)
</dt> <dt>

[<span data-ttu-id="f9f8c-131">Livelli di traccia Winsock</span><span class="sxs-lookup"><span data-stu-id="f9f8c-131">Winsock Tracing Levels</span></span>](winsock-tracing-levels.md)
</dt> <dt>

[<span data-ttu-id="f9f8c-132">Dettagli della traccia delle modifiche del catalogo Winsock</span><span class="sxs-lookup"><span data-stu-id="f9f8c-132">Winsock Catalog Change Tracing Details</span></span>](winsock-layered-service-provider-tracing-event-details.md)
</dt> </dl>

 

 
