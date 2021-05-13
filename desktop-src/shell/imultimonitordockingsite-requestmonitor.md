---
description: Verifica che il monitoraggio sia attivo e disponibile.
title: Metodo IMultiMonitorDockingSite::RequestMonitor
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
ms.openlocfilehash: 7f219e5fd62fb4f85fd206501e6a53ac3927195a
ms.sourcegitcommit: 3caaa3c92dcb1ef12f84464d14ce6262e65e988e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 05/12/2021
ms.locfileid: "109841972"
---
# <a name="imultimonitordockingsiterequestmonitor-method"></a><span data-ttu-id="dbdfa-103">Metodo IMultiMonitorDockingSite::RequestMonitor</span><span class="sxs-lookup"><span data-stu-id="dbdfa-103">IMultiMonitorDockingSite::RequestMonitor method</span></span>

<span data-ttu-id="dbdfa-104">Verifica che il monitoraggio sia attivo e disponibile.</span><span class="sxs-lookup"><span data-stu-id="dbdfa-104">Verifies that the monitor is active and available.</span></span>

## <a name="syntax"></a><span data-ttu-id="dbdfa-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="dbdfa-105">Syntax</span></span>


```C++
HRESULT RequestMonitor(
  [in] IUnknown *punkSrc,
  [in] HMONITOR *phMon
);
```



## <a name="parameters"></a><span data-ttu-id="dbdfa-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="dbdfa-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="dbdfa-107">*punkSrc* \[ Pollici\]</span><span class="sxs-lookup"><span data-stu-id="dbdfa-107">*punkSrc* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="dbdfa-108">Tipo: **[ **IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown)\***</span><span class="sxs-lookup"><span data-stu-id="dbdfa-108">Type: **[**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown)\***</span></span>

<span data-ttu-id="dbdfa-109">Puntatore all'oggetto che implementa [**l'interfaccia IDockingWindow.**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-idockingwindow)</span><span class="sxs-lookup"><span data-stu-id="dbdfa-109">A pointer to the object implementing the [**IDockingWindow**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-idockingwindow) interface.</span></span>

</dd> <dt>

<span data-ttu-id="dbdfa-110">*phMon* \[ Pollici\]</span><span class="sxs-lookup"><span data-stu-id="dbdfa-110">*phMon* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="dbdfa-111">Tipo: **HMONITOR \***</span><span class="sxs-lookup"><span data-stu-id="dbdfa-111">Type: **HMONITOR\***</span></span>

<span data-ttu-id="dbdfa-112">Puntatore all'handle del monitoraggio predefinito.</span><span class="sxs-lookup"><span data-stu-id="dbdfa-112">A pointer to the default monitor's handle.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="dbdfa-113">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="dbdfa-113">Return value</span></span>

<span data-ttu-id="dbdfa-114">Tipo: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="dbdfa-114">Type: **HRESULT**</span></span>

<span data-ttu-id="dbdfa-115">Se questo metodo ha esito positivo, restituisce **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="dbdfa-115">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="dbdfa-116">In caso contrario, restituisce un **codice di errore HRESULT.**</span><span class="sxs-lookup"><span data-stu-id="dbdfa-116">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="dbdfa-117">Requisiti</span><span class="sxs-lookup"><span data-stu-id="dbdfa-117">Requirements</span></span>



| <span data-ttu-id="dbdfa-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="dbdfa-118">Requirement</span></span> | <span data-ttu-id="dbdfa-119">Valore</span><span class="sxs-lookup"><span data-stu-id="dbdfa-119">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------|
| <span data-ttu-id="dbdfa-120">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="dbdfa-120">Minimum supported client</span></span><br/> | <span data-ttu-id="dbdfa-121">Solo app desktop windows 2000 Professional e Windows XP \[\]</span><span class="sxs-lookup"><span data-stu-id="dbdfa-121">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="dbdfa-122">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="dbdfa-122">Minimum supported server</span></span><br/> | <span data-ttu-id="dbdfa-123">Solo app desktop di Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="dbdfa-123">Windows Server 2003 \[desktop apps only\]</span></span><br/>                   |



 

 
