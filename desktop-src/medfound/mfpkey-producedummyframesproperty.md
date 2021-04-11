---
description: Specifica se il codificatore produce voci di frame fittizie nel flusso di bit per i frame duplicati.
ms.assetid: dc09cecb-98c0-40bb-9e5d-f4661bf98522
title: Proprietà MFPKEY_PRODUCEDUMMYFRAMES (Wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1b40bdaa54b3dc14a2b4ef44235d7f87cab5b905
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104226995"
---
# <a name="mfpkey_producedummyframes-property"></a>\_Proprietà PRODUCEDUMMYFRAMES di MFPKEY

Specifica se il codificatore produce voci di frame fittizie nel flusso di bit per i frame duplicati.

## <a name="constant-for-ipropertybag"></a>Costante per IPropertyBag

g \_ wszWMVCProduceDummyFrames

## <a name="data-type"></a>Tipo di dati

\_bool VT

## <a name="default-value"></a>Valore predefinito

VARIANTE \_ false

## <a name="remarks"></a>Commenti

Se questo valore è VARIANT \_ false, il codec non inserisce i dati nel flusso di bit per i frame duplicati.

I frame fittizi possono essere importanti nelle applicazioni in cui i numeri dei frame sono salvati in permanenza. Un esempio comune è quando vengono conservati i codici temporali SMPTE per il contenuto codificato.

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

 

 




