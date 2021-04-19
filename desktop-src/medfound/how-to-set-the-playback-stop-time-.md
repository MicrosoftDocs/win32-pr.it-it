---
description: Questo argomento descrive come impostare un'ora di arresto per la riproduzione quando si usa la sessione multimediale.
ms.assetid: B8BA2154-2824-4573-AE71-853EB8AB911D
title: Come impostare l'ora di arresto della riproduzione
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 65269260b1e40d7907f0233fad653deb9636848b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106308756"
---
# <a name="how-to-set-the-playback-stop-time"></a><span data-ttu-id="1a921-103">Come impostare l'ora di arresto della riproduzione</span><span class="sxs-lookup"><span data-stu-id="1a921-103">How to Set the Playback Stop Time</span></span>

<span data-ttu-id="1a921-104">Questo argomento descrive come impostare un'ora di arresto per la riproduzione quando si usa la [sessione multimediale](media-session.md).</span><span class="sxs-lookup"><span data-stu-id="1a921-104">This topic describes how to set a stop time for playback when using the [Media Session](media-session.md).</span></span>

## <a name="setting-the-stop-time-before-playback-begins"></a><span data-ttu-id="1a921-105">Impostazione dell'ora di arresto prima dell'inizio della riproduzione</span><span class="sxs-lookup"><span data-stu-id="1a921-105">Setting the Stop Time Before Playback Begins</span></span>

<span data-ttu-id="1a921-106">Prima di accodare una topologia per la riproduzione, è possibile specificare l'ora di arresto usando l'attributo [MF \_ TOPONODE \_ MEDIASTOP](mf-toponode-mediastop-attribute.md) .</span><span class="sxs-lookup"><span data-stu-id="1a921-106">Before you queue a topology for playback, you can specify the stop time by using the [MF\_TOPONODE\_MEDIASTOP](mf-toponode-mediastop-attribute.md) attribute.</span></span> <span data-ttu-id="1a921-107">Per ogni nodo di output nella topologia, impostare il valore di MF \_ TOPONODE \_ MEDIASTOP sull'ora di arresto in unità 100-nanosecondi.</span><span class="sxs-lookup"><span data-stu-id="1a921-107">For each output node in the topology, set the value of the MF\_TOPONODE\_MEDIASTOP to the stop time in 100-nanosecond units.</span></span>

<span data-ttu-id="1a921-108">Si noti che l'impostazione di questo attributo dopo l'avvio della riproduzione non ha alcun effetto.</span><span class="sxs-lookup"><span data-stu-id="1a921-108">Note that setting this attribute after playback starts has no effect.</span></span> <span data-ttu-id="1a921-109">Quindi, impostare l'attributo prima di chiamare [**IMFMediaSession:: Start**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-start).</span><span class="sxs-lookup"><span data-stu-id="1a921-109">Therefore, set the attribute before calling [**IMFMediaSession::Start**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-start).</span></span>

<span data-ttu-id="1a921-110">Nel codice seguente viene illustrato come impostare l'ora di arresto di una topologia esistente.</span><span class="sxs-lookup"><span data-stu-id="1a921-110">The following code shows how to set the stop time on an existing topology.</span></span>


```C++
template <class Q>
HRESULT GetCollectionObject(IMFCollection *pCollection, DWORD dwIndex, Q **ppObject)
{
    *ppObject = NULL;   // zero output

    IUnknown *pUnk = NULL;
    HRESULT hr = pCollection->GetElement(dwIndex, &pUnk);
    if (SUCCEEDED(hr))
    {
        hr = pUnk->QueryInterface(IID_PPV_ARGS(ppObject));
        pUnk->Release();
    }
    return hr;
}

HRESULT SetMediaStop(IMFTopology *pTopology, const LONGLONG& stop)
{
    IMFCollection *pCol = NULL;
    DWORD cNodes;

    HRESULT hr = pTopology->GetSourceNodeCollection(&pCol);
    if (SUCCEEDED(hr))
    {
        hr = pCol->GetElementCount(&cNodes);
    }
    if (SUCCEEDED(hr))
    {
        for (DWORD i = 0; i < cNodes; i++)
        {
            IMFTopologyNode *pNode;
            hr = GetCollectionObject(pCol, i, &pNode);
            if (SUCCEEDED(hr))
            {
                pNode->SetUINT64(MF_TOPONODE_MEDIASTOP, stop);
            }
            pNode->Release();
        }
    }
    SafeRelease(&pCol);
    return hr;
}
```



## <a name="setting-the-stop-time-after-playback-has-started"></a><span data-ttu-id="1a921-111">Impostazione dell'ora di arresto dopo l'avvio della riproduzione</span><span class="sxs-lookup"><span data-stu-id="1a921-111">Setting the Stop Time After Playback Has Started</span></span>

<span data-ttu-id="1a921-112">È possibile impostare l'ora di arresto dopo che la [sessione multimediale](media-session.md) avvia la riproduzione usando l'interfaccia [**IMFTopologyNodeAttributeEditor**](/windows/desktop/api/mfidl/nn-mfidl-imftopologynodeattributeeditor) .</span><span class="sxs-lookup"><span data-stu-id="1a921-112">There is a way to set the stop time after the [Media Session](media-session.md) starts playback, by using the [**IMFTopologyNodeAttributeEditor**](/windows/desktop/api/mfidl/nn-mfidl-imftopologynodeattributeeditor) interface.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="1a921-113">Questa interfaccia presenta una grave limitazione, perché l'ora di arresto viene specificata come valore a 32 bit.</span><span class="sxs-lookup"><span data-stu-id="1a921-113">This interface has a serious limitation, because the stop time is specified as a 32-bit value.</span></span> <span data-ttu-id="1a921-114">Ciò significa che il tempo di arresto massimo che è possibile impostare utilizzando questa interfaccia è 0xFFFFFFFF o solo in 7 minuti.</span><span class="sxs-lookup"><span data-stu-id="1a921-114">That means the maximum stop time that you can set using this interface is 0xFFFFFFFF, or just over 7 minutes.</span></span> <span data-ttu-id="1a921-115">Questa limitazione è dovuta a una definizione di struttura non corretta.</span><span class="sxs-lookup"><span data-stu-id="1a921-115">This limitation is due to an incorrect structure definition.</span></span>

 

<span data-ttu-id="1a921-116">Per impostare l'ora di arresto usando l'interfaccia [**IMFTopologyNodeAttributeEditor**](/windows/desktop/api/mfidl/nn-mfidl-imftopologynodeattributeeditor) , seguire questa procedura.</span><span class="sxs-lookup"><span data-stu-id="1a921-116">To set the stop time using the [**IMFTopologyNodeAttributeEditor**](/windows/desktop/api/mfidl/nn-mfidl-imftopologynodeattributeeditor) interface, perform the following steps.</span></span>

1.  <span data-ttu-id="1a921-117">Chiamare [**MFGetService**](/windows/desktop/api/mfidl/nf-mfidl-mfgetservice) per ottenere l'interfaccia [**IMFTopologyNodeAttributeEditor**](/windows/desktop/api/mfidl/nn-mfidl-imftopologynodeattributeeditor) dalla sessione multimediale.</span><span class="sxs-lookup"><span data-stu-id="1a921-117">Call [**MFGetService**](/windows/desktop/api/mfidl/nf-mfidl-mfgetservice) to get the [**IMFTopologyNodeAttributeEditor**](/windows/desktop/api/mfidl/nn-mfidl-imftopologynodeattributeeditor) interface from the Media Session.</span></span>
2.  <span data-ttu-id="1a921-118">Chiamare [**IMFTopology:: GetTopologyID**](/windows/desktop/api/mfidl/nf-mfidl-imftopology-gettopologyid) per ottenere l'ID della topologia di riproduzione.</span><span class="sxs-lookup"><span data-stu-id="1a921-118">Call [**IMFTopology::GetTopologyID**](/windows/desktop/api/mfidl/nf-mfidl-imftopology-gettopologyid) to get the ID of the playback topology.</span></span>
3.  <span data-ttu-id="1a921-119">Per ogni nodo di output nella topologia, chiamare [**IMFTopologyNodeAttributeEditor:: UpdateNodeAttributes**](/windows/desktop/api/mfidl/nf-mfidl-imftopologynodeattributeeditor-updatenodeattributes).</span><span class="sxs-lookup"><span data-stu-id="1a921-119">For each output node in the topology, call [**IMFTopologyNodeAttributeEditor::UpdateNodeAttributes**](/windows/desktop/api/mfidl/nf-mfidl-imftopologynodeattributeeditor-updatenodeattributes).</span></span> <span data-ttu-id="1a921-120">Questo metodo accetta l'ID topologia e un puntatore a una struttura di [**\_ \_ aggiornamento degli attributi di MFTOPONODE**](/windows/desktop/api/mfidl/ns-mfidl-mftoponode_attribute_update) .</span><span class="sxs-lookup"><span data-stu-id="1a921-120">This method takes the topology ID and a pointer to a [**MFTOPONODE\_ATTRIBUTE\_UPDATE**](/windows/desktop/api/mfidl/ns-mfidl-mftoponode_attribute_update) structure.</span></span> <span data-ttu-id="1a921-121">Inizializzare la struttura come indicato di seguito.</span><span class="sxs-lookup"><span data-stu-id="1a921-121">Initialize the structure as follows.</span></span>

    | <span data-ttu-id="1a921-122">Membro</span><span class="sxs-lookup"><span data-stu-id="1a921-122">Member</span></span>               | <span data-ttu-id="1a921-123">Valore</span><span class="sxs-lookup"><span data-stu-id="1a921-123">Value</span></span>                                                                                                               |
    |----------------------|---------------------------------------------------------------------------------------------------------------------|
    | <span data-ttu-id="1a921-124">**NodeId**</span><span class="sxs-lookup"><span data-stu-id="1a921-124">**NodeId**</span></span>           | <span data-ttu-id="1a921-125">ID del nodo.</span><span class="sxs-lookup"><span data-stu-id="1a921-125">The node ID.</span></span> <span data-ttu-id="1a921-126">Per ottenere l'ID del nodo, chiamare Call [**IMFTopologyNode:: GetTopoNodeID**](/windows/desktop/api/mfidl/nf-mfidl-imftopologynode-gettoponodeid).</span><span class="sxs-lookup"><span data-stu-id="1a921-126">To get the node ID, call call [**IMFTopologyNode::GetTopoNodeID**](/windows/desktop/api/mfidl/nf-mfidl-imftopologynode-gettoponodeid).</span></span> |
    | <span data-ttu-id="1a921-127">**guidAttributeKey**</span><span class="sxs-lookup"><span data-stu-id="1a921-127">**guidAttributeKey**</span></span> | <span data-ttu-id="1a921-128">**MF \_ TOPONODE \_ MEDIASTOP**</span><span class="sxs-lookup"><span data-stu-id="1a921-128">**MF\_TOPONODE\_MEDIASTOP**</span></span>                                                                                         |
    | <span data-ttu-id="1a921-129">**attrType**</span><span class="sxs-lookup"><span data-stu-id="1a921-129">**attrType**</span></span>         | <span data-ttu-id="1a921-130">**\_Attributo MF \_ UInt64**</span><span class="sxs-lookup"><span data-stu-id="1a921-130">**MF\_ATTRIBUTE\_UINT64**</span></span>                                                                                           |
    | <span data-ttu-id="1a921-131">**u64**</span><span class="sxs-lookup"><span data-stu-id="1a921-131">**u64**</span></span>              | <span data-ttu-id="1a921-132">Ora di arresto, in unità di 100 nanosecondi.</span><span class="sxs-lookup"><span data-stu-id="1a921-132">The stop time, in 100-nanosecond units.</span></span>                                                                             |

    

     

<span data-ttu-id="1a921-133">Prestare attenzione a impostare correttamente il valore di **attrType** .</span><span class="sxs-lookup"><span data-stu-id="1a921-133">Be careful to set the value of **attrType** correctly.</span></span> <span data-ttu-id="1a921-134">Sebbene **U64** sia un tipo a 32 bit, il metodo richiede che **attrType** sia impostato su **MF \_ attributo \_ UInt64**.</span><span class="sxs-lookup"><span data-stu-id="1a921-134">Although **u64** is a 32-bit type, the method requires that **attrType** be set to **MF\_ATTRIBUTE\_UINT64**.</span></span>

<span data-ttu-id="1a921-135">Nel codice seguente vengono illustrati questi passaggi.</span><span class="sxs-lookup"><span data-stu-id="1a921-135">The following code shows these steps.</span></span>


```C++
HRESULT SetMediaStopDynamic(IMFMediaSession *pSession, IMFTopology *pTopology, const LONGLONG& stop)
{
    if (stop > MAXUINT32)
    {
        return E_INVALIDARG;
    }

    IMFTopologyNodeAttributeEditor *pAttr = NULL;
    IMFCollection *pCol = NULL;
    IMFTopologyNode *pNode = NULL;

    HRESULT hr = MFGetService(pSession, MF_TOPONODE_ATTRIBUTE_EDITOR_SERVICE, IID_PPV_ARGS(&pAttr));
    if (FAILED(hr))
    {
        goto done;
    }

    TOPOID id;
    hr = pTopology->GetTopologyID(&id);
    if (FAILED(hr))
    {
        goto done;
    }

    DWORD cNodes;
    hr = pTopology->GetSourceNodeCollection(&pCol);
    if (FAILED(hr))
    {
        goto done;
    }

    hr = pCol->GetElementCount(&cNodes);
    if (FAILED(hr))
    {
        goto done;
    }

    for (DWORD i = 0; i < cNodes; i++)
    {
        IMFTopologyNode *pNode;
        hr = GetCollectionObject(pCol, i, &pNode);
        if (FAILED(hr))
        {
            goto done;
        }

        TOPOID nodeID;
        hr = pNode->GetTopoNodeID(&nodeID);
        if (FAILED(hr))
        {
            goto done;
        }

        MFTOPONODE_ATTRIBUTE_UPDATE update;
        update.NodeId = nodeID;
        update.guidAttributeKey = MF_TOPONODE_MEDIASTOP;
        update.attrType = MF_ATTRIBUTE_UINT64;
        update.u64 = (UINT32)stop;

        hr = pAttr->UpdateNodeAttributes(id, 1, &update);
        if (FAILED(hr))
        {
            goto done;
        }
        SafeRelease(&pNode);
    }

done:
    SafeRelease(&pNode);
    SafeRelease(&pCol);
    SafeRelease(&pAttr);
    return hr;
}
```



## <a name="related-topics"></a><span data-ttu-id="1a921-136">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="1a921-136">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="1a921-137">Riproduzione di audio/video</span><span class="sxs-lookup"><span data-stu-id="1a921-137">Audio/Video Playback</span></span>](audio-video-playback.md)
</dt> </dl>

 

 



