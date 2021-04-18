---
description: Specifica se una trasformazione Media Foundation (MFT) supporta le modifiche al formato dinamico.
ms.assetid: 64d32c78-8bee-4d3c-a770-5a097cb71b13
title: Attributo MFT_SUPPORT_DYNAMIC_FORMAT_CHANGE (Mfapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d8224e9b7f0f05f430afac464e61900c7ce879fd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106310209"
---
# <a name="mft_support_dynamic_format_change-attribute"></a>L' \_ \_ attributo di \_ modifica del formato dinamico del supporto MFT \_

Specifica se una trasformazione Media Foundation (MFT) supporta le modifiche al formato dinamico.

## <a name="data-type"></a>Tipo di dati

**UINT32**

Considera come valore booleano.

## <a name="remarks"></a>Commenti

Questo attributo può avere i valori seguenti.



| Valore     | Descrizione                                                            |
|-----------|------------------------------------------------------------------------|
| **TRUE**  | Il client può modificare il formato di input durante il flusso.               |
| **FALSE** | Il MFT deve essere svuotato prima che il client possa modificare il formato di input. |



 

Per ottenere questo attributo, chiamare prima [**IMFTransform:: GetAttributes**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getattributes) per ottenere l'archivio di attributi globale per MFT. Chiamare quindi [**IMFAttributes:: GetUInt32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32) per ottenere il valore dell'attributo.

Se [**GetAttributes**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getattributes) ha esito negativo o se l'attributo non è presente, il valore predefinito è **false**.

[MFTS asincrono](asynchronous-mfts.md) deve restituire il valore **true**.

Per ulteriori informazioni, vedere [gestione delle modifiche al flusso](handling-stream-changes.md).

La costante GUID per questo attributo viene esportata da mfuuid. lib.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | App desktop di Windows Vista app \[ \| UWP\]<br/>                              |
| Server minimo supportato<br/> | App UWP per \[ app desktop di Windows Server 2008 \|\]<br/>                        |
| Intestazione<br/>                   | <dl> <dt>Mfapi. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Elenco alfabetico degli attributi di Media Foundation](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[MFTs asincrono](asynchronous-mfts.md)
</dt> <dt>

[Attributi di trasformazione](transform-attributes.md)
</dt> <dt>

[**IMFAttributes:: GetUInt32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32)
</dt> <dt>

[**IMFAttributes:: seuint32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)
</dt> <dt>

[**IMFTransform**](/windows/desktop/api/mftransform/nn-mftransform-imftransform)
</dt> </dl>

 

 




