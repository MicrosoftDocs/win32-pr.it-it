---
description: Creazione dell'oggetto multiplexer
ms.assetid: a5adc40c-abb4-4012-b6f2-eb871eaed7b9
title: Creazione dell'oggetto multiplexer
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b28dd7933bdd7c3a8587c96cb490c4e4122ecc04
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104225825"
---
# <a name="creating-the-multiplexer-object"></a>Creazione dell'oggetto multiplexer

Il multiplexing ASF è un oggetto livello WMContainer che funziona con l' [oggetto dati ASF](asf-file-structure.md) e fornisce a un'applicazione la possibilità di generare pacchetti di dati ASF per flussi multimediali.

L'oggetto multiplexer espone l'interfaccia [**IMFASFMultiplexer**](/windows/desktop/api/wmcontainer/nn-wmcontainer-imfasfmultiplexer) . Per creare il multiplexer, chiamare [**MFCreateASFMultiplexer**](/windows/desktop/api/wmcontainer/nf-wmcontainer-mfcreateasfmultiplexer). Questa funzione restituisce un puntatore a un oggetto vuoto. Se l'applicazione sta scrivendo un nuovo file ASF, l'applicazione deve inizializzare il multiplexer con un oggetto ContentInfo. A tale scopo, chiamare [**IMFASFMultiplexer:: Initialize**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfmultiplexer-initialize). L'oggetto ContentInfo specificato rappresenta l'oggetto intestazione ASF del nuovo file. Per informazioni sulla creazione e l'inizializzazione dell'oggetto ContentInfo per un nuovo file, vedere [inizializzazione dell'oggetto ContentInfo di un nuovo file ASF](initializing-the-contentinfo-object-of-a-new-asf-file.md).

Il metodo [**Initialize**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfmultiplexer-initialize) analizza l'oggetto ContentInfo per raccogliere informazioni sulla configurazione del flusso, ad esempio il numero di flussi, le dimensioni del pacchetto e la preroll. Facoltativamente, il multiplexer potrebbe avere anche bisogno di parametri di bucket a perdita e delle unità di estensione del payload. Queste informazioni sono necessarie per generare pacchetti di dati che soddisfano i requisiti definiti nell'oggetto intestazione ASF. Il metodo **Initialize** configura il multiplexer in base al tipo di supporto e alle impostazioni di configurazione dei flussi. Ad esempio, se un flusso è configurato per avere estensioni del payload (vedere [creazione e configurazione di flussi ASF](creating-and-configuring-asf-streams.md)), il multiplexer è configurato per aggiungere tali valori ai pacchetti di dati generati.

Il metodo [**Initialize**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfmultiplexer-initialize) ottiene anche un handle per l'oggetto dati iniziale creato durante la creazione dell'oggetto ContentInfo per la scrittura. Durante la generazione dei pacchetti di dati, il multiplexer aggiunge pacchetti all'oggetto dati e li aggiorna in modo appropriato. Dopo che il multiplexer ha generato tutti i pacchetti di dati, aggiorna l'oggetto ContentInfo fornito in modo che vengano aggiornati determinati valori, ad esempio il numero di pacchetti di dati.

Nell'esempio di codice seguente viene illustrato come creare un multiplexer e come inizializzarlo con un oggetto ContentInfo.


```C++
//-------------------------------------------------------------------
// CreateOutputGenerators
//
// Creates the ASF mux and the ASF Content Info object for the 
// output file.
//-------------------------------------------------------------------

HRESULT CreateOutputGenerators(
    IMFASFProfile *pProfile, 
    IMFASFContentInfo **ppContentInfo, 
    IMFASFMultiplexer **ppMux
    )
{
    IMFASFContentInfo *pContentInfo = NULL;
    IMFASFMultiplexer *pMux = NULL;

    // Use the ASF profile to create the ContentInfo object.
    HRESULT hr = MFCreateASFContentInfo(&pContentInfo);

    if (SUCCEEDED(hr))
    {
        hr = pContentInfo->SetProfile(pProfile);
    }

    // Create the ASF Multiplexer object.
    if (SUCCEEDED(hr))
    {
        hr = MFCreateASFMultiplexer(&pMux);
    }
    
    // Initialize it using the new ContentInfo object.
    if (SUCCEEDED(hr))
    {
        hr = pMux->Initialize(pContentInfo);
    }

    // Return the pointers to the caller.
    if (SUCCEEDED(hr))
    {
        *ppContentInfo = pContentInfo;
        (*ppContentInfo)->AddRef();

        *ppMux = pMux;
        (*ppMux)->AddRef();
    }

    SafeRelease(&pContentInfo);
    SafeRelease(&pMux);

    return hr;
}
```



Per visualizzare questa funzione utilizzata in un'applicazione completa, vedere [esercitazione: copia di flussi ASF da un file a un altro](tutorial--copying-asf-streams-from-one-file-to-another.md).

## <a name="multiplexer-initialization-and-leaky-bucket-settings"></a>Impostazioni di inizializzazione del multiplexer e bucket a perdita

Il metodo [**IMFASFMultiplexer:: Initialize**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfmultiplexer-initialize) configura il multiplexer per determinare il flusso di dati del bucket di perdita. Per configurare questi parametri, verificare che i valori di proprietà seguenti siano impostati sull'oggetto ContentInfo specificato. Per informazioni sull'impostazione di queste proprietà, vedere [impostazione delle proprietà nell'oggetto ContentInfo](setting-properties-in-the-contentinfo-object.md).

-   [**MFPKEY \_ ASFMEDIASINK \_ AutoAdjust \_ bitrate**](mfpkey-asfmediasink-autoadjust-bitrate-property.md) Property: indica se il multiplexer deve modificare automaticamente la velocità in bit per mantenere il flusso di dati nel bucket. Questa impostazione può essere modificata dall'applicazione chiamando [**IMFASFMultiplexer:: Seflags**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfmultiplexer-setflags) e passando il flag **MFASF \_ multiplexer \_ AutoAdjust \_ bitrate** .

-   [**MFPKEY \_ ASFMEDIASINK \_ base \_ SENDTIME**](mfpkey-asfmediasink-base-sendtime-property.md) Property: il tempo di invio indica quando verrà rilasciato il payload all'interno del bucket Leaky. L'ora di invio deve essere uguale o precedente all'ora di presentazione perché il payload deve avere tempo per arrivare alla destinazione prima dell'ora di presentazione.

    Il valore di questa proprietà è il primo tempo di invio. Il multiplexer usa questo valore per calcolare i tempi di invio successivi per assicurarsi che i dati scorrano regolarmente nel bucket. Se sul multiplexer è stato impostato il flag di velocità in bit di regolazione automatica di **MFASF \_ multiplexer \_ \_** , il multiplexer modificherà la velocità in bit in modo che il payload venga inviato quando la finestra del buffer è quasi piena. Se il flag non è impostato, il multiplexer non riesce a generare pacchetti di dati a causa del sovraccarico della larghezza di banda.

Il multiplexer ottiene le informazioni di configurazione del flusso dal profilo ASF associato all'oggetto ContentInfo specificato nel metodo [**Initialize**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfmultiplexer-initialize) . Le informazioni di configurazione del flusso includono parametri di bucket persi. Questo valore è richiesto dal multiplexer per generare pacchetti di dati.

Per specificare i parametri del bucket di perdita, impostare i valori nell'attributo [**MF \_ ASFSTREAMCONFIG \_ LEAKYBUCKET1**](mf-asfstreamconfig-leakybucket1-attribute.md) nell'oggetto di configurazione del flusso che rappresenta il flusso nel profilo. Per utilizzare il valore della finestra del buffer, utilizzato dal codificatore, chiamare [**IWMCodecLeakyBucket:: GetBufferSizeBits**](../wmformat/iwmcodecleakybucket-getbuffersizebits.md). Il valore effettivo della finestra del buffer è noto solo dopo l'impostazione del tipo di supporto di output del codificatore. Per informazioni sull'impostazione del tipo di supporto di output, vedere [Media Type Negotiation sul codificatore](media-type-negotiation-on-the-encoder.md).

> [!Note]  
> I valori dei bucket con perdita di tempo utilizzati dal codificatore potrebbero essere diversi nell'oggetto ContentInfo fornito dal profilo ASF utilizzato per creare il multiplexer.

 

Il metodo [**Initialize**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfmultiplexer-initialize) aggiorna l'oggetto ContentInfo in modo che i valori corretti vengano riflessi nell'oggetto intestazione ASF finale.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Multiplexer ASF](asf-multiplexer.md)
</dt> <dt>

[Generazione di nuovi pacchetti di dati ASF](generating-new-asf-data-packets.md)
</dt> </dl>

 

 
