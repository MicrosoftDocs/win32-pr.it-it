---
title: EQUALIZERSETTINGS.nextPreset
description: Il metodo nextPreset applica il set di impostazioni dell'equalizzatore successivo.
ms.assetid: 67d40ec9-2744-4d63-aa56-0ee20496e896
keywords:
- EQUALIZERSETTINGS.nextPreset Windows Media Player
topic_type:
- apiref
api_name:
- EQUALIZERSETTINGS.nextPreset
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 715c5ee514cf2818cbab8b5553cab9565a2b448e47d1f6fe2282f17940cfc5b7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117748696"
---
# <a name="equalizersettingsnextpreset"></a>EQUALIZERSETTINGS.nextPreset

Il **metodo nextPreset applica** il set di impostazioni dell'equalizzatore successivo.

``` syntax
        elementID.nextPreset()
```

## <a name="parameters"></a>Parametri

Questo metodo non presenta parametri.

## <a name="return-value"></a>Valore restituito

Questo metodo non restituisce valori.

## <a name="remarks"></a>Commenti

Se il set di impostazioni corrente è l'ultimo disponibile, il primo set di impostazioni viene reso corrente.

## <a name="examples"></a>Esempio


```JScript
<SUBVIEW id="eqtray">
  <EQUALIZERSETTINGS id="eq"/>
  <BUTTON
    id="nextPreset" 
    onClick="eq.nextPreset();"
  />
  <BUTTON
    id="prevPreset" 
    onClick="eq.previousPreset();"
  />
  <TEXT
    id="currentPreset" 
    value="wmpprop:eq.currentPresetTitle" 
  />
</SUBVIEW>
```



## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|------------------------------------------------------|
| Versione<br/> | Windows Media Player versione 7.0 o successiva<br/> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Elemento EQUALIZERSETTINGS**](equalizersettings-element.md)
</dt> <dt>

[**EQUALIZERSETTINGS.previousPreset**](equalizersettings-previouspreset.md)
</dt> </dl>

 

 





