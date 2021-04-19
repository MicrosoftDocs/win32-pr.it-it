---
title: Evento Player. KeyPress
description: L'evento KeyPress si verifica quando un tasto viene premuto e rilasciato. | Evento Player. KeyPress
ms.assetid: fc51dfd3-7968-464a-a4e2-669ffcb52a59
keywords:
- Media Player di eventi KeyPress Windows
- Evento KeyPress Media Player Windows, classe Player
- Classe Player Windows Media Player, evento KeyPress
topic_type:
- apiref
api_name:
- Player.KeyPress
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c78b72dd703c13019c71b23af53790aa974927f1
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106326311"
---
# <a name="playerkeypress-event"></a>Evento Player. KeyPress

L'evento **KeyPress** si verifica quando un tasto viene premuto e rilasciato.

## <a name="syntax"></a>Sintassi


```JScript
Player.KeyPress(
  nKeyAscii
)
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*nKeyAscii* 
</dt> <dd>

**Number** (**int**) che specifica il codice ANSI numerico standard per il carattere.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo evento non restituisce un valore.

## <a name="remarks"></a>Commenti

Questo evento si verifica quando la sequenza di tasti restituisce un carattere di tastiera stampabile, il tasto CTRL combinato con un carattere dell'alfabeto standard o uno dei caratteri speciali e il tasto invio o BACKSPACE.

Il valore dei parametri evento viene specificato da Windows Media Player ed è possibile accedervi o passarli a un metodo in un file JScript importato usando il nome del parametro specificato. Questo nome di parametro deve essere digitato esattamente come illustrato, incluse le maiuscole.

**Windows Media Player 10 Mobile:** Questo evento non è supportato.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|------------------------------------------------------------------------------------|
| Versione<br/> | Windows Media Player 9 serie o versione successiva.<br/>                                 |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Oggetto Player**](player-object.md)
</dt> </dl>

 

 





