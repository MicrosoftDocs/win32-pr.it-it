---
title: Controls. getLanguageName, metodo
description: Il metodo getLanguageName Recupera il nome della lingua audio con l'identificatore delle impostazioni locali (LCID) specificato.
ms.assetid: 9e142c89-92bf-476f-bae7-b94f5b5ebe01
keywords:
- Metodo getLanguageName Windows Media Player
- Metodo getLanguageName Windows Media Player, classe Controls
- Classe Controls Media Player Windows, metodo getLanguageName
topic_type:
- apiref
api_name:
- Controls.getLanguageName
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 798a6b22f344953df716e4df4ed8a9a0daff2a7b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106331247"
---
# <a name="controlsgetlanguagename-method"></a>Controls. getLanguageName, metodo

Il metodo **getLanguageName** Recupera il nome della lingua audio con l'identificatore delle impostazioni locali (LCID) specificato.

## <a name="syntax"></a>Sintassi


```JScript
strRetVal = Controls.getLanguageName(
  LCID
)
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*LCID* \[ in\]
</dt> <dd>

**Numero** (**Long**) che specifica l'identificatore LCID.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo metodo restituisce una **stringa**.

## <a name="remarks"></a>Commenti

Un LCID identifica in modo univoco un dialetto di lingua particolare, denominato impostazioni locali.

Per il contenuto basato su Windows Media, le proprietà e i metodi relativi alla selezione della lingua supportano solo un singolo output.

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

[**Controls. getAudioLanguageDescription**](controls-getaudiolanguagedescription.md)
</dt> <dt>

[**Controls. getAudioLanguageID**](controls-getaudiolanguageid.md)
</dt> </dl>

 

 





