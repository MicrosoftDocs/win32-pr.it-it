---
description: Specifica la direzione di un oggetto IContextLink.
ms.assetid: 4ba7dca7-6801-45bf-bbf1-1dd3172fbfa2
title: Enumerazione ContextLinkDirection (IACom. h)
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
ms.openlocfilehash: 82e10c7e908b4cc4035d8bfdde55d863f7b6ecf2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103882473"
---
# <a name="contextlinkdirection-enumeration"></a>Enumerazione ContextLinkDirection

Specifica la direzione di un oggetto [**IContextLink**](icontextlink.md) .

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

<span id="ContextLinkDirection_LinksWith"></span><span id="contextlinkdirection_linkswith"></span><span id="CONTEXTLINKDIRECTION_LINKSWITH"></span>**\_LinksWith ContextLinkDirection**
</dt> <dd>

[**IContextNode**](icontextnode.md) è un disegno direzionale che punta lontano da [**IContextLink**](icontextlink.md).

</dd> <dt>

<span id="ContextLinkDirection_LinksFrom"></span><span id="contextlinkdirection_linksfrom"></span><span id="CONTEXTLINKDIRECTION_LINKSFROM"></span>**\_LinksFrom ContextLinkDirection**
</dt> <dd>

[**IContextNode**](icontextnode.md) è un disegno direzionale che punta al [**IContextLink**](icontextlink.md).

</dd> <dt>

<span id="ContextLinkDirection_LinksTo"></span><span id="contextlinkdirection_linksto"></span><span id="CONTEXTLINKDIRECTION_LINKSTO"></span>**\_CollegamentiPer ContextLinkDirection**
</dt> <dd>

Nessun disegno direzionale nel collegamento. Un disegno Ink può ad esempio sottolineare una parola di input penna. Non esiste alcuna direzione dedotta dalla sottolineatura.

</dd> </dl>

## <a name="examples"></a>Esempio

Nell'esempio seguente viene utilizzato un oggetto [**IContextNode**](icontextnode.md) , `m_pSelectedNode` , e vengono salvati tutti gli oggetti **IContextNode** a cui si collegano spostando l'albero predecessore e aggiungendo gli oggetti in un `CArray` oggetto `linkedToNodes` . `CheckHResult` è una funzione che accetta un oggetto `HRESULT` e una stringa e genera un'eccezione creata con la stringa se `HRESULT` non ha **esito positivo**.


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
| Client minimo supportato<br/> | Solo app desktop Windows XP Tablet PC Edition \[\]<br/>                                                 |
| Server minimo supportato<br/> | Nessuno supportato<br/>                                                                                     |
| Intestazione<br/>                   | <dl> <dt>IACom. h (richiede anche IACom \_ i. c)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**IContextLink**](icontextlink.md)
</dt> <dt>

[**IContextNode::AddContextLink**](icontextnode-addcontextlink.md)
</dt> </dl>

 

 




