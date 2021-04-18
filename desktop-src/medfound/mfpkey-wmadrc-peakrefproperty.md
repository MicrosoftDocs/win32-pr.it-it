---
description: Specifica il livello di volume massimo che si verifica nel contenuto audio.
ms.assetid: 177311c4-c348-4d38-8c8d-b6690643529c
title: Proprietà MFPKEY_WMADRC_PEAKREF (Wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 88e91df613541f91f2efd2fd71ea38d7b1ca9a60
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106309109"
---
# <a name="mfpkey_wmadrc_peakref-property"></a>MFPKEY \_ WMADRC- \_ Proprietà PEAKREF

Specifica il livello di volume massimo che si verifica nel contenuto audio.

## <a name="constant-for-ipropertybag"></a>Costante per IPropertyBag

g \_ wszWMADRCPeakReference

## <a name="data-type"></a>Tipo di dati

VT \_ I4

## <a name="remarks"></a>Commenti

È possibile ottenere questo valore dal codificatore dopo l'elaborazione del contenuto. Questo valore può essere impostato anche nel decodificatore per il controllo dinamico degli intervalli.

Per ulteriori informazioni sul controllo dinamico degli intervalli, vedere l'articolo Web [Windows Media audio funzionalità dei codec professionali](/previous-versions/ms867218(v=msdn.10)).

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

 

 
