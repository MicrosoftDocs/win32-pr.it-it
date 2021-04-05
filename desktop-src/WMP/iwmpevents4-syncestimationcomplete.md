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
# <a name="iwmpevents4syncestimationcomplete-method"></a>Metodo IWMPEvents4:: SyncEstimationComplete

L'evento **SyncEstimationComplete** si verifica quando viene completata una stima delle dimensioni, avviata in precedenza da [**IWMPSyncDevice3:: estimateSyncSize**](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpsyncdevice3-estimatesyncsize).

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

*PDEVICE* \[ in\]
</dt> <dd>

Puntatore all'interfaccia [**IWMPSyncDevice**](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpsyncdevice) che rappresenta il dispositivo per il quale è stata avviata la stima delle dimensioni.

</dd> <dt>

*hrResult* \[ in\]
</dt> <dd>

Valore che indica l'esito positivo o negativo della stima.



| Valore                                                                                                                                       | Significato                                |
|---------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------|
| <span id="S_OK"></span><span id="s_ok"></span><dl> <dt>**\_OK**</dt> </dl>          | La stima è riuscita.<br/>   |
| <span id="E_ABORT"></span><span id="e_abort"></span><dl> <dt>**\_Interrompi E**</dt> </dl> | La stima è stata interrotta.<br/> |



 

</dd> <dt>

*lEstimatedUsedSpace* \[ in\]
</dt> <dd>

Spazio stimato (in byte) che verrebbe usato nel dispositivo.

</dd> <dt>

*lEstimatedSize* \[ in\]
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

 

 





