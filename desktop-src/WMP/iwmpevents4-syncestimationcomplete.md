---
title: Metodo IWMPEvents4 SyncEstimationComplete
description: L'evento SyncEstimationComplete si verifica quando una stima delle dimensioni, avviata in precedenza da IWMPSyncDevice3 estimateSyncSize, è completa.
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
ms.openlocfilehash: b3f444cdc66874c907bb4c6412fa10384fde67145563d79153c28cb675c6fc3b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118575606"
---
# <a name="iwmpevents4syncestimationcomplete-method"></a>Metodo IWMPEvents4::SyncEstimationComplete

**L'evento SyncEstimationComplete** si verifica quando una stima delle dimensioni, avviata in precedenza da [**IWMPSyncDevice3::estimateSyncSize,**](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpsyncdevice3-estimatesyncsize)è completa.

## <a name="syntax"></a>Sintassi


```C++
void SyncEstimationComplete(
  [in] IWMPSyncDevice *pDevice,
  [in] long           hrResult,
  [in] long           lEstimatedUsedSpace,
  [in] long           lEstimatedSize
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pDevice* \[ Pollici\]
</dt> <dd>

Puntatore [**all'interfaccia IWMPSyncDevice**](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpsyncdevice) che rappresenta il dispositivo per cui è stata avviata la stima delle dimensioni.

</dd> <dt>

*hrResult* \[ Pollici\]
</dt> <dd>

Valore che indica l'esito positivo o negativo della stima.



| Valore                                                                                                                                       | Significato                                |
|---------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------|
| <span id="S_OK"></span><span id="s_ok"></span><dl> <dt>**S \_ OK**</dt> </dl>          | La stima è riuscita.<br/>   |
| <span id="E_ABORT"></span><span id="e_abort"></span><dl> <dt>**E \_ ABORT**</dt> </dl> | La stima è stata interrotta.<br/> |



 

</dd> <dt>

*lEstimatedUsedSpace* \[ Pollici\]
</dt> <dd>

Spazio stimato (in byte) che verrebbe usato nel dispositivo.

</dd> <dt>

*lEstimatedSize* \[ Pollici\]
</dt> <dd>

Dimensioni stimate (in byte) dei dati da sincronizzare.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo metodo non restituisce valori.

## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Interfaccia IWMPEvents4**](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpevents4)
</dt> <dt>

[**IWMPSyncDevice3::estimateSyncSize**](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpsyncdevice3-estimatesyncsize)
</dt> </dl>

 

 





