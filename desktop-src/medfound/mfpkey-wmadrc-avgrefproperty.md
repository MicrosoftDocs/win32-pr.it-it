---
description: Specifica il livello di volume medio del contenuto audio.
ms.assetid: eabb36ff-300f-4ed1-aca3-9415627ac1a7
title: MFPKEY_WMADRC_AVGREF proprietà (Wmcodecdsp.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cf7d3575b81ca878c610aed95ca25f73fa94c292ec16f9245a72a3a9515198c7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118973240"
---
# <a name="mfpkey_wmadrc_avgref-property"></a>Proprietà AVGREF MFPKEY \_ \_ WMADRC

Specifica il livello di volume medio del contenuto audio.

## <a name="constant-for-ipropertybag"></a>Costante per IPropertyBag

g \_ wszWMADRCAverageReference

## <a name="data-type"></a>Tipo di dati

VT \_ I4

## <a name="remarks"></a>Commenti

È possibile ottenere questo valore dal codificatore dopo l'elaborazione del contenuto. Questo valore può essere impostato anche nel decodificatore ai fini del controllo di intervallo dinamico, ma avrà effetto solo se è impostata la proprietà [MFPKEY \_ WMADEC \_ DRCMODE.](mfpkey-wmadec-drcmodeproperty.md)

Per altre informazioni sul controllo dinamico degli intervalli, vedere l'articolo Web [Windows Audio multimediale Professional codec.](/previous-versions/ms867218(v=msdn.10))

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop XP\]<br/>                                             |
| Server minimo supportato<br/> | Windows Solo app desktop di Server 2003 \[\]<br/>                                    |
| Intestazione<br/>                   | <dl> <dt>Wmcodecdsp.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Media Foundation proprietà](media-foundation-properties.md)
</dt> </dl>

 

 
