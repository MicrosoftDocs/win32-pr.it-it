---
description: Specifica se l'origine multimediale ASF usa la ricerca approssimativa.
ms.assetid: 4877b67c-524c-4717-a90f-6de21918d3d8
title: MFPKEY_ASFMediaSource_ApproxSeek proprietà (Mfidl.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5f68dedbf2b008870021e620029a039c21465d4bb45a23428225d7c88fae6583
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117874335"
---
# <a name="mfpkey_asfmediasource_approxseek-property"></a>MFPKEY \_ ASFMediaSource \_ ApproxSeek - proprietà

Specifica se l'origine multimediale ASF usa la ricerca approssimativa.



Tipo di dati

Tipo PROPVARIANT (vt)

membro PROPVARIANT

**VARIANT \_ BOOL**

VT \_ BOOL

**boolVal**



## <a name="remarks"></a>Commenti

Le applicazioni possono usare questa proprietà per configurare l'origine multimediale ASF. Per impostare la proprietà, passare un **puntatore IPropertyStore** al sistema di risoluzione di origine. Per altre informazioni, vedere [Configurazione di un'origine multimediale](configuring-a-media-source.md).

L'origine multimediale ASF gestisce la ricerca nel modo seguente:

-   Se il valore di questa proprietà è **VARIANT \_ TRUE,** l'origine multimediale usa la ricerca approssimativa, che è meno accurata ma più veloce della ricerca esatta.
-   Se il valore è **VARIANT \_ FALSE** e il file ASF ha un indice, l'origine multimediale usa la ricerca esatta.
-   Se il file ASF non contiene un indice, l'origine multimediale usa una ricerca approssimata a meno che la proprietà [MFPKEY \_ ASFMediaSource \_ IterativeSeekIfNoIndex](mfpkey-asfmediasource-iterativeseekifnoindex.md) non sia impostata su **VARIANT \_ TRUE.**
-   Se il file ASF non contiene un indice e la proprietà [MFPKEY \_ ASFMediaSource \_ IterativeSeekIfNoIndex](mfpkey-asfmediasource-iterativeseekifnoindex.md) è **VARIANT \_ TRUE,** l'origine multimediale usa la ricerca iterativa. La ricerca iterativa è più accurata, ma più lenta della ricerca approssimativa (ma in genere meno accurata della ricerca esatta).
    > [!Note]  
    > Richiede Windows 7.

     

Il valore predefinito di questa proprietà è **VARIANT \_ FALSE.**

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop di Vista\]<br/>                                     |
| Server minimo supportato<br/> | Windows Solo app desktop server 2008 \[\]<br/>                               |
| Intestazione<br/>                   | <dl> <dt>Mfidl.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Media Foundation proprietà](media-foundation-properties.md)
</dt> </dl>

 

 




