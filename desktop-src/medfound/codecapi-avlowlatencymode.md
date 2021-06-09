---
description: Abilita la modalità a bassa latenza in un codec.
ms.assetid: 15E8FF6F-AD8C-436F-B3C0-5062B1F86E32
title: CODECAPI_AVLowLatencyMode proprietà (Codecapi.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5be7e23a29e9dd5f88f7a96e6c32fd42b68a7204
ms.sourcegitcommit: adba238660d8a5f4fe98fc6f5d105d56aac3a400
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/09/2021
ms.locfileid: "111826905"
---
# <a name="codecapi_avlowlatencymode-property"></a>CODECAPI \_ AVLowLatencyMode - proprietà

Abilita la modalità a bassa latenza in un codec.

## <a name="data-type"></a>Tipo di dati

**ULONG** (**VT \_ BOOL**)

## <a name="property-guid"></a>GUID proprietà

**CODECAPI \_ AVLowLatencyMode**

## <a name="property-value"></a>Valore proprietà

Se il valore è diverso da zero, viene abilitata la modalità a bassa latenza. Se il valore è zero, la modalità a bassa latenza è disabilitata.

## <a name="remarks"></a>Commenti

Questa proprietà si applica sia ai codificatori che ai decodificatori.

La modalità a bassa latenza è utile per le comunicazioni in tempo reale o l'acquisizione in tempo reale, quando la latenza deve essere ridotta al minimo. Tuttavia, la modalità a bassa latenza potrebbe anche ridurre la qualità di decodifica o codifica.

Il codificatore non dovrebbe aggiungere alcun ritardo del campione a causa del riordinamento dei fotogrammi nel processo di codifica e un campione di input genererà un campione di output. Le sezioni/fotogrammi B possono essere presenti purché non introduca alcun ordinamento dei fotogrammi nel codificatore.

> [!WARNING] 
> Nell'implementazione corrente il Media Foundation decodificatore H.264 usa il **tipo VT_UI4** per questa proprietà. Tutte le altre implementazioni, incluso il codificatore H.264, usano il **tipo VT_BOOL**.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 8 app \[ desktop \| UWP\]<br/>                                     |
| Server minimo supportato<br/> | App desktop di Windows Server 2012 \[ \| per app UWP\]<br/>                           |
| Intestazione<br/>                   | <dl> <dt>Codecapi.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Media Foundation proprietà](media-foundation-properties.md)
</dt> <dt>

[**ICodecAPI**](/windows/desktop/api/strmif/nn-strmif-icodecapi)
</dt> </dl>

 

