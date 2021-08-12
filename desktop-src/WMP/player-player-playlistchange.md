---
title: Evento Player.PlaylistChange
description: L'evento PlaylistChange si verifica quando cambia una playlist. | Evento Player.PlaylistChange
ms.assetid: 09ab0560-e18d-4ee8-a649-2b2468b40c31
keywords:
- Gestore eventi PlaylistChange Windows Media Player
- PlaylistChange event Windows Media Player , Player class
- Classe player Windows Media Player , evento PlaylistChange
topic_type:
- apiref
api_name:
- Player.PlaylistChange
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3ff4c45449c8de2062aa53ce9bda89c8d634dd30bc1ac8c03f091e8b97e9ce60
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118572804"
---
# <a name="playerplaylistchange-event"></a>Evento Player.PlaylistChange

**L'evento PlaylistChange** si verifica quando cambia una playlist.

## <a name="syntax"></a>Sintassi


```JScript
Player.PlaylistChange(
  Playlist,
  change
)
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*Playlist* 
</dt> <dd>

**Oggetto playlist** modificato.

</dd> <dt>

*change* 
</dt> <dd>

**Numero** (**long**) che indica il tipo di modifica apportata alla playlist. Contiene uno dei valori seguenti.



| Numero | Nome          |
|--------|---------------|
| 0      | Sconosciuto       |
| 1      | Cancella         |
| 2      | InfoChange    |
| 3      | Sposta          |
| 4      | Delete        |
| 5      | Insert        |
| 6      | Accodamento        |
| 7      | Non supportato |
| 8      | NameChange    |
| 9      | Non supportate |
| 10     | Ordina          |



 

La costante di enumerazione di tipo C può essere derivata antecendo al valore del nome "wmplc". Ad esempio, la costante per lo stato Move è **wmplcMove**.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo evento non restituisce un valore.

## <a name="remarks"></a>Commenti

Il valore dei parametri dell'evento viene specificato da Windows Media Player ed è accessibile o passato a un metodo in un file JScript importato usando il nome del parametro specificato. Questo nome di parametro deve essere digitato esattamente come illustrato, inclusa l'maiuscola.

**Windows Media Player 10 Mobile:** Questo evento non è supportato.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|------------------------------------------------------------------------------------|
| Versione<br/> | Windows Media Player versione 7.0 o successiva.<br/>                              |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Oggetto Player**](player-object.md)
</dt> </dl>

 

 





