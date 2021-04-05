---
description: Descrive i dati dell'oggetto sink di visualizzazione inclusi in un risultato di notifica o di notifica.
ms.assetid: 40D931F6-C068-48EB-A968-9CBAA3F9FAD8
title: Struttura WFD_DISPLAY_SINK_OBJECT_HEADER (Wfdsink. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WFD_DISPLAY_SINK_OBJECT_HEADER
api_type:
- HeaderDef
api_location:
- wfdsink.h
ms.openlocfilehash: cdefd6b0b91fefb0f42a6e37e7584f7cd966884b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103881453"
---
# <a name="wfd_display_sink_object_header-structure"></a><span data-ttu-id="55f11-103">\_Struttura dell' \_ \_ intestazione dell'oggetto sink di visualizzazione della direttiva. \_</span><span class="sxs-lookup"><span data-stu-id="55f11-103">WFD\_DISPLAY\_SINK\_OBJECT\_HEADER structure</span></span>

<span data-ttu-id="55f11-104">La struttura dell' **\_ \_ \_ \_ intestazione dell'oggetto sink di visualizzazione della direttiva GMA** descrive i dati dell'oggetto sink di visualizzazione inclusi nei risultati di una notifica o di una notifica.</span><span class="sxs-lookup"><span data-stu-id="55f11-104">The **WFD\_DISPLAY\_SINK\_OBJECT\_HEADER** structure describes the display sink object data included in a notification or notification result.</span></span>

## <a name="syntax"></a><span data-ttu-id="55f11-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="55f11-105">Syntax</span></span>


```C++
typedef struct _WFD_DISPLAY_SINK_OBJECT_HEADER {
  UCHAR  Type;
  UCHAR  Revision;
  USHORT Length;
} WFD_DISPLAY_SINK_OBJECT_HEADER, *PWFD_DISPLAY_SINK_OBJECT_HEADER;
```



## <a name="members"></a><span data-ttu-id="55f11-106">Members</span><span class="sxs-lookup"><span data-stu-id="55f11-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="55f11-107">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="55f11-107">**Type**</span></span>
</dt> <dd>

<span data-ttu-id="55f11-108">Tipo dell'oggetto sink di visualizzazione.</span><span class="sxs-lookup"><span data-stu-id="55f11-108">The type of the display sink object.</span></span> <span data-ttu-id="55f11-109">È possibile utilizzare il valore **\_ predefinito del \_ \_ tipo di \_ oggetto \_ sink di visualizzazione** dell'identificatore, definito come valore 1.</span><span class="sxs-lookup"><span data-stu-id="55f11-109">You can use the identifier **WFD\_DISPLAY\_SINK\_OBJECT\_TYPE\_DEFAULT** which is defined as the value 1.</span></span>

</dd> <dt>

<span data-ttu-id="55f11-110">**Revisione**</span><span class="sxs-lookup"><span data-stu-id="55f11-110">**Revision**</span></span>
</dt> <dd>

<span data-ttu-id="55f11-111">Versione di revisione dell'oggetto sink di visualizzazione.</span><span class="sxs-lookup"><span data-stu-id="55f11-111">The revision version of the display sink object.</span></span> <span data-ttu-id="55f11-112">È possibile usare l'identificatore **di \_ visualizzazione del sink di visualizzazione dell' \_ \_ oggetto sink \_ \_ versione \_ 1** , definito come valore 1.</span><span class="sxs-lookup"><span data-stu-id="55f11-112">You can use the identifier **WFD\_DISPLAY\_SINK\_OBJECT\_REVISION\_VERSION\_1** which is defined as the value 1.</span></span>

</dd> <dt>

<span data-ttu-id="55f11-113">**Length**</span><span class="sxs-lookup"><span data-stu-id="55f11-113">**Length**</span></span>
</dt> <dd>

<span data-ttu-id="55f11-114">Lunghezza dei dati nel risultato della notifica o della notifica.</span><span class="sxs-lookup"><span data-stu-id="55f11-114">The length of the data in the notification or notification result.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="55f11-115">Requisiti</span><span class="sxs-lookup"><span data-stu-id="55f11-115">Requirements</span></span>



| <span data-ttu-id="55f11-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="55f11-116">Requirement</span></span> | <span data-ttu-id="55f11-117">Valore</span><span class="sxs-lookup"><span data-stu-id="55f11-117">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="55f11-118">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="55f11-118">Minimum supported client</span></span><br/> | <span data-ttu-id="55f11-119">Windows 8.1 \[ solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="55f11-119">Windows 8.1 \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="55f11-120">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="55f11-120">Minimum supported server</span></span><br/> | <span data-ttu-id="55f11-121">Solo app desktop Windows Server 2012 R2 \[\]</span><span class="sxs-lookup"><span data-stu-id="55f11-121">Windows Server 2012 R2 \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="55f11-122">Intestazione</span><span class="sxs-lookup"><span data-stu-id="55f11-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="55f11-123"><dt>Wfdsink. h</dt></span><span class="sxs-lookup"><span data-stu-id="55f11-123"><dt>Wfdsink.h</dt></span></span> </dl> |



 

 




