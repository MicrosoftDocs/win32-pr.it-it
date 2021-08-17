---
description: Specifica la complessità dell'algoritmo di codifica.
ms.assetid: 5dd34818-f282-4859-b423-97e9c4944aec
title: MFPKEY_ENCCOMPLEXITY proprietà (Wmcodecdsp.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d93abe02b50f862fec706f75449e00643228a3917bc22ca9dafa9285d9d46be3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117690126"
---
# <a name="mfpkey_enccomplexity-property"></a>Proprietà MFPKEY \_ ENCCOMPLEXITY

Specifica la complessità dell'algoritmo di codifica. Il valore è un numero intero compreso tra 0 e 100, dove 0 specifica l'algoritmo meno complesso e 100 specifica l'algoritmo più complesso.

## <a name="constant-for-ipropertybag"></a>Costante per IPropertyBag

Disponibile solo tramite [**IPropertyStore.**](/windows/win32/api/propsys/nn-propsys-ipropertystore)

## <a name="data-type"></a>Tipo di dati

**VT \_ UI4**

## <a name="default-value"></a>Valore predefinito

100 per Windows Media Audio 10 e Windows Media Audio 10 Professional

100 per la Windows Vista di Windows Media Audio 10 Lossless

0 per la versione Windows 7 Windows Media Audio 10 Lossless

## <a name="remarks"></a>Commenti

Se il valore della proprietà [**MFPKEY \_ CONSTRAINECOMPLEXITY**](mfpkey-constrainenccomplexityproperty.md) è **VARIANT \_ TRUE,** il codificatore regola la complessità dell'algoritmo in base al valore di questa proprietà.

Per il codificatore Windows Media Audio 10 e il codificatore Windows Media Audio 10 Professional, se il valore di questa proprietà è 100, il codificatore pone una domanda elevata sulla CPU e produce l'output di massima qualità. Quando il valore di questa proprietà diminuisce, la domanda sulla CPU diminuisce, ma anche la qualità dell'output diminuisce.

Per il Windows media audio 10 senza perdita di dati, se il valore di questa proprietà è 0, il codificatore pone una domanda bassa sulla CPU. Con l'aumentare del valore di questa proprietà, la domanda sulla CPU aumenta e le dimensioni dell'output del codificatore diminuiscono leggermente. L'output è senza perdita di dati indipendentemente dal valore di questa proprietà.

Se si lascia questa proprietà sul valore predefinito **VARIANT \_ FALSE,** il codificatore usa l'algoritmo predefinito. L'algoritmo predefinito dipende dal codificatore in uso e dalla versione Windows in esecuzione. Nella tabella seguente viene descritto il comportamento predefinito per le diverse combinazioni.



| Sistema operativo | Comportamento predefinito                                                                                                                                                                                                |
|------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Windows Vista    | I codificatori Windows Media Audio 10, Windows Media Audio 10 Professional e Windows Media Audio 10 Lossless usano tutti l'algoritmo più complesso per impostazione predefinita.                                                    |
| Windows 7        | I Windows media audio 10 e Windows media audio 10 Professional usano l'algoritmo più complesso per impostazione predefinita. Il Windows media audio 10 senza perdita usa l'algoritmo meno complesso per impostazione predefinita. |



 

Se il valore della proprietà [**MFPKEY \_ CONSTRAINECOMPLEXITY**](mfpkey-constrainenccomplexityproperty.md) è **VARIANT \_ FALSE,** il codificatore ignora questa proprietà.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop Vista\]<br/>                                          |
| Server minimo supportato<br/> | Windows Solo app desktop di Server 2008 \[\]<br/>                                    |
| Intestazione<br/>                   | <dl> <dt>Wmcodecdsp.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Media Foundation proprietà](media-foundation-properties.md)
</dt> </dl>

 

 
