---
title: Controls.currentAudioLanguage
description: La proprietà currentAudioLanguage specifica o recupera l'identificatore delle impostazioni locali (LCID) della lingua audio per la riproduzione.
ms.assetid: 628845df-add3-4068-9c3d-b4a9b818808c
keywords:
- Controlli.currentAudioLanguage Windows Media Player
topic_type:
- apiref
api_name:
- Controls.currentAudioLanguage
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 63c5eb53c9f408a9d50a7f738434e5dcd30fc804970b3e1ea95c985c90d62063
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117750613"
---
# <a name="controlscurrentaudiolanguage"></a>Controls.currentAudioLanguage

La **proprietà currentAudioLanguage** specifica o recupera l'identificatore delle impostazioni locali (LCID) della lingua audio per la riproduzione.

``` syntax
player.controls.currentAudioLanguage
      
```

## <a name="possible-values"></a>Valori possibili

Questa proprietà è un numero di **lettura/scrittura** (**long**).

## <a name="remarks"></a>Commenti

Un LCID identifica in modo univoco un particolare dialetto di lingua, denominato impostazioni locali.

Ad Windows contenuto basato su contenuti multimediali, le proprietà e i metodi correlati alla selezione della lingua supportano solo un singolo output.

Quando si utilizza contenuto DVD, se si specifica un LCID, verrà selezionata la prima traccia audio disponibile con l'ID lingua specificato.

**Windows Media Player 10 Mobile:** Questa proprietà accetta o restituisce solo l'LCID indipendente dalla lingua (0).

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

[**Controls.currentAudioLanguageIndex**](controls-currentaudiolanguageindex.md)
</dt> <dt>

[**Controls.getAudioLanguageDescription**](controls-getaudiolanguagedescription.md)
</dt> <dt>

[**Controls.getAudioLanguageID**](controls-getaudiolanguageid.md)
</dt> <dt>

[**Controls.getLanguageName**](controls-getlanguagename.md)
</dt> </dl>

 

 





