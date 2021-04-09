---
description: Ottiene il tempo rimanente prima che un'operazione di sospensione dell'app ritardata continui.
ms.assetid: A90347F3-75CB-4EEB-930D-30882F43D192
title: ISuspendingOperation::D Proprietà eadline (Windows. ApplicationModel. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISuspendingOperation.Deadline
- ISuspendingOperation.get_Deadline
- ISuspendingOperation.put_Deadline
api_type:
- COM
api_location:
- Windows.ApplicationModel.h
ms.openlocfilehash: 305610108b7a138693ccdce97e35ddbe90451806
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103966687"
---
# <a name="isuspendingoperationdeadline-property"></a><span data-ttu-id="5f321-103">ISuspendingOperation::D Proprietà eadline</span><span class="sxs-lookup"><span data-stu-id="5f321-103">ISuspendingOperation::Deadline property</span></span>

<span data-ttu-id="5f321-104">Ottiene il tempo rimanente prima che un'operazione di sospensione dell'app ritardata continui.</span><span class="sxs-lookup"><span data-stu-id="5f321-104">Gets the time remaining before a delayed app suspending operation continues.</span></span>

<span data-ttu-id="5f321-105">Si tratta di una proprietà di lettura/scrittura.</span><span class="sxs-lookup"><span data-stu-id="5f321-105">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="5f321-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="5f321-106">Syntax</span></span>


```C++
HRESULT put_Deadline();

HRESULT get_Deadline(
  [out, retval] DateTime *value
);
```



## <a name="property-value"></a><span data-ttu-id="5f321-107">Valore proprietà</span><span class="sxs-lookup"><span data-stu-id="5f321-107">Property value</span></span>

<span data-ttu-id="5f321-108">Il tempo rimanente prima che l'operazione di sospensione dell'app ritardata continui.</span><span class="sxs-lookup"><span data-stu-id="5f321-108">The time remaining before a delayed app suspending operation continues.</span></span>

## <a name="requirements"></a><span data-ttu-id="5f321-109">Requisiti</span><span class="sxs-lookup"><span data-stu-id="5f321-109">Requirements</span></span>



| <span data-ttu-id="5f321-110">Requisito</span><span class="sxs-lookup"><span data-stu-id="5f321-110">Requirement</span></span> | <span data-ttu-id="5f321-111">Valore</span><span class="sxs-lookup"><span data-stu-id="5f321-111">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5f321-112">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="5f321-112">Minimum supported client</span></span><br/> | <span data-ttu-id="5f321-113">Windows 8</span><span class="sxs-lookup"><span data-stu-id="5f321-113">Windows 8</span></span><br/>                                                                                    |
| <span data-ttu-id="5f321-114">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="5f321-114">Minimum supported server</span></span><br/> | <span data-ttu-id="5f321-115">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="5f321-115">Windows Server 2012</span></span><br/>                                                                          |
| <span data-ttu-id="5f321-116">Intestazione</span><span class="sxs-lookup"><span data-stu-id="5f321-116">Header</span></span><br/>                   | <dl> <span data-ttu-id="5f321-117"><dt>Windows. ApplicationModel. h</dt></span><span class="sxs-lookup"><span data-stu-id="5f321-117"><dt>Windows.ApplicationModel.h</dt></span></span> </dl>   |
| <span data-ttu-id="5f321-118">IDL</span><span class="sxs-lookup"><span data-stu-id="5f321-118">IDL</span></span><br/>                      | <dl> <span data-ttu-id="5f321-119"><dt>Windows. ApplicationModel. idl</dt></span><span class="sxs-lookup"><span data-stu-id="5f321-119"><dt>Windows.ApplicationModel.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5f321-120">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="5f321-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5f321-121">**ISuspendingOperation**</span><span class="sxs-lookup"><span data-stu-id="5f321-121">**ISuspendingOperation**</span></span>](isuspendingoperation.md)
</dt> </dl>

 

 




