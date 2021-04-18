---
description: Descrittori di presentazione
ms.assetid: 714c8bda-5ce1-47e2-ba73-9304e26b3129
title: Descrittori di presentazione
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 44f1581e35fe6d875c691efdd5ef5736c1aa5215
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106309031"
---
# <a name="presentation-descriptors"></a>Descrittori di presentazione

Una *presentazione* è un set di flussi multimediali correlati che condividono un tempo di presentazione comune. Una presentazione, ad esempio, può essere costituita da flussi audio e video di un film. Un *descrittore di presentazione* è un oggetto che contiene la descrizione di una particolare presentazione. I descrittori di presentazione vengono usati per configurare origini multimediali e alcuni sink di supporto.

Ogni descrittore di presentazione contiene un elenco di uno o più descrittori di *flusso*. Che descrivono i flussi nella presentazione. I flussi possono essere selezionati o deselezionati. Solo i flussi selezionati generano dati. I flussi deselezionati non sono attivi e non producono dati. Ogni descrittore di flusso ha un *gestore di tipo di supporto*, che viene usato per modificare il tipo di supporto del flusso o ottenere il tipo di supporto corrente del flusso. Per ulteriori informazioni sui tipi di supporto, vedere [tipi di supporti](media-types.md).

Nella tabella seguente sono illustrate le interfacce primarie esposte da ciascuno di questi oggetti.



| Oggetto                  | Interfaccia                                                      |
|-------------------------|----------------------------------------------------------------|
| Descrittore presentazione | [**IMFPresentationDescriptor**](/windows/desktop/api/mfidl/nn-mfidl-imfpresentationdescriptor) |
| Descrittore di flusso       | [**IMFStreamDescriptor**](/windows/desktop/api/mfidl/nn-mfidl-imfstreamdescriptor)             |
| Gestore del tipo di supporto      | [**IMFMediaTypeHandler**](/windows/desktop/api/mfidl/nn-mfidl-imfmediatypehandler)             |



 

## <a name="media-source-presentations"></a>Presentazioni di origini multimediali

Ogni origine multimediale fornisce un descrittore di presentazione che descrive la configurazione predefinita per l'origine. Nella configurazione predefinita è selezionato almeno un flusso e ogni flusso selezionato ha un tipo di supporto. Per ottenere il descrittore della presentazione, chiamare [**IMFMediaSource:: CreatePresentationDescriptor**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-createpresentationdescriptor). Il metodo restituisce un puntatore [**IMFPresentationDescriptor**](/windows/desktop/api/mfidl/nn-mfidl-imfpresentationdescriptor) .

È possibile modificare il descrittore di presentazione dell'origine per selezionare un set di flussi diverso. Non modificare il descrittore della presentazione, a meno che l'origine del supporto non sia stata arrestata. Le modifiche vengono applicate quando si chiama [**IMFMediaSource:: Start**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-start) per avviare l'origine.

Per ottenere il numero di flussi, chiamare [**IMFPresentationDescriptor:: GetStreamDescriptorCount**](/windows/desktop/api/mfidl/nf-mfidl-imfpresentationdescriptor-getstreamdescriptorcount). Per ottenere il descrittore del flusso per un flusso, chiamare [**IMFPresentationDescriptor:: GetStreamDescriptorByIndex**](/windows/desktop/api/mfidl/nf-mfidl-imfpresentationdescriptor-getstreamdescriptorbyindex) e passare l'indice del flusso. I flussi sono indicizzati da zero. Il metodo **GetStreamDescriptorByIndex** restituisce un puntatore [**IMFStreamDescriptor**](/windows/desktop/api/mfidl/nn-mfidl-imfstreamdescriptor) . Restituisce anche un flag booleano che indica se il flusso è selezionato. Se il flusso è selezionato, l'origine multimediale produce dati per quel flusso. In caso contrario, l'origine non produce alcun dato per quel flusso. Per selezionare un flusso, chiamare [**IMFPresentationDescriptor:: SelectStream**](/windows/desktop/api/mfidl/nf-mfidl-imfpresentationdescriptor-selectstream) con l'indice del flusso. Per deselezionare un flusso, chiamare [**IMFPresentationDescriptor::D eselectstream**](/windows/desktop/api/mfidl/nf-mfidl-imfpresentationdescriptor-deselectstream).

Il codice seguente illustra come ottenere il descrittore di presentazione da un'origine multimediale ed enumerare i flussi.


```C++
HRESULT hr = S_OK;
DWORD cStreams = 0;
BOOL  fSelected = FALSE;

IMFPresentationDescriptor *pPresentation = NULL;
IMFStreamDescriptor *pStreamDesc = NULL;

hr = pSource->CreatePresentationDescriptor(&pPresentation);

if (SUCCEEDED(hr))
{
    hr = pPresentation->GetStreamDescriptorCount(&cStreams);
}

if (SUCCEEDED(hr))
{
    for (DWORD iStream = 0; iStream < cStreams; iStream++)
    {
        hr = pPresentation->GetStreamDescriptorByIndex(
            iStream, &fSelected, &pStreamDesc);

        if (FAILED(hr))
        {
            break;
        }

        /*  Use the stream descriptor. (Not shown.) */

        SAFE_RELEASE(pStreamDesc);
    }
}
SAFE_RELEASE(pPresentation);
SAFE_RELEASE(pStreamDesc);
```



## <a name="media-type-handlers"></a>Gestori di tipi multimediali

Per modificare il tipo di supporto del flusso o per ottenere il tipo di supporto corrente del flusso, usare il gestore del tipo di supporto del descrittore del flusso. Chiamare [**IMFStreamDescriptor:: GetMediaTypeHandler**](/windows/desktop/api/mfidl/nf-mfidl-imfstreamdescriptor-getmediatypehandler) per ottenere il gestore del tipo di supporto. Questo metodo restituisce un puntatore [**IMFMediaTypeHandler**](/windows/desktop/api/mfidl/nn-mfidl-imfmediatypehandler) .

Se si vuole semplicemente conoscere il tipo di dati nel flusso, ad esempio audio o video, chiamare [**IMFMediaTypeHandler:: GetMajorType**](/windows/desktop/api/mfidl/nf-mfidl-imfmediatypehandler-getmajortype). Questo metodo restituisce il GUID per il tipo di supporto principale. Ad esempio, un'applicazione di riproduzione connette in genere un flusso audio al renderer audio e un flusso video al renderer video. Se si usa la sessione multimediale o il caricatore della topologia per compilare una topologia, il GUID di tipo principale potrebbe essere l'unica informazione di formato necessaria.

Se per l'applicazione sono necessarie informazioni più dettagliate sul formato corrente, chiamare [**IMFMediaTypeHandler:: GetCurrentMediaType**](/windows/desktop/api/mfidl/nf-mfidl-imfmediatypehandler-getcurrentmediatype). Questo metodo restituisce un puntatore all'interfaccia [**IMFMediaType**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype) del tipo di supporto. Usare questa interfaccia per ottenere i dettagli del formato.

Il gestore del tipo di supporto contiene anche un elenco dei tipi di supporto supportati per il flusso. Per ottenere le dimensioni dell'elenco, chiamare [**IMFMediaTypeHandler:: GetMediaTypeCount**](/windows/desktop/api/mfidl/nf-mfidl-imfmediatypehandler-getmediatypecount). Per ottenere un tipo di supporto dall'elenco, chiamare [**IMFMediaTypeHandler:: GetMediaTypeByIndex**](/windows/desktop/api/mfidl/nf-mfidl-imfmediatypehandler-getmediatypebyindex) con l'indice del tipo di supporto. I tipi di supporto vengono restituiti nell'ordine di preferenza approssimativo. Per i formati audio, ad esempio, sono preferite frequenze di campionamento maggiori rispetto alle frequenze di campionamento inferiori. Tuttavia, non esiste una regola definitiva che regola l'ordinamento, pertanto è consigliabile gestirla semplicemente come linee guida.

L'elenco dei tipi supportati potrebbe non contenere tutti i possibili tipi di supporto supportati dal flusso. Per verificare se è supportato un particolare tipo di supporto, chiamare [**IMFMediaTypeHandler:: IsMediaTypeSupported**](/windows/desktop/api/mfidl/nf-mfidl-imfmediatypehandler-ismediatypesupported). Per impostare il tipo di supporto, chiamare [**IMFMediaTypeHandler:: SetCurrentMediaType**](/windows/desktop/api/mfidl/nf-mfidl-imfmediatypehandler-setcurrentmediatype). Se il metodo ha esito positivo, il flusso conterrà dati conformi al formato specificato. Il metodo **SetCurrentMediaType** non modifica l'elenco dei tipi preferiti.

Nel codice seguente viene illustrato come ottenere il gestore del tipo di supporto, enumerare i tipi di supporto preferiti e impostare il tipo di supporto. In questo esempio si presuppone che l'applicazione disponga di un algoritmo, non illustrato di seguito, per la selezione del tipo di supporto. Le specifiche variano in base all'applicazione.


```C++
HRESULT hr = S_OK;
DWORD cTypes = 0;
BOOL  bTypeOK = FALSE;

IMFMediaTypeHandler *pHandler = NULL;
IMFMediaType *pMediaType = NULL;

hr = pStreamDesc->GetMediaTypeHandler(&pHandler);

if (SUCCEEDED(hr))
{
    hr = pHandler->GetMediaTypeCount(&cTypes);
}

if (SUCCEEDED(hr))
{
    for (DWORD iType = 0; iType < cTypes; iType++)
    {   
        hr = pHandler->GetMediaTypeByIndex(iType, &pMediaType);

        if (FAILED(hr))
        {
            break;
        }

        /* Examine the media type. (Not shown.)  */

        /* If this media type is acceptable, set the media type. */

        if (bTypeOK)
        {
            hr = pHandler->SetCurrentMediaType(pMediaType);
            break;
        }

        SAFE_RELEASE(pMediaType);
    }
}    

SAFE_RELEASE(pMediaType);
SAFE_RELEASE(pHandler);
```



## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Origini supporti](media-sources.md)
</dt> <dt>

[API della piattaforma Media Foundation](media-foundation-platform-apis.md)
</dt> </dl>

 

 



