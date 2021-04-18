---
description: Specifica la durata di ECHO che l'algoritmo AEC (Acoustic Echo Cancel) può gestire, in millisecondi.
ms.assetid: d451b90f-7ef7-4f66-be83-aca93e3ad894
title: Proprietà MFPKEY_WMAAECMA_FEATR_ECHO_LENGTH (Wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2d66f7dcc4764447495e0f3ae55d2d038c2a8d8e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106309133"
---
# <a name="mfpkey_wmaaecma_featr_echo_length-property"></a>\_ \_ \_ Proprietà lunghezza Echo MFPKEY WMAAECMA featr \_

Specifica la durata di ECHO che l'algoritmo AEC (Acoustic Echo Cancel) può gestire, in millisecondi.

## <a name="constant-for-ipropertybag"></a>Costante per IPropertyBag

Disponibile solo tramite [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore).

## <a name="data-type"></a>Tipo di dati

VT \_ I4

## <a name="default-value"></a>Valore predefinito

256

## <a name="applies-to"></a>Si applica a

-   [DSP di acquisizione vocale](voicecapturedmo.md)

## <a name="remarks"></a>Commenti

L'algoritmo AEC utilizza un filtro adattivo la cui lunghezza è determinata dalla durata dell'eco. È consigliabile che le applicazioni usino uno dei valori seguenti:

-   128
-   256
-   512
-   1024

Il valore predefinito è 256 millisecondi, che è sufficiente per la maggior parte degli ambienti Office e Home. Prima di impostare questa proprietà, è necessario impostare la proprietà [MFPKEY \_ WMAAECMA \_ feature \_ mode](mfpkey-wmaaecma-feature-modeproperty.md) su Variant \_ true.

Il DSP usa questa proprietà solo quando è abilitata l'elaborazione AEC.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                          |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2008\]<br/>                                    |
| Intestazione<br/>                   | <dl> <dt>Wmcodecdsp. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Proprietà Media Foundation](media-foundation-properties.md)
</dt> <dt>

[DSP di acquisizione vocale](voicecapturedmo.md)
</dt> </dl>

 

 
