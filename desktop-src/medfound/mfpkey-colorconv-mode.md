---
description: 'MFPKEY_COLORCONV_MODE proprietà : specifica se il flusso di input è interlacciato.'
ms.assetid: d0d93151-5b0d-44a7-8497-f11b3e23a031
title: MFPKEY_COLORCONV_MODE proprietà (Wmcodecdsp.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9f86ed10873c1587aefba342392afa7f84f8c635788339d64deca18b76629255
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118242890"
---
# <a name="mfpkey_colorconv_mode-property"></a>Proprietà MFPKEY \_ COLORCONV \_ MODE

Specifica se il flusso di input è interlacciato.

## <a name="constant-for-ipropertybag"></a>Costante per IPropertyBag

Disponibile solo tramite [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore).

## <a name="data-type"></a>Tipo di dati

VT \_ I4

## <a name="default-value"></a>Valore predefinito

Calcolato dal provider di servizi di data e ora dal video di origine.

## <a name="applies-to"></a>Si applica a

-   [DSP del convertitore di colori](colorconverter.md)

## <a name="remarks"></a>Commenti

Usare uno dei valori seguenti.



| Valore | Descrizione |
|-------|-------------|
| 0     | Progressivo |
| 2     | Interlaced  |



 

Se questa proprietà non è impostata, DSP usa il tipo di supporto di input per determinare se il video è interlacciato. È possibile impostare questa proprietà per eseguire l'override dell'impostazione del tipo di supporto.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop XP\]<br/>                                             |
| Server minimo supportato<br/> | Windows Solo app desktop server 2003 \[\]<br/>                                    |
| Intestazione<br/>                   | <dl> <dt>Wmcodecdsp.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Media Foundation proprietà](media-foundation-properties.md)
</dt> </dl>

 

 
