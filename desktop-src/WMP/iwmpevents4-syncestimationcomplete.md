---
title: Metodo IWMPEvents4 SyncEstimationComplete
description: L'evento SyncEstimationComplete si verifica quando viene completata una stima delle dimensioni, avviata in precedenza da IWMPSyncDevice3 estimateSyncSize.
ms.assetid: 2fb45a13-d82b-48b6-b9bb-46409f33a33f
keywords:
- Metodo SyncEstimationComplete Windows Media Player
- Metodo SyncEstimationComplete Windows Media Player, interfaccia IWMPEvents4
- Interfaccia IWMPEvents4 Windows Media Player, metodo SyncEstimationComplete
topic_type:
- apiref
api_name:
- IWMPEvents4.SyncEstimationComplete
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 209ed2f2bd0f075dbaa8d442a276c994d50ce2e5
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/19/2020
ms.locfileid: "103723383"
---
# <a name="iwmpevents4syncestimationcomplete-method"></a><span data-ttu-id="edb53-106">Metodo IWMPEvents4:: SyncEstimationComplete</span><span class="sxs-lookup"><span data-stu-id="edb53-106">IWMPEvents4::SyncEstimationComplete method</span></span>

<span data-ttu-id="edb53-107">L'evento **SyncEstimationComplete** si verifica quando viene completata una stima delle dimensioni, avviata in precedenza da [**IWMPSyncDevice3:: estimateSyncSize**](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpsyncdevice3-estimatesyncsize).</span><span class="sxs-lookup"><span data-stu-id="edb53-107">The **SyncEstimationComplete** event occurs when a size estimation, previously initiated by [**IWMPSyncDevice3::estimateSyncSize**](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpsyncdevice3-estimatesyncsize), is complete.</span></span>

## <a name="syntax"></a><span data-ttu-id="edb53-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="edb53-108">Syntax</span></span>


```C++
void SyncEstimationComplete(
  [in] IWMPSyncDevice *pDevice,
  [in] long           hrResult,
  [in] long           lEstimatedUsedSpace,
  [in] long           lEstimatedSize
);
```



## <a name="parameters"></a><span data-ttu-id="edb53-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="edb53-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="edb53-110">*PDEVICE* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="edb53-110">*pDevice* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="edb53-111">Puntatore all'interfaccia [**IWMPSyncDevice**](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpsyncdevice) che rappresenta il dispositivo per il quale è stata avviata la stima delle dimensioni.</span><span class="sxs-lookup"><span data-stu-id="edb53-111">Pointer to the [**IWMPSyncDevice**](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpsyncdevice) interface that represents the device for which the size estimation was initiated.</span></span>

</dd> <dt>

<span data-ttu-id="edb53-112">*hrResult* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="edb53-112">*hrResult* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="edb53-113">Valore che indica l'esito positivo o negativo della stima.</span><span class="sxs-lookup"><span data-stu-id="edb53-113">A value that indicates the success or failure of the estimation.</span></span>



| <span data-ttu-id="edb53-114">Valore</span><span class="sxs-lookup"><span data-stu-id="edb53-114">Value</span></span>                                                                                                                                       | <span data-ttu-id="edb53-115">Significato</span><span class="sxs-lookup"><span data-stu-id="edb53-115">Meaning</span></span>                                |
|---------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------|
| <span id="S_OK"></span><span id="s_ok"></span><dl> <span data-ttu-id="edb53-116"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="edb53-116"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="edb53-117">La stima è riuscita.</span><span class="sxs-lookup"><span data-stu-id="edb53-117">The estimation succeeded.</span></span><br/>   |
| <span id="E_ABORT"></span><span id="e_abort"></span><dl> <span data-ttu-id="edb53-118"><dt>**\_Interrompi E**</dt></span><span class="sxs-lookup"><span data-stu-id="edb53-118"><dt>**E\_ABORT**</dt></span></span> </dl> | <span data-ttu-id="edb53-119">La stima è stata interrotta.</span><span class="sxs-lookup"><span data-stu-id="edb53-119">The estimation was aborted.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="edb53-120">*lEstimatedUsedSpace* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="edb53-120">*lEstimatedUsedSpace* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="edb53-121">Spazio stimato (in byte) che verrebbe usato nel dispositivo.</span><span class="sxs-lookup"><span data-stu-id="edb53-121">The estimated space (in bytes) that would be used on the device.</span></span>

</dd> <dt>

<span data-ttu-id="edb53-122">*lEstimatedSize* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="edb53-122">*lEstimatedSize* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="edb53-123">Dimensioni stimate (in byte) dei dati da sincronizzare.</span><span class="sxs-lookup"><span data-stu-id="edb53-123">The estimated size (in bytes) of the data to be synchronized.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="edb53-124">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="edb53-124">Return value</span></span>

<span data-ttu-id="edb53-125">Questo metodo non restituisce valori.</span><span class="sxs-lookup"><span data-stu-id="edb53-125">This method does not return a value.</span></span>

## <a name="see-also"></a><span data-ttu-id="edb53-126">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="edb53-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="edb53-127">**Interfaccia IWMPEvents4**</span><span class="sxs-lookup"><span data-stu-id="edb53-127">**IWMPEvents4 Interface**</span></span>](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpevents4)
</dt> <dt>

[<span data-ttu-id="edb53-128">**IWMPSyncDevice3::estimateSyncSize**</span><span class="sxs-lookup"><span data-stu-id="edb53-128">**IWMPSyncDevice3::estimateSyncSize**</span></span>](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpsyncdevice3-estimatesyncsize)
</dt> </dl>

 

 





