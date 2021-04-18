---
description: Contiene i tipi di output registrati per una trasformazione Media Foundation (MFT).
ms.assetid: 925267a2-4421-4874-a8a2-437876c729f1
title: Attributo MFT_OUTPUT_TYPES_Attributes (Mftransform. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 991b94b52782eb631846ee1ce182b4676a3cfd2f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106309075"
---
# <a name="mft_output_types_attributes-attribute"></a>\_ \_ Attributo attributi tipi di output MFT \_

Contiene i tipi di output registrati per una trasformazione Media Foundation (MFT).

## <a name="data-type"></a>Tipo di dati

**MFT \_ Registra \_ \_ informazioni \[ sul \] tipo** archiviate come **byte \[ \]**

## <a name="remarks"></a>Commenti

Questo attributo viene impostato sui puntatori [**IMFActivate**](/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate) restituiti dalla funzione [**MFTEnumEx**](/windows/desktop/api/mfapi/nf-mfapi-mftenumex) .

Questo attributo contiene una matrice di strutture di [**\_ informazioni sul \_ tipo \_ di registro MFT**](/windows/win32/api/mfobjects/ns-mfobjects-mft_register_type_info) che descrivono uno o più formati di output supportati da MFT. Questi valori vengono ricavati dal registro di sistema e sono intesi come hint per l'applicazione. Il MFT potrebbe supportare formati aggiuntivi. Per impostare il formato di output effettivo, è necessario creare il MFT e chiamare [**IMFTransform:: SetOutputType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-setoutputtype).

La costante GUID per questo attributo viene esportata da mfuuid. lib.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | App desktop di Windows 7 \[ \| UWP\]<br/>                                        |
| Server minimo supportato<br/> | App desktop di Windows Server 2008 R2 \[ \| UWP\]<br/>                           |
| Intestazione<br/>                   | <dl> <dt>Mftransform. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Elenco alfabetico degli attributi di Media Foundation](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[Attributi di trasformazione](transform-attributes.md)
</dt> </dl>

 

 




