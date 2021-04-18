---
title: Metodo Settings. semode
description: Il metodo semode imposta varie modalità su attivo o inattivo.
ms.assetid: 9ab88aeb-53f6-4798-9299-14961e373ca6
keywords:
- Metodo di Media Player di Windows
- Metodo di Media Player Windows, classe Settings
- Classe Settings Media Player Windows, metodo semode
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
ms.openlocfilehash: cf5740bf5638ce34e161414ac96eaa0fc80fcdb7
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106327369"
---
# <a name="settingssetmode-method"></a>Metodo Settings. semode

Il metodo **semode** imposta varie modalità su attivo o inattivo.

## <a name="syntax"></a>Sintassi


```JScript
Settings.setMode(
  modeName,
  state
)
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*modeName* \[ in\]
</dt> <dd>

**Stringa** che specifica il nome della modalità da modificare, contenente uno dei valori seguenti.



| string     | Descrizione                                                                                                                                                       |
|------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| riavvolgimento rapido | Modalità che indica se le tracce vengono riferite all'inizio dopo la riproduzione fino alla fine. Lo stato predefinito è true.                                                  |
| loop       | Modalità che indica se la sequenza di tracce si ripete. Lo stato predefinito è false.                                                                            |
| showFrame  | Modalità che indica se il fotogramma chiave video più vicino viene visualizzato nella posizione corrente quando non viene riprodotto. Lo stato predefinito è false. Non ha alcun effetto sulle tracce audio. |
| shuffle    | Modalità che indica se le tracce vengono riprodotte in ordine casuale. Lo stato predefinito è false.                                                                            |



 

</dd> <dt>

*stato* \[ di in\]
</dt> <dd>

**Valore booleano** che specifica se la nuova modalità specificata è attiva o meno.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo metodo non restituisce valori.

## <a name="remarks"></a>Commenti

Quando la modalità showFrame è attiva, il lettore deve accedere al contenuto della traccia per recuperare il frame video. A causa delle considerazioni sulla larghezza di banda, usare questa modalità con cautela quando si giocano contenuti non locali.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Versione<br/> | Per le modalità ciclo e riproduzione casuale, Windows Media Player versione 7,0 o successiva. Per le modalità AutoRewind e showFrame, Windows Media Player 9 Series o versione successiva.<br/> |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl>                                                                            |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Oggetto Settings**](settings-object.md)
</dt> <dt>

[**Settings. getMode**](settings-getmode.md)
</dt> </dl>

 

 





