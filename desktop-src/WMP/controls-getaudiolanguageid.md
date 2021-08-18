---
title: Metodo Controls.getAudioLanguageID
description: Il metodo getAudioLanguageID recupera l'identificatore delle impostazioni locali (LCID) per un indice della lingua audio specificato.
ms.assetid: 8134a7ce-bdc7-46b2-b10e-2bf1215b0de1
keywords:
- Metodo getAudioLanguageID Windows Media Player
- Metodo getAudioLanguageID Windows Media Player , classe Controls
- Classe Controls Windows Media Player metodo , getAudioLanguageID
topic_type:
- apiref
api_name:
- Controls.getAudioLanguageID
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2352162d810ca75aeeee6db1c3d59c297b85414be46a365909c4ed56af179f8b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118119340"
---
# <a name="controlsgetaudiolanguageid-method"></a>Metodo Controls.getAudioLanguageID

Il **metodo getAudioLanguageID** recupera l'identificatore delle impostazioni locali (LCID) per un indice della lingua audio specificato.

## <a name="syntax"></a>Sintassi


```JScript
retVal = Controls.getAudioLanguageID(
  index
)
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*index* \[ Pollici\]
</dt> <dd>

**Numero** (**long**) che specifica l'indice della lingua audio.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo metodo restituisce un **valore Number** (**long**).

## <a name="remarks"></a>Commenti

Un LCID identifica in modo univoco un particolare dialetto di lingua, denominato impostazioni locali.

Ad Windows contenuto basato su contenuti multimediali, le proprietà e i metodi correlati alla selezione della lingua supportano solo un singolo output.

**Windows Media Player 10 Mobile:** Questa proprietà restituisce sempre l'LCID indipendente dalla lingua (0).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|------------------------------------------------------------------------------------|
| Versione<br/> | Windows Media Player serie 9 o successiva.<br/>                                 |
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

[**Controls.getAudioLanguageDescription**](controls-getaudiolanguagedescription.md)
</dt> <dt>

[**Controls.getLanguageName**](controls-getlanguagename.md)
</dt> </dl>

 

 





