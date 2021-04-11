---
description: Si verifica quando viene attivata un'app di Windows Store.
ms.assetid: CA0DB2D4-3417-48F5-8455-D87D0F323A1E
title: 'Evento ICoreApplicationView:: Activated (Windows. ApplicationModel. Core. h)'
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 612f7110aa149396b18815afe664ee404c70fc52
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104226100"
---
# <a name="icoreapplicationviewactivated-event"></a><span data-ttu-id="9826a-103">Evento ICoreApplicationView:: Activated</span><span class="sxs-lookup"><span data-stu-id="9826a-103">ICoreApplicationView::Activated event</span></span>

<span data-ttu-id="9826a-104">Si verifica quando viene attivata un'app di Windows Store.</span><span class="sxs-lookup"><span data-stu-id="9826a-104">Occurs when a Windows Store app is activated.</span></span>

## <a name="syntax"></a><span data-ttu-id="9826a-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="9826a-105">Syntax</span></span>


```C++
void Activated(
  [in] ITypedEventHandler<ICoreApplicationView*, IActivatedEventArgs*> handler
);
```



## <a name="parameters"></a><span data-ttu-id="9826a-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="9826a-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9826a-107">*gestore* \[ di in\]</span><span class="sxs-lookup"><span data-stu-id="9826a-107">*handler* \[in\]</span></span>
<span data-ttu-id="9826a-108"></dt> <dd></dd> </dl></span><span class="sxs-lookup"><span data-stu-id="9826a-108"></dt> <dd></dd> </dl></span></span>

## <a name="return-value"></a><span data-ttu-id="9826a-109">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="9826a-109">Return value</span></span>

<span data-ttu-id="9826a-110">Questo evento non restituisce un valore.</span><span class="sxs-lookup"><span data-stu-id="9826a-110">This event does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="9826a-111">Commenti</span><span class="sxs-lookup"><span data-stu-id="9826a-111">Remarks</span></span>

<span data-ttu-id="9826a-112">Non chiamare il metodo [**Exit**](/previous-versions//hh438368(v=vs.85)) dall'interno del *gestore*.</span><span class="sxs-lookup"><span data-stu-id="9826a-112">Do not call the [**Exit**](/previous-versions//hh438368(v=vs.85)) method from within *handler*.</span></span>

## <a name="requirements"></a><span data-ttu-id="9826a-113">Requisiti</span><span class="sxs-lookup"><span data-stu-id="9826a-113">Requirements</span></span>



| <span data-ttu-id="9826a-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="9826a-114">Requirement</span></span> | <span data-ttu-id="9826a-115">Valore</span><span class="sxs-lookup"><span data-stu-id="9826a-115">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9826a-116">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="9826a-116">Minimum supported client</span></span><br/> | <span data-ttu-id="9826a-117">Windows 8</span><span class="sxs-lookup"><span data-stu-id="9826a-117">Windows 8</span></span><br/>                                                                                         |
| <span data-ttu-id="9826a-118">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="9826a-118">Minimum supported server</span></span><br/> | <span data-ttu-id="9826a-119">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="9826a-119">Windows Server 2012</span></span><br/>                                                                               |
| <span data-ttu-id="9826a-120">Intestazione</span><span class="sxs-lookup"><span data-stu-id="9826a-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="9826a-121"><dt>Windows. ApplicationModel. Core. h</dt></span><span class="sxs-lookup"><span data-stu-id="9826a-121"><dt>Windows.ApplicationModel.Core.h</dt></span></span> </dl>   |
| <span data-ttu-id="9826a-122">IDL</span><span class="sxs-lookup"><span data-stu-id="9826a-122">IDL</span></span><br/>                      | <dl> <span data-ttu-id="9826a-123"><dt>Windows. ApplicationModel. Core. idl</dt></span><span class="sxs-lookup"><span data-stu-id="9826a-123"><dt>Windows.ApplicationModel.Core.idl</dt></span></span> </dl> |



 

 
