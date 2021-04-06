---
title: Metodo IAccessibilityDockingService GetAvailableSize
description: Ottiene le dimensioni disponibili per l'ancoraggio di una finestra di accessibilità su un monitor.
ms.assetid: 1C838B01-EF26-4FCC-878F-A36DEFBA3142
keywords:
- Metodo GetAvailableSize COM
- Metodo GetAvailableSize COM, interfaccia IAccessibilityDockingService
- Interfaccia IAccessibilityDockingService COM, metodo GetAvailableSize
topic_type:
- apiref
api_name:
- IAccessibilityDockingService.GetAvailableSize
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: e1b9f113792b14f5fb86e0349d083ea48ffdb3fd
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/25/2019
ms.locfileid: "104045682"
---
# <a name="iaccessibilitydockingservicegetavailablesize-method"></a><span data-ttu-id="2ce28-106">Metodo IAccessibilityDockingService:: GetAvailableSize</span><span class="sxs-lookup"><span data-stu-id="2ce28-106">IAccessibilityDockingService::GetAvailableSize method</span></span>

<span data-ttu-id="2ce28-107">Ottiene le dimensioni disponibili per l'ancoraggio di una finestra di accessibilità su un monitor.</span><span class="sxs-lookup"><span data-stu-id="2ce28-107">Gets the dimensions available for docking an accessibility window on a monitor.</span></span>

## <a name="syntax"></a><span data-ttu-id="2ce28-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="2ce28-108">Syntax</span></span>


```C++
HRESULT GetAvailableSize(
  [in]  HMONITOR hMonitor,
  [out] UINT     *puMaxHeight,
  [out] UINT     *puFixedWidth
);
```



## <a name="parameters"></a><span data-ttu-id="2ce28-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="2ce28-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2ce28-110">*hMonitor* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="2ce28-110">*hMonitor* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2ce28-111">Specifica il monitoraggio per cui verranno recuperate le dimensioni di ancoraggio disponibili.</span><span class="sxs-lookup"><span data-stu-id="2ce28-111">Specifies the monitor for which the available docking size will be retrieved.</span></span>

</dd> <dt>

<span data-ttu-id="2ce28-112">*puMaxHeight* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="2ce28-112">*puMaxHeight* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="2ce28-113">Se l'operazione riesce, impostare sull'altezza massima disponibile per l'ancoraggio sul *hMonitor* specificato, in pixel.</span><span class="sxs-lookup"><span data-stu-id="2ce28-113">On success, set to the maximum height available for docking on the specified *hMonitor*, in pixels.</span></span>

<span data-ttu-id="2ce28-114">In caso di errore, impostare su zero.</span><span class="sxs-lookup"><span data-stu-id="2ce28-114">On failure, set to zero.</span></span>

</dd> <dt>

<span data-ttu-id="2ce28-115">*puFixedWidth* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="2ce28-115">*puFixedWidth* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="2ce28-116">Se l'operazione riesce, impostare sulla larghezza fissa disponibile per l'ancoraggio sul *hMonitor* specificato, in pixel.</span><span class="sxs-lookup"><span data-stu-id="2ce28-116">On success, set to the fixed width available for docking on the specified *hMonitor*, in pixels.</span></span> <span data-ttu-id="2ce28-117">Tutte le finestre ancorate a questo *hMonitor* verranno ridimensionate in base a questa larghezza.</span><span class="sxs-lookup"><span data-stu-id="2ce28-117">Any window docked to this *hMonitor* will be sized to this width.</span></span>

<span data-ttu-id="2ce28-118">In caso di errore, impostare su zero.</span><span class="sxs-lookup"><span data-stu-id="2ce28-118">On failure, set to zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2ce28-119">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="2ce28-119">Return value</span></span>



| <span data-ttu-id="2ce28-120">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="2ce28-120">Return code</span></span>                                                                                                                          | <span data-ttu-id="2ce28-121">Descrizione</span><span class="sxs-lookup"><span data-stu-id="2ce28-121">Description</span></span>                                                                      |
|--------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="2ce28-122"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="2ce28-122"><dt>**S\_OK**</dt></span></span> </dl>                                                 | <span data-ttu-id="2ce28-123">Esito positivo.</span><span class="sxs-lookup"><span data-stu-id="2ce28-123">Success.</span></span><br/>                                                              |
| <dl> <span data-ttu-id="2ce28-124"><dt>**HRESULT \_ da \_ Win32 (errore \_ dell' \_ handle di monitoraggio non valido \_ )**</dt></span><span class="sxs-lookup"><span data-stu-id="2ce28-124"><dt>**HRESULT\_FROM\_WIN32(ERROR\_INVALID\_MONITOR\_HANDLE)**</dt></span></span> </dl> | <span data-ttu-id="2ce28-125">Il monitoraggio specificato dall'handle di monitoraggio non supporta l'ancoraggio.</span><span class="sxs-lookup"><span data-stu-id="2ce28-125">The monitor specified by the monitor handle does not support docking.</span></span><br/> |



 

<span data-ttu-id="2ce28-126">Se *puMaxHeight* o *puFixedWidth* sono null, si verificherà una violazione di accesso.</span><span class="sxs-lookup"><span data-stu-id="2ce28-126">If either *puMaxHeight* or *puFixedWidth* are null, an access violation will occur.</span></span>

## <a name="remarks"></a><span data-ttu-id="2ce28-127">Commenti</span><span class="sxs-lookup"><span data-stu-id="2ce28-127">Remarks</span></span>

<span data-ttu-id="2ce28-128">Le finestre di accessibilità possono essere ancorate a un monitor con almeno 768 pixel di schermo verticali.</span><span class="sxs-lookup"><span data-stu-id="2ce28-128">Accessibility windows can only be docked to a monitor that has at least 768 vertical screen pixels.</span></span> <span data-ttu-id="2ce28-129">Questa API non consentirà a tali finestre di essere ancorate con un'altezza che comporterebbe la visualizzazione delle app di Windows Store con meno di 768 pixel di schermo verticali.</span><span class="sxs-lookup"><span data-stu-id="2ce28-129">This API will not allow such windows to be docked with a height that would cause Windows Store apps to have less than 768 vertical screen pixels.</span></span>

## <a name="examples"></a><span data-ttu-id="2ce28-130">Esempi</span><span class="sxs-lookup"><span data-stu-id="2ce28-130">Examples</span></span>


```
IAccessibilityDockingService *pDockingService;
HRESULT hr = CoCreateInstance(CLSID_AccessibilityDockingService, CLSCTX_INPROV_SERVER, nullptr, IID_PPV_ARGS(&pDockingService));
if (SUCCEEDED(hr))
{
    UINT uMaxHeight;
    UINT uFixedWidth;

    HMONITOR hMonitor = MonitorFromWindow(_hwndMyApplication, MONITOR_DEFAULTTONULL);
    if (hMonitor != nullptr)
    {
        hr = pDockingService->GetAvailableSize(hMonitor, &uMaxHeight, &uFixedWidth);
    }
}
```



## <a name="see-also"></a><span data-ttu-id="2ce28-131">Vedere anche</span><span class="sxs-lookup"><span data-stu-id="2ce28-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2ce28-132">**IAccessibilityDockingService**</span><span class="sxs-lookup"><span data-stu-id="2ce28-132">**IAccessibilityDockingService**</span></span>](/windows/desktop/api/shobjidl/nn-shobjidl-iaccessibilitydockingservice)
</dt> </dl>

 

 





