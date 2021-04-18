---
description: Specifica il modello di conformità del dispositivo che si vuole usare per la codifica video.
ms.assetid: cd2c068a-dbbc-42c5-bc92-bbb73f0259d1
title: Proprietà MFPKEY_DECODERCOMPLEXITYREQUESTED (Wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7e017361d7e8267d33ecb2cfdbce2a6e79758fac
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106310639"
---
# <a name="mfpkey_decodercomplexityrequested-property"></a>\_Proprietà DECODERCOMPLEXITYREQUESTED di MFPKEY

Specifica il modello di conformità del dispositivo che si vuole usare per la codifica video.

## <a name="data-type"></a>Tipo di dati

VT \_ I4

## <a name="default-value"></a>Valore predefinito

1

## <a name="constant-for-ipropertybag"></a>Costante per IPropertyBag

g \_ wszWMVCDecoderComplexityRequested

## <a name="data-type-for-ipropertybag"></a>Tipo di dati per IPropertyBag

\_BSTR VT

## <a name="default-value-for-ipropertybag"></a>Valore predefinito per IPropertyBag

MP

## <a name="remarks"></a>Commenti

Il codec tenterà di codificare il contenuto usando il modello di conformità del dispositivo specificato da questo valore. Il modello effettivo in cui è conforme il contenuto codificato può essere recuperato dalla proprietà [MFPKEY \_ DECODERCOMPLEXITYPROFILE](mfpkey-decodercomplexityprofileproperty.md) dopo la codifica.

Questa proprietà deve essere uno dei valori seguenti.



| Valore per IPropertyStore | Valore per IPropertyBag | Descrizione         |
|--------------------------|------------------------|---------------------|
| 0                        | SP                   | Profilo semplice      |
| 1                        | MP                   | profilo principale        |
| 2                        | CP                   | non più supportato |



 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop Windows XP\]<br/>                                             |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2003\]<br/>                                    |
| Intestazione<br/>                   | <dl> <dt>Wmcodecdsp. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Proprietà Media Foundation](media-foundation-properties.md)
</dt> </dl>

 

 




