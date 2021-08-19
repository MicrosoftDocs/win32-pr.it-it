---
title: Proprietà currentAudioLanguage IWMPControls3
description: La proprietà currentAudioLanguage ottiene o imposta l'identificatore delle impostazioni locali (LCID) della lingua audio per la riproduzione.
ms.assetid: 4adf26c7-077a-483e-8a76-accf871eca4c
keywords:
- Proprietà currentAudioLanguage Windows Media Player
- Proprietà currentAudioLanguage Windows Media Player, interfaccia IWMPControls3
- Interfaccia IWMPControls3 Windows Media Player proprietà , currentAudioLanguage
topic_type:
- apiref
api_name:
- IWMPControls3.currentAudioLanguage
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1e1a4f668cec560528270d52a2abe4777ce32d3ceb38ce21345342ef87866c38
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118115878"
---
# <a name="iwmpcontrols3currentaudiolanguage-property"></a>Proprietà IWMPControls3::currentAudioLanguage

La **proprietà currentAudioLanguage** ottiene o imposta l'identificatore delle impostazioni locali (LCID) della lingua audio per la riproduzione.

## <a name="syntax"></a>Sintassi


```CSharp
public System.Int32 currentAudioLanguage {get; set;}
```


```VB

Public Property currentAudioLanguage As System.Int32
```





## <a name="property-value"></a>Valore proprietà

**System.Int32** che rappresenta l'LCID della lingua audio.

## <a name="remarks"></a>Commenti

Un LCID identifica in modo univoco un particolare dialetto di lingua, denominato impostazioni locali.

Per il contenuto basato su Windows Media, le proprietà e i metodi correlati alla selezione della lingua supportano un solo output.

Quando si utilizza contenuto DVD, se si specifica un LCID, verrà selezionata la prima traccia audio disponibile con l'ID lingua specificato.

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

[**IWMPControls3.currentAudioLanguageIndex (VB e C#)**](wmplibiwmpcontrols3-iwmpcontrols3-currentaudiolanguageindex--vb-and-c.md)
</dt> <dt>

[**IWMPControls3.getAudioLanguageDescription (VB e C#)**](wmplibiwmpcontrols3-iwmpcontrols3-getaudiolanguagedescription--vb-and-c.md)
</dt> <dt>

[**IWMPControls3.getAudioLanguageID (VB e C#)**](wmplibiwmpcontrols3-iwmpcontrols3-getaudiolanguageid--vb-and-c.md)
</dt> <dt>

[**IWMPControls3.getLanguageName (VB e C#)**](wmplibiwmpcontrols3-iwmpcontrols3-getlanguagename--vb-and-c.md)
</dt> </dl>

 

 





