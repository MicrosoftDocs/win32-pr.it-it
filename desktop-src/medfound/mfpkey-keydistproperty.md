---
description: Specifica il tempo massimo, in millisecondi, tra fotogrammi chiave nell'output del codec.
ms.assetid: 2a52e6a5-10a0-46dd-aa31-cb55094903b5
title: MFPKEY_KEYDIST proprietà (Wmcodecdsp.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8d3c59e3002cff6d0962f0ebf77dc20b2858ab5db3cfda8acceb9c5577d7cb7e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117689930"
---
# <a name="mfpkey_keydist-property"></a>Proprietà MFPKEY \_ KEYDIST

Specifica il tempo massimo, in millisecondi, tra fotogrammi chiave nell'output del codec.

## <a name="constant-for-ipropertybag"></a>Costante per IPropertyBag

g \_ wszWMVCKeyframeDistance

## <a name="data-type"></a>Tipo di dati

VT \_ I4

## <a name="default-value"></a>Valore predefinito

Il valore predefinito dipende dalla versione di Windows in esecuzione, come illustrato nella tabella seguente.



| Sistema operativo | Valore predefinito |
|------------------|---------------|
| Windows XP       | 8000          |
| Windows Vista    | 8000          |
| Windows 7        | 2000          |



 

## <a name="remarks"></a>Commenti

La logica interna del codec determina la posizione effettiva di ogni fotogramma chiave. La distanza tra due fotogrammi chiave può essere minore del valore di questa proprietà, ma non sarà mai maggiore.

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

 

 




