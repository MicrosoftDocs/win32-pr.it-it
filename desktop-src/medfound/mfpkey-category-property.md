---
description: Contiene il GUID di categoria per una trasformazione Media Foundation (MFT).
ms.assetid: 3c0948fc-42ea-4e43-a312-c98038020214
title: Proprietà MFPKEY_CATEGORY (Mftransform. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0bbb83ab2c824ff9a4510e520b13c49ae5b3a52a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103882221"
---
# <a name="mfpkey_category-property"></a>\_Proprietà di categoria MFPKEY

Contiene il GUID di categoria per una trasformazione Media Foundation (MFT).



Tipo di dati

Tipo PROPVARIANT (VT)

membro PROPVARIANT

**GUID** (**CLSID** \* )

\_CLSID VT

**puuid**



## <a name="remarks"></a>Commenti

Il valore di questa proprietà è un GUID che identifica la categoria MFT. Per un elenco di categorie, vedere [**la \_ categoria MFT**](mft-category.md).

Questa proprietà è facoltativa ed è solo informativa. Un MFT può usare questa proprietà per segnalare la categoria in cui è registrata. Per ottenere questa proprietà, eseguire una query su MFT per l'interfaccia **IPropertyStore** .

Per enumerare una categoria MFT, chiamare la funzione [**MFTEnum**](/windows/desktop/api/mfapi/nf-mfapi-mftenum) . Non esiste un collegamento diretto tra la funzione **MFTEnum** e questa proprietà.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                           |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2008\]<br/>                                     |
| Intestazione<br/>                   | <dl> <dt>Mftransform. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Proprietà Media Foundation](media-foundation-properties.md)
</dt> <dt>

[Trasformazioni Media Foundation](media-foundation-transforms.md)
</dt> </dl>

 

 




