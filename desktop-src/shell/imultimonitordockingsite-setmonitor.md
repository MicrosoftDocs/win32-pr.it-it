---
description: Modifica il monitoraggio usato per le barre degli strumenti ancorate in un sistema a più monitor.
title: 'Metodo IMultiMonitorDockingSite:: tomonitor'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IMultiMonitorDockingSite.SetMonitor
api_type:
- COM
api_location: ''
ms.assetid: ba4ace13-7096-4f05-bcb0-ab37f1632406
ms.openlocfilehash: cc177316a850bbf5059cabf48362ab8d5cbe2466
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104995200"
---
# <a name="imultimonitordockingsitesetmonitor-method"></a><span data-ttu-id="e45aa-103">Metodo IMultiMonitorDockingSite:: tomonitor</span><span class="sxs-lookup"><span data-stu-id="e45aa-103">IMultiMonitorDockingSite::SetMonitor method</span></span>

<span data-ttu-id="e45aa-104">Modifica il monitoraggio usato per le barre degli strumenti ancorate in un sistema a più monitor.</span><span class="sxs-lookup"><span data-stu-id="e45aa-104">Changes which monitor is used for docked toolbars on a multiple monitor system.</span></span>

## <a name="syntax"></a><span data-ttu-id="e45aa-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="e45aa-105">Syntax</span></span>


```C++
HRESULT SetMonitor(
  [in]  IUnknown *punkSrc,
  [in]  HMONITOR hMonNew,
  [out] HMONITOR *phMonOld
);
```



## <a name="parameters"></a><span data-ttu-id="e45aa-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="e45aa-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e45aa-107">*punkSrc* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="e45aa-107">*punkSrc* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e45aa-108">Tipo: \**[**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) \** _</span><span class="sxs-lookup"><span data-stu-id="e45aa-108">Type: \**[**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown)\** _</span></span>

<span data-ttu-id="e45aa-109">Puntatore all'oggetto che implementa l'interfaccia [_ *IDockingWindow* \*](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-idockingwindow) per la quale viene modificato il monitoraggio.</span><span class="sxs-lookup"><span data-stu-id="e45aa-109">A pointer to the object implementing the [_ *IDockingWindow*\*](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-idockingwindow) interface for which the monitor is being altered.</span></span>

</dd> <dt>

<span data-ttu-id="e45aa-110">*hMonNew* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="e45aa-110">*hMonNew* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e45aa-111">Tipo: **HMONITOR**</span><span class="sxs-lookup"><span data-stu-id="e45aa-111">Type: **HMONITOR**</span></span>

<span data-ttu-id="e45aa-112">Handle per il monitoraggio che sostituisce il monitoraggio predefinito esistente.</span><span class="sxs-lookup"><span data-stu-id="e45aa-112">A handle to the monitor that replaces the existing default monitor.</span></span>

</dd> <dt>

<span data-ttu-id="e45aa-113">*phMonOld* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="e45aa-113">*phMonOld* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="e45aa-114">Tipo: \**HMONITOR \** _</span><span class="sxs-lookup"><span data-stu-id="e45aa-114">Type: \**HMONITOR\** _</span></span>

<span data-ttu-id="e45aa-115">Quando la funzione restituisce un risultato, contiene un puntatore all'handle del monitor predefinito precedente.</span><span class="sxs-lookup"><span data-stu-id="e45aa-115">When this function returns, contains a pointer to the previous default monitor's handle.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e45aa-116">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="e45aa-116">Return value</span></span>

<span data-ttu-id="e45aa-117">Tipo: _ *HRESULT*\*</span><span class="sxs-lookup"><span data-stu-id="e45aa-117">Type: _ *HRESULT*\*</span></span>

<span data-ttu-id="e45aa-118">Se questo metodo ha esito positivo, restituisce **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="e45aa-118">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="e45aa-119">In caso contrario, restituisce un codice di errore **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="e45aa-119">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="e45aa-120">Requisiti</span><span class="sxs-lookup"><span data-stu-id="e45aa-120">Requirements</span></span>



| <span data-ttu-id="e45aa-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="e45aa-121">Requirement</span></span> | <span data-ttu-id="e45aa-122">Valore</span><span class="sxs-lookup"><span data-stu-id="e45aa-122">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------|
| <span data-ttu-id="e45aa-123">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="e45aa-123">Minimum supported client</span></span><br/> | <span data-ttu-id="e45aa-124">Windows 2000 Professional, \[ solo app desktop Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="e45aa-124">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="e45aa-125">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="e45aa-125">Minimum supported server</span></span><br/> | <span data-ttu-id="e45aa-126">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="e45aa-126">Windows Server 2003 \[desktop apps only\]</span></span><br/>                   |



 

 
