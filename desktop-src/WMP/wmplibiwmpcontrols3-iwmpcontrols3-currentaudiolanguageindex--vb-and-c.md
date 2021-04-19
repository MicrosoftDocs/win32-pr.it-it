---
title: Proprietà currentAudioLanguageIndex di IWMPControls3
description: La proprietà currentAudioLanguageIndex Ottiene o imposta l'indice in base uno che corrisponde alla lingua audio per la riproduzione.
ms.assetid: 3ed60827-c4e9-4455-b95e-b6eebf7a9a08
keywords:
- Finestra delle proprietà di currentAudioLanguageIndex Media Player
- Proprietà di currentAudioLanguageIndex Media Player Windows, interfaccia IWMPControls3
- Interfaccia IWMPControls3 Windows Media Player, proprietà currentAudioLanguageIndex
topic_type:
- apiref
api_name:
- IWMPControls3.currentAudioLanguageIndex
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f4fb36eea4038322cacd7f233892151ab77e5eea
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106332464"
---
# <a name="iwmpcontrols3currentaudiolanguageindex-property"></a>Proprietà IWMPControls3:: currentAudioLanguageIndex

La proprietà **currentAudioLanguageIndex** Ottiene o imposta l'indice in base uno che corrisponde alla lingua audio per la riproduzione.

## <a name="syntax"></a>Sintassi


```CSharp
public System.Int32 currentAudioLanguageIndex {get; set;}
```


```VB

Public Property currentAudioLanguageIndex As System.Int32
```





## <a name="property-value"></a>Valore proprietà

**System. Int32** che rappresenta l'indice in base uno della lingua.

## <a name="remarks"></a>Commenti

Per il contenuto basato su Windows Media, le proprietà e i metodi relativi alla selezione della lingua supportano solo un singolo output.

Usare la proprietà **audioLanguageCount** per ottenere il numero di lingue audio supportate.

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

[**IWMPControls3. currentAudioLanguage (VB e C#)**](wmplibiwmpcontrols3-iwmpcontrols3-currentaudiolanguage--vb-and-c.md)
</dt> <dt>

[**IWMPControls3. getAudioLanguageDescription (VB e C#)**](wmplibiwmpcontrols3-iwmpcontrols3-getaudiolanguagedescription--vb-and-c.md)
</dt> <dt>

[**IWMPControls3. getAudioLanguageID (VB e C#)**](wmplibiwmpcontrols3-iwmpcontrols3-getaudiolanguageid--vb-and-c.md)
</dt> <dt>

[**IWMPControls3. getLanguageName (VB e C#)**](wmplibiwmpcontrols3-iwmpcontrols3-getlanguagename--vb-and-c.md)
</dt> </dl>

 

 





