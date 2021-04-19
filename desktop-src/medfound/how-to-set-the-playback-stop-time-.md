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
# <a name="how-to-set-the-playback-stop-time"></a>Come impostare l'ora di arresto della riproduzione

Questo argomento descrive come impostare un'ora di arresto per la riproduzione quando si usa la [sessione multimediale](media-session.md).

## <a name="setting-the-stop-time-before-playback-begins"></a>Impostazione dell'ora di arresto prima dell'inizio della riproduzione

Prima di accodare una topologia per la riproduzione, è possibile specificare l'ora di arresto usando l'attributo [MF \_ TOPONODE \_ MEDIASTOP](mf-toponode-mediastop-attribute.md) . Per ogni nodo di output nella topologia, impostare il valore di MF \_ TOPONODE \_ MEDIASTOP sull'ora di arresto in unità 100-nanosecondi.

Si noti che l'impostazione di questo attributo dopo l'avvio della riproduzione non ha alcun effetto. Quindi, impostare l'attributo prima di chiamare [**IMFMediaSession:: Start**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-start).

Nel codice seguente viene illustrato come impostare l'ora di arresto di una topologia esistente.


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



## <a name="setting-the-stop-time-after-playback-has-started"></a>Impostazione dell'ora di arresto dopo l'avvio della riproduzione

È possibile impostare l'ora di arresto dopo che la [sessione multimediale](media-session.md) avvia la riproduzione usando l'interfaccia [**IMFTopologyNodeAttributeEditor**](/windows/desktop/api/mfidl/nn-mfidl-imftopologynodeattributeeditor) .

> [!IMPORTANT]
> Questa interfaccia presenta una grave limitazione, perché l'ora di arresto viene specificata come valore a 32 bit. Ciò significa che il tempo di arresto massimo che è possibile impostare utilizzando questa interfaccia è 0xFFFFFFFF o solo in 7 minuti. Questa limitazione è dovuta a una definizione di struttura non corretta.

 

Per impostare l'ora di arresto usando l'interfaccia [**IMFTopologyNodeAttributeEditor**](/windows/desktop/api/mfidl/nn-mfidl-imftopologynodeattributeeditor) , seguire questa procedura.

1.  Chiamare [**MFGetService**](/windows/desktop/api/mfidl/nf-mfidl-mfgetservice) per ottenere l'interfaccia [**IMFTopologyNodeAttributeEditor**](/windows/desktop/api/mfidl/nn-mfidl-imftopologynodeattributeeditor) dalla sessione multimediale.
2.  Chiamare [**IMFTopology:: GetTopologyID**](/windows/desktop/api/mfidl/nf-mfidl-imftopology-gettopologyid) per ottenere l'ID della topologia di riproduzione.
3.  Per ogni nodo di output nella topologia, chiamare [**IMFTopologyNodeAttributeEditor:: UpdateNodeAttributes**](/windows/desktop/api/mfidl/nf-mfidl-imftopologynodeattributeeditor-updatenodeattributes). Questo metodo accetta l'ID topologia e un puntatore a una struttura di [**\_ \_ aggiornamento degli attributi di MFTOPONODE**](/windows/desktop/api/mfidl/ns-mfidl-mftoponode_attribute_update) . Inizializzare la struttura come indicato di seguito.

    | Membro               | Valore                                                                                                               |
    |----------------------|---------------------------------------------------------------------------------------------------------------------|
    | **NodeId**           | ID del nodo. Per ottenere l'ID del nodo, chiamare Call [**IMFTopologyNode:: GetTopoNodeID**](/windows/desktop/api/mfidl/nf-mfidl-imftopologynode-gettoponodeid). |
    | **guidAttributeKey** | **MF \_ TOPONODE \_ MEDIASTOP**                                                                                         |
    | **attrType**         | **\_Attributo MF \_ UInt64**                                                                                           |
    | **u64**              | Ora di arresto, in unità di 100 nanosecondi.                                                                             |

    

     

Prestare attenzione a impostare correttamente il valore di **attrType** . Sebbene **U64** sia un tipo a 32 bit, il metodo richiede che **attrType** sia impostato su **MF \_ attributo \_ UInt64**.

Nel codice seguente vengono illustrati questi passaggi.


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



## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Riproduzione di audio/video](audio-video-playback.md)
</dt> </dl>

 

 



