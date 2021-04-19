---
description: Specifica il numero di fotogrammi video codificati dal codec che contengono effettivamente i dati.
ms.assetid: f96fd0b2-8c81-4318-b44c-4b794b3945a3
title: Proprietà MFPKEY_CODEDNONZEROFRAMES (Wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1b1ca5fb26288e2ea9ff801ba13aa7bef570ca95
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106311583"
---
# <a name="mfpkey_codednonzeroframes-property"></a>\_Proprietà CODEDNONZEROFRAMES di MFPKEY

Specifica il numero di fotogrammi video codificati dal codec che contengono effettivamente i dati.

## <a name="constant-for-ipropertybag"></a>Costante per IPropertyBag

Disponibile solo tramite [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore).

## <a name="data-type"></a>Tipo di dati

VT \_ I4

## <a name="remarks"></a>Commenti

Questo valore è uguale a [MFPKEY \_ TOTALFRAMES](mfpkey-totalframesproperty.md) meno tutti i frame eliminati a causa di vincoli di velocità di bit, meno qualsiasi frame di zero byte. È possibile ottenere questo valore al termine del passaggio degli esempi. I frame a zero byte possono essere creati per i frame duplicati.

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

 

 
