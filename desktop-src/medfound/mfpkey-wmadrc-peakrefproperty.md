---
description: Specifica il livello di volume massimo che si verifica nel contenuto audio.
ms.assetid: 177311c4-c348-4d38-8c8d-b6690643529c
title: MFPKEY_WMADRC_PEAKREF proprietà (Wmcodecdsp.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 58013ba116b9217ad6c16c93e420a09872cd887c4d5068f7c5b5dd68bf013377
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119953452"
---
# <a name="mfpkey_wmadrc_peakref-property"></a>Proprietà MFPKEY \_ WMADRC \_ PEAKREF

Specifica il livello di volume massimo che si verifica nel contenuto audio.

## <a name="constant-for-ipropertybag"></a>Costante per IPropertyBag

g \_ wszWMADRCPeakReference

## <a name="data-type"></a>Tipo di dati

VT \_ I4

## <a name="remarks"></a>Commenti

È possibile ottenere questo valore dal codificatore dopo l'elaborazione del contenuto. Questo valore può essere impostato anche nel decodificatore per il controllo dinamico dell'intervallo.

Per altre informazioni sul controllo dinamico degli intervalli, vedere l'articolo Web [Windows Media Audio Professional Codec Features](/previous-versions/ms867218(v=msdn.10)).

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

 

 
