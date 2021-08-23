---
description: Abilita la modalità a bassa latenza in un codec.
ms.assetid: 15E8FF6F-AD8C-436F-B3C0-5062B1F86E32
title: CODECAPI_AVLowLatencyMode proprietà (Codecapi.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2d1466f7874fe743dbc865df251f077440885103853e3784af19624c4733a1e4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119606271"
---
# <a name="codecapi_avlowlatencymode-property"></a>PROPRIETÀ CODECAPI \_ AVLowLatencyMode

Abilita la modalità a bassa latenza in un codec.

## <a name="data-type"></a>Tipo di dati

**ULONG** (**VT \_ BOOL**)

## <a name="property-guid"></a>GUID proprietà

**CODECAPI \_ AVLowLatencyMode**

## <a name="property-value"></a>Valore proprietà

Se il valore è diverso da zero, è abilitata la modalità a bassa latenza. Se il valore è zero, la modalità a bassa latenza è disabilitata.

## <a name="remarks"></a>Commenti

Questa proprietà si applica sia ai codificatori che ai decodificatori.

La modalità a bassa latenza è utile per le comunicazioni in tempo reale o l'acquisizione in tempo reale, quando la latenza deve essere ridotta al minimo. Tuttavia, la modalità a bassa latenza potrebbe anche ridurre la qualità di decodifica o codifica.

Si prevede che il codificatore non aggiungerà alcun ritardo del campione a causa del riordinamento dei frame nel processo di codifica e un campione di input genererà un campione di output. Le sezioni/fotogrammi B possono essere presenti purché non introduca un nuovo ordinamento dei fotogrammi nel codificatore.

> [!WARNING] 
> Nell'implementazione corrente il Media Foundation decodificatore H.264 usa il tipo **VT_UI4** per questa proprietà. Tutte le altre implementazioni, incluso il codificatore H.264, usano il **tipo VT_BOOL**.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Windows 8 app desktop \| app UWP\]<br/>                                     |
| Server minimo supportato<br/> | \[Windows Server 2012 app desktop \| app UWP\]<br/>                           |
| Intestazione<br/>                   | <dl> <dt>Codecapi.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Media Foundation proprietà](media-foundation-properties.md)
</dt> <dt>

[**ICodecAPI**](/windows/desktop/api/strmif/nn-strmif-icodecapi)
</dt> </dl>

 

