---
title: Proprietà currentAudioLanguage di IWMPControls3
description: La proprietà currentAudioLanguage Ottiene o imposta l'identificatore delle impostazioni locali (LCID) della lingua audio per la riproduzione.
ms.assetid: 4adf26c7-077a-483e-8a76-accf871eca4c
keywords:
- Finestra delle proprietà di currentAudioLanguage Media Player
- Proprietà di currentAudioLanguage Media Player Windows, interfaccia IWMPControls3
- Interfaccia IWMPControls3 Windows Media Player, proprietà currentAudioLanguage
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
ms.openlocfilehash: 7c4621b5eace56cb883a6c8b14c3b1f082b12d3a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106332466"
---
# <a name="iwmpcontrols3currentaudiolanguage-property"></a>Proprietà IWMPControls3:: currentAudioLanguage

La proprietà **currentAudioLanguage** Ottiene o imposta l'identificatore delle impostazioni locali (LCID) della lingua audio per la riproduzione.

## <a name="syntax"></a>Sintassi


```CSharp
public System.Int32 currentAudioLanguage {get; set;}
```


```VB

Public Property currentAudioLanguage As System.Int32
```





## <a name="property-value"></a>Valore proprietà

**System. Int32** che rappresenta l'identificatore LCID della lingua audio.

## <a name="remarks"></a>Commenti

Un LCID identifica in modo univoco un dialetto di lingua particolare, denominato impostazioni locali.

Per il contenuto basato su Windows Media, le proprietà e i metodi relativi alla selezione della lingua supportano solo un singolo output.

Quando si usa il contenuto DVD, se si specifica un LCID, verrà selezionata la prima traccia audio disponibile con l'ID lingua specificato.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| Versione<br/>   | Windows Media Player 9 serie o versione successiva<br/>                                                                      |
| Spazio dei nomi<br/> | **WMPLib**<br/>                                                                                                  |
| Assembly<br/>  | <dl> <dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Interfaccia IWMPControls3 (VB e C#)**](iwmpcontrols3--vb-and-c.md)
</dt> <dt>

[**IWMPControls3. audioLanguageCount (VB e C#)**](wmplibiwmpcontrols3-iwmpcontrols3-audiolanguagecount--vb-and-c.md)
</dt> <dt>

[**IWMPControls3. currentAudioLanguageIndex (VB e C#)**](wmplibiwmpcontrols3-iwmpcontrols3-currentaudiolanguageindex--vb-and-c.md)
</dt> <dt>

[**IWMPControls3. getAudioLanguageDescription (VB e C#)**](wmplibiwmpcontrols3-iwmpcontrols3-getaudiolanguagedescription--vb-and-c.md)
</dt> <dt>

[**IWMPControls3. getAudioLanguageID (VB e C#)**](wmplibiwmpcontrols3-iwmpcontrols3-getaudiolanguageid--vb-and-c.md)
</dt> <dt>

[**IWMPControls3. getLanguageName (VB e C#)**](wmplibiwmpcontrols3-iwmpcontrols3-getlanguagename--vb-and-c.md)
</dt> </dl>

 

 





