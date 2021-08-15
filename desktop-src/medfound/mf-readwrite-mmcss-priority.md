---
description: Imposta la priorità del thread di base per il lettore di origine o il writer di sink.
ms.assetid: 9513AE28-2AF4-45EC-AC19-C0718540E26F
title: MF_READWRITE_MMCSS_PRIORITY attributo (Mfreadwrite.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 56f108b7cce9f1c9d6226803bf2a2cc32b62ac94077f7f84cbc78e632cb25ea8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118740603"
---
# <a name="mf_readwrite_mmcss_priority-attribute"></a>Attributo MF \_ READWRITE \_ MMCSS \_ PRIORITY

Imposta la priorità del thread di base per il lettore di origine o il writer di sink.

## <a name="data-type"></a>Tipo di dati

**INT32** archiviato come **UINT32**

## <a name="getset"></a>Ottenere/impostare

Per ottenere questo attributo, chiamare [**IMFAttributes::GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).

Per impostare questo attributo, chiamare [**IMFAttributes::SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).

## <a name="remarks"></a>Commenti

Facoltativamente, impostare questo attributo quando si crea un'istanza del lettore di [origine](source-reader.md) o del [writer di sink.](sink-writer.md) Se si imposta questo attributo, impostare anche [l'attributo MF \_ READWRITE \_ MMCSS \_ CLASS.](mf-readwrite-mmcss-class.md) In caso contrario, questo attributo viene ignorato.

Quando il lettore di origine o il writer sink registra i thread con il servizio [Utilità](../procthread/multimedia-class-scheduler-service.md)di pianificazione classi multimediali , il valore di questo attributo specifica la priorità del thread di base. Se questo attributo non è impostato, il valore predefinito è zero.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Windows 8 app desktop \| app UWP\]<br/>                                        |
| Server minimo supportato<br/> | \[Windows Server 2012 app desktop \| app UWP\]<br/>                              |
| Intestazione<br/>                   | <dl> <dt>Mfreadwrite.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Elenco alfabetico degli Media Foundation personalizzati](alphabetical-list-of-media-foundation-attributes.md)
</dt> </dl>

 

 
