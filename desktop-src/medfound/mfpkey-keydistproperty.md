---
description: Specifica il tempo massimo, in millisecondi, tra i fotogrammi chiave nell'output del codec.
ms.assetid: 2a52e6a5-10a0-46dd-aa31-cb55094903b5
title: Proprietà MFPKEY_KEYDIST (Wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d55925811db71f24cf360113aa6d03a325bcdc11
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103880797"
---
# <a name="mfpkey_keydist-property"></a>\_Proprietà MFPKEY

Specifica il tempo massimo, in millisecondi, tra i fotogrammi chiave nell'output del codec.

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

La logica interna del codec determina la posizione effettiva di ogni fotogramma chiave. La distanza tra due fotogrammi chiave può essere inferiore al valore di questa proprietà, tuttavia, non sarà mai maggiore.

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

 

 




