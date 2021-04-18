---
description: Specifica se un flusso si escludono a vicenda con altri flussi dello stesso tipo.
ms.assetid: 00a426ae-297c-4fcb-8132-d9c538bc9f1a
title: Attributo MF_SD_MUTUALLY_EXCLUSIVE (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 24e3604eb9424bb646766f57261f745c57e18f3e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106315014"
---
# <a name="mf_sd_mutually_exclusive-attribute"></a>Attributo che si \_ \_ escludono a vicenda MF SD \_

Specifica se un flusso si escludono a vicenda con altri flussi dello stesso tipo.

## <a name="data-type"></a>Tipo di dati

**UINT32**

## <a name="getset"></a>Ottenere/impostare

Per ottenere questo attributo, chiamare [**IMFAttributes:: GetUInt32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).

Per impostare questo attributo, chiamare [**IMFAttributes::**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)SetAttribute.

## <a name="applies-to"></a>Si applica a

[**IMFStreamDescriptor**](/windows/desktop/api/mfidl/nn-mfidl-imfstreamdescriptor)

## <a name="remarks"></a>Commenti

Se questo attributo è **true** (diverso da zero), il flusso si escludono a vicenda con altri flussi dello stesso tipo, ad esempio audio o video, all'interno della stessa presentazione. Se, ad esempio, un file AVI contiene più flussi audio, viene contrassegnato come si escludono a vicenda, perché deve essere riprodotto un solo flusso audio alla volta.

Il valore predefinito è **false**.

> [!Note]  
> Questo attributo non viene usato per i file di formato Advanced Systems (ASF), che hanno un modo più sofisticato per rappresentare i criteri di esclusione reciproca. Per ulteriori informazioni, vedere [**IMFASFMutualExclusion**](/windows/desktop/api/wmcontainer/nn-wmcontainer-imfasfmutualexclusion).

 

La costante GUID per questo attributo viene esportata da mfuuid. lib.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | App desktop di Windows 7 \[ \| UWP\]<br/>                                  |
| Server minimo supportato<br/> | App desktop di Windows Server 2008 R2 \[ \| UWP\]<br/>                     |
| Intestazione<br/>                   | <dl> <dt>Mfidl. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Elenco alfabetico degli attributi di Media Foundation](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[Attributi del descrittore di flusso](stream-descriptor-attributes.md)
</dt> </dl>

 

 




