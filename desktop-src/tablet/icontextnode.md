---
description: Rappresenta un nodo in un albero di oggetti creati come parte dell'analisi dell'input penna.
ms.assetid: 44ef4401-cb14-4348-9ed8-b11a40d04940
title: Interfaccia IContextNode (IACom.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IContextNode
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 9e6ca9e65b7c14f1df3af00acece8e2ba37c85d6a2193989ab232839f1863c32
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119713466"
---
# <a name="icontextnode-interface"></a>Interfaccia IContextNode

Rappresenta un nodo in un albero di oggetti creati come parte dell'analisi dell'input penna.

## <a name="members"></a>Membri

**L'interfaccia IContextNode** eredita dall'interfaccia [**IUnknown.**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) **IContextNode** include anche questi tipi di membri:

-   [Metodi](#methods)

### <a name="methods"></a>Metodi

**L'interfaccia IContextNode** include questi metodi.



| Metodo                                                                                  | Descrizione                                                                                                                                                                                                                   |
|:----------------------------------------------------------------------------------------|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**AddContextLink**](icontextnode-addcontextlink.md)                                   | Aggiunge un nuovo [**IContextLink**](icontextlink.md) alla raccolta di collegamenti di contesto dell'oggetto **IContextNode.**<br/>                                                                                                          |
| [**AddPropertyData**](icontextnode-addpropertydata.md)                                 | Aggiunge una parte di dati specifici dell'applicazione.<br/>                                                                                                                                                                         |
| [**Confirm**](icontextnode-confirm.md)                                                 | Modifica il tipo di conferma, che controlla cosa può cambiare [**l'oggetto IInkAnalyzer**](iinkanalyzer.md) **sull'oggetto IContextNode.**<br/>                                                                         |
| [**ContainsPropertyData**](icontextnode-containspropertydata.md)                       | Determina se **l'oggetto IContextNode** contiene dati archiviati nell'identificatore specificato.<br/>                                                                                                                |
| [**CreatePartiallyPopulatedSubNode**](icontextnode-createpartiallypopulatedsubnode.md) | Crea un oggetto **IContextNode** figlio che contiene solo informazioni su tipo, identificatore e posizione.<br/>                                                                                                          |
| [**CreateSubNode**](icontextnode-createsubnode.md)                                     | Crea un nuovo oggetto **IContextNode** figlio.<br/>                                                                                                                                                                       |
| [**DeleteContextLink**](icontextnode-deletecontextlink.md)                             | Elimina un [**oggetto IContextLink**](icontextlink.md) dalla raccolta di collegamenti dell'oggetto **IContextNode.**<br/>                                                                                                         |
| [**DeleteSubNode**](icontextnode-deletesubnode.md)                                     | Rimuove un **elemento IContextNode figlio.**<br/>                                                                                                                                                                                  |
| [**GetContextLinks**](icontextnode-getcontextlinks.md)                                 | Recupera una raccolta di oggetti [**IContextLink**](icontextlink.md) che rappresenta le relazioni con altri **oggetti IContextNode.**<br/>                                                                          |
| [**GetId**](icontextnode-getid.md)                                                     | Recupera l'identificatore per **l'oggetto IContextNode.**<br/>                                                                                                                                                          |
| [**GetLocation**](icontextnode-getlocation.md)                                         | Recupera la posizione e le dimensioni **dell'oggetto IContextNode.**<br/>                                                                                                                                                    |
| [**GetParentNode**](icontextnode-getparentnode.md)                                     | Recupera il nodo padre di questo **IContextNode** nell'albero dei nodi di contesto.<br/>                                                                                                                                       |
| [**GetPartiallyPopulated**](icontextnode-getpartiallypopulated.md)                     | Recupera il valore che indica se un **oggetto IContextNode** è parzialmente popolato o completamente popolato.<br/>                                                                                                   |
| [**GetPropertyData**](icontextnode-getpropertydata.md)                                 | Recupera dati specifici dell'applicazione o altri dati di proprietà in base all'identificatore specificato.<br/>                                                                                                                         |
| [**GetPropertyDataIds**](icontextnode-getpropertydataids.md)                           | Recupera gli identificatori per i quali sono presenti dati di proprietà.<br/>                                                                                                                                                        |
| [**GetStrokeCount**](icontextnode-getstrokecount.md)                                   | Recupera il numero di tratti associati **all'oggetto IContextNode.**<br/>                                                                                                                                       |
| [**GetStrokeId**](icontextnode-getstrokeid.md)                                         | Recupera l'identificatore del tratto a cui fa riferimento un valore di indice all'interno **dell'oggetto IContextNode.**<br/>                                                                                                    |
| [**GetStrokeIds**](icontextnode-getstrokeids.md)                                       | Recupera una matrice di identificatori per i tratti all'interno **dell'oggetto IContextNode.**<br/>                                                                                                                              |
| [**GetStrokePacketDataById**](icontextnode-getstrokepacketdatabyid.md)                 | Recupera una matrice contenente i dati delle proprietà del pacchetto per il tratto specificato.<br/>                                                                                                                                   |
| [**GetStrokePacketDescriptionById**](icontextnode-getstrokepacketdescriptionbyid.md)   | Recupera una matrice contenente gli identificatori di proprietà del pacchetto per il tratto specificato.<br/>                                                                                                                            |
| [**GetSubNodes**](icontextnode-getsubnodes.md)                                         | Recupera i nodi figlio diretti **dell'oggetto IContextNode.**<br/>                                                                                                                                                   |
| [**GetType**](icontextnode-gettype.md)                                                 | Recupera il tipo **dell'oggetto IContextNode.**<br/>                                                                                                                                                                 |
| [**GetTypeName**](icontextnode-gettypename.md)                                         | Recupera un nome di tipo leggibile dall'utente di **questo oggetto IContextNode.**<br/>                                                                                                                                                     |
| [**IsConfirmed**](icontextnode-isconfirmed.md)                                         | Recupera un valore che indica se **l'oggetto IContextNode** è confermato. [**IInkAnalyzer**](iinkanalyzer.md) non può modificare il tipo di nodo e i tratti associati per gli oggetti **IContextNode** confermati.<br/> |
| [**LoadPropertiesData**](icontextnode-loadpropertiesdata.md)                           | Ricrea i dati delle proprietà interne e specifici dell'applicazione per una matrice di byte creata in precedenza con [**IContextNode::SavePropertiesData**](icontextnode-savepropertiesdata.md).<br/>                  |
| [**MoveSubNodeToPosition**](icontextnode-movesubnodetoposition.md)                     | Riordina un oggetto **IContextNode** figlio specificato in base all'indice specificato.<br/>                                                                                                                                         |
| [**RemovePropertyData**](icontextnode-removepropertydata.md)                           | Rimuove una parte di dati specifici dell'applicazione.<br/>                                                                                                                                                                      |
| [**Reparent**](icontextnode-reparent.md)                                               | Sposta questo **oggetto IContextNode** dalla raccolta di sottonodi del nodo di contesto padre alla raccolta di sottonodi del nodo di contesto specificato.<br/>                                                                         |
| [**ReparentStrokeByIdToNode**](icontextnode-reparentstrokebyidtonode.md)               | Sposta i dati del tratto **da questo oggetto IContextNode** all'oggetto **IContextNode specificato.**<br/>                                                                                                                                    |
| [**SavePropertiesData**](icontextnode-savepropertiesdata.md)                           | Recupera una matrice di byte che contiene i dati delle proprietà interne e specifici dell'applicazione per **questo IContextNode.**<br/>                                                                                           |
| [**SetLocation**](icontextnode-setlocation.md)                                         | Aggiorna la posizione e le dimensioni di **questo oggetto IContextNode.**<br/>                                                                                                                                                            |
| [**SetPartiallyPopulated**](icontextnode-setpartiallypopulated.md)                     | Modifica il valore che indica se questo **IContextNode** è parzialmente o completamente popolato.<br/>                                                                                                                   |
| [**SetStrokes**](icontextnode-setstrokes.md)                                           | Associa i tratti specificati a questo **oggetto IContextNode.**<br/>                                                                                                                                                       |



 

## <a name="remarks"></a>Commenti

I tipi di nodi sono descritti nelle costanti [Context Node Types.](context-node-types.md)

## <a name="examples"></a>Esempio

Nell'esempio seguente viene illustrato un metodo che esamina **un oggetto IContextNode**. Il metodo esegue le operazioni seguenti:

-   Ottiene il tipo del nodo di contesto. Se il nodo di contesto è un input penna non classificato, un hint di analisi o un nodo di riconoscimento personalizzato, chiama un metodo helper per esaminare proprietà specifiche del tipo di nodo.
-   Se il nodo ha sottonodi, esamina ogni sottonodo chiamando se stesso.
-   Se il nodo è un nodo foglia input penna, esamina i dati del tratto per il nodo chiamando un metodo helper.

L'API Ihe InkAnalysis consente di creare un nodo riga contenente parole input penna e parole di testo. Tuttavia, il parser ignorerà questi nodi misti e li tratterà come nodi estranei. Ciò avrà un impatto sull'accuratezza di analisi del rilevamento delle annotazioni dell'input penna quando l'utente finale scrive su o intorno a questo nodo misto.


```C++
HRESULT CMyClass::ExploreContextNode(
    IContextNode *pContextNode)
{
    // Check for certain types of context nodes.
    GUID ContextNodeType;
    HRESULT hr = pContextNode->GetType(&ContextNodeType);

    if (SUCCEEDED(hr))
    {
        if (IsEqualGUID(GUID_CNT_UNCLASSIFIEDINK, ContextNodeType))
        {
            // Call a helper method that explores unclassified ink nodes.
            hr = this->ExploreUnclassifiedInkNode(pContextNode);
        }
        else if (IsEqualGUID(GUID_CNT_ANALYSISHINT, ContextNodeType))
        {
            // Call a helper method that explores analysis hint nodes.
            hr = this->ExploreAnalysisHintNode(pContextNode);
        }
        else if (IsEqualGUID(GUID_CNT_CUSTOMRECOGNIZER, ContextNodeType))
        {
            // Call a helper method that explores custom recognizer nodes.
            hr = this->ExploreCustomRecognizerNode(pContextNode);
        }

        if (SUCCEEDED(hr))
        {
            // Check if this node is a branch or a leaf node.
            IContextNodes *pSubNodes = NULL;
            hr = pContextNode->GetSubNodes(&pSubNodes);

            if (SUCCEEDED(hr))
            {
                ULONG ulSubNodeCount;
                hr = pSubNodes->GetCount(&ulSubNodeCount);

                if (SUCCEEDED(hr))
                {
                    if (ulSubNodeCount > 0)
                    {
                        // This node has child nodes; explore each child node.
                        IContextNode *pSubNode = NULL;
                        for (ULONG index=0; index<ulSubNodeCount; index++)
                        {
                            hr = pSubNodes->GetContextNode(index, &pSubNode);

                            if (SUCCEEDED(hr))
                            {
                                // Recursive call to explore the child node of this
                                // context node.
                                hr = this->ExploreContextNode(pSubNode);
                            }

                            // Release this reference to the child context node.
                            if (pSubNode != NULL)
                            {
                                pSubNode->Release();
                                pSubNode = NULL;
                            }

                            if (FAILED(hr))
                            {
                                break;
                            }
                        }
                    }
                    else
                    {
                        // This is a leaf node. Check if it contains stroke data.
                        ULONG ulStrokeCount;
                        hr = pContextNode->GetStrokeCount(&ulStrokeCount);

                        if (SUCCEEDED(hr))
                        {
                            if (ulStrokeCount > 0)
                            {
                                // This node is an ink leaf node; call helper
                                // method that explores available stroke data.
                                hr = this->ExploreNodeStrokeData(pContextNode);
                            }
                        }
                    }
                }
            }

            // Release this reference to the subnodes collection.
            if (pSubNodes != NULL)
            {
                pSubNodes->Release();
                pSubNodes = NULL;
            }
        }
    }

    return hr;
}
```



## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo app desktop tablet PC Edition \[ XP\]<br/>                                                 |
| Server minimo supportato<br/> | Nessuno supportato<br/>                                                                                     |
| Intestazione<br/>                   | <dl> <dt>IACom.h (richiede anche IACom \_ i.c)</dt> </dl> |
| DLL<br/>                      | <dl> <dt>IACom.dll</dt> </dl>                          |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**IContextNodes**](icontextnodes.md)
</dt> <dt>

[Tipi di nodi di contesto](context-node-types.md)
</dt> <dt>

[**IInkAnalyzer**](iinkanalyzer.md)
</dt> <dt>

[Informazioni di riferimento per l'analisi input penna](ink-analysis-reference.md)
</dt> </dl>

 

