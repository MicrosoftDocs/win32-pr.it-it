---
description: L'interfaccia IMonitorEventer fornisce metodi per l'invio di eventi e l'allocazione e la liberazione di risorse di monitoraggio.
ms.assetid: d59a8b42-cce3-410b-a62e-97d66d058d90
title: Interfaccia IMonitorEventer (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IMonitorEventer
api_type:
- COM
api_location:
- Netmon.h
ms.openlocfilehash: 7d4ca58b5a0787638eee54b7733b4e1a8fbf7ffe
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103879054"
---
# <a name="imonitoreventer-interface"></a><span data-ttu-id="1dd15-103">Interfaccia IMonitorEventer</span><span class="sxs-lookup"><span data-stu-id="1dd15-103">IMonitorEventer interface</span></span>

<span data-ttu-id="1dd15-104">L'interfaccia **IMonitorEventer** fornisce metodi per l'invio di eventi e l'allocazione e la liberazione di risorse di monitoraggio.</span><span class="sxs-lookup"><span data-stu-id="1dd15-104">The **IMonitorEventer** interface provides methods for submitting events and allocating and freeing monitor resources.</span></span>

## <a name="members"></a><span data-ttu-id="1dd15-105">Membri</span><span class="sxs-lookup"><span data-stu-id="1dd15-105">Members</span></span>

<span data-ttu-id="1dd15-106">L'interfaccia **IMonitorEventer** eredita dall'interfaccia [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="1dd15-106">The **IMonitorEventer** interface inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="1dd15-107">**IMonitorEventer** dispone anche di questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="1dd15-107">**IMonitorEventer** also has these types of members:</span></span>

-   [<span data-ttu-id="1dd15-108">Metodi</span><span class="sxs-lookup"><span data-stu-id="1dd15-108">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="1dd15-109">Metodi</span><span class="sxs-lookup"><span data-stu-id="1dd15-109">Methods</span></span>

<span data-ttu-id="1dd15-110">L'interfaccia **IMonitorEventer** dispone di questi metodi.</span><span class="sxs-lookup"><span data-stu-id="1dd15-110">The **IMonitorEventer** interface has these methods.</span></span>



| <span data-ttu-id="1dd15-111">Metodo</span><span class="sxs-lookup"><span data-stu-id="1dd15-111">Method</span></span>                                                 | <span data-ttu-id="1dd15-112">Descrizione</span><span class="sxs-lookup"><span data-stu-id="1dd15-112">Description</span></span>                                        |
|:-------------------------------------------------------|:---------------------------------------------------|
| [<span data-ttu-id="1dd15-113">**FreeEventData**</span><span class="sxs-lookup"><span data-stu-id="1dd15-113">**FreeEventData**</span></span>](imonitoreventer-freeeventdata.md) | <span data-ttu-id="1dd15-114">Libera lo spazio allocato per i dati di monitoraggio.</span><span class="sxs-lookup"><span data-stu-id="1dd15-114">Frees space allocated for monitor data.</span></span><br/> |
| [<span data-ttu-id="1dd15-115">**GetEventData**</span><span class="sxs-lookup"><span data-stu-id="1dd15-115">**GetEventData**</span></span>](imonitoreventer-geteventdata.md)   | <span data-ttu-id="1dd15-116">Alloca spazio per i dati di monitoraggio.</span><span class="sxs-lookup"><span data-stu-id="1dd15-116">Allocates space for monitor data.</span></span><br/>       |
| [<span data-ttu-id="1dd15-117">**SendNMEvent**</span><span class="sxs-lookup"><span data-stu-id="1dd15-117">**SendNMEvent**</span></span>](imonitoreventer-sendnmevent.md)     | <span data-ttu-id="1dd15-118">Invia eventi a WMI.</span><span class="sxs-lookup"><span data-stu-id="1dd15-118">Submits events to WMI.</span></span><br/>                  |



 

## <a name="requirements"></a><span data-ttu-id="1dd15-119">Requisiti</span><span class="sxs-lookup"><span data-stu-id="1dd15-119">Requirements</span></span>



| <span data-ttu-id="1dd15-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="1dd15-120">Requirement</span></span> | <span data-ttu-id="1dd15-121">Valore</span><span class="sxs-lookup"><span data-stu-id="1dd15-121">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="1dd15-122">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="1dd15-122">Minimum supported client</span></span><br/> | <span data-ttu-id="1dd15-123">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="1dd15-123">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="1dd15-124">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="1dd15-124">Minimum supported server</span></span><br/> | <span data-ttu-id="1dd15-125">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="1dd15-125">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="1dd15-126">Intestazione</span><span class="sxs-lookup"><span data-stu-id="1dd15-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="1dd15-127"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="1dd15-127"><dt>Netmon.h</dt></span></span> </dl> |



 

