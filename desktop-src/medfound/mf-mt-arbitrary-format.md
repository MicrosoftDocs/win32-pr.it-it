---
description: Dati di formato aggiuntivi per un flusso binario in un file di formato Advanced Systems (ASF).
ms.assetid: fc5b9890-1508-498e-b2ce-ed4fa2052f9c
title: Attributo MF_MT_ARBITRARY_FORMAT (Mfapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6cf98da23fbc4631ca67462dfc58f870abe73885
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106314040"
---
# <a name="mf_mt_arbitrary_format-attribute"></a>\_ \_ Attributo formato arbitrario MF mt \_

Dati di formato aggiuntivi per un flusso binario in un file di formato Advanced Systems (ASF).

## <a name="data-type"></a>Tipo di dati

**BYTE\[\]**

## <a name="getset"></a>Ottenere/impostare

Per ottenere questo attributo, chiamare [**IMFAttributes:: GetBlob**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getblob).

Per impostare questo attributo, chiamare [**IMFAttributes::**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setblob)SetAttribute.

## <a name="remarks"></a>Commenti

Le applicazioni possono utilizzare flussi binari per mantenere i tipi di dati personalizzati. L'origine dei supporti ASF considera il valore di questo attributo come un BLOB opaco. Il membro **formatType** della struttura [**dell' \_ \_ intestazione mt arbitraria**](/windows/desktop/api/mfapi/ns-mfapi-mt_arbitrary_header) definisce il layout dei dati del formato.

Questa struttura corrisponde al campo dati di formato dei dati specifici del tipo nell'oggetto proprietà del flusso, nei file in cui il tipo di flusso è un **\_ \_ supporto binario ASF**. Per ulteriori informazioni, vedere la specifica ASF.

> [!Note]  
> In Windows Media Format SDK i flussi binari sono denominati *flussi arbitrari* o *flussi di dati arbitrari*.

 

La costante GUID per questo attributo viene esportata da mfuuid. lib.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows 7\]<br/>                                         |
| Server minimo supportato<br/> | Solo app desktop Windows Server 2008 R2 \[\]<br/>                            |
| Intestazione<br/>                   | <dl> <dt>Mfapi. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Elenco alfabetico degli attributi di Media Foundation](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[Attributi del tipo di supporto](media-type-attributes.md)
</dt> <dt>

[\_ \_ intestazione arbitraria MF \_ mt](mf-mt-arbitrary-header.md)
</dt> </dl>

 

 




