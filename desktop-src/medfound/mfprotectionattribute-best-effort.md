---
description: Imposta come attributo per un oggetto IMFOutputSchema.
ms.assetid: 0CCCAB27-DEB0-41D8-A70C-D6CCEFE0601F
title: Attributo MFPROTECTIONATTRIBUTE_BEST_EFFORT (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fd7d2f173b5bf85080e0de65866f84b3a317b7ac
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104226913"
---
# <a name="mfprotectionattribute_best_effort-attribute"></a>\_Attributo MFPROTECTIONATTRIBUTE Best \_ effort

Imposta come attributo per un oggetto [**IMFOutputSchema**](/windows/desktop/api/mfidl/nn-mfidl-imfoutputschema) . Se questo attributo è presente, un tentativo non riuscito di applicare la protezione viene ignorato. Se il valore dell'attributo associato è **true**, deve essere applicato lo schema di protezione con l'attributo di [ \_ failover \_ MFPROTECTIONATTRIBUTE](mfprotectionattribute-fail-over.md) .

## <a name="data-type"></a>Tipo di dati

**Bool** archiviato come **UInt32**

## <a name="remarks"></a>Commenti

Se **true**, applica lo schema di protezione con l'attributo di [ \_ failover MFPROTECTIONATTRIBUTE \_](mfprotectionattribute-fail-over.md) se l'impostazione di questa protezione ha esito negativo.

Imposta come attributo per un oggetto [**IMFOutputSchema**](/windows/desktop/api/mfidl/nn-mfidl-imfoutputschema) .

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app UWP Windows 8\]<br/>                                             |
| Server minimo supportato<br/> | \[Solo app UWP Windows Server 2012\]<br/>                                   |
| Intestazione<br/>                   | <dl> <dt>Mfidl. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Elenco alfabetico degli attributi di Media Foundation](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[Attributi del tipo di supporto](media-type-attributes.md)
</dt> </dl>

 

 




