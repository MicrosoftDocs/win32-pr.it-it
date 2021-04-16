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
# <a name="binding-output-nodes-to-media-sinks"></a><span data-ttu-id="b1197-103">Associazione di nodi di output a sink di supporto</span><span class="sxs-lookup"><span data-stu-id="b1197-103">Binding Output Nodes to Media Sinks</span></span>

<span data-ttu-id="b1197-104">In questo argomento viene descritto come inizializzare i nodi di output in una topologia, se si utilizza il caricatore della topologia al di fuori della sessione multimediale.</span><span class="sxs-lookup"><span data-stu-id="b1197-104">This topic describes how to initialize the output nodes in a topology, if you are using the topology loader outside of the Media Session.</span></span> <span data-ttu-id="b1197-105">Un nodo di output contiene inizialmente uno dei seguenti elementi:</span><span class="sxs-lookup"><span data-stu-id="b1197-105">An output node initially contains one of the following:</span></span>

-   <span data-ttu-id="b1197-106">Puntatore [**IMFStreamSink**](/windows/desktop/api/mfidl/nn-mfidl-imfstreamsink) .</span><span class="sxs-lookup"><span data-stu-id="b1197-106">An [**IMFStreamSink**](/windows/desktop/api/mfidl/nn-mfidl-imfstreamsink) pointer.</span></span>
-   <span data-ttu-id="b1197-107">Puntatore [**IMFActivate**](/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate) .</span><span class="sxs-lookup"><span data-stu-id="b1197-107">An [**IMFActivate**](/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate) pointer.</span></span>

<span data-ttu-id="b1197-108">Nel secondo caso, il puntatore [**IMFActivate**](/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate) deve essere convertito in un puntatore [**IMFStreamSink**](/windows/desktop/api/mfidl/nn-mfidl-imfstreamsink) prima che il caricatore della topologia risolva la topologia.</span><span class="sxs-lookup"><span data-stu-id="b1197-108">In the latter case, the [**IMFActivate**](/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate) pointer must be converted to an [**IMFStreamSink**](/windows/desktop/api/mfidl/nn-mfidl-imfstreamsink) pointer before the topology loader resolves the topology.</span></span> <span data-ttu-id="b1197-109">Nella maggior parte degli scenari il processo funziona nel modo seguente:</span><span class="sxs-lookup"><span data-stu-id="b1197-109">In most scenarios, the process works as follows:</span></span>

1.  <span data-ttu-id="b1197-110">L'applicazione Accoda una topologia parziale nella sessione multimediale.</span><span class="sxs-lookup"><span data-stu-id="b1197-110">The application queues a partial topology on the Media Session.</span></span>
2.  <span data-ttu-id="b1197-111">Per tutti i nodi di output, la sessione multimediale converte i puntatori [**IMFActivate**](/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate) in puntatori [**IMFStreamSink**](/windows/desktop/api/mfidl/nn-mfidl-imfstreamsink) .</span><span class="sxs-lookup"><span data-stu-id="b1197-111">For all output nodes, the Media Session converts [**IMFActivate**](/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate) pointers to [**IMFStreamSink**](/windows/desktop/api/mfidl/nn-mfidl-imfstreamsink) pointers.</span></span> <span data-ttu-id="b1197-112">Questo processo viene chiamato *Binding* del nodo di output a un sink multimediale.</span><span class="sxs-lookup"><span data-stu-id="b1197-112">This process is called *binding* the output node to a media sink.</span></span>
3.  <span data-ttu-id="b1197-113">La sessione multimediale Invia la topologia modificata al metodo [**IMFTopoLoader:: Load**](/windows/desktop/api/mfidl/nf-mfidl-imftopoloader-load) .</span><span class="sxs-lookup"><span data-stu-id="b1197-113">The Media Session sends the modified topology to the [**IMFTopoLoader::Load**](/windows/desktop/api/mfidl/nf-mfidl-imftopoloader-load) method.</span></span>

<span data-ttu-id="b1197-114">Tuttavia, se si utilizza direttamente il caricatore della topologia (all'esterno del supporto sessione), l'applicazione deve associare i nodi di output prima di chiamare [**IMFTopoLoader:: Load**](/windows/desktop/api/mfidl/nf-mfidl-imftopoloader-load).</span><span class="sxs-lookup"><span data-stu-id="b1197-114">However, if you are using the topology loader directly (outside of the media sesssion), your application must bind the output nodes prior to calling [**IMFTopoLoader::Load**](/windows/desktop/api/mfidl/nf-mfidl-imftopoloader-load).</span></span> <span data-ttu-id="b1197-115">Per associare un nodo di output, procedere come segue:</span><span class="sxs-lookup"><span data-stu-id="b1197-115">To bind an output node, do the following:</span></span>

1.  <span data-ttu-id="b1197-116">Chiamare [**IMFTopologyNode:: GetObject**](/windows/desktop/api/mfidl/nf-mfidl-imftopologynode-getobject) per ottenere il puntatore all'oggetto del nodo.</span><span class="sxs-lookup"><span data-stu-id="b1197-116">Call [**IMFTopologyNode::GetObject**](/windows/desktop/api/mfidl/nf-mfidl-imftopologynode-getobject) to get the node's object pointer.</span></span>
2.  <span data-ttu-id="b1197-117">Eseguire una query sul puntatore all'oggetto per l'interfaccia [**IMFStreamSink**](/windows/desktop/api/mfidl/nn-mfidl-imfstreamsink) .</span><span class="sxs-lookup"><span data-stu-id="b1197-117">Query the object pointer for the [**IMFStreamSink**](/windows/desktop/api/mfidl/nn-mfidl-imfstreamsink) interface.</span></span> <span data-ttu-id="b1197-118">Se la chiamata ha esito positivo, non c'è altro da fare, quindi ignorare i passaggi rimanenti.</span><span class="sxs-lookup"><span data-stu-id="b1197-118">If this call succeeds, there is nothing more to do, so skip the remaining steps.</span></span>
3.  <span data-ttu-id="b1197-119">Se il passaggio precedente ha esito negativo, eseguire una query sul puntatore all'oggetto per l'interfaccia [**IMFActivate**](/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate) .</span><span class="sxs-lookup"><span data-stu-id="b1197-119">If the previous step failed, query the object pointer for the [**IMFActivate**](/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate) interface.</span></span>
4.  <span data-ttu-id="b1197-120">Creare il sink multimediale chiamando [**IMFActivate:: ActivateObject**](/windows/desktop/api/mfobjects/nf-mfobjects-imfactivate-activateobject).</span><span class="sxs-lookup"><span data-stu-id="b1197-120">Create the media sink by calling [**IMFActivate::ActivateObject**](/windows/desktop/api/mfobjects/nf-mfobjects-imfactivate-activateobject).</span></span> <span data-ttu-id="b1197-121">Specificare **IID \_ IMFMediaSink** per ottenere un puntatore all'interfaccia [**IMFMediaSink**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasink) del sink multimediale.</span><span class="sxs-lookup"><span data-stu-id="b1197-121">Specify **IID\_IMFMediaSink** to get a pointer to the media sink's [**IMFMediaSink**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasink) interface.</span></span>
5.  <span data-ttu-id="b1197-122">Eseguire una query sul nodo per l'attributo [**MF \_ TOPONODE \_ STREAMID**](mf-toponode-streamid-attribute.md) .</span><span class="sxs-lookup"><span data-stu-id="b1197-122">Query the node for the [**MF\_TOPONODE\_STREAMID**](mf-toponode-streamid-attribute.md) attribute.</span></span> <span data-ttu-id="b1197-123">Il valore di questo attributo è l'identificatore del sink di flusso per questo nodo.</span><span class="sxs-lookup"><span data-stu-id="b1197-123">The value of this attribute is the identifier of the stream sink for this node.</span></span> <span data-ttu-id="b1197-124">Se l'attributo **MF \_ TOPONODE \_ STREAMID** non è impostato, l'identificatore di flusso predefinito è zero.</span><span class="sxs-lookup"><span data-stu-id="b1197-124">If the **MF\_TOPONODE\_STREAMID** attribute is not set, the default stream identifier is zero.</span></span>
6.  <span data-ttu-id="b1197-125">Il sink di flusso appropriato potrebbe essere già presente nel sink multimediale.</span><span class="sxs-lookup"><span data-stu-id="b1197-125">The appropriate stream sink might already exist on the media sink.</span></span> <span data-ttu-id="b1197-126">Per controllare, chiamare [**IMFMediaSink:: GetStreamSinkById**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasink-getstreamsinkbyid) sul sink del supporto.</span><span class="sxs-lookup"><span data-stu-id="b1197-126">To check, call [**IMFMediaSink::GetStreamSinkById**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasink-getstreamsinkbyid) on the media sink.</span></span> <span data-ttu-id="b1197-127">Se il sink del flusso esiste, il metodo restituisce un puntatore alla relativa interfaccia [**IMFStreamSink**](/windows/desktop/api/mfidl/nn-mfidl-imfstreamsink) .</span><span class="sxs-lookup"><span data-stu-id="b1197-127">If the stream sink exists, the method returns a pointer to its [**IMFStreamSink**](/windows/desktop/api/mfidl/nn-mfidl-imfstreamsink) interface.</span></span> <span data-ttu-id="b1197-128">Se la chiamata ha esito negativo, provare ad aggiungere un nuovo sink di flusso chiamando [**IMFMediaSink:: AddStreamSink**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasink-addstreamsink).</span><span class="sxs-lookup"><span data-stu-id="b1197-128">If this call fails, try to add a new stream sink by calling [**IMFMediaSink::AddStreamSink**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasink-addstreamsink).</span></span> <span data-ttu-id="b1197-129">Se entrambe le chiamate hanno esito negativo, significa che il sink multimediale non supporta l'identificatore di flusso richiesto e che il nodo della topologia non è configurato correttamente.</span><span class="sxs-lookup"><span data-stu-id="b1197-129">If both calls fail, it means the media sink does not support the requested stream identifier, and this topology node is not configured correctly.</span></span> <span data-ttu-id="b1197-130">Restituire un codice di errore e ignorare il passaggio successivo.</span><span class="sxs-lookup"><span data-stu-id="b1197-130">Return an error code and skip the next step.</span></span>
7.  <span data-ttu-id="b1197-131">Chiamare [**IMFTopologyNode:: seobject**](/windows/desktop/api/mfidl/nf-mfidl-imftopologynode-setobject), passando il puntatore [**IMFStreamSink**](/windows/desktop/api/mfidl/nn-mfidl-imfstreamsink) dal passaggio precedente.</span><span class="sxs-lookup"><span data-stu-id="b1197-131">Call [**IMFTopologyNode::SetObject**](/windows/desktop/api/mfidl/nf-mfidl-imftopologynode-setobject), passing in the [**IMFStreamSink**](/windows/desktop/api/mfidl/nn-mfidl-imfstreamsink) pointer from the previous step.</span></span> <span data-ttu-id="b1197-132">Questa chiamata sostituisce il puntatore all'oggetto del nodo, in modo che il nodo contenga un puntatore al sink del flusso anziché un puntatore all'oggetto attivazione.</span><span class="sxs-lookup"><span data-stu-id="b1197-132">This call replaces the node's object pointer, so that the node contains a pointer to the stream sink, instead of a pointer to the activation object.</span></span>

<span data-ttu-id="b1197-133">Nel codice seguente viene illustrato come associare un nodo di output.</span><span class="sxs-lookup"><span data-stu-id="b1197-133">The following code shows how to bind an output node.</span></span>


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
> <span data-ttu-id="b1197-134">Questo esempio usa la funzione [SafeRelease](saferelease.md) per rilasciare i puntatori a interfaccia.</span><span class="sxs-lookup"><span data-stu-id="b1197-134">This example uses the [SafeRelease](saferelease.md) function to release interface pointers.</span></span>

 

<span data-ttu-id="b1197-135">Nell'esempio seguente viene illustrato come associare tutti i nodi di output in una topologia.</span><span class="sxs-lookup"><span data-stu-id="b1197-135">The next example shows how to bind all of the output nodes in a topology.</span></span> <span data-ttu-id="b1197-136">Questo esempio usa il metodo [**IMFTopology:: GetOutputNodeCollection**](/windows/desktop/api/mfidl/nf-mfidl-imftopology-getoutputnodecollection) per ottenere una raccolta di nodi di output dalla topologia.</span><span class="sxs-lookup"><span data-stu-id="b1197-136">This example uses the [**IMFTopology::GetOutputNodeCollection**](/windows/desktop/api/mfidl/nf-mfidl-imftopology-getoutputnodecollection) method to get a collection of output nodes from the topology.</span></span> <span data-ttu-id="b1197-137">Chiama quindi la funzione illustrata nell'esempio precedente in ognuno di questi nodi.</span><span class="sxs-lookup"><span data-stu-id="b1197-137">Then it calls the function shown in the previous example on each of those nodes in turn.</span></span>


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



## <a name="related-topics"></a><span data-ttu-id="b1197-138">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="b1197-138">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b1197-139">Compilazione avanzata della topologia</span><span class="sxs-lookup"><span data-stu-id="b1197-139">Advanced Topology Building</span></span>](advanced-topology-building.md)
</dt> <dt>

[<span data-ttu-id="b1197-140">Sink di supporti</span><span class="sxs-lookup"><span data-stu-id="b1197-140">Media Sinks</span></span>](media-sinks.md)
</dt> <dt>

[<span data-ttu-id="b1197-141">**IMFTopoLoader**</span><span class="sxs-lookup"><span data-stu-id="b1197-141">**IMFTopoLoader**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imftopoloader)
</dt> </dl>

 

 



