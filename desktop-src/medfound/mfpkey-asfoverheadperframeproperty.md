---
description: Specifica l'overhead, in byte per pacchetto, necessario per il contenitore usato per archiviare il contenuto compresso.
ms.assetid: 73ec52de-c74a-45b3-a453-7f32510b4484
title: Proprietà MFPKEY_ASFOVERHEADPERFRAME (Wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 208acf55871b18bb029279a27abd36a33ea8c79c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106318406"
---
# <a name="mfpkey_asfoverheadperframe-property"></a>\_Proprietà ASFOVERHEADPERFRAME di MFPKEY

Specifica l'overhead, in byte per pacchetto, necessario per il contenitore usato per archiviare il contenuto compresso.

## <a name="constant-for-ipropertybag"></a>Costante per IPropertyBag

g \_ wszWMVPacketOverhead

## <a name="data-type"></a>Tipo di dati

VT \_ I4

## <a name="default-value"></a>Valore predefinito

17

## <a name="remarks"></a>Commenti

Se si utilizza la struttura di file ASF (Advanced Systems Format), non modificare il valore predefinito. Se i dati non vengono archiviati in un file ASF, è necessario impostare questo valore su 0.

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

 

 




