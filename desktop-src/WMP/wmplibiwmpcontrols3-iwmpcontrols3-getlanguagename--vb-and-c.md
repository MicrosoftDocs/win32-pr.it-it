---
title: Metodo IWMPControls3 getLanguageName
description: Il metodo getLanguageName restituisce il nome della lingua audio con l'identificatore delle impostazioni locali (LCID) specificato.
ms.assetid: a0651e8d-0ba1-4fff-93f0-fe097231723e
keywords:
- Metodo getLanguageName Windows Media Player
- Metodo getLanguageName Windows Media Player, interfaccia IWMPControls3
- Interfaccia IWMPControls3 Windows Media Player metodo , getLanguageName
topic_type:
- apiref
api_name:
- IWMPControls3.getLanguageName
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c6850bd73c9add044bdb845d17341745c7546918f7824b611ed2f018f66139d7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120000491"
---
# <a name="iwmpcontrols3getlanguagename-method"></a>Metodo IWMPControls3::getLanguageName

Il **metodo getLanguageName** restituisce il nome della lingua audio con l'identificatore delle impostazioni locali (LCID) specificato.

## <a name="syntax"></a>Sintassi


```CSharp
public System.String getLanguageName(
  System.Int32 lLangID
);
```


```VB

Public Function getLanguageName( _
  ByVal lLangID As System.Int32 _
) As System.String
Implements IWMPControls3.getLanguageName
```





## <a name="parameters"></a>Parametri

<dl> <dt>

*lLangID* \[ Pollici\]
</dt> <dd>

Oggetto **System.Int32** che rappresenta l'LCID.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Oggetto **System.String** che rappresenta il nome della lingua audio.

## <a name="remarks"></a>Commenti

Un LCID identifica in modo univoco un particolare dialetto di lingua, denominato impostazioni locali.

Ad Windows contenuto basato su supporti, le proprietà e i metodi correlati alla selezione della lingua supportano solo un singolo output.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| Versione<br/>   | Windows Media Player serie 9 o successive<br/>                                                                      |
| Spazio dei nomi<br/> | **WMPLib**<br/>                                                                                                  |
| Assembly<br/>  | <dl> <dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Interfaccia IWMPControls3 (VB e C#)**](iwmpcontrols3--vb-and-c.md)
</dt> <dt>

[**IWMPControls3.audioLanguageCount (VB e C#)**](wmplibiwmpcontrols3-iwmpcontrols3-audiolanguagecount--vb-and-c.md)
</dt> <dt>

[**IWMPControls3.currentAudioLanguage (VB e C#)**](wmplibiwmpcontrols3-iwmpcontrols3-currentaudiolanguage--vb-and-c.md)
</dt> <dt>

[**IWMPControls3.currentAudioLanguageIndex (VB e C#)**](wmplibiwmpcontrols3-iwmpcontrols3-currentaudiolanguageindex--vb-and-c.md)
</dt> <dt>

[**IWMPControls3.getAudioLanguageDescription (VB e C#)**](wmplibiwmpcontrols3-iwmpcontrols3-getaudiolanguagedescription--vb-and-c.md)
</dt> <dt>

[**IWMPControls3.getAudioLanguageID (VB e C#)**](wmplibiwmpcontrols3-iwmpcontrols3-getaudiolanguageid--vb-and-c.md)
</dt> </dl>

 

 





