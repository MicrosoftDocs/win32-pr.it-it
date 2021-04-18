---
title: Player. enableContextMenu
description: La proprietà enableContextMenu specifica o recupera un valore che indica se abilitare il menu di scelta rapida che viene visualizzato quando si fa clic con il pulsante destro del mouse.
ms.assetid: 736c8714-5650-4912-9e97-914a20137b91
keywords:
- Player. enableContextMenu Windows Media Player
topic_type:
- apiref
api_name:
- Player.enableContextMenu
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 324ab0f14b83621651869e715c1fd4a882ceb650
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106324985"
---
# <a name="playerenablecontextmenu"></a>Player. enableContextMenu

La proprietà **enableContextMenu** specifica o recupera un valore che indica se abilitare il menu di scelta rapida che viene visualizzato quando si fa clic con il pulsante destro del mouse.

## <a name="syntax"></a>Sintassi

*Player*. **enableContextMenu**

## <a name="possible-values"></a>Valori possibili

Questa proprietà è un valore booleano di lettura/scrittura.



| Valore | Descrizione                       |
|-------|-----------------------------------|
| true  | Valore predefinito. Attivare il menu di scelta rapida. |
| false | Non abilitare il menu di scelta rapida.   |



 

## <a name="remarks"></a>Commenti

Durante la riproduzione a schermo intero, Windows Media Player nasconde il cursore del mouse quando **enableContextMenu** è uguale a false e **uiMode** è uguale a "None".

**Windows Media Player 10 Mobile:** Questa proprietà non è supportata.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|------------------------------------------------------------------------------------|
| Versione<br/> | Windows Media Player versione 7,0 o successiva.<br/>                              |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Oggetto Player**](player-object.md)
</dt> </dl>

 

 





