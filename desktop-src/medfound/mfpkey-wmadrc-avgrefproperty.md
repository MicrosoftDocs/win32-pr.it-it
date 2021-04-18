---
description: Specifica il livello di volume medio del contenuto audio.
ms.assetid: eabb36ff-300f-4ed1-aca3-9415627ac1a7
title: Proprietà MFPKEY_WMADRC_AVGREF (Wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cf18c37b00f84cc3ae3fdf1f44b2fbefcc56d9f8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106309110"
---
# <a name="mfpkey_wmadrc_avgref-property"></a>MFPKEY \_ WMADRC- \_ Proprietà AVGREF

Specifica il livello di volume medio del contenuto audio.

## <a name="constant-for-ipropertybag"></a>Costante per IPropertyBag

g \_ wszWMADRCAverageReference

## <a name="data-type"></a>Tipo di dati

VT \_ I4

## <a name="remarks"></a>Commenti

È possibile ottenere questo valore dal codificatore dopo l'elaborazione del contenuto. Questo valore può essere impostato anche nel decodificatore allo scopo di un controllo intervallo dinamico, ma avrà effetto solo se è impostata la proprietà [MFPKEY \_ WMADEC \_ DRCMODE](mfpkey-wmadec-drcmodeproperty.md) .

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

 

 
