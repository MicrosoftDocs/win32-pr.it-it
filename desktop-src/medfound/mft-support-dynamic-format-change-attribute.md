---
description: Specifica se una trasformazione Media Foundation (MFT) supporta le modifiche di formato dinamico.
ms.assetid: 64d32c78-8bee-4d3c-a770-5a097cb71b13
title: MFT_SUPPORT_DYNAMIC_FORMAT_CHANGE attributo (Mfapi.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3286d9bfd2185006975cf128cc60f2b774eba6ba74229b3e290c743c4cde3930
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120012611"
---
# <a name="mft_support_dynamic_format_change-attribute"></a>Attributo MFT \_ SUPPORT \_ DYNAMIC FORMAT \_ \_ CHANGE

Specifica se una trasformazione Media Foundation (MFT) supporta le modifiche di formato dinamico.

## <a name="data-type"></a>Tipo di dati

**UINT32**

Considera come valore booleano.

## <a name="remarks"></a>Commenti

Questo attributo può avere i valori seguenti.



| Valore     | Descrizione                                                            |
|-----------|------------------------------------------------------------------------|
| **TRUE**  | Il client può modificare il formato di input durante il flusso.               |
| **FALSE** | Il MFT deve essere svuotato prima che il client possa modificare il formato di input. |



 

Per ottenere questo attributo, chiamare prima [**IMFTransform::GetAttributes**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getattributes) per ottenere l'archivio attributi globale per MFT. Chiamare quindi [**IMFAttributes::GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32) per ottenere il valore dell'attributo.

Se [**GetAttributes ha**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getattributes) esito negativo o l'attributo non è presente, il valore predefinito è **FALSE.**

[I MFT asincroni](asynchronous-mfts.md) devono restituire il **valore TRUE.**

Per altre informazioni, vedere [Gestione delle modifiche ai flussi.](handling-stream-changes.md)

La costante GUID per questo attributo viene esportata da mfuuid.lib.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows App desktop vista \[ \| app UWP\]<br/>                              |
| Server minimo supportato<br/> | Windows App desktop di Server 2008 \[ \| app UWP\]<br/>                        |
| Intestazione<br/>                   | <dl> <dt>Mfapi.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Elenco alfabetico degli Media Foundation personalizzati](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[MFT asincroni](asynchronous-mfts.md)
</dt> <dt>

[Attributi di trasformazione](transform-attributes.md)
</dt> <dt>

[**IMFAttributes::GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32)
</dt> <dt>

[**IMFAttributes::SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)
</dt> <dt>

[**IMFTransform**](/windows/desktop/api/mftransform/nn-mftransform-imftransform)
</dt> </dl>

 

 




