---
description: Impostazione dei tipi di supporto in un DMO
ms.assetid: 9ff1542d-6a67-414d-8336-aae80c74d5d0
title: Impostazione dei tipi di supporto in un DMO
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d8d657977079a75bf5f1eeccc389da6ad67f63b5
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/03/2021
ms.locfileid: "106320744"
---
# <a name="setting-media-types-on-a-dmo"></a>Impostazione dei tipi di supporto in un DMO

Prima che un DMO possa elaborare i dati, il client deve impostare il tipo di supporto per ogni flusso. Esiste una sola eccezione secondaria a questa regola. vedere [flussi facoltativi](optional-streams.md). Per trovare il numero di flussi, chiamare il metodo [**IMediaObject:: GetStreamCount**](/previous-versions/windows/desktop/api/Mediaobj/nf-mediaobj-imediaobject-getstreamcount) :


```C++
DWORD cInput = 0, cOutput = 0;
pDMO->GetStreamCount(&cInput, &cOutput);
```



Questo metodo restituisce due valori, il numero di input e il numero di output. Questi valori sono corretti per la durata di DMO.

**Tipi preferiti**

Per ogni flusso, DMO assegna un elenco di tipi di supporti possibili, in ordine di preferenza. Ad esempio, i tipi preferiti possono essere 32-RGB, RGB a 24 bit e RGB a 16 bit, in questo ordine. Quando il client imposta i tipi di supporto, può utilizzare questi elenchi come hint. Per recuperare un tipo preferito per un flusso, chiamare il metodo [**IMediaObject:: GetInputType**](/previous-versions/windows/desktop/api/Mediaobj/nf-mediaobj-imediaobject-getinputtype) o [**IMediaObject:: GetOutputType**](/previous-versions/windows/desktop/api/Mediaobj/nf-mediaobj-imediaobject-getoutputtype) . Specificare il numero di flusso e un valore di indice per il tipo (a partire da zero). Il codice seguente, ad esempio, recupera il primo tipo preferito dal primo flusso di input:


```C++
DMO_MEDIA_TYPE mt
hr = pDMO->GetInputType(0, 0, &mt)
if (SUCCEEDED(hr))
{
    // Examine this media type (not shown).
    /* ... */

    // Free the format block.
    MoFreeMediaType(&mt);
}
```



Per enumerare tutti i tipi di supporto preferiti in un determinato flusso, usare un ciclo che incrementa l'indice del tipo fino a quando il metodo non restituisce DMO \_ E \_ nessun \_ altro \_ elemento, come illustrato nell'esempio seguente:


```C++
DMO_MEDIA_TYPE mt;
DWORD dwType = 0;
while (hr = pDMO->GetInputType(0, dwType, &mt), SUCCEEDED(hr))
{
    // Examine this media type (not shown).
    /* ... */

    // Free the format block.
    MoFreeMediaType(&mt);
    ++dwType;
}
```



Si notino i seguenti punti sui tipi preferiti:

-   DMO potrebbe restituire un tipo senza blocco di formato. Ad esempio, un DMO potrebbe specificare un tipo video, ad esempio RGB a 24 bit, senza fornire la larghezza e l'altezza dell'immagine. Quando si imposta il tipo, tuttavia, è necessario fornire un blocco di formato completo. (Alcuni tipi di supporti, ad esempio MIDI, non richiedono mai un blocco di formato. in tal caso, questo contrassegno non è applicabile).
-   Non è necessario che DMO supporti ogni combinazione di tipi preferiti restituiti. Se, ad esempio, in un DMO sono presenti due flussi e ogni flusso dispone di quattro tipi preferiti, sono disponibili 16 combinazioni, ma non tutte sono sicuramente valide.
-   Quando il client imposta il tipo di supporto per un flusso, DMO potrebbe aggiornare i tipi preferiti affinché altri flussi riflettano il nuovo stato. Tuttavia, non è necessario eseguire questa operazione.
-   Per alcuni flussi, DMO potrebbe non offrire i tipi preferiti. In genere, un DMO dovrebbe offrire almeno alcuni tipi preferiti in alcuni flussi.
-   Non è necessario che DMO offra un elenco completo dei tipi di supporti che può accettare. Potrebbero essere presenti tipi "non pubblicizzati" supportati da DMO ma che non sono disponibili come tipi preferiti.

In breve, il client deve considerare i tipi preferiti solo come linee guida. L'unico modo per stabilire quali tipi sono supportati consiste nel testarli, come descritto nella sezione successiva.

**Impostazione del tipo di supporto in un flusso**

Usare i metodi [**IMediaObject:: SetInputType**](/previous-versions/windows/desktop/api/Mediaobj/nf-mediaobj-imediaobject-setinputtype) e [**IMediaObject:: SetOutputType**](/previous-versions/windows/desktop/api/Mediaobj/nf-mediaobj-imediaobject-setoutputtype) per impostare il tipo per ogni flusso. È necessario fornire una struttura del **\_ \_ tipo di supporto DMO** che contiene una descrizione completa del tipo di supporto. L'esempio seguente imposta il tipo di supporto nel flusso di input 0, usando audio PCM stereo a 16 bit 44,1-kHz:


```C++
DMO_MEDIA_TYPE mt;
ZeroMemory(&mt, sizeof(DMO_MEDIA_TYPE));
// Allocate memory for the format block.
HRESULT hr = MoInitMediaType(&mt, sizeof(WAVEFORMATEX));
if (SUCCEEDED(hr))
{
    // Set the type GUIDs.
    mt.majortype  = MEDIATYPE_Audio;
    mt.subtype    = MEDIASUBTYPE_PCM;
    mt.formattype = FORMAT_WaveFormatEx;

    // Initialize the format block.
    WAVEFORMATEX *pWave = reinterpret_cast<WAVEFORMATEX*>(mt.pbFormat);
    pWave->wFormatTag = WAVE_FORMAT_PCM;
    pWave->nChannels = 2;
    pWave->nSamplesPerSec = 44100;
    pWave->wBitsPerSample = 16;
    pWave->nBlockAlign = (pWave->nChannels * pWave->wBitsPerSample) / 8;
    pWave->nAvgBytesPerSec = pWave->nSamplesPerSec * pWave->nBlockAlign;
    pWave->cbSize = 0;

    // Set the media type.
    hr = pDMO->SetInputType(0, &mt, 0); 

    // Release the format block.
    MoFreeMediaType(&mt);
}
```



Per testare un tipo di supporto senza impostarlo, chiamare **SetInputType** o **SetOutputType** con il \_ flag DMO set \_ TYPEF \_ test \_ only. Il metodo restituisce \_ OK se il tipo è accettabile oppure s \_ false in caso contrario:


```C++
if (S_OK == pDMO->SetInputType(0, &mt, DMO_SET_TYPEF_TEST_ONLY)
{
    // Media type is OK.
}
```



Poiché le impostazioni in un flusso possono influire su un altro flusso, potrebbe essere necessario cancellare il tipo di supporto di un flusso. A tale scopo, chiamare **SetInputType** o **SetOutputType** con il \_ flag DMO set \_ TYPEF \_ Clear.

Per un decodificatore DMO, il client in genere imposta innanzitutto il tipo di input e quindi sceglie un tipo di output. Per un codificatore DMO, il client imposterà prima il tipo di output e quindi il tipo di input.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Hosting diretto di un DMO](directly-hosting-a-dmo.md)
</dt> </dl>

 

 



