---
description: Specifica se l'origine multimediale ASF utilizza la ricerca approssimativa.
ms.assetid: 4877b67c-524c-4717-a90f-6de21918d3d8
title: Proprietà MFPKEY_ASFMediaSource_ApproxSeek (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 253a18ebbdf78e3aa0ef0e79f41c4bf180a04b48
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/03/2021
ms.locfileid: "106320749"
---
# <a name="mfpkey_asfmediasource_approxseek-property"></a>MFPKEY \_ ASFMediaSource- \_ Proprietà ApproxSeek

Specifica se l'origine multimediale ASF utilizza la ricerca approssimativa.



Tipo di dati

Tipo PROPVARIANT (VT)

membro PROPVARIANT

**\_bool Variant**

\_bool VT

**boolVal**



## <a name="remarks"></a>Commenti

Le applicazioni possono usare questa proprietà per configurare l'origine dei supporti ASF. Per impostare la proprietà, passare un puntatore **IPropertyStore** al resolver di origine. Per altre informazioni, vedere [configurazione di un'origine multimediale](configuring-a-media-source.md).

L'origine dei supporti ASF gestisce la ricerca come segue:

-   Se il valore di questa proprietà è **Variant \_ true**, l'origine multimediale usa la ricerca approssimativa, che è meno accurata ma più veloce rispetto alla ricerca esatta.
-   Se il valore è **Variant \_ false** e il file ASF include un indice, l'origine multimediale usa la ricerca esatta.
-   Se il file ASF non contiene un indice, l'origine multimediale USA approxmate seeking a meno che la proprietà [MFPKEY \_ ASFMediaSource \_ IterativeSeekIfNoIndex](mfpkey-asfmediasource-iterativeseekifnoindex.md) non sia impostata su **Variant \_ true**.
-   Se il file ASF non contiene un indice e la proprietà [MFPKEY \_ ASFMediaSource \_ IterativeSeekIfNoIndex](mfpkey-asfmediasource-iterativeseekifnoindex.md) è **Variant \_ true**, l'origine multimediale usa la ricerca iterativa. La ricerca iterativa è più precisa ma più lenta rispetto alla ricerca approssimativa, ma in genere meno accurata della ricerca esatta.
    > [!Note]  
    > Richiede Windows 7.

     

Il valore predefinito di questa proprietà è **Variant \_ false**.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                     |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2008\]<br/>                               |
| Intestazione<br/>                   | <dl> <dt>Mfidl. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Proprietà Media Foundation](media-foundation-properties.md)
</dt> </dl>

 

 




