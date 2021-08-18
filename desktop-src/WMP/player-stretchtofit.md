---
title: Player.stretchToFit
description: La proprietà stretchToFit specifica o recupera un valore che indica se il video visualizzato dal controllo Windows Media Player si adatta automaticamente alla finestra video, quando la finestra video è più grande delle dimensioni dell'immagine video.
ms.assetid: 9ea02959-602e-4bac-a8aa-dce502d1bb54
keywords:
- Player.stretchToFit Windows Media Player
topic_type:
- apiref
api_name:
- Player.stretchToFit
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 570d0b9bf7e266af769944b675a85c0ac1518c321d11038ff94cab035dfb316c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118995841"
---
# <a name="playerstretchtofit"></a>Player.stretchToFit

La proprietà **stretchToFit** specifica o recupera un valore che indica se il video visualizzato dal controllo Windows Media Player si adatta automaticamente alla finestra video, quando la finestra video è più grande delle dimensioni dell'immagine video.

## <a name="syntax"></a>Sintassi

*lettore*. **stretchToFit**

## <a name="possible-values"></a>Valori possibili

Questa proprietà è un valore booleano di **lettura/scrittura.**



| Valore | Descrizione                                            |
|-------|--------------------------------------------------------|
| true  | Il video verrà adattato alla finestra.              |
| false | Valore predefinito. Il video non verrà adattato alla finestra. |



 

## <a name="remarks"></a>Commenti

Quando **stretchToFit** è impostato su true, il controllo Windows Media Player mantiene le proporzioni originali del video. Se le proporzioni del video non corrispondono alle proporzioni della finestra video, è possibile che le aree della maschera nera vengano visualizzate nella parte superiore e inferiore o a sinistra e a destra dell'immagine video.

Questa proprietà si applica al controllo Windows Media Player solo se incorporata in una pagina Web.

**Windows Media Player 10 Mobile:** Questa proprietà non è supportata.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|------------------------------------------------------------------------------------|
| Versione<br/> | Windows Media Player versione 7.1 o successiva.<br/>                              |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Oggetto Player**](player-object.md)
</dt> </dl>

 

 





