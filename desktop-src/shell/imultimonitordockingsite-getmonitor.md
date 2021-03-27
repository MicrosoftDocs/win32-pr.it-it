---
description: Ottiene il monitoraggio predefinito corrente.
title: 'Metodo IMultiMonitorDockingSite:: getmonitor'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IMultiMonitorDockingSite.GetMonitor
api_type:
- COM
api_location: ''
ms.assetid: 0bae75eb-ebd5-4de4-9249-0e9bb489f61f
ms.openlocfilehash: 1260da5ee4404a7ec4597a57e7e3836d6f133426
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104994944"
---
# <a name="imultimonitordockingsitegetmonitor-method"></a><span data-ttu-id="99b1d-103">Metodo IMultiMonitorDockingSite:: getmonitor</span><span class="sxs-lookup"><span data-stu-id="99b1d-103">IMultiMonitorDockingSite::GetMonitor method</span></span>

<span data-ttu-id="99b1d-104">Ottiene il monitoraggio predefinito corrente.</span><span class="sxs-lookup"><span data-stu-id="99b1d-104">Gets the current default monitor.</span></span>

## <a name="syntax"></a><span data-ttu-id="99b1d-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="99b1d-105">Syntax</span></span>


```C++
HRESULT GetMonitor(
  [in]  IUnknown *punkSrc,
  [out] HMONITOR *phMon
);
```



## <a name="parameters"></a><span data-ttu-id="99b1d-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="99b1d-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="99b1d-107">*punkSrc* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="99b1d-107">*punkSrc* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="99b1d-108">Tipo: \**[**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) \** _</span><span class="sxs-lookup"><span data-stu-id="99b1d-108">Type: \**[**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown)\** _</span></span>

<span data-ttu-id="99b1d-109">Puntatore all'oggetto che implementa l'interfaccia [_ *IDockingWindow* \*](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-idockingwindow) per la quale viene richiesto il monitoraggio.</span><span class="sxs-lookup"><span data-stu-id="99b1d-109">A pointer to the object implementing the [_ *IDockingWindow*\*](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-idockingwindow) interface for which the monitor is being requested.</span></span>

</dd> <dt>

<span data-ttu-id="99b1d-110">*phMon* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="99b1d-110">*phMon* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="99b1d-111">Tipo: \**HMONITOR \** _</span><span class="sxs-lookup"><span data-stu-id="99b1d-111">Type: \**HMONITOR\** _</span></span>

<span data-ttu-id="99b1d-112">Quando la funzione restituisce un risultato, contiene un puntatore all'handle del monitor predefinito.</span><span class="sxs-lookup"><span data-stu-id="99b1d-112">When the function returns, contains a pointer to the default monitor's handle.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="99b1d-113">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="99b1d-113">Return value</span></span>

<span data-ttu-id="99b1d-114">Tipo: _ *HRESULT*\*</span><span class="sxs-lookup"><span data-stu-id="99b1d-114">Type: _ *HRESULT*\*</span></span>

<span data-ttu-id="99b1d-115">Se questo metodo ha esito positivo, restituisce **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="99b1d-115">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="99b1d-116">In caso contrario, restituisce un codice di errore **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="99b1d-116">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="99b1d-117">Requisiti</span><span class="sxs-lookup"><span data-stu-id="99b1d-117">Requirements</span></span>



| <span data-ttu-id="99b1d-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="99b1d-118">Requirement</span></span> | <span data-ttu-id="99b1d-119">Valore</span><span class="sxs-lookup"><span data-stu-id="99b1d-119">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------|
| <span data-ttu-id="99b1d-120">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="99b1d-120">Minimum supported client</span></span><br/> | <span data-ttu-id="99b1d-121">Windows 2000 Professional, \[ solo app desktop Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="99b1d-121">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="99b1d-122">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="99b1d-122">Minimum supported server</span></span><br/> | <span data-ttu-id="99b1d-123">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="99b1d-123">Windows Server 2003 \[desktop apps only\]</span></span><br/>                   |



 

 
