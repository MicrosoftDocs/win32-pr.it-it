---
description: Il tipo di enumerazione WPD DEVICE TYPES descrive i diversi tipi \_ di Windows Portable Device (WPD) comunemente usati per determinare la classificazione di base e l'aspetto visivo di \_ un dispositivo portatile.
ms.assetid: 51714e0f-e9b7-4474-a8bb-da3875ef5399
title: WPD_DEVICE_TYPES enumerazione (PortableDevice.h)
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
ms.openlocfilehash: 747c4631bc2c24a6550904e36e58a6fc02547bc010da7fa1d08b896c6c17489c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119657461"
---
# <a name="wpd_device_types-enumeration"></a>Enumerazione WPD \_ DEVICE \_ TYPES

Il tipo di enumerazione **WPD \_ DEVICE \_ TYPES** descrive i diversi tipi di Windows Portable Device (WPD) comunemente usati per determinare la classificazione di base e l'aspetto visivo di un dispositivo portatile.

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

<span id="WPD_DEVICE_TYPE_GENERIC"></span><span id="wpd_device_type_generic"></span>**TIPO DI DISPOSITIVO WPD \_ \_ \_ GENERICO**
</dt> <dd>

WPD generico che include dispositivi multifunzione che non rientrano in uno degli altri valori di enumerazione [**DEVICE \_ \_ TYPES WPD.**](wpd-device-types.md)

</dd> <dt>

<span id="WPD_DEVICE_TYPE_CAMERA"></span><span id="wpd_device_type_camera"></span>**FOTOCAMERA CON TIPO DI DISPOSITIVO WPD \_ \_ \_**
</dt> <dd>

Un dispositivo fotocamera, ad esempio una fotocamera digitale.

</dd> <dt>

<span id="WPD_DEVICE_TYPE_MEDIA_PLAYER"></span><span id="wpd_device_type_media_player"></span>**LETTORE \_ MULTIMEDIALE \_ DI TIPO \_ DISPOSITIVO \_ WPD**
</dt> <dd>

Dispositivo lettore multimediale che supporta la riproduzione di immagini audio, video o di visualizzazione, ad esempio un lettore musicale portatile o un media center portatile. Non tutto questo funzionalmente è classificato come LETTORE MULTIMEDIALE TIPO \_ DI DISPOSITIVO WPD. \_ \_ \_ Ad esempio, i dispositivi lettore di musica portatile sono classificati come WPD \_ DEVICE \_ TYPE MEDIA \_ \_ PLAYER.

</dd> <dt>

<span id="WPD_DEVICE_TYPE_PHONE"></span><span id="wpd_device_type_phone"></span>**TELEFONO CON TIPO DI DISPOSITIVO WPD \_ \_ \_**
</dt> <dd>

Un dispositivo telefonico, ad esempio un telefono cellulare.

</dd> <dt>

<span id="WPD_DEVICE_TYPE_VIDEO"></span><span id="wpd_device_type_video"></span>**VIDEO SUL TIPO DI DISPOSITIVO WPD \_ \_ \_**
</dt> <dd>

Un dispositivo video.

</dd> <dt>

<span id="WPD_DEVICE_TYPE_PERSONAL_INFORMATION_MANAGER"></span><span id="wpd_device_type_personal_information_manager"></span>**TIPO DI DISPOSITIVO WPD \_ \_ PERSONAL INFORMATION \_ \_ \_ MANAGER**
</dt> <dd>

Un dispositivo di gestione delle informazioni personali.

</dd> <dt>

<span id="WPD_DEVICE_TYPE_AUDIO_RECORDER"></span><span id="wpd_device_type_audio_recorder"></span>**REGISTRATORE \_ AUDIO DI TIPO DISPOSITIVO \_ \_ \_ WPD**
</dt> <dd>

Un dispositivo di registrazione audio.

</dd> </dl>

## <a name="remarks"></a>Commenti

**WPD \_ I \_ TIPI DI** DISPOSITIVO vengono letti tramite [**l'interfaccia IPortableDeviceManager.**](/windows/desktop/api/PortableDeviceApi/nn-portabledeviceapi-iportabledevicemanager) Le applicazioni WPD possono usare questi valori per determinare l'aspetto visivo generico del dispositivo. In altri, viene visualizzata un'immagine della fotocamera per i dispositivi simili a una fotocamera, un'immagine del telefono cellulare viene visualizzata per i dispositivi simili al telefono e così via.

> [!Note]  
> Le applicazioni WPD devono usare le funzionalità del dispositivo portatile per determinare funzionalmente, non il **valore WPD \_ DEVICE \_ TYPES.**

 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------|---------------------------------------------------------------------------------------------|
| Intestazione<br/> | <dl> <dt>PortableDevice.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Strutture e tipi di enumerazione**](structures-and-enumeration-types.md)
</dt> </dl>

 

 




