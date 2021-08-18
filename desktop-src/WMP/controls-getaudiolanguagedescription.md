---
title: Metodo Controls.getAudioLanguageDescription
description: Il metodo getAudioLanguageDescription recupera la descrizione della lingua audio corrispondente all'indice in base uno specificato.
ms.assetid: 995a2568-f15f-4b92-9782-92ba5273f444
keywords:
- Metodo getAudioLanguageDescription Windows Media Player
- Metodo getAudioLanguageDescription Windows Media Player , classe Controls
- Classe Controls Windows Media Player metodo , getAudioLanguageDescription
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
ms.openlocfilehash: 29aa5f7b5c0ad72ff13b571505283b243bd62d79ebc4339717ed8283cccb2a5b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118997501"
---
# <a name="controlsgetaudiolanguagedescription-method"></a>Metodo Controls.getAudioLanguageDescription

Il **metodo getAudioLanguageDescription** recupera la descrizione della lingua audio corrispondente all'indice in base uno specificato.

## <a name="syntax"></a>Sintassi


```JScript
strRetVal = Controls.getAudioLanguageDescription(
  index
)
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*index* \[ Pollici\]
</dt> <dd>

**Numero** (**long**) che specifica l'indice della lingua audio in base uno.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo metodo restituisce un **valore String.**

## <a name="remarks"></a>Commenti

Ad Windows contenuto basato su supporti, le proprietà e i metodi correlati alla selezione della lingua supportano solo un singolo output.

Usare la **proprietà audioLanguageCount** per ottenere il numero di lingue audio supportate e quindi accedere a una lingua audio singolarmente usando un indice in base uno.

**Windows Media Player 10 Mobile:** Questo metodo non è supportato.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|------------------------------------------------------------------------------------|
| Versione<br/> | Windows Media Player serie 9 o successive.<br/>                                 |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Oggetto Controls**](controls-object.md)
</dt> <dt>

[**Controls.audioLanguageCount**](controls-audiolanguagecount.md)
</dt> <dt>

[**Controls.currentAudioLanguage**](controls-currentaudiolanguage.md)
</dt> <dt>

[**Controls.currentAudioLanguageIndex**](controls-currentaudiolanguageindex.md)
</dt> <dt>

[**Controls.getAudioLanguageID**](controls-getaudiolanguageid.md)
</dt> <dt>

[**Controls.getLanguageName**](controls-getlanguagename.md)
</dt> </dl>

 

 





