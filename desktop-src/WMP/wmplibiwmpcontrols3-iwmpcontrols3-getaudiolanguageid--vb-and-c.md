---
title: Metodo IWMPControls3 getAudioLanguageID
description: Il metodo getAudioLanguageID restituisce l'identificatore delle impostazioni locali (LCID) per un indice di lingua audio specificato.
ms.assetid: 880bbfca-6f69-41ce-a078-467c1939fae5
keywords:
- Metodo getAudioLanguageID Windows Media Player
- Metodo getAudioLanguageID Windows Media Player, interfaccia IWMPControls3
- Interfaccia IWMPControls3 Windows Media Player, metodo getAudioLanguageID
topic_type:
- apiref
api_name:
- IWMPControls3.getAudioLanguageID
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fb8112eafec018b12012d20b37bfe30f7b464377
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106332452"
---
# <a name="iwmpcontrols3getaudiolanguageid-method"></a>Metodo IWMPControls3:: getAudioLanguageID

Il metodo **getAudioLanguageID** restituisce l'identificatore delle impostazioni locali (LCID) per un indice di lingua audio specificato.

## <a name="syntax"></a>Sintassi


```CSharp
public System.Int32 getAudioLanguageID(
  System.Int32 lIndex
);
```


```VB

Public Function getAudioLanguageID( _
  ByVal lIndex As System.Int32 _
) As System.Int32
Implements IWMPControls3.getAudioLanguageID
```





## <a name="parameters"></a>Parametri

<dl> <dt>

*lIndex* \[ in\]
</dt> <dd>

**System. Int32** che rappresenta l'indice in base uno della lingua audio.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

**System. Int32** che rappresenta l'identificatore LCID.

## <a name="remarks"></a>Commenti

Un LCID identifica in modo univoco un dialetto di lingua particolare, denominato impostazioni locali.

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

[**IWMPControls3. currentAudioLanguage (VB e C#)**](wmplibiwmpcontrols3-iwmpcontrols3-currentaudiolanguage--vb-and-c.md)
</dt> <dt>

[**IWMPControls3. currentAudioLanguageIndex (VB e C#)**](wmplibiwmpcontrols3-iwmpcontrols3-currentaudiolanguageindex--vb-and-c.md)
</dt> <dt>

[**IWMPControls3. getAudioLanguageDescription (VB e C#)**](wmplibiwmpcontrols3-iwmpcontrols3-getaudiolanguagedescription--vb-and-c.md)
</dt> <dt>

[**IWMPControls3. getLanguageName (VB e C#)**](wmplibiwmpcontrols3-iwmpcontrols3-getlanguagename--vb-and-c.md)
</dt> </dl>

 

 





