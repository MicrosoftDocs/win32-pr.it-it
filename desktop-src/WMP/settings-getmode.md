---
title: Impostazioni.getMode
description: Il metodo getMode determina se la modalità loop o shuffle è attiva.
ms.assetid: 41c3725f-ae8f-4b45-856a-b7245c9ad2b3
keywords:
- Metodo getMode Windows Media Player
- Metodo getMode Windows Media Player , Impostazioni classe
- Impostazioni classe Windows Media Player , metodo getMode
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
ms.openlocfilehash: 779c775319cbe0d6dc443b4eb99febd494db3d30fb35228b7310f8f1ae7d691d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118995331"
---
# <a name="settingsgetmode-method"></a>Impostazioni.getMode

Il **metodo getMode** determina se la modalità loop o shuffle è attiva.

## <a name="syntax"></a>Sintassi


```JScript
bRetVal = Settings.getMode(
  modeName
)
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*modeName* \[ Pollici\]
</dt> <dd>

**Stringa** che specifica il nome della modalità in questione, contenente uno dei valori seguenti.



| string     | Descrizione                                                                                                              |
|------------|--------------------------------------------------------------------------------------------------------------------------|
| riavvolgimento automatico | Le tracce vengono riavviate all'inizio dopo la riproduzione fino alla fine.                                                          |
| loop       | La sequenza di tracce si ripete.                                                                                   |
| showFrame  | Il fotogramma chiave più vicino viene visualizzato nella posizione corrente quando non viene riprodotto. Questa modalità non è rilevante per le tracce audio. |
| shuffle    | Le tracce vengono riprodotte in ordine casuale.                                                                                       |



 

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo metodo restituisce un **valore booleano** che indica se la modalità specificata è attiva.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Versione<br/> | Per le modalità loop e shuffle, Windows Media Player versione 7.0 o successiva. Per le modalità autoRewind e showFrame, Windows Media Player serie 9 o successive.<br/> |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl>                                                                            |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Impostazioni Oggetto**](settings-object.md)
</dt> <dt>

[**Impostazioni.setMode**](settings-setmode.md)
</dt> </dl>

 

 





