---
description: Specifica la direzione di un oggetto IContextLink.
ms.assetid: 4ba7dca7-6801-45bf-bbf1-1dd3172fbfa2
title: Enumerazione ContextLinkDirection (IACom.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ContextLinkDirection
api_type:
- HeaderDef
api_location:
- IACom.h
ms.openlocfilehash: 1cd187b2a6efed6de5e6ee866cbd2e75ad67defc67b4b6d2250eb9117c62d89e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119941181"
---
# <a name="contextlinkdirection-enumeration"></a>Enumerazione ContextLinkDirection

Specifica la direzione di un [**oggetto IContextLink.**](icontextlink.md)

## <a name="syntax"></a>Sintassi


```C++
typedef enum ContextLinkDirection { 
  ContextLinkDirection_LinksWith  = 0,
  ContextLinkDirection_LinksFrom  = 1,
  ContextLinkDirection_LinksTo    = 2
} ContextLinkDirection;
```



## <a name="constants"></a>Costanti

<dl> <dt>

<span id="ContextLinkDirection_LinksWith"></span><span id="contextlinkdirection_linkswith"></span><span id="CONTEXTLINKDIRECTION_LINKSWITH"></span>**Collegamenti \_ ContextLinkDirectionWith**
</dt> <dd>

[**IContextNode è**](icontextnode.md) un disegno direzionale che punta [**all'oggetto IContextLink.**](icontextlink.md)

</dd> <dt>

<span id="ContextLinkDirection_LinksFrom"></span><span id="contextlinkdirection_linksfrom"></span><span id="CONTEXTLINKDIRECTION_LINKSFROM"></span>**Collegamenti \_ ContextLinkDirectionFrom**
</dt> <dd>

[**IContextNode è**](icontextnode.md) un disegno direzionale che punta a [**IContextLink.**](icontextlink.md)

</dd> <dt>

<span id="ContextLinkDirection_LinksTo"></span><span id="contextlinkdirection_linksto"></span><span id="CONTEXTLINKDIRECTION_LINKSTO"></span>**Collegamenti \_ ContextLinkDirectionTo**
</dt> <dd>

Non sono presenti disegni direzionali nel collegamento. Ad esempio, un disegno a penna può sottolineare una parola input penna. Non è presente alcuna direzione dedotto dalla sottolineatura.

</dd> </dl>

## <a name="examples"></a>Esempio

L'esempio seguente accetta un oggetto [**IContextNode,**](icontextnode.md) e salva tutti gli oggetti `m_pSelectedNode` **IContextNode** a cui si collega, percorrendo l'albero predecessore e aggiungendo gli oggetti in un `CArray` oggetto , `linkedToNodes` . `CheckHResult` è una funzione che accetta e una stringa e genera un'eccezione creata con `HRESULT` la stringa se non è `HRESULT` **SUCCESS**.


```C++
// Find all first ancestor that contains links of type Enclose
CArray<IContextNode*,IContextNode*> linkedToNodes = CArray<IContextNode*,IContextNode*>();
IContextNode* pAncestor;
CheckHResult(m_pSelectedNode->GetParentNode(&pAncestor),
    "IContextNode::GetParentNode failed");
while (pAncestor != NULL)
{
    // Get the links
    IContextLinks* pLinks;
    CheckHResult(pAncestor->GetContextLinks(&pLinks),
        "IContextNode::GetContextLinks failed");
    ULONG nLinks;
    CheckHResult(pLinks->GetCount(&nLinks), "IContextLinks::GetCount failed");
    for (ULONG i = 0; i < nLinks; i++)
    {
        IContextLink* pLink;
        CheckHResult(pLinks->GetContextLink(i, &pLink),
            "IContextLinks::GetContextLink failed");
        // Check link direction
        ContextLinkDirection linkDirection;
        CheckHResult(pLink->GetContextLinkDirection(&linkDirection),
            "IContextLink:GetContextLinkDirection failed");
        if (linkDirection == ContextLinkDirection_LinksTo)
        {
            // Get source node and add the array
            IContextNode* pSourceNode;
            CheckHResult(pLink->GetSourceNode(&pSourceNode),
                "IContextLink::GetSourceNode failed");
            linkedToNodes.Add(pSourceNode);
        }
    }
            
    // Go up another level
    IContextNode* pNewAncestor;
    CheckHResult(pAncestor->GetParentNode(&pNewAncestor),
        "IContextNode::GetParentNode failed");
    pAncestor = pNewAncestor;
}
```



## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo app desktop tablet PC Edition \[ XP\]<br/>                                                 |
| Server minimo supportato<br/> | Nessuno supportato<br/>                                                                                     |
| Intestazione<br/>                   | <dl> <dt>IACom.h (richiede anche IACom \_ i.c)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**IContextLink**](icontextlink.md)
</dt> <dt>

[**IContextNode::AddContextLink**](icontextnode-addcontextlink.md)
</dt> </dl>

 

 




