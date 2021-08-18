---
title: Impostazioni.setMode
description: Il metodo setMode imposta varie modalità su attiva o inattiva.
ms.assetid: 9ab88aeb-53f6-4798-9299-14961e373ca6
keywords:
- Metodo setMode Windows Media Player
- Metodo setMode Windows Media Player , Impostazioni classe
- Impostazioni classe Windows Media Player, metodo setMode
topic_type:
- apiref
api_name:
- Settings.setMode
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f504fe429dddf1b3db191545e2f34a3605a8fc390346c8f00afe8c3d005f0277
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118995321"
---
# <a name="settingssetmode-method"></a>Impostazioni.setMode

Il **metodo setMode** imposta varie modalità su attiva o inattiva.

## <a name="syntax"></a>Sintassi


```JScript
Settings.setMode(
  modeName,
  state
)
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*modeName* \[ Pollici\]
</dt> <dd>

**Stringa** che specifica il nome della modalità da modificare, contenente uno dei valori seguenti.



| string     | Descrizione                                                                                                                                                       |
|------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| riavvolgimento automatico | Modalità che indica se le tracce vengono riassolite all'inizio dopo la riproduzione fino alla fine. Lo stato predefinito è true.                                                  |
| loop       | Modalità che indica se la sequenza di tracce si ripete. Lo stato predefinito è false.                                                                            |
| showFrame  | Modalità che indica se il fotogramma chiave video più vicino viene visualizzato nella posizione corrente quando non viene riprodotto. Lo stato predefinito è false. Non ha alcun effetto sulle tracce audio. |
| shuffle    | Modalità che indica se le tracce vengono riprodotte in ordine casuale. Lo stato predefinito è false.                                                                            |



 

</dd> <dt>

*state* \[ Pollici\]
</dt> <dd>

**Valore** booleano che specifica se la nuova modalità specificata è attiva o meno.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo metodo non restituisce valori.

## <a name="remarks"></a>Commenti

Quando la modalità showFrame è attiva, il lettore deve accedere al contenuto della traccia per recuperare il fotogramma video. Per considerazioni sulla larghezza di banda, usare questa modalità con cautela durante la riproduzione di contenuto non locale.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Versione<br/> | Per le modalità loop e shuffle, Windows Media Player versione 7.0 o successiva. Per le modalità autoRewind e showFrame, Windows Media Player serie 9 o successive.<br/> |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl>                                                                            |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Impostazioni Oggetto**](settings-object.md)
</dt> <dt>

[**Impostazioni.getMode**](settings-getmode.md)
</dt> </dl>

 

 





