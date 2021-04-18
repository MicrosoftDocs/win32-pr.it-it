---
title: System (EventType) (elemento)
description: Contiene informazioni che identificano il provider e il modo in cui è stato abilitato, l'evento, il canale in cui è stato scritto l'evento e le informazioni di sistema, ad esempio gli ID processo e thread.
ms.assetid: c532cfa3-b722-4227-a403-5c050d62a92c
keywords:
- Log degli elementi di sistema
topic_type:
- apiref
api_name:
- System
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 4fef0f9f9e24a855564a8d3df2f94610ff9a8248
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106300984"
---
# <a name="system-eventtype-element"></a><span data-ttu-id="efc21-104">System (EventType) (elemento)</span><span class="sxs-lookup"><span data-stu-id="efc21-104">System (EventType) Element</span></span>

<span data-ttu-id="efc21-105">Contiene informazioni che identificano il provider e il modo in cui è stato abilitato, l'evento, il canale in cui è stato scritto l'evento e le informazioni di sistema, ad esempio gli ID processo e thread.</span><span class="sxs-lookup"><span data-stu-id="efc21-105">Contains information that identifies the provider and how it was enabled, the event, the channel to which the event was written, and system information such as the process and thread IDs.</span></span>

``` syntax
<xs:element name="System"
    type="SystemPropertiesType"
 />
```

<span data-ttu-id="efc21-106">L'elemento **System** è definito dal tipo complesso [**eventType**](eventschema-eventtype-complextype.md) .</span><span class="sxs-lookup"><span data-stu-id="efc21-106">The **System** element is defined by the [**EventType**](eventschema-eventtype-complextype.md) complex type.</span></span>

## <a name="requirements"></a><span data-ttu-id="efc21-107">Requisiti</span><span class="sxs-lookup"><span data-stu-id="efc21-107">Requirements</span></span>



| <span data-ttu-id="efc21-108">Requisito</span><span class="sxs-lookup"><span data-stu-id="efc21-108">Requirement</span></span> | <span data-ttu-id="efc21-109">Valore</span><span class="sxs-lookup"><span data-stu-id="efc21-109">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="efc21-110">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="efc21-110">Minimum supported client</span></span><br/> | <span data-ttu-id="efc21-111">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="efc21-111">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="efc21-112">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="efc21-112">Minimum supported server</span></span><br/> | <span data-ttu-id="efc21-113">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="efc21-113">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="efc21-114">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="efc21-114">See also</span></span>

<dl> <dt>

<span data-ttu-id="efc21-115">**Elemento padre**</span><span class="sxs-lookup"><span data-stu-id="efc21-115">**Parent element**</span></span>
</dt> <dt>

[<span data-ttu-id="efc21-116">**event**</span><span class="sxs-lookup"><span data-stu-id="efc21-116">**Event**</span></span>](eventschema-event-element.md)
</dt> </dl>

 

 





