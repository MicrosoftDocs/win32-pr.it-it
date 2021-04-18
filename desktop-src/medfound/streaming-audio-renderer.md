---
description: Il renderer di streaming audio (SAR) è un sink multimediale che esegue il rendering dell'audio.
ms.assetid: 5884a128-597d-432b-a706-e10c894d7965
title: Renderer audio di streaming
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f59c5b55f197d5e9770c6f1be55f680c7f9136f3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106308989"
---
# <a name="streaming-audio-renderer"></a>Renderer audio di streaming

Il renderer di streaming audio (SAR) è un sink multimediale che esegue il rendering dell'audio. Ogni istanza del SAR esegue il rendering di un singolo flusso audio. Per eseguire il rendering di più flussi, usare più istanze del SAR.

Per creare il SAR, chiamare una delle funzioni seguenti:

-   [**MFCreateAudioRenderer**](/windows/desktop/api/mfidl/nf-mfidl-mfcreateaudiorenderer). Restituisce un puntatore a SAR.
-   [**MFCreateAudioRendererActivate**](/windows/desktop/api/mfidl/nf-mfidl-mfcreateaudiorendereractivate). Restituisce un puntatore a un oggetto Activation, che può essere usato per creare il SAR.

La seconda funzione, che restituisce un oggetto Activation, è obbligatoria se si sta riproducendo contenuto protetto, perché l'oggetto di attivazione deve essere serializzato nel processo protetto. Per il contenuto non crittografato, è possibile usare una delle due funzioni.

Il SAR può ricevere audio non compresso in formato PCM o IEEE a virgola mobile. Se la velocità di riproduzione è più veloce o più lenta di 1 ×, il valore di SAR regola automaticamente il passo.

## <a name="configuring-the-audio-renderer"></a>Configurazione del renderer audio

Il SAR supporta diversi attributi di configurazione. Il meccanismo per l'impostazione di questi attributi dipende dalla funzione chiamata per creare il SAR. Se si usa la funzione [**MFCreateAudioRenderer**](/windows/desktop/api/mfidl/nf-mfidl-mfcreateaudiorenderer) , eseguire le operazioni seguenti:

1.  Creare un nuovo archivio di attributi chiamando [**MFCreateAttributes**](/windows/desktop/api/mfapi/nf-mfapi-mfcreateattributes).
2.  Aggiungere gli attributi all'archivio attributi.
3.  Passare l'archivio attributi alla funzione [**MFCreateAudioRenderer**](/windows/desktop/api/mfidl/nf-mfidl-mfcreateaudiorenderer) nel parametro *pAudioAttributes* .

Se si usa la funzione [**MFCreateAudioRendererActivate**](/windows/desktop/api/mfidl/nf-mfidl-mfcreateaudiorendereractivate) , la funzione restituisce un puntatore all'interfaccia [**IMFAttributes**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes) nel parametro *ppActivate* . Utilizzare questo puntatore per aggiungere gli attributi.

Per un elenco degli attributi di configurazione, vedere [attributi del renderer audio](audio-renderer-attributes.md).

## <a name="selecting-the-audio-endpoint-device"></a>Selezione del dispositivo dell'endpoint audio

Un *dispositivo endpoint audio* è un dispositivo hardware che esegue il rendering o acquisisce audio. Gli esempi includono altoparlanti, cuffie, microfoni e lettori CD. Il SAR usa sempre un dispositivo di rendering audio. Esistono due modi per selezionare il dispositivo.

Il primo approccio consiste nell'enumerare i dispositivi di rendering audio nel sistema, usando l'interfaccia [**IMMDeviceEnumerator**](/windows/win32/api/mmdeviceapi/nn-mmdeviceapi-immdeviceenumerator) . Questa interfaccia è documentata nella documentazione principale dell'API audio.

1.  Creare l'oggetto enumeratore del dispositivo.
2.  Usare l'enumeratore Device per enumerare i dispositivi di rendering audio. Ogni dispositivo è rappresentato da un puntatore all'interfaccia [**IMMDevice**](/windows/win32/api/mmdeviceapi/nn-mmdeviceapi-immdevice) .
3.  Selezionare un dispositivo in base alle proprietà del dispositivo o alla selezione dell'utente.
4.  Chiamare [**IMMDevice:: GetId**](/windows/win32/api/mmdeviceapi/nf-mmdeviceapi-immdevice-getid) per ottenere l'identificatore del dispositivo.
5.  Impostare l'identificatore del dispositivo come valore dell'attributo [**dell' \_ \_ \_ \_ \_ ID endpoint dell'attributo MF audio RENDERER**](mf-audio-renderer-attribute-endpoint-id-attribute.md) .

Anziché enumerare i dispositivi, è possibile specificare il dispositivo audio in base al *ruolo*. Un ruolo audio identifica una categoria generale di utilizzo. Ad esempio, il ruolo *console* è definito per i giochi e le notifiche di sistema, mentre il ruolo *multimediale* è definito per musica e filmati. A ogni ruolo è assegnato un dispositivo di rendering audio e l'utente può modificare queste assegnazioni. Se si specifica un ruolo del dispositivo, il SAR usa qualsiasi dispositivo audio assegnato a tale ruolo. Per specificare il ruolo del dispositivo, impostare l'attributo del [**\_ \_ \_ \_ \_ ruolo endpoint dell'attributo MF audio RENDERER**](mf-audio-renderer-attribute-endpoint-role-attribute.md) .

I due attributi elencati in questa sezione si escludono a vicenda. Se non si imposta una di esse, il SAR usa il dispositivo audio assegnato al ruolo **eConsole** .

Il codice seguente enumera i dispositivi di rendering audio e assegna il primo dispositivo nell'elenco al SAR. In questo esempio viene usata la funzione [**MFCreateAudioRenderer**](/windows/desktop/api/mfidl/nf-mfidl-mfcreateaudiorenderer) per creare il SAR.


```C++
#include <mmdeviceapi.h>

HRESULT hr = S_OK;

IMMDeviceEnumerator *pEnum = NULL;      // Audio device enumerator.
IMMDeviceCollection *pDevices = NULL;   // Audio device collection.
IMMDevice *pDevice = NULL;              // An audio device.
IMFAttributes *pAttributes = NULL;      // Attribute store.
IMFMediaSink *pSink = NULL;             // Streaming audio renderer (SAR)

LPWSTR wstrID = NULL;                   // Device ID.

// Create the device enumerator.
hr = CoCreateInstance(
    __uuidof(MMDeviceEnumerator), 
    NULL,
    CLSCTX_ALL, 
    __uuidof(IMMDeviceEnumerator), 
    (void**)&pEnum
    );

// Enumerate the rendering devices.
if (SUCCEEDED(hr))
{
    hr = pEnum->EnumAudioEndpoints(eRender, DEVICE_STATE_ACTIVE, &pDevices);
}

// Get ID of the first device in the list.
if (SUCCEEDED(hr))
{
    hr = pDevices->Item(0, &pDevice);
}

if (SUCCEEDED(hr))
{
    hr = pDevice->GetId(&wstrID);
}

// Create an attribute store and set the device ID attribute.
if (SUCCEEDED(hr))
{
    hr = MFCreateAttributes(&pAttributes, 2);
}

if (SUCCEEDED(hr))
{
    hr = pAttributes->SetString(
        MF_AUDIO_RENDERER_ATTRIBUTE_ENDPOINT_ID, 
        wstrID
        );
}

// Create the audio renderer.
if (SUCCEEDED(hr))
{
    hr = MFCreateAudioRenderer(pAttributes, &pSink);    
}

SAFE_RELEASE(pEnum);
SAFE_RELEASE(pDevices);
SAFE_RELEASE(pDevice); 
SAFE_RELEASE(pAttributes);
CoTaskMemFree(wstrID);
```



Per creare l'oggetto attivazione per il SAR, modificare il codice visualizzato dopo la chiamata a [**IMMDevice:: GetId**](/windows/win32/api/mmdeviceapi/nf-mmdeviceapi-immdevice-getid) come indicato di seguito:


```C++
IMFActivate *pActivate = NULL;          // Activation object.

if (SUCCEEDED(hr))
{
    hr = MFCreateAudioRendererActivate(&pActivate);    
}

if (SUCCEEDED(hr))
{
    hr = pActivate->SetString(
        MF_AUDIO_RENDERER_ATTRIBUTE_ENDPOINT_ID, 
        wstrID
        );
}

SAFE_RELEASE(pActivate);
```



## <a name="selecting-the-audio-session"></a>Selezione della sessione audio

Una sessione audio è un gruppo di flussi audio correlati che un'applicazione può gestire collettivamente. L'applicazione può controllare il livello del volume e lo stato di silenziamento di ogni sessione. Le sessioni sono identificate dal GUID. Per specificare la sessione audio per il SAR, usare l'attributo dell' [ID di sessione dell' \_ attributo MF audio \_ RENDERER \_ \_ \_ ](mf-audio-renderer-attribute-session-id-attribute.md) . Se non si imposta questo attributo, il SAR viene aggiunto alla sessione predefinita per il processo, identificato dal **GUID \_ null**.

Per impostazione predefinita, una sessione audio è specifica del processo, ovvero contiene solo flussi dal processo chiamante. Per partecipare a una sessione tra processi, impostare l'attributo per l'attributo dei [ \_ \_ \_ \_ flag di rendering dell'audio MF](mf-audio-renderer-attribute-flags-attribute.md) con il valore **MF \_ audio \_ renderer \_ Attribute \_ flags \_ CROSSPROCESS**.

Dopo aver creato il SAR, utilizzare l'interfaccia [**IMFAudioPolicy**](/windows/desktop/api/mfidl/nn-mfidl-imfaudiopolicy) per aggiungere la sessione a un gruppo di sessioni, tutte controllate dallo stesso controllo volume nel pannello di controllo. È anche possibile usare questa interfaccia per impostare il nome visualizzato e l'icona che vengono visualizzati nel controllo volume.

## <a name="controlling-volume-levels"></a>Controllo di livelli di volume

Per controllare il livello del volume master di tutti i flussi nella sessione audio di SAR, usare l'interfaccia [**IMFSimpleAudioVolume**](/windows/desktop/api/mfidl/nn-mfidl-imfsimpleaudiovolume) . Per controllare il volume di un singolo flusso o per controllare il volume dei singoli canali all'interno di un flusso, usare l'interfaccia [**IMFAudioStreamVolume**](/windows/desktop/api/mfidl/nn-mfidl-imfaudiostreamvolume) . Entrambe le interfacce vengono ottenute chiamando [**IMFGetService:: GetService**](/windows/desktop/api/mfidl/nf-mfidl-imfgetservice-getservice). È possibile chiamare **GetService** direttamente sul SAR o chiamarlo nella sessione multimediale. I livelli di volume sono espressi come valori di attenuazione. Per ogni canale, il livello di attenuazione è il prodotto del volume master e del volume del canale.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Riproduzione di audio/video](audio-video-playback.md)
</dt> </dl>

 

 
