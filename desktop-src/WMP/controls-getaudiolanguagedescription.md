---
title: Controls. getAudioLanguageDescription, metodo
description: Il metodo getAudioLanguageDescription recupera la descrizione della lingua audio corrispondente all'indice in base uno specificato.
ms.assetid: 995a2568-f15f-4b92-9782-92ba5273f444
keywords:
- Metodo getAudioLanguageDescription Windows Media Player
- Metodo getAudioLanguageDescription Windows Media Player, classe Controls
- Classe Controls Media Player Windows, metodo getAudioLanguageDescription
topic_type:
- apiref
api_name:
- Controls.getAudioLanguageDescription
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1d28e82648a1047252402694f4948d2a2734f344
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106326476"
---
# <a name="controlsgetaudiolanguagedescription-method"></a>Controls. getAudioLanguageDescription, metodo

Il metodo **getAudioLanguageDescription** recupera la descrizione della lingua audio corrispondente all'indice in base uno specificato.

## <a name="syntax"></a>Sintassi


```JScript
strRetVal = Controls.getAudioLanguageDescription(
  index
)
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*Indice* \[ di in\]
</dt> <dd>

**Numero** (**Long**) che specifica l'indice della lingua audio in base uno.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo metodo restituisce un valore **stringa** .

## <a name="remarks"></a>Commenti

Per il contenuto basato su Windows Media, le proprietà e i metodi relativi alla selezione della lingua supportano solo un singolo output.

Utilizzare la proprietà **audioLanguageCount** per ottenere il numero di lingue audio supportate e accedere a una lingua audio singolarmente utilizzando un indice in base uno.

**Windows Media Player 10 Mobile:** Questo metodo non è supportato.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|------------------------------------------------------------------------------------|
| Versione<br/> | Windows Media Player 9 serie o versione successiva.<br/>                                 |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Oggetto Controls**](controls-object.md)
</dt> <dt>

[**Controls. audioLanguageCount**](controls-audiolanguagecount.md)
</dt> <dt>

[**Controls. currentAudioLanguage**](controls-currentaudiolanguage.md)
</dt> <dt>

[**Controls. currentAudioLanguageIndex**](controls-currentaudiolanguageindex.md)
</dt> <dt>

[**Controls. getAudioLanguageID**](controls-getaudiolanguageid.md)
</dt> <dt>

[**Controls. getLanguageName**](controls-getlanguagename.md)
</dt> </dl>

 

 





