---
description: Ottiene l'operazione di sospensione dell'app.
ms.assetid: 33FCAED5-7568-4483-A643-A536B53F7003
title: 'Proprietà ISuspendingEventArgs:: SuspendingOperation (Windows. ApplicationModel. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISuspendingEventArgs.SuspendingOperation
- ISuspendingEventArgs.get_SuspendingOperation
- ISuspendingEventArgs.put_SuspendingOperation
api_type:
- COM
api_location:
- Windows.ApplicationModel.h
ms.openlocfilehash: e12ccbb372d7c712585766bba8d7921fae57a617
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103879257"
---
# <a name="isuspendingeventargssuspendingoperation-property"></a><span data-ttu-id="addb5-103">Proprietà ISuspendingEventArgs:: SuspendingOperation</span><span class="sxs-lookup"><span data-stu-id="addb5-103">ISuspendingEventArgs::SuspendingOperation property</span></span>

<span data-ttu-id="addb5-104">Ottiene l'operazione di sospensione dell'app.</span><span class="sxs-lookup"><span data-stu-id="addb5-104">Gets the app suspending operation.</span></span>

<span data-ttu-id="addb5-105">Si tratta di una proprietà di lettura/scrittura.</span><span class="sxs-lookup"><span data-stu-id="addb5-105">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="addb5-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="addb5-106">Syntax</span></span>


```C++
HRESULT put_SuspendingOperation();

HRESULT get_SuspendingOperation(
  [out, retval] ISuspendingOperation **value
);
```



## <a name="property-value"></a><span data-ttu-id="addb5-107">Valore proprietà</span><span class="sxs-lookup"><span data-stu-id="addb5-107">Property value</span></span>

<span data-ttu-id="addb5-108">Operazione di sospensione.</span><span class="sxs-lookup"><span data-stu-id="addb5-108">The suspending operation.</span></span>

## <a name="requirements"></a><span data-ttu-id="addb5-109">Requisiti</span><span class="sxs-lookup"><span data-stu-id="addb5-109">Requirements</span></span>



| <span data-ttu-id="addb5-110">Requisito</span><span class="sxs-lookup"><span data-stu-id="addb5-110">Requirement</span></span> | <span data-ttu-id="addb5-111">Valore</span><span class="sxs-lookup"><span data-stu-id="addb5-111">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="addb5-112">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="addb5-112">Minimum supported client</span></span><br/> | <span data-ttu-id="addb5-113">Windows 8</span><span class="sxs-lookup"><span data-stu-id="addb5-113">Windows 8</span></span><br/>                                                                                    |
| <span data-ttu-id="addb5-114">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="addb5-114">Minimum supported server</span></span><br/> | <span data-ttu-id="addb5-115">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="addb5-115">Windows Server 2012</span></span><br/>                                                                          |
| <span data-ttu-id="addb5-116">Intestazione</span><span class="sxs-lookup"><span data-stu-id="addb5-116">Header</span></span><br/>                   | <dl> <span data-ttu-id="addb5-117"><dt>Windows. ApplicationModel. h</dt></span><span class="sxs-lookup"><span data-stu-id="addb5-117"><dt>Windows.ApplicationModel.h</dt></span></span> </dl>   |
| <span data-ttu-id="addb5-118">IDL</span><span class="sxs-lookup"><span data-stu-id="addb5-118">IDL</span></span><br/>                      | <dl> <span data-ttu-id="addb5-119"><dt>Windows. ApplicationModel. idl</dt></span><span class="sxs-lookup"><span data-stu-id="addb5-119"><dt>Windows.ApplicationModel.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="addb5-120">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="addb5-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="addb5-121">**ISuspendingEventArgs**</span><span class="sxs-lookup"><span data-stu-id="addb5-121">**ISuspendingEventArgs**</span></span>](isuspendingeventargs.md)
</dt> </dl>

 

 




