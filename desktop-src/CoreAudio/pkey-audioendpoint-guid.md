---
description: La \_ Proprietà pkey AudioEndpoint \_ GUID fornisce l'identificatore di dispositivo DirectSound che corrisponde al dispositivo dell'endpoint audio.
ms.assetid: d3119504-9b6a-47b8-b3c6-15cb329929cb
title: PKEY_AudioEndpoint_GUID (mmdeviceapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 45405cd2350777e535b50859e77aa56755d191fc
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106305150"
---
# <a name="pkey_audioendpoint_guid"></a>\_GUID AUDIOENDPOINT \_ pkey

La proprietà **pkey \_ AudioEndpoint \_ GUID** fornisce l'identificatore di dispositivo DirectSound che corrisponde al dispositivo dell'endpoint audio. Il valore della proprietà è un GUID che il client può fornire come identificatore del dispositivo alla funzione **DirectSoundCreate** o **DirectSoundCaptureCreate** nell'API DirectSound. Questo valore identifica in modo univoco il dispositivo dell'endpoint audio in tutti i dispositivi dell'endpoint audio nel sistema. Per ulteriori informazioni su DirectSound, vedere la documentazione di DirectX SDK.

Il membro **VT** della struttura **PROPVARIANT** è impostato su VT \_ LPWSTR.

Il membro **pwszVal** della struttura **PROPVARIANT** punta a una stringa di caratteri wide con terminazione null contenente un GUID che identifica il dispositivo dell'endpoint audio in DirectSound.

Come spiegato in precedenza, l' [API MMDevice](mmdevice-api.md) supporta i [ruoli del dispositivo](device-roles.md). Sebbene DirectSound non supporti direttamente i ruoli del dispositivo, un client DirectSound può utilizzare la \_ Proprietà pkey AudioEndpoint \_ GUID per selezionare un dispositivo di rendering o acquisizione DirectSound basato sul relativo ruolo del dispositivo.

Ad esempio, un'applicazione DirectSound esegue i passaggi seguenti per creare un dispositivo DirectSound che corrisponde al dispositivo dell'endpoint di rendering a cui l'utente ha assegnato il ruolo eMultimedia:

1.  Chiamare il metodo [**IMMDeviceEnumerator:: GetDefaultAudioEndpoint**](/windows/desktop/api/Mmdeviceapi/nf-mmdeviceapi-immdeviceenumerator-getdefaultaudioendpoint) per ottenere l'interfaccia [**IMMDevice**](/windows/desktop/api/Mmdeviceapi/nn-mmdeviceapi-immdevice) del dispositivo dell'endpoint di rendering con il ruolo eMultimedia.
2.  Chiamare il metodo [**IMMDevice:: OpenPropertyStore**](/windows/desktop/api/Mmdeviceapi/nf-mmdeviceapi-immdevice-openpropertystore) per ottenere l'interfaccia **IPropertyStore** del dispositivo eMultimedia. Per ulteriori informazioni su **IPropertyStore**, vedere la documentazione Windows SDK.
3.  Chiamare il metodo **IPropertyStore:: GetValue** per ottenere il \_ valore della proprietà pkey AudioEndpoint \_ GUID.
4.  Converte il valore della proprietà da un GUID in formato stringa a una struttura GUID a 16 byte.
5.  Chiamare la funzione **DirectSoundCreate** con il GUID per creare il dispositivo con il ruolo eMultimedia.

> [!Note]  
> **Pkey \_ Il \_ GUID AudioEndpoint** è una proprietà di sola lettura indipendentemente dalla modalità di accesso all'archiviazione richiesta dall'applicazione in [**IMMDevice:: OpenPropertyStore**](/windows/desktop/api/Mmdeviceapi/nf-mmdeviceapi-immdevice-openpropertystore). Se un'applicazione tenta di impostare un valore utilizzando **IPropertyStore:: SetValue**, questa chiamata ha esito negativo con il \_ codice di errore E AccessDenied.

 

Si noti che il GUID a 16 byte generato nel passaggio 4 corrisponde al GUID del dispositivo che identifica il dispositivo durante l'enumerazione del dispositivo DirectSound. La funzione **DirectSoundEnumerate** enumera i dispositivi endpoint di rendering e la funzione **DirectSoundCaptureEnumerate** enumera i dispositivi dell'endpoint di acquisizione. In entrambi i casi, il GUID del dispositivo è il primo parametro passato alla funzione di callback di enumerazione. Per ulteriori informazioni sull'enumerazione DirectSound, vedere la documentazione di DirectX SDK.

Per un esempio di codice che usa la \_ proprietà GUID AudioEndpoint di pkey \_ , vedere [ruoli del dispositivo per le applicazioni DirectSound](device-roles-for-directsound-applications.md).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                           |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2008\]<br/>                                     |
| Intestazione<br/>                   | <dl> <dt>Mmdeviceapi. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Proprietà endpoint audio**](audio-endpoint-properties.md)
</dt> <dt>

[Proprietà audio principali](core-audio-properties.md)
</dt> </dl>

 

 




