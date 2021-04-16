---
description: Associazione di nodi di output a sink di supporto
ms.assetid: d4f93f34-0af1-431f-9333-70ea09691b64
title: Associazione di nodi di output a sink di supporto
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8cbea075badf74ac9e0e9354d82f4100a6167a0c
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/03/2021
ms.locfileid: "104530480"
---
# <a name="binding-output-nodes-to-media-sinks"></a>Associazione di nodi di output a sink di supporto

In questo argomento viene descritto come inizializzare i nodi di output in una topologia, se si utilizza il caricatore della topologia al di fuori della sessione multimediale. Un nodo di output contiene inizialmente uno dei seguenti elementi:

-   Puntatore [**IMFStreamSink**](/windows/desktop/api/mfidl/nn-mfidl-imfstreamsink) .
-   Puntatore [**IMFActivate**](/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate) .

Nel secondo caso, il puntatore [**IMFActivate**](/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate) deve essere convertito in un puntatore [**IMFStreamSink**](/windows/desktop/api/mfidl/nn-mfidl-imfstreamsink) prima che il caricatore della topologia risolva la topologia. Nella maggior parte degli scenari il processo funziona nel modo seguente:

1.  L'applicazione Accoda una topologia parziale nella sessione multimediale.
2.  Per tutti i nodi di output, la sessione multimediale converte i puntatori [**IMFActivate**](/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate) in puntatori [**IMFStreamSink**](/windows/desktop/api/mfidl/nn-mfidl-imfstreamsink) . Questo processo viene chiamato *Binding* del nodo di output a un sink multimediale.
3.  La sessione multimediale Invia la topologia modificata al metodo [**IMFTopoLoader:: Load**](/windows/desktop/api/mfidl/nf-mfidl-imftopoloader-load) .

Tuttavia, se si utilizza direttamente il caricatore della topologia (all'esterno del supporto sessione), l'applicazione deve associare i nodi di output prima di chiamare [**IMFTopoLoader:: Load**](/windows/desktop/api/mfidl/nf-mfidl-imftopoloader-load). Per associare un nodo di output, procedere come segue:

1.  Chiamare [**IMFTopologyNode:: GetObject**](/windows/desktop/api/mfidl/nf-mfidl-imftopologynode-getobject) per ottenere il puntatore all'oggetto del nodo.
2.  Eseguire una query sul puntatore all'oggetto per l'interfaccia [**IMFStreamSink**](/windows/desktop/api/mfidl/nn-mfidl-imfstreamsink) . Se la chiamata ha esito positivo, non c'è altro da fare, quindi ignorare i passaggi rimanenti.
3.  Se il passaggio precedente ha esito negativo, eseguire una query sul puntatore all'oggetto per l'interfaccia [**IMFActivate**](/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate) .
4.  Creare il sink multimediale chiamando [**IMFActivate:: ActivateObject**](/windows/desktop/api/mfobjects/nf-mfobjects-imfactivate-activateobject). Specificare **IID \_ IMFMediaSink** per ottenere un puntatore all'interfaccia [**IMFMediaSink**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasink) del sink multimediale.
5.  Eseguire una query sul nodo per l'attributo [**MF \_ TOPONODE \_ STREAMID**](mf-toponode-streamid-attribute.md) . Il valore di questo attributo è l'identificatore del sink di flusso per questo nodo. Se l'attributo **MF \_ TOPONODE \_ STREAMID** non è impostato, l'identificatore di flusso predefinito è zero.
6.  Il sink di flusso appropriato potrebbe essere già presente nel sink multimediale. Per controllare, chiamare [**IMFMediaSink:: GetStreamSinkById**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasink-getstreamsinkbyid) sul sink del supporto. Se il sink del flusso esiste, il metodo restituisce un puntatore alla relativa interfaccia [**IMFStreamSink**](/windows/desktop/api/mfidl/nn-mfidl-imfstreamsink) . Se la chiamata ha esito negativo, provare ad aggiungere un nuovo sink di flusso chiamando [**IMFMediaSink:: AddStreamSink**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasink-addstreamsink). Se entrambe le chiamate hanno esito negativo, significa che il sink multimediale non supporta l'identificatore di flusso richiesto e che il nodo della topologia non è configurato correttamente. Restituire un codice di errore e ignorare il passaggio successivo.
7.  Chiamare [**IMFTopologyNode:: seobject**](/windows/desktop/api/mfidl/nf-mfidl-imftopologynode-setobject), passando il puntatore [**IMFStreamSink**](/windows/desktop/api/mfidl/nn-mfidl-imfstreamsink) dal passaggio precedente. Questa chiamata sostituisce il puntatore all'oggetto del nodo, in modo che il nodo contenga un puntatore al sink del flusso anziché un puntatore all'oggetto attivazione.

Nel codice seguente viene illustrato come associare un nodo di output.


```C++
// BindOutputNode
// Sets the IMFStreamSink pointer on an output node.

HRESULT BindOutputNode(IMFTopologyNode *pNode)
{
    IUnknown *pNodeObject = NULL;
    IMFActivate *pActivate = NULL;
    IMFStreamSink *pStream = NULL;
    IMFMediaSink *pSink = NULL;

    // Get the node's object pointer.
    HRESULT hr = pNode->GetObject(&pNodeObject);
    if (FAILED(hr))
    {
        return hr;
    }

    // The object pointer should be one of the following:
    // 1. An activation object for the media sink.
    // 2. The stream sink.

    // If it's #2, then we're already done.

    // First, check if it's an activation object.
    hr = pNodeObject->QueryInterface(IID_PPV_ARGS(&pActivate));

    if (SUCCEEDED(hr))
    {
        DWORD dwStreamID = 0;

        // The object pointer is an activation object. 
        
        // Try to create the media sink.
        hr = pActivate->ActivateObject(IID_PPV_ARGS(&pSink));

        // Look up the stream ID. (Default to zero.)

        if (SUCCEEDED(hr))
        {
           dwStreamID = MFGetAttributeUINT32(pNode, MF_TOPONODE_STREAMID, 0);
        }

        // Now try to get or create the stream sink.

        // Check if the media sink already has a stream sink with the requested ID.

        if (SUCCEEDED(hr))
        {
            hr = pSink->GetStreamSinkById(dwStreamID, &pStream);
            if (FAILED(hr))
            {
                // Try to add a new stream sink.
                hr = pSink->AddStreamSink(dwStreamID, NULL, &pStream);
            }
        }

        // Replace the node's object pointer with the stream sink. 
        if (SUCCEEDED(hr))
        {
            hr = pNode->SetObject(pStream);
        }
    }
    else
    {
        // Not an activation object. Is it a stream sink?
        hr = pNodeObject->QueryInterface(IID_PPV_ARGS(&pStream));
    }

    SafeRelease(&pNodeObject);
    SafeRelease(&pActivate);
    SafeRelease(&pStream);
    SafeRelease(&pSink);
    return hr;
}
```



> [!Note]  
> Questo esempio usa la funzione [SafeRelease](saferelease.md) per rilasciare i puntatori a interfaccia.

 

Nell'esempio seguente viene illustrato come associare tutti i nodi di output in una topologia. Questo esempio usa il metodo [**IMFTopology:: GetOutputNodeCollection**](/windows/desktop/api/mfidl/nf-mfidl-imftopology-getoutputnodecollection) per ottenere una raccolta di nodi di output dalla topologia. Chiama quindi la funzione illustrata nell'esempio precedente in ognuno di questi nodi.


```C++
// BindOutputNodes
// Sets the IMFStreamSink pointers on all of the output nodes in a topology.

HRESULT BindOutputNodes(IMFTopology *pTopology)
{
    DWORD cNodes = 0;

    IMFCollection *pCol = NULL;
    IUnknown *pUnk = NULL;
    IMFTopologyNode *pNode = NULL;

    // Get the collection of output nodes. 
    HRESULT hr = pTopology->GetOutputNodeCollection(&pCol);
    
    // Enumerate all of the nodes in the collection.
    if (SUCCEEDED(hr))
    {
        hr = pCol->GetElementCount(&cNodes);
    }

    if (SUCCEEDED(hr))
    {
        for (DWORD i = 0; i < cNodes; i++)
        {
            hr = pCol->GetElement(i, &pUnk);

            if (FAILED(hr)) { break; }

            hr = pUnk->QueryInterface(IID_IMFTopologyNode, (void**)&pNode);

            if (FAILED(hr)) { break; }

            // Bind this node.
            hr = BindOutputNode(pNode);

            if (FAILED(hr)) { break; }
        }
    }

    SafeRelease(&pCol);
    SafeRelease(&pUnk);
    SafeRelease(&pNode);
    return hr;
}
```



## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Compilazione avanzata della topologia](advanced-topology-building.md)
</dt> <dt>

[Sink di supporti](media-sinks.md)
</dt> <dt>

[**IMFTopoLoader**](/windows/desktop/api/mfidl/nn-mfidl-imftopoloader)
</dt> </dl>

 

 



