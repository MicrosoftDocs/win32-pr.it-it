---
title: Metodo Settings. getMode
description: Il metodo GetMode determina se la modalità ciclo o shuffle è attiva.
ms.assetid: 41c3725f-ae8f-4b45-856a-b7245c9ad2b3
keywords:
- Metodo GetMode Windows Media Player
- Metodo GetMode Windows Media Player, classe Settings
- Classe Settings Media Player Windows, metodo GetMode
topic_type:
- apiref
api_name:
- Settings.getMode
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a5fc3e82091200d05bb173c71f2c0e5a7d213b80
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106327384"
---
# <a name="settingsgetmode-method"></a>Metodo Settings. getMode

Il metodo **GetMode** determina se la modalità ciclo o shuffle è attiva.

## <a name="syntax"></a>Sintassi


```JScript
bRetVal = Settings.getMode(
  modeName
)
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*modeName* \[ in\]
</dt> <dd>

**Stringa** che specifica il nome della modalità in questione, contenente uno dei valori seguenti.



| string     | Descrizione                                                                                                              |
|------------|--------------------------------------------------------------------------------------------------------------------------|
| riavvolgimento rapido | Le tracce vengono riavviate all'inizio dopo la riproduzione fino alla fine.                                                          |
| loop       | La sequenza di tracce si ripete.                                                                                   |
| showFrame  | Il fotogramma chiave più vicino viene visualizzato nella posizione corrente quando non viene riprodotto. Questa modalità non è pertinente per le tracce audio. |
| shuffle    | Le tracce vengono riprodotte in ordine casuale.                                                                                       |



 

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo metodo restituisce un valore **booleano** che indica se la modalità specificata è attiva.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Versione<br/> | Per le modalità ciclo e riproduzione casuale, Windows Media Player versione 7,0 o successiva. Per le modalità AutoRewind e showFrame, Windows Media Player 9 Series o versione successiva.<br/> |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl>                                                                            |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Oggetto Settings**](settings-object.md)
</dt> <dt>

[**Settings. semode**](settings-setmode.md)
</dt> </dl>

 

 





