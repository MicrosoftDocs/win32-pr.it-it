---
description: Specifica il livello di volume massimo desiderato per il contenuto audio di output.
ms.assetid: 231b7296-ca80-4918-bae6-674b976db24c
title: Proprietà MFPKEY_WMADRC_PEAKTARGET (Wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6c40fa68e2b580c5d3e8550d6e46c9f6b9fe4bfc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106310262"
---
# <a name="mfpkey_wmadrc_peaktarget-property"></a>MFPKEY \_ WMADRC- \_ Proprietà PEAKTARGET

Specifica il livello di volume massimo desiderato per il contenuto audio di output.

## <a name="constant-for-ipropertybag"></a>Costante per IPropertyBag

g \_ wszWMADRCPeakTarget

## <a name="data-type"></a>Tipo di dati

VT \_ I4

## <a name="default-value"></a>Valore predefinito

Vedere la sezione Osservazioni.

## <a name="remarks"></a>Commenti

È possibile impostare questo valore nel decodificatore allo scopo di un controllo intervallo dinamico, ma avrà effetto solo se viene impostata la proprietà [MFPKEY \_ WMADEC \_ DRCMODE](mfpkey-wmadec-drcmodeproperty.md) .

Se si richiede il controllo dinamico degli intervalli dal decodificatore quando questa proprietà non è impostata, il codec calcolerà un valore predefinito.

Usare le proprietà [MFPKEY \_ WMADRC \_ AVGREF](mfpkey-wmadrc-avgrefproperty.md) e [MFPKEY \_ WMADRC \_ PEAKREF](mfpkey-wmadrc-peakrefproperty.md) per calcolare i valori appropriati per questa proprietà.

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

 

 
