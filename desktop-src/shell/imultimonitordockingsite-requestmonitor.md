---
description: Verifica che il monitoraggio sia attivo e disponibile.
title: 'Metodo IMultiMonitorDockingSite:: RequestMonitor'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IMultiMonitorDockingSite.RequestMonitor
api_type:
- COM
api_location: ''
ms.assetid: 9aa6eb20-de39-41f7-a17e-183f4088f972
ms.openlocfilehash: 5389b10af9aaa3da5d3106d82a4fbdcbd614a094
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103968697"
---
# <a name="imultimonitordockingsiterequestmonitor-method"></a><span data-ttu-id="e288e-103">Metodo IMultiMonitorDockingSite:: RequestMonitor</span><span class="sxs-lookup"><span data-stu-id="e288e-103">IMultiMonitorDockingSite::RequestMonitor method</span></span>

<span data-ttu-id="e288e-104">Verifica che il monitoraggio sia attivo e disponibile.</span><span class="sxs-lookup"><span data-stu-id="e288e-104">Verifies that the monitor is active and available.</span></span>

## <a name="syntax"></a><span data-ttu-id="e288e-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="e288e-105">Syntax</span></span>


```C++
HRESULT RequestMonitor(
  [in] IUnknown *punkSrc,
  [in] HMONITOR *phMon
);
```



## <a name="parameters"></a><span data-ttu-id="e288e-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="e288e-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e288e-107">*punkSrc* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="e288e-107">*punkSrc* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e288e-108">Tipo: \**[**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) \** _</span><span class="sxs-lookup"><span data-stu-id="e288e-108">Type: \**[**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown)\** _</span></span>

<span data-ttu-id="e288e-109">Puntatore all'oggetto che implementa l'interfaccia [_ *IDockingWindow* \*](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-idockingwindow) .</span><span class="sxs-lookup"><span data-stu-id="e288e-109">A pointer to the object implementing the [_ *IDockingWindow*\*](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-idockingwindow) interface.</span></span>

</dd> <dt>

<span data-ttu-id="e288e-110">*phMon* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="e288e-110">*phMon* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e288e-111">Tipo: \**HMONITOR \** _</span><span class="sxs-lookup"><span data-stu-id="e288e-111">Type: \**HMONITOR\** _</span></span>

<span data-ttu-id="e288e-112">Puntatore all'handle del monitor predefinito.</span><span class="sxs-lookup"><span data-stu-id="e288e-112">A pointer to the default monitor's handle.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e288e-113">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="e288e-113">Return value</span></span>

<span data-ttu-id="e288e-114">Tipo: _ *HRESULT*\*</span><span class="sxs-lookup"><span data-stu-id="e288e-114">Type: _ *HRESULT*\*</span></span>

<span data-ttu-id="e288e-115">Se questo metodo ha esito positivo, restituisce **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="e288e-115">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="e288e-116">In caso contrario, restituisce un codice di errore **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="e288e-116">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="e288e-117">Requisiti</span><span class="sxs-lookup"><span data-stu-id="e288e-117">Requirements</span></span>



| <span data-ttu-id="e288e-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="e288e-118">Requirement</span></span> | <span data-ttu-id="e288e-119">Valore</span><span class="sxs-lookup"><span data-stu-id="e288e-119">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------|
| <span data-ttu-id="e288e-120">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="e288e-120">Minimum supported client</span></span><br/> | <span data-ttu-id="e288e-121">Windows 2000 Professional, \[ solo app desktop Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="e288e-121">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="e288e-122">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="e288e-122">Minimum supported server</span></span><br/> | <span data-ttu-id="e288e-123">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="e288e-123">Windows Server 2003 \[desktop apps only\]</span></span><br/>                   |



 

 
