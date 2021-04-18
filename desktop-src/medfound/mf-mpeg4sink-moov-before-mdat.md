---
description: Indica che Moov verrà scritto prima della casella mdat nel file generato.
ms.assetid: 97B68B0A-8266-4FCF-8CD9-35890E1AC774
title: Attributo MF_MPEG4SINK_MOOV_BEFORE_MDAT (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5b5d345dc027c457ceb6123ce3854fff4b74f987
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106313052"
---
# <a name="mf_mpeg4sink_moov_before_mdat-attribute"></a>MF \_ MPEG4SINK \_ Moov \_ prima dell' \_ attributo mdat

Indica che "Moov" verrà scritto prima della casella "mdat" nel file generato.

## <a name="data-type"></a>Tipo di dati

**UINT32**

## <a name="remarks"></a>Commenti

Il comportamento predefinito del sink multimediale MPEG4 consiste nel scrivere ' Moov ' dopo ' mdat ' box. Se si imposta questo attributo, il file generato scriverà' Moov ' prima della casella ' mdat '.

Affinché il sink MPEG4 usi questo attributo, il flusso di byte passato non deve essere una ricerca lenta o remota per.

Questa funzionalità prevede un file di copia/remuxing aggiuntivo.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | App desktop di Windows 8 app \[ \| UWP\]<br/>                                  |
| Server minimo supportato<br/> | App UWP per \[ app desktop di Windows Server 2012 \|\]<br/>                        |
| Intestazione<br/>                   | <dl> <dt>Mfidl. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Elenco alfabetico degli attributi di Media Foundation](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[Attributi del tipo di supporto](media-type-attributes.md)
</dt> </dl>

 

 




