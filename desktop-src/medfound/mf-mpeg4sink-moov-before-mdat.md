---
description: Indica che moov verrà scritto prima della casella mdat nel file generato.
ms.assetid: 97B68B0A-8266-4FCF-8CD9-35890E1AC774
title: MF_MPEG4SINK_MOOV_BEFORE_MDAT attributo (Mfidl.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e98614484beee5187364570e3c5517ba0f61e0d77161484b59af93a9f5a6512c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119104737"
---
# <a name="mf_mpeg4sink_moov_before_mdat-attribute"></a>MF \_ MPEG4SINK \_ MOOV \_ PRIMA \_ dell'attributo MDAT

Indica che 'moov' verrà scritto prima della casella 'mdat' nel file generato.

## <a name="data-type"></a>Tipo di dati

**UINT32**

## <a name="remarks"></a>Commenti

Il comportamento predefinito del sink multimediale mpeg4 è scrivere 'moov' dopo la casella 'mdat'. Se si imposta questo attributo, il file generato scriverà 'moov' prima della casella 'mdat'.

Perché il sink mpeg4 usi questo attributo, il flusso di byte passato non deve essere lento o remoto per .

Questa funzionalità comporta un'ulteriore copia/remuxing dei file.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Windows 8 app desktop \| app UWP\]<br/>                                  |
| Server minimo supportato<br/> | \[Windows Server 2012 app desktop \| app UWP\]<br/>                        |
| Intestazione<br/>                   | <dl> <dt>Mfidl.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Elenco alfabetico di Media Foundation attributi](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[Attributi del tipo di supporto](media-type-attributes.md)
</dt> </dl>

 

 




