---
description: I dispositivi portatili Windows supportano le seguenti proprietà dell'attività.
ms.assetid: 9bd6c2e1-740a-453d-b390-120700af7c93
title: Proprietà attività (PortableDevice. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Task
api_type:
- HeaderDef
api_location:
- PortableDevice.h
ms.openlocfilehash: 829685ac3fa5737356c172ed9e66303b3d6115ca
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106326592"
---
# <a name="task-properties"></a><span data-ttu-id="23cd3-103">Proprietà attività</span><span class="sxs-lookup"><span data-stu-id="23cd3-103">Task Properties</span></span>

<span data-ttu-id="23cd3-104">I dispositivi portatili Windows supportano le seguenti proprietà dell'attività.</span><span class="sxs-lookup"><span data-stu-id="23cd3-104">Windows Portable Devices supports the following task properties.</span></span>



| <span data-ttu-id="23cd3-105">Proprietà</span><span class="sxs-lookup"><span data-stu-id="23cd3-105">Property</span></span>                         | <span data-ttu-id="23cd3-106">VarType</span><span class="sxs-lookup"><span data-stu-id="23cd3-106">VarType</span></span>        | <span data-ttu-id="23cd3-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="23cd3-107">Description</span></span>                                                                                 |
|----------------------------------|----------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="23cd3-108">**\_proprietario attività \_ WPD**</span><span class="sxs-lookup"><span data-stu-id="23cd3-108">**WPD\_TASK\_OWNER**</span></span>             | <span data-ttu-id="23cd3-109">**\_LPWSTR VT**</span><span class="sxs-lookup"><span data-stu-id="23cd3-109">**VT\_LPWSTR**</span></span> | <span data-ttu-id="23cd3-110">Proprietario dell'attività.</span><span class="sxs-lookup"><span data-stu-id="23cd3-110">The owner of the task.</span></span>                                                                      |
| <span data-ttu-id="23cd3-111">**\_ \_ percentuale completamento attività \_ WPD**</span><span class="sxs-lookup"><span data-stu-id="23cd3-111">**WPD\_TASK\_PERCENT\_COMPLETE**</span></span> | <span data-ttu-id="23cd3-112">**\_UI4 VT**</span><span class="sxs-lookup"><span data-stu-id="23cd3-112">**VT\_UI4**</span></span>    | <span data-ttu-id="23cd3-113">Numero compreso tra 0 e 100 che specifica la modalità di completamento dell'attività.</span><span class="sxs-lookup"><span data-stu-id="23cd3-113">A number between 0 and 100 that specifies how complete the task is.</span></span>                         |
| <span data-ttu-id="23cd3-114">**\_Data di \_ promemoria attività WPD \_**</span><span class="sxs-lookup"><span data-stu-id="23cd3-114">**WPD\_TASK\_REMINDER\_DATE**</span></span>    | <span data-ttu-id="23cd3-115">**\_Data VT**</span><span class="sxs-lookup"><span data-stu-id="23cd3-115">**VT\_DATE**</span></span>   | <span data-ttu-id="23cd3-116">Valore che specifica quando inviare un promemoria per eseguire l'attività, se non è stata completata.</span><span class="sxs-lookup"><span data-stu-id="23cd3-116">A value that specifies when a reminder should be sent to perform the task, if not complete.</span></span> |
| <span data-ttu-id="23cd3-117">**\_stato attività \_ WPD**</span><span class="sxs-lookup"><span data-stu-id="23cd3-117">**WPD\_TASK\_STATUS**</span></span>            | <span data-ttu-id="23cd3-118">**\_LPWSTR VT**</span><span class="sxs-lookup"><span data-stu-id="23cd3-118">**VT\_LPWSTR**</span></span> | <span data-ttu-id="23cd3-119">Una descrizione di stringa dello stato dell'attività, ad esempio "in corso".</span><span class="sxs-lookup"><span data-stu-id="23cd3-119">A string description of the status of the task, for example, "In Progress".</span></span>                 |



 

## <a name="requirements"></a><span data-ttu-id="23cd3-120">Requisiti</span><span class="sxs-lookup"><span data-stu-id="23cd3-120">Requirements</span></span>



| <span data-ttu-id="23cd3-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="23cd3-121">Requirement</span></span> | <span data-ttu-id="23cd3-122">Valore</span><span class="sxs-lookup"><span data-stu-id="23cd3-122">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="23cd3-123">Intestazione</span><span class="sxs-lookup"><span data-stu-id="23cd3-123">Header</span></span><br/> | <dl> <span data-ttu-id="23cd3-124"><dt>PortableDevice. h</dt></span><span class="sxs-lookup"><span data-stu-id="23cd3-124"><dt>PortableDevice.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="23cd3-125">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="23cd3-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="23cd3-126">**Proprietà e attributi di WPD**</span><span class="sxs-lookup"><span data-stu-id="23cd3-126">**WPD Properties and Attributes**</span></span>](properties-and-attributes.md)
</dt> </dl>

 

 




