---
description: La proprietà \_ PKEY AudioEndpoint GUID fornisce \_ l'identificatore di dispositivo DirectSound che corrisponde al dispositivo endpoint audio.
ms.assetid: d3119504-9b6a-47b8-b3c6-15cb329929cb
title: PKEY_AudioEndpoint_GUID (Mmdeviceapi.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 357531a76316381e9ae39f867a5b6cfa0a055a04f41b0cba5fab95fcccbcc7fb
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120104361"
---
# <a name="pkey_audioendpoint_guid"></a>PKEY \_ AudioEndpoint \_ GUID

La **proprietà \_ PKEY AudioEndpoint \_ GUID** fornisce l'identificatore di dispositivo DirectSound che corrisponde al dispositivo endpoint audio. Il valore della proprietà è un GUID che il client può fornire come identificatore di dispositivo alla funzione **DirectSoundCreate** o **DirectSoundCaptureCreate** nell'API DirectSound. Questo valore identifica in modo univoco il dispositivo endpoint audio in tutti i dispositivi endpoint audio nel sistema. Per altre informazioni su DirectSound, vedere la documentazione di DirectX SDK.

Il **membro vt** della **struttura PROPVARIANT** è impostato su VT \_ LPWSTR.

Il **membro pwszVal** della struttura **PROPVARIANT** punta a una stringa di caratteri wide con terminazione Null che contiene un GUID che identifica il dispositivo endpoint audio in DirectSound.

Come illustrato in precedenza, [l'API MMDevice](mmdevice-api.md) supporta i [ruoli del dispositivo](device-roles.md). Anche se DirectSound non supporta direttamente i ruoli dispositivo, un client DirectSound può usare la proprietà PKEY AudioEndpoint GUID per selezionare un dispositivo di rendering o acquisizione \_ DirectSound in base al ruolo del \_ dispositivo.

Ad esempio, un'applicazione DirectSound esegue la procedura seguente per creare un dispositivo DirectSound corrispondente al dispositivo endpoint di rendering a cui l'utente ha assegnato il ruolo eMultimedia:

1.  Chiamare il [**metodo IMMDeviceEnumerator::GetDefaultAudioEndpoint**](/windows/desktop/api/Mmdeviceapi/nf-mmdeviceapi-immdeviceenumerator-getdefaultaudioendpoint) per ottenere l'interfaccia [**IMMDevice**](/windows/desktop/api/Mmdeviceapi/nn-mmdeviceapi-immdevice) del dispositivo endpoint di rendering con il ruolo eMultimedia.
2.  Chiamare il [**metodo IMMDevice::OpenPropertyStore**](/windows/desktop/api/Mmdeviceapi/nf-mmdeviceapi-immdevice-openpropertystore) per ottenere **l'interfaccia IPropertyStore** del dispositivo eMultimedia. Per altre informazioni su **IPropertyStore,** vedere la documentazione Windows SDK.
3.  Chiamare il **metodo IPropertyStore::GetValue** per ottenere il valore della proprietà \_ GUID AudioEndpoint \_ PKEY.
4.  Convertire il valore della proprietà da un GUID in formato stringa a una struttura GUID a 16 byte.
5.  Chiamare la **funzione DirectSoundCreate** con il GUID per creare il dispositivo con il ruolo eMultimedia.

> [!Note]  
> **Chiave PKEY \_ Il \_ GUID AudioEndpoint** è una proprietà di sola lettura indipendentemente dalla modalità di accesso alle risorse di archiviazione richiesta dall'applicazione in [**IMMDevice::OpenPropertyStore.**](/windows/desktop/api/Mmdeviceapi/nf-mmdeviceapi-immdevice-openpropertystore) Se un'applicazione tenta di impostare un valore usando **IPropertyStore::SetValue,** questa chiamata non riesce con il codice di errore E \_ ACCESSDENIED.

 

Si noti che il GUID a 16 byte generato nel passaggio 4 corrisponde al GUID del dispositivo che identifica il dispositivo durante l'enumerazione del dispositivo DirectSound. La **funzione DirectSoundEnumerate** enumera i dispositivi endpoint di rendering e la **funzione DirectSoundCaptureEnumerate** enumera i dispositivi endpoint di acquisizione. In entrambi i casi, il GUID del dispositivo è il primo parametro passato alla funzione di callback di enumerazione. Per altre informazioni sull'enumerazione DirectSound, vedere la documentazione di DirectX SDK.

Per un esempio di codice che usa la proprietà \_ PKEY AudioEndpoint GUID, vedere Ruoli del dispositivo \_ per applicazioni [DirectSound.](device-roles-for-directsound-applications.md)

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop Vista\]<br/>                                           |
| Server minimo supportato<br/> | Windows Solo app desktop di Server 2008 \[\]<br/>                                     |
| Intestazione<br/>                   | <dl> <dt>Mmdeviceapi.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Proprietà dell'endpoint audio**](audio-endpoint-properties.md)
</dt> <dt>

[Proprietà audio principali](core-audio-properties.md)
</dt> </dl>

 

 




