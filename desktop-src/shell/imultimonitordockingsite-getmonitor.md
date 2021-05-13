---
description: Ottiene il monitoraggio predefinito corrente.
title: Metodo IMultiMonitorDockingSite::GetMonitor
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
ms.openlocfilehash: 2cd437fd6c0e842eb314db6c57420af6b54b05ff
ms.sourcegitcommit: 3caaa3c92dcb1ef12f84464d14ce6262e65e988e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 05/12/2021
ms.locfileid: "109840642"
---
# <a name="imultimonitordockingsitegetmonitor-method"></a><span data-ttu-id="3f919-103">Metodo IMultiMonitorDockingSite::GetMonitor</span><span class="sxs-lookup"><span data-stu-id="3f919-103">IMultiMonitorDockingSite::GetMonitor method</span></span>

<span data-ttu-id="3f919-104">Ottiene il monitoraggio predefinito corrente.</span><span class="sxs-lookup"><span data-stu-id="3f919-104">Gets the current default monitor.</span></span>

## <a name="syntax"></a><span data-ttu-id="3f919-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="3f919-105">Syntax</span></span>


```C++
HRESULT GetMonitor(
  [in]  IUnknown *punkSrc,
  [out] HMONITOR *phMon
);
```



## <a name="parameters"></a><span data-ttu-id="3f919-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="3f919-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3f919-107">*punkSrc* \[ Pollici\]</span><span class="sxs-lookup"><span data-stu-id="3f919-107">*punkSrc* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3f919-108">Tipo: **[ **IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown)\***</span><span class="sxs-lookup"><span data-stu-id="3f919-108">Type: **[**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown)\***</span></span>

<span data-ttu-id="3f919-109">Puntatore all'oggetto che implementa [**l'interfaccia IDockingWindow**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-idockingwindow) per cui viene richiesto il monitoraggio.</span><span class="sxs-lookup"><span data-stu-id="3f919-109">A pointer to the object implementing the [**IDockingWindow**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-idockingwindow) interface for which the monitor is being requested.</span></span>

</dd> <dt>

<span data-ttu-id="3f919-110">*phMon* \[ Cambio\]</span><span class="sxs-lookup"><span data-stu-id="3f919-110">*phMon* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="3f919-111">Tipo: **HMONITOR \***</span><span class="sxs-lookup"><span data-stu-id="3f919-111">Type: **HMONITOR\***</span></span>

<span data-ttu-id="3f919-112">Quando la funzione viene restituita, contiene un puntatore all'handle del monitoraggio predefinito.</span><span class="sxs-lookup"><span data-stu-id="3f919-112">When the function returns, contains a pointer to the default monitor's handle.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3f919-113">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="3f919-113">Return value</span></span>

<span data-ttu-id="3f919-114">Tipo: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="3f919-114">Type: **HRESULT**</span></span>

<span data-ttu-id="3f919-115">Se questo metodo ha esito positivo, restituisce **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="3f919-115">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="3f919-116">In caso contrario, restituisce un **codice di errore HRESULT.**</span><span class="sxs-lookup"><span data-stu-id="3f919-116">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="3f919-117">Requisiti</span><span class="sxs-lookup"><span data-stu-id="3f919-117">Requirements</span></span>



| <span data-ttu-id="3f919-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="3f919-118">Requirement</span></span> | <span data-ttu-id="3f919-119">Valore</span><span class="sxs-lookup"><span data-stu-id="3f919-119">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------|
| <span data-ttu-id="3f919-120">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="3f919-120">Minimum supported client</span></span><br/> | <span data-ttu-id="3f919-121">Solo app desktop windows 2000 Professional e Windows XP \[\]</span><span class="sxs-lookup"><span data-stu-id="3f919-121">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="3f919-122">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="3f919-122">Minimum supported server</span></span><br/> | <span data-ttu-id="3f919-123">Solo app desktop di Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="3f919-123">Windows Server 2003 \[desktop apps only\]</span></span><br/>                   |



 

 
