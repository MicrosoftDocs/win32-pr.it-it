---
description: Modifica il monitoraggio usato per le barre degli strumenti ancorate in un sistema a più monitor.
title: Metodo IMultiMonitorDockingSite::SetMonitor
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
ms.openlocfilehash: be773ee68c214f6a2fab8da89f1f48b867e71239
ms.sourcegitcommit: 3caaa3c92dcb1ef12f84464d14ce6262e65e988e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 05/12/2021
ms.locfileid: "109841942"
---
# <a name="imultimonitordockingsitesetmonitor-method"></a><span data-ttu-id="b4947-103">Metodo IMultiMonitorDockingSite::SetMonitor</span><span class="sxs-lookup"><span data-stu-id="b4947-103">IMultiMonitorDockingSite::SetMonitor method</span></span>

<span data-ttu-id="b4947-104">Modifica il monitoraggio usato per le barre degli strumenti ancorate in un sistema a più monitor.</span><span class="sxs-lookup"><span data-stu-id="b4947-104">Changes which monitor is used for docked toolbars on a multiple monitor system.</span></span>

## <a name="syntax"></a><span data-ttu-id="b4947-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="b4947-105">Syntax</span></span>


```C++
HRESULT SetMonitor(
  [in]  IUnknown *punkSrc,
  [in]  HMONITOR hMonNew,
  [out] HMONITOR *phMonOld
);
```



## <a name="parameters"></a><span data-ttu-id="b4947-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="b4947-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b4947-107">*punkSrc* \[ Pollici\]</span><span class="sxs-lookup"><span data-stu-id="b4947-107">*punkSrc* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b4947-108">Tipo: **[ **IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown)\***</span><span class="sxs-lookup"><span data-stu-id="b4947-108">Type: **[**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown)\***</span></span>

<span data-ttu-id="b4947-109">Puntatore all'oggetto che implementa [**l'interfaccia IDockingWindow**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-idockingwindow) per cui viene modificato il monitoraggio.</span><span class="sxs-lookup"><span data-stu-id="b4947-109">A pointer to the object implementing the [**IDockingWindow**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-idockingwindow) interface for which the monitor is being altered.</span></span>

</dd> <dt>

<span data-ttu-id="b4947-110">*hMonNew* \[ Pollici\]</span><span class="sxs-lookup"><span data-stu-id="b4947-110">*hMonNew* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b4947-111">Tipo: **HMONITOR**</span><span class="sxs-lookup"><span data-stu-id="b4947-111">Type: **HMONITOR**</span></span>

<span data-ttu-id="b4947-112">Handle per il monitoraggio che sostituisce il monitoraggio predefinito esistente.</span><span class="sxs-lookup"><span data-stu-id="b4947-112">A handle to the monitor that replaces the existing default monitor.</span></span>

</dd> <dt>

<span data-ttu-id="b4947-113">*phMonOld* \[ Cambio\]</span><span class="sxs-lookup"><span data-stu-id="b4947-113">*phMonOld* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="b4947-114">Tipo: **HMONITOR \***</span><span class="sxs-lookup"><span data-stu-id="b4947-114">Type: **HMONITOR\***</span></span>

<span data-ttu-id="b4947-115">Quando questa funzione viene restituita, contiene un puntatore all'handle del monitoraggio predefinito precedente.</span><span class="sxs-lookup"><span data-stu-id="b4947-115">When this function returns, contains a pointer to the previous default monitor's handle.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b4947-116">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="b4947-116">Return value</span></span>

<span data-ttu-id="b4947-117">Tipo: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="b4947-117">Type: **HRESULT**</span></span>

<span data-ttu-id="b4947-118">Se questo metodo ha esito positivo, restituisce **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="b4947-118">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="b4947-119">In caso contrario, restituisce un **codice di errore HRESULT.**</span><span class="sxs-lookup"><span data-stu-id="b4947-119">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="b4947-120">Requisiti</span><span class="sxs-lookup"><span data-stu-id="b4947-120">Requirements</span></span>



| <span data-ttu-id="b4947-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="b4947-121">Requirement</span></span> | <span data-ttu-id="b4947-122">Valore</span><span class="sxs-lookup"><span data-stu-id="b4947-122">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------|
| <span data-ttu-id="b4947-123">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="b4947-123">Minimum supported client</span></span><br/> | <span data-ttu-id="b4947-124">Solo app desktop di Windows 2000 Professional e Windows XP \[\]</span><span class="sxs-lookup"><span data-stu-id="b4947-124">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="b4947-125">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="b4947-125">Minimum supported server</span></span><br/> | <span data-ttu-id="b4947-126">Solo app desktop di Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="b4947-126">Windows Server 2003 \[desktop apps only\]</span></span><br/>                   |



 

 
