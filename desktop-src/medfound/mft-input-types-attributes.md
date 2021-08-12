---
description: Contiene i tipi di input registrati per una trasformazione Media Foundation (MFT).
ms.assetid: 0fb1d9f2-2b57-41bc-8365-0b88bd5a2f3d
title: MFT_INPUT_TYPES_Attributes attributo (Mftransform.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2a750094361cdaa877bff82e20a74c1beae4e1a1f76ea0a9ad5be83f308c1f2d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118240236"
---
# <a name="mft_input_types_attributes-attribute"></a>Attributo MFT \_ INPUT \_ TYPES \_ Attributes

Contiene i tipi di input registrati per una trasformazione Media Foundation (MFT).

## <a name="data-type"></a>Tipo di dati

**MFT \_ REGISTER \_ TYPE \_ INFO \[ \] archiviato** come **BYTE \[ \]**

## <a name="getset"></a>Ottenere/impostare

Per ottenere questo attributo, chiamare [**IMFAttributes::GetBlob**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getblob).

Per impostare questo attributo, chiamare [**IMFAttributes::SetBlob**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setblob).

## <a name="remarks"></a>Commenti

Questo attributo viene impostato sui [**puntatori IMFActivate**](/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate) restituiti dalla [**funzione MFTEnumEx.**](/windows/desktop/api/mfapi/nf-mfapi-mftenumex)

Questo attributo contiene una matrice di [**strutture MFT \_ REGISTER TYPE \_ \_ INFO**](/windows/win32/api/mfobjects/ns-mfobjects-mft_register_type_info) che descrivono uno o più formati di input supportati da MFT. Questi valori vengono presi dal Registro di sistema e sono destinati all'applicazione come suggerimento. MFT potrebbe supportare formati aggiuntivi. Per impostare il formato di input effettivo, è necessario creare MFT e chiamare [**IMFTransform::SetInputType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-setinputtype).

La costante GUID per questo attributo viene esportata da mfuuid.lib.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 7 \[ app desktop app \| UWP\]<br/>                                        |
| Server minimo supportato<br/> | Windows App UWP per app desktop server 2008 R2 \[ \|\]<br/>                           |
| Intestazione<br/>                   | <dl> <dt>Mftransform.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Elenco alfabetico di Media Foundation attributi](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[Attributi di trasformazione](transform-attributes.md)
</dt> </dl>

 

 




