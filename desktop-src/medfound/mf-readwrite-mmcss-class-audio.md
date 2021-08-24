---
description: Specifica una classe MMCSS (Multimedia Class Scheduler Service) per i thread di elaborazione audio nel lettore di origine o nel writer di sink.
ms.assetid: F1B8A8C8-2E41-4321-A94D-C50447C69941
title: MF_READWRITE_MMCSS_CLASS_AUDIO attributo (Mfreadwrite.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f416c22619c0777ef244e6566328154bf7a7336587fc73a3f29626fcdaa1c462
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119345281"
---
# <a name="mf_readwrite_mmcss_class_audio-attribute"></a>Attributo MF \_ READWRITE \_ MMCSS \_ CLASS \_ AUDIO

Specifica una classe [MMCSS (Multimedia Class Scheduler Service)](../procthread/multimedia-class-scheduler-service.md) per i thread di elaborazione audio nel lettore di origine o nel writer di sink.

## <a name="data-type"></a>Tipo di dati

**LPWSTR**

## <a name="getset"></a>Ottenere/impostare

Per ottenere questo attributo, chiamare [**IMFAttributes::GetString**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getstring).

Per impostare questo attributo, chiamare [**IMFAttributes::SetString**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setstring).

## <a name="remarks"></a>Commenti

Facoltativamente, impostare questo attributo quando si crea un'istanza del lettore [di](source-reader.md) origine o del [writer di sink.](sink-writer.md) Il valore dell'attributo deve essere un nome di classe MMCSS valido.

Se questo attributo è impostato, il lettore di origine o il sink writer registra i thread di elaborazione audio con la classe MMCSS specificata. MMCSS garantisce che l'elaborazione dei dati nel lettore di origine o nel writer di sink abbia la priorità rispetto ad altre attività di sistema.

Per specificare la priorità di base per i thread audio, impostare l'attributo [ \_ MF READWRITE \_ MMCSS \_ PRIORITY \_ AUDIO.](mf-readwrite-mmcss-priority-audio.md) Se tale attributo non è impostato, la priorità di base per i thread audio è zero.

Questo attributo esegue l'override [dell'attributo \_ MF READWRITE \_ MMCSS \_ CLASS](mf-readwrite-mmcss-class.md) per i thread di elaborazione audio. Se nessuno dei due attributi è impostato, i thread audio non vengono registrati con MCSS.

Per la maggior parte delle applicazioni, la glitch audio è molto più evidente per l'utente che per glitch video e quindi meno accettabile. Per questo motivo, un'applicazione deve in genere impostare MF READWRITE MMCSS CLASS AUDIO su una classe MMCSS con priorità più alta rispetto \_ \_ a \_ \_ [MF \_ READWRITE \_ MMCSS \_ CLASS](mf-readwrite-mmcss-class.md). In questo modo si garantisce che all'elaborazione audio sia data una priorità più alta rispetto ad altre attività.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Windows 8 app desktop \| app UWP\]<br/>                                        |
| Server minimo supportato<br/> | \[Windows Server 2012 app desktop \| app UWP\]<br/>                              |
| Intestazione<br/>                   | <dl> <dt>Mfreadwrite.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Elenco alfabetico di Media Foundation attributi](alphabetical-list-of-media-foundation-attributes.md)
</dt> </dl>

 

 
