---
description: Impostazione dei tipi di supporti in un DMO
ms.assetid: 9ff1542d-6a67-414d-8336-aae80c74d5d0
title: Impostazione dei tipi di supporti in un DMO
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 85fd437ae54d2e5baec35eb415dd8d04e4d3a3fe5992b8ba73f6d25c77f0475a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119904251"
---
# <a name="setting-media-types-on-a-dmo"></a>Impostazione dei tipi di supporti in un DMO

Prima che un DMO possa elaborare dati, il client deve impostare il tipo di supporto per ogni flusso. È presente un'eccezione secondaria a questa regola. Vedere [Optional Flussi](optional-streams.md).) Per trovare il numero di flussi, chiamare il [**metodo IMediaObject::GetStreamCount:**](/previous-versions/windows/desktop/api/Mediaobj/nf-mediaobj-imediaobject-getstreamcount)


```C++
DWORD cInput = 0, cOutput = 0;
pDMO->GetStreamCount(&cInput, &cOutput);
```



Questo metodo restituisce due valori, il numero di input e il numero di output. Questi valori sono fissi per la durata del DMO.

**Tipi preferiti**

Per ogni flusso, il DMO assegna un elenco di possibili tipi di supporti, in ordine di preferenza. Ad esempio, i tipi preferiti potrebbero essere RGB a 32, RGB a 24 bit e RGB a 16 bit, nell'ordine indicato. Quando il client imposta i tipi di supporti, può usare questi elenchi come suggerimento. Per recuperare un tipo preferito per un flusso, chiamare il metodo [**IMediaObject::GetInputType**](/previous-versions/windows/desktop/api/Mediaobj/nf-mediaobj-imediaobject-getinputtype) o il metodo [**IMediaObject::GetOutputType.**](/previous-versions/windows/desktop/api/Mediaobj/nf-mediaobj-imediaobject-getoutputtype) Specificare il numero di flusso e un valore di indice per il tipo (a partire da zero). Ad esempio, il codice seguente recupera il primo tipo preferito dal primo flusso di input:


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



Per enumerare tutti i tipi di supporti preferiti in un flusso specificato, usare un ciclo che incrementa l'indice dei tipi fino a quando il metodo non restituisce DMO E NO MORE ITEMS, come illustrato \_ \_ \_ nell'esempio \_ seguente:


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



È necessario tenere presente i punti seguenti sui tipi preferiti:

-   Il DMO potrebbe restituire un tipo senza blocco di formato. Ad esempio, un DMO può specificare un tipo di video, ad esempio RGB a 24 bit, senza specificare la larghezza e l'altezza dell'immagine. Quando si imposta il tipo, tuttavia, è necessario fornire un blocco di formato completo. Alcuni tipi di supporti, ad esempio MIDI, non richiedono mai un blocco di formato, nel qual caso questa osservazione non è applicabile.
-   Il DMO non è necessario per supportare ogni combinazione di tipi preferiti restituiti. Ad esempio, se un DMO ha due flussi e ogni flusso ha quattro tipi preferiti, sono disponibili 16 combinazioni possibili, ma non tutte sono valide.
-   Quando il client imposta il tipo di supporto per un flusso, il DMO potrebbe aggiornare i tipi preferiti per gli altri flussi in modo che riflettano il nuovo stato. Non è tuttavia necessario eseguire questa operazione.
-   Per alcuni flussi, il DMO potrebbe non offrire alcun tipo preferito. In genere, un DMO deve offrire almeno alcuni tipi preferiti in alcuni flussi.
-   Il DMO non è necessario per offrire un elenco completo dei tipi di supporti che può accettare. Potrebbero essere presenti tipi "non deviati" supportati dall'DMO ma non offerti come tipi preferiti.

In breve, il client deve considerare solo i tipi preferiti come linee guida. L'unico modo per sapere quali tipi sono supportati è testarli, come descritto nella sezione successiva.

**Impostazione del tipo di supporto in un flusso**

Usare i [**metodi IMediaObject::SetInputType**](/previous-versions/windows/desktop/api/Mediaobj/nf-mediaobj-imediaobject-setinputtype) e [**IMediaObject::SetOutputType**](/previous-versions/windows/desktop/api/Mediaobj/nf-mediaobj-imediaobject-setoutputtype) per impostare il tipo per ogni flusso. È necessario fornire una **DMO \_ MEDIA \_ TYPE** contenente una descrizione completa del tipo di supporto. L'esempio seguente imposta il tipo di supporto sul flusso di input 0, usando audio PCM stereo a 44,1 kHz a 16 bit:


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



Per testare un tipo di supporto senza impostarlo, chiamare **SetInputType** o **SetOutputType** con DMO \_ SET \_ TYPEF \_ TEST \_ ONLY. Il metodo restituisce S \_ OK se il tipo è accettabile oppure S FALSE in caso \_ contrario:


```C++
if (S_OK == pDMO->SetInputType(0, &mt, DMO_SET_TYPEF_TEST_ONLY)
{
    // Media type is OK.
}
```



Poiché le impostazioni in un flusso possono influire su un altro flusso, potrebbe essere necessario cancellare il tipo di supporto di un flusso. A tale scopo, chiamare **SetInputType** o **SetOutputType** con il flag SET TYPEF CLEAR DMO \_ SET \_ TYPEF \_ CLEAR.

Per un decodificatore DMO, il client in genere imposta prima il tipo di input e quindi sceglie un tipo di output. Per un codificatore DMO, il client imposta prima il tipo di output e quindi il tipo di input.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Hosting diretto di un DMO](directly-hosting-a-dmo.md)
</dt> </dl>

 

 



