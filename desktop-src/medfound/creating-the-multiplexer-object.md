---
description: Creazione dell'oggetto Multiplexer
ms.assetid: a5adc40c-abb4-4012-b6f2-eb871eaed7b9
title: Creazione dell'oggetto Multiplexer
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: aedf314a63e9475342a7a2091e1d8531bc5bb2839f8c53ae71fa760cdd58b32e
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119942941"
---
# <a name="creating-the-multiplexer-object"></a>Creazione dell'oggetto Multiplexer

Il multiplexer ASF è un oggetto livello WMContainer che funziona con l'oggetto dati [ASF](asf-file-structure.md) e offre a un'applicazione la possibilità di generare pacchetti di dati ASF per i flussi multimediali.

L'oggetto multiplexer espone [**l'interfaccia IMFASFMultiplexer.**](/windows/desktop/api/wmcontainer/nn-wmcontainer-imfasfmultiplexer) Per creare il multiplexer, chiamare [**MFCreateASFMultiplexer**](/windows/desktop/api/wmcontainer/nf-wmcontainer-mfcreateasfmultiplexer). Questa funzione restituisce un puntatore a un oggetto vuoto. Se l'applicazione sta scrivendo un nuovo file ASF, l'applicazione deve inizializzare il multiplexer con un oggetto ContentInfo. A tale scopo, chiamare [**IMFASFMultiplexer::Initialize**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfmultiplexer-initialize). L'oggetto ContentInfo specificato rappresenta l'oggetto intestazione ASF del nuovo file. Per informazioni sulla creazione e l'inizializzazione dell'oggetto ContentInfo per un nuovo file, vedere Inizializzazione dell'oggetto [ContentInfo di un nuovo file ASF.](initializing-the-contentinfo-object-of-a-new-asf-file.md)

Il [**metodo Initialize**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfmultiplexer-initialize) analizza l'oggetto ContentInfo per raccogliere informazioni di configurazione del flusso, ad esempio il numero di flussi, le dimensioni dei pacchetti e la pre-registrazione. Facoltativamente, il multiplexer potrebbe anche richiedere parametri di bucket persi e le unità di estensione del payload. Queste informazioni sono necessarie per generare pacchetti di dati che soddisfano i requisiti definiti nell'oggetto intestazione ASF. Il **metodo Initialize** configura il multiplexer in base al tipo di supporto e alle impostazioni di configurazione dei flussi. Ad esempio, se un flusso è configurato per avere estensioni del payload (vedere Creazione e [configurazione di ASF Flussi)](creating-and-configuring-asf-streams.md)e quindi il multiplexer è configurato per aggiungere tali valori ai pacchetti di dati generati.

Il [**metodo Initialize**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfmultiplexer-initialize) ottiene anche un handle per l'oggetto dati iniziale creato durante la creazione dell'oggetto ContentInfo per la scrittura. Durante la generazione di pacchetti di dati, il multiplexer aggiunge pacchetti all'oggetto dati e lo aggiorna in modo appropriato. Dopo che il multiplexer ha generato tutti i pacchetti di dati, aggiorna l'oggetto ContentInfo fornito in modo che determinati valori, ad esempio il numero di pacchetti di dati, siano aggiornati.

L'esempio di codice seguente illustra come creare un multiplexer e inizializzarlo con un oggetto ContentInfo.


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



Per visualizzare questa funzione usata in un'applicazione completa, vedere Esercitazione: Copia di file [ASF Flussi da un file](tutorial--copying-asf-streams-from-one-file-to-another.md)a un altro.

## <a name="multiplexer-initialization-and-leaky-bucket-settings"></a>Inizializzazione del multiplexer e bucket di perdita Impostazioni

Il [**metodo IMFASFMultiplexer::Initialize**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfmultiplexer-initialize) configura il multiplexer per determinare il flusso di dati del bucket che perde. Per configurare questi parametri, assicurarsi che i valori delle proprietà seguenti siano impostati sull'oggetto ContentInfo specificato. Per informazioni sull'impostazione di queste proprietà, vedere [Impostazione delle proprietà nell'oggetto ContentInfo.](setting-properties-in-the-contentinfo-object.md)

-   [**MFPKEY \_ Proprietà ASFMEDIASINK \_ AUTOADJUST \_ BITRATE:**](mfpkey-asfmediasink-autoadjust-bitrate-property.md) indica se il multiplexer deve regolare automaticamente la velocità in bit per mantenere il flusso di dati nel bucket che perde. Questa impostazione può essere modificata dall'applicazione chiamando [**IMFASFMultiplexer::SetFlags**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfmultiplexer-setflags) e passando il flag **MFASF \_ MULTIPLEXER \_ AUTOADJUST \_ BITRATE.**

-   [**MFPKEY \_ Proprietà ASFMEDIASINK \_ BASE \_ SENDTIME:**](mfpkey-asfmediasink-base-sendtime-property.md) l'ora di invio indica quando verrà rilasciato il payload all'interno del bucket persa. Gli orari di invio devono essere uguali o precedenti all'ora di presentazione perché il payload deve avere tempo per raggiungere la destinazione prima dell'ora di presentazione.

    Il valore di questa proprietà è la prima volta che si invia. Il multiplexer usa questo valore per calcolare i tempi di invio successivi per garantire che i dati sfluino costantemente attraverso il bucket. Se il flag **MFASF \_ MULTIPLEXER \_ AUTOADJUST \_ BITRATE** è stato impostato nel multiplexer, il multiplexer regola la velocità in bit in modo che il payload venga inviato quando la finestra del buffer è quasi piena. Se il flag non è impostato, il multiplexer non riesce a generare pacchetti di dati a causa di un sovraccarico della larghezza di banda.

Il multiplexer ottiene le informazioni di configurazione del flusso dal profilo ASF associato all'oggetto ContentInfo specificato nel [**metodo Initialize.**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfmultiplexer-initialize) Le informazioni di configurazione del flusso includono parametri di bucket persi. Questo valore è richiesto dal multiplexer per generare pacchetti di dati.

Per specificare i parametri del bucket di perdita, impostare i valori nell'attributo [**MF \_ ASFSTREAMCONFIG \_ LEAKYBUCKET1**](mf-asfstreamconfig-leakybucket1-attribute.md) nell'oggetto di configurazione del flusso che rappresenta il flusso nel profilo. Per usare il valore della finestra del buffer, usato dal codificatore, chiamare [**IWMCodecLeakyBucket::GetBufferSizeBits**](../wmformat/iwmcodecleakybucket-getbuffersizebits.md). Il valore effettivo della finestra del buffer è noto solo dopo l'impostazione del tipo di supporto di output del codificatore. Per informazioni sull'impostazione del tipo di supporto di output, vedere [Media Type Negotiation on the Encoder](media-type-negotiation-on-the-encoder.md).

> [!Note]  
> I valori di bucket persi usati dal codificatore potrebbero essere diversi nell'oggetto ContentInfo fornito dal profilo ASF usato per creare il multiplexer.

 

Il [**metodo Initialize**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfmultiplexer-initialize) aggiorna l'oggetto ContentInfo in modo che i valori corretti si riflettano nell'oggetto intestazione ASF finale.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[ASF Multiplexer](asf-multiplexer.md)
</dt> <dt>

[Generazione di nuovi pacchetti di dati ASF](generating-new-asf-data-packets.md)
</dt> </dl>

 

 
