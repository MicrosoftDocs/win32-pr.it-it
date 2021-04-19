---
description: Il \_ \_ tipo di enumerazione dei tipi di dispositivi WPD descrive i diversi tipi di dispositivi portatili Windows (WPD) usati comunemente per determinare la classificazione di base e l'aspetto visivo di un dispositivo portatile.
ms.assetid: 51714e0f-e9b7-4474-a8bb-da3875ef5399
title: Enumerazione WPD_DEVICE_TYPES (PortableDevice. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WPD_DEVICE_TYPES
api_type:
- HeaderDef
api_location:
- PortableDevice.h
ms.openlocfilehash: 3e71acf200a95bba05b7298a5824bfa353e4a90b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106324206"
---
# <a name="wpd_device_types-enumeration"></a>Enumerazione dei tipi di \_ dispositivi WPD \_

Il tipo di enumerazione dei **\_ \_ tipi di dispositivi WPD** descrive i diversi tipi di dispositivi portatili Windows (WPD) usati comunemente per determinare la classificazione di base e l'aspetto visivo di un dispositivo portatile.

## <a name="syntax"></a>Sintassi


```C++
typedef enum tagWPD_DEVICE_TYPES { 
  WPD_DEVICE_TYPE_GENERIC                       = 0,
  WPD_DEVICE_TYPE_CAMERA                        = 1,
  WPD_DEVICE_TYPE_MEDIA_PLAYER                  = 2,
  WPD_DEVICE_TYPE_PHONE                         = 3,
  WPD_DEVICE_TYPE_VIDEO                         = 4,
  WPD_DEVICE_TYPE_PERSONAL_INFORMATION_MANAGER  = 5,
  WPD_DEVICE_TYPE_AUDIO_RECORDER                = 6
} WPD_DEVICE_TYPES;
```



## <a name="constants"></a>Costanti

<dl> <dt>

<span id="WPD_DEVICE_TYPE_GENERIC"></span><span id="wpd_device_type_generic"></span>**\_tipo di dispositivo WPD \_ \_ generico**
</dt> <dd>

WPD generico che include dispositivi multifunzione che non rientrano in uno degli altri valori di enumerazione dei [**\_ \_ tipi di dispositivo WPD**](wpd-device-types.md) .

</dd> <dt>

<span id="WPD_DEVICE_TYPE_CAMERA"></span><span id="wpd_device_type_camera"></span>**\_fotocamera del \_ tipo di dispositivo WPD \_**
</dt> <dd>

Un dispositivo della fotocamera, ad esempio una fotocamera digitale ancora.

</dd> <dt>

<span id="WPD_DEVICE_TYPE_MEDIA_PLAYER"></span><span id="wpd_device_type_media_player"></span>**\_ \_ \_ media \_ Player tipo di dispositivo WPD**
</dt> <dd>

Dispositivo multimediale che supporta la riproduzione di immagini audio, video o di visualizzazione, ad esempio un lettore musicale portatile o un Media Center portatile. Non tutte queste funzioni sono classificate come un tipo di \_ dispositivo \_ WPD \_ media \_ Player. I dispositivi portatili Music Player, ad esempio, vengono classificati come \_ tipo di dispositivo WPD \_ \_ media \_ Player.

</dd> <dt>

<span id="WPD_DEVICE_TYPE_PHONE"></span><span id="wpd_device_type_phone"></span>**\_ \_ telefono tipo di dispositivo WPD \_**
</dt> <dd>

Un dispositivo telefonico, ad esempio un telefono cellulare.

</dd> <dt>

<span id="WPD_DEVICE_TYPE_VIDEO"></span><span id="wpd_device_type_video"></span>**\_video del \_ tipo di dispositivo WPD \_**
</dt> <dd>

Un dispositivo video.

</dd> <dt>

<span id="WPD_DEVICE_TYPE_PERSONAL_INFORMATION_MANAGER"></span><span id="wpd_device_type_personal_information_manager"></span>**\_ \_ \_ \_ Gestione informazioni personali del tipo di dispositivo WPD \_**
</dt> <dd>

Un dispositivo Personal Information Manager.

</dd> <dt>

<span id="WPD_DEVICE_TYPE_AUDIO_RECORDER"></span><span id="wpd_device_type_audio_recorder"></span>**\_ \_ registratore audio del tipo di dispositivo \_ WPD \_**
</dt> <dd>

Un dispositivo registratore audio.

</dd> </dl>

## <a name="remarks"></a>Commenti

**WPD \_ I \_ tipi di dispositivo** vengono letti usando l'interfaccia [**IPortableDeviceManager**](/windows/desktop/api/PortableDeviceApi/nn-portabledeviceapi-iportabledevicemanager) . Le applicazioni WPD possono usare questi valori per determinare l'aspetto visivo generico del dispositivo. Ovvero viene visualizzata un'immagine della fotocamera per i dispositivi di tipo fotocamera, viene visualizzata un'immagine del telefono cellulare per i dispositivi simili al telefono e così via.

> [!Note]  
> Le applicazioni WPD devono usare le funzionalità del dispositivo portatile per determinare la funzione, non il valore dei **\_ \_ tipi di dispositivo WPD** .

 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------|---------------------------------------------------------------------------------------------|
| Intestazione<br/> | <dl> <dt>PortableDevice. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Strutture e tipi di enumerazione**](structures-and-enumeration-types.md)
</dt> </dl>

 

 




