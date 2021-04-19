---
title: Metodo IWMPControls3 getAudioLanguageDescription
description: Il metodo getAudioLanguageDescription restituisce la descrizione della lingua audio corrispondente all'indice in base uno specificato.
ms.assetid: bf3db27f-ba14-409e-8942-fe863d6f3670
keywords:
- Metodo getAudioLanguageDescription Windows Media Player
- Metodo getAudioLanguageDescription Windows Media Player, interfaccia IWMPControls3
- Interfaccia IWMPControls3 Windows Media Player, metodo getAudioLanguageDescription
topic_type:
- apiref
api_name:
- IWMPControls3.getAudioLanguageDescription
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bb45ceb166ca9c948823e516029569e457f35e27
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106332454"
---
# <a name="iwmpcontrols3getaudiolanguagedescription-method"></a>Metodo IWMPControls3:: getAudioLanguageDescription

Il metodo **getAudioLanguageDescription** restituisce la descrizione della lingua audio corrispondente all'indice in base uno specificato.

## <a name="syntax"></a>Sintassi


```CSharp
public System.String getAudioLanguageDescription(
  System.Int32 lIndex
);
```


```VB

Public Function getAudioLanguageDescription( _
  ByVal lIndex As System.Int32 _
) As System.String
Implements IWMPControls3.getAudioLanguageDescription
```





## <a name="parameters"></a>Parametri

<dl> <dt>

*lIndex* \[ in\]
</dt> <dd>

**System. Int32** che è l'indice del linguaggio audio basato su uno.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

**System. String** che rappresenta la descrizione della lingua audio.

## <a name="remarks"></a>Commenti

Per il contenuto basato su Windows Media, le proprietà e i metodi relativi alla selezione della lingua supportano solo un singolo output.

Utilizzare la proprietà **audioLanguageCount** per ottenere il numero di lingue audio supportate e accedere a una lingua audio singolarmente utilizzando un indice in base uno.

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

[**IWMPControls3. currentAudioLanguage (VB e C#)**](wmplibiwmpcontrols3-iwmpcontrols3-currentaudiolanguage--vb-and-c.md)
</dt> <dt>

[**IWMPControls3. getAudioLanguageID (VB e C#)**](wmplibiwmpcontrols3-iwmpcontrols3-getaudiolanguageid--vb-and-c.md)
</dt> <dt>

[**IWMPControls3. getLanguageName (VB e C#)**](wmplibiwmpcontrols3-iwmpcontrols3-getlanguagename--vb-and-c.md)
</dt> </dl>

 

 





