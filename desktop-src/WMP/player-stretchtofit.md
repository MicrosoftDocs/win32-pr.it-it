---
title: Player. stretchToFit
description: La proprietà stretchToFit specifica o recupera un valore che indica se il video visualizzato dal controllo Media Player di Windows viene ridimensionato automaticamente per adattarsi alla finestra video, quando la finestra video è più grande delle dimensioni dell'immagine video.
ms.assetid: 9ea02959-602e-4bac-a8aa-dce502d1bb54
keywords:
- Player. stretchToFit Windows Media Player
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
ms.openlocfilehash: fb7b68042cf2a5bd0e7f718d1e19641edecdf548
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106324824"
---
# <a name="playerstretchtofit"></a>Player. stretchToFit

La proprietà **stretchToFit** specifica o recupera un valore che indica se il video visualizzato dal controllo Media Player di Windows viene ridimensionato automaticamente per adattarsi alla finestra video, quando la finestra video è più grande delle dimensioni dell'immagine video.

## <a name="syntax"></a>Sintassi

*Player*. **stretchToFit**

## <a name="possible-values"></a>Valori possibili

Questa proprietà è un **valore booleano** di lettura/scrittura.



| Valore | Descrizione                                            |
|-------|--------------------------------------------------------|
| true  | Il video si estenderà per adattarsi alla finestra.              |
| false | Valore predefinito. Il video non si adatta alla finestra. |



 

## <a name="remarks"></a>Commenti

Quando **stretchToFit** è impostato su true, il controllo Media Player Windows mantiene le proporzioni originali del video. Se le proporzioni del video non corrispondono alle proporzioni della finestra video, le aree della maschera nera possono essere visualizzate nella parte superiore e inferiore, o a sinistra e a destra, dell'immagine del video.

Questa proprietà si applica al controllo Windows Media Player solo se è incorporata in una pagina Web.

**Windows Media Player 10 Mobile:** Questa proprietà non è supportata.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|------------------------------------------------------------------------------------|
| Versione<br/> | Windows Media Player versione 7,1 o successiva.<br/>                              |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Oggetto Player**](player-object.md)
</dt> </dl>

 

 





