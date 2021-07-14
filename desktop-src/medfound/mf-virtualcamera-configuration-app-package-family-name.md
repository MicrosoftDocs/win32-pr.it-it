---
description: Specifica il nome della famiglia di pacchetti dell'app per un'applicazione di configurazione della fotocamera virtuale.
title: MF_VIRTUALCAMERA_APP_PACKAGE_FAMILY_NAME attributo (Mfapi.h)
ms.topic: reference
ms.date: 05/24/2021
ms.openlocfilehash: e821a273c44b1d5c9e654e34bbfb928ea707cdc0
ms.sourcegitcommit: 63c93e0ad0b48d60b11008767196718feb475cb0
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 07/13/2021
ms.locfileid: "113691858"
---
# <a name="mf_virtualcamera_app_package_family_name-attribute"></a>Attributo \_ MF VIRTUALCAMERA \_ APP \_ PACKAGE FAMILY \_ \_ NAME

Specifica il nome della famiglia di pacchetti dell'app per un'applicazione di configurazione della fotocamera virtuale. Se disponibile, la pipeline associa l'applicazione di configurazione alla fotocamera virtuale e fornisce un punto di lancio all'interno della pagina Impostazioni fotocamera.

## <a name="data-type"></a>Tipo di dati

[MF_ATTRIBUTE_STRING](/windows/win32/api/mfobjects/ne-mfobjects-mf_attribute_type)

## <a name="remarks"></a>Commenti

Questo attributo può essere esposto dall'origine multimediale personalizzata della fotocamera virtuale dall'archivio attributi di origine multimediale [IMFMediaSourceEx::GetSourceAttributes](/windows/win32/api/mfvirtualcamera/nf-mfvirtualcamera-imfvirtualcamera-getmediasource).  

Se l'applicazione di configurazione non è ancora installata nel computer, l'applicazione Store verrà avviata e passa alla pagina dell'applicazione specificata dal nome della famiglia di pacchetti. In caso contrario, l'applicazione installata verrà avviata per l'utente.


## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Build 22000<br/>                          |
| Server minimo supportato<br/> | Windows Build 22000<br/>                      |
| Intestazione<br/>                   | <dl> <dt>Mfapi.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Elenco alfabetico di Media Foundation attributi](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[**IMFAttributes::GetString**](/windows/win32/api/mfobjects/nf-mfobjects-imfattributes-getstring)
</dt> <dt>

[**IMFAttributes::SetString**](/windows/win32/api/mfobjects/nf-mfobjects-imfattributes-setstring)
</dt> 
</dl>
 




