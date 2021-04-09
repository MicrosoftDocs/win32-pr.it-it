---
description: Specifica la complessità dell'algoritmo di codifica.
ms.assetid: 5dd34818-f282-4859-b423-97e9c4944aec
title: Proprietà MFPKEY_ENCCOMPLEXITY (Wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 51f50e7966a05affe8ae75869b670cf75f088b53
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103880809"
---
# <a name="mfpkey_enccomplexity-property"></a>\_Proprietà ENCCOMPLEXITY di MFPKEY

Specifica la complessità dell'algoritmo di codifica. Il valore è un numero intero compreso tra 0 e 100, dove 0 specifica l'algoritmo meno complesso e 100 specifica l'algoritmo più complesso.

## <a name="constant-for-ipropertybag"></a>Costante per IPropertyBag

Disponibile solo tramite [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore).

## <a name="data-type"></a>Tipo di dati

**\_UI4 VT**

## <a name="default-value"></a>Valore predefinito

100 per Windows Media Audio 10 e Windows Media Audio 10 Professional

100 per la versione di Windows Vista di Windows Media Audio 10 Lossless

0 per la versione di Windows 7 Windows Media Audio 10 Lossless

## <a name="remarks"></a>Commenti

Se la proprietà [**MFPKEY \_ CONSTRAINECOMPLEXITY**](mfpkey-constrainenccomplexityproperty.md) ha un valore **Variant \_ true**, il codificatore regola la complessità dell'algoritmo in base al valore di questa proprietà.

Per il codificatore Windows Media Audio 10 e il codificatore Windows Media Audio 10 Professional, se il valore di questa proprietà è 100, il codificatore pone una domanda elevata sulla CPU e produce l'output di qualità superiore. Poiché il valore di questa proprietà diminuisce, la richiesta sulla CPU diminuisce, ma anche la qualità dell'output diminuisce.

Per il codificatore Windows Media Audio 10 Lossless, se il valore di questa proprietà è 0, il codificatore pone una domanda bassa sulla CPU. Man mano che aumenta il valore di questa proprietà, la domanda sulla CPU aumenta e le dimensioni dell'output del codificatore diminuiscono leggermente. L'output è lossless indipendentemente dal valore di questa proprietà.

Se si lascia questa proprietà sul valore predefinito **Variant \_ false**, il codificatore usa l'algoritmo predefinito. L'algoritmo predefinito dipende dal codificatore in uso e dalla versione di Windows in esecuzione. Nella tabella seguente viene descritto il comportamento predefinito per le diverse combinazioni.



| Sistema operativo | Comportamento predefinito                                                                                                                                                                                                |
|------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Windows Vista    | Per impostazione predefinita, i codificatori Windows Media Audio 10, Windows Media Audio 10 Professional e Windows Media Audio 10 Lossless utilizzano l'algoritmo più complesso.                                                    |
| Windows 7        | Per impostazione predefinita, i codificatori Windows Media Audio 10 e Windows Media Audio 10 Professional utilizzano l'algoritmo più complesso. Per impostazione predefinita, il codificatore Windows Media Audio 10 Lossless usa l'algoritmo meno complesso. |



 

Se la proprietà [**MFPKEY \_ CONSTRAINECOMPLEXITY**](mfpkey-constrainenccomplexityproperty.md) ha un valore **Variant \_ false**, il codificatore ignora questa proprietà.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                          |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2008\]<br/>                                    |
| Intestazione<br/>                   | <dl> <dt>Wmcodecdsp. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Proprietà Media Foundation](media-foundation-properties.md)
</dt> </dl>

 

 
