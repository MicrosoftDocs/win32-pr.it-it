---
description: Dati di formato aggiuntivi per un flusso binario in un file ASF (Advanced Systems Format).
ms.assetid: fc5b9890-1508-498e-b2ce-ed4fa2052f9c
title: MF_MT_ARBITRARY_FORMAT attributo (Mfapi.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: aa7629e92eea07059f562d553985628f2099df1da03bd371617f0eed5183dd69
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118973610"
---
# <a name="mf_mt_arbitrary_format-attribute"></a>Attributo MF \_ MT \_ ARBITRARY \_ FORMAT

Dati di formato aggiuntivi per un flusso binario in un file ASF (Advanced Systems Format).

## <a name="data-type"></a>Tipo di dati

**BYTE\[\]**

## <a name="getset"></a>Ottenere/impostare

Per ottenere questo attributo, chiamare [**IMFAttributes::GetBlob**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getblob).

Per impostare questo attributo, chiamare [**IMFAttributes::SetBlob**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setblob).

## <a name="remarks"></a>Commenti

Le applicazioni possono usare flussi binari per contenere tipi di dati personalizzati. L'origine multimediale ASF considera il valore di questo attributo come BLOB opaco. Il **membro formattype** della [**struttura MT \_ ARBITRARY \_ HEADER**](/windows/desktop/api/mfapi/ns-mfapi-mt_arbitrary_header) definisce il layout dei dati di formato.

Questa struttura corrisponde al campo Format Data (Formato dati) dei dati specifici del tipo nell'oggetto Proprietà flusso, nei file in cui il tipo di flusso è **ASF \_ Binary \_ Media.** Per altre informazioni, vedere la specifica ASF.

> [!Note]  
> Nell'SDK Windows Media Format i flussi binari sono denominati flussi *arbitrari* o *flussi di dati arbitrari.*

 

La costante GUID per questo attributo viene esportata da mfuuid.lib.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 7 \[ app desktop\]<br/>                                         |
| Server minimo supportato<br/> | Windows Solo app desktop server 2008 R2 \[\]<br/>                            |
| Intestazione<br/>                   | <dl> <dt>Mfapi.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Elenco alfabetico degli Media Foundation personalizzati](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[Attributi del tipo di supporto](media-type-attributes.md)
</dt> <dt>

[INTESTAZIONE \_ ARBITRARIA MF \_ \_ MT](mf-mt-arbitrary-header.md)
</dt> </dl>

 

 




