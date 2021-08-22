---
description: Contiene i tipi di output registrati per una trasformazione Media Foundation (MFT).
ms.assetid: 925267a2-4421-4874-a8a2-437876c729f1
title: MFT_OUTPUT_TYPES_Attributes attributo (Mftransform.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2699d244bc5184652d0ba1d89ebf4e1beaddb472bb1d6fa09c05d1edf99030fa
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119462781"
---
# <a name="mft_output_types_attributes-attribute"></a>Attributo MFT \_ OUTPUT \_ TYPES \_

Contiene i tipi di output registrati per una trasformazione Media Foundation (MFT).

## <a name="data-type"></a>Tipo di dati

**MFT \_ REGISTER \_ TYPE \_ INFO \[ \] archiviato** come **BYTE \[ \]**

## <a name="remarks"></a>Commenti

Questo attributo viene impostato sui [**puntatori IMFActivate**](/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate) restituiti dalla [**funzione MFTEnumEx.**](/windows/desktop/api/mfapi/nf-mfapi-mftenumex)

Questo attributo contiene una matrice di [**strutture MFT \_ REGISTER TYPE \_ \_ INFO**](/windows/win32/api/mfobjects/ns-mfobjects-mft_register_type_info) che descrivono uno o più formati di output supportati da MFT. Questi valori vengono prelevati dal Registro di sistema e sono da intendersi come suggerimento per l'applicazione. MFT potrebbe supportare formati aggiuntivi. Per impostare il formato di output effettivo, è necessario creare il MFT e chiamare [**IMFTransform::SetOutputType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-setoutputtype).

La costante GUID per questo attributo viene esportata da mfuuid.lib.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 7 \[ app desktop app \| UWP\]<br/>                                        |
| Server minimo supportato<br/> | Windows App desktop di Server 2008 R2 \[ \| app UWP\]<br/>                           |
| Intestazione<br/>                   | <dl> <dt>Mftransform.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Elenco alfabetico degli Media Foundation personalizzati](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[Attributi di trasformazione](transform-attributes.md)
</dt> </dl>

 

 




