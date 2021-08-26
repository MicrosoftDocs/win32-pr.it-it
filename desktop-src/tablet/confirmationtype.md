---
description: Specifica il tipo di conferma che può verificarsi in un oggetto IContextNode.
ms.assetid: 5c906548-dbf5-4448-b248-070bd43b054e
title: Enumerazione ConfirmationType (IACom.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ConfirmationType
api_type:
- HeaderDef
api_location:
- IACom.h
ms.openlocfilehash: 9f89d5457e3d75bcf781a100449e4da9f8b45624af38760ca0cdda358fbf47ea
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119936951"
---
# <a name="confirmationtype-enumeration"></a>Enumerazione ConfirmationType

Specifica il tipo di conferma che può verificarsi in un [**oggetto IContextNode.**](icontextnode.md)

## <a name="syntax"></a>Sintassi


```C++
typedef enum ConfirmationType { 
  ConfirmationType_None                   = 0,
  ConfirmationType_NodeTypeAndProperties  = 1,
  ConfirmationType_TopBoundary            = 4
} ConfirmationType;
```



## <a name="constants"></a>Costanti

<dl> <dt>

<span id="ConfirmationType_None"></span><span id="confirmationtype_none"></span><span id="CONFIRMATIONTYPE_NONE"></span>**ConfirmationType \_ None**
</dt> <dd>

Non viene applicata alcuna conferma. [**IInkAnalyzer**](iinkanalyzer.md) è libero di modificare un nodo di contesto o uno dei relativi discendenti in base alle esigenze.

</dd> <dt>

<span id="ConfirmationType_NodeTypeAndProperties"></span><span id="confirmationtype_nodetypeandproperties"></span><span id="CONFIRMATIONTYPE_NODETYPEANDPROPERTIES"></span>**ConfirmationType \_ NodeTypeAndProperties**
</dt> <dd>

[**IInkAnalyzer non**](iinkanalyzer.md) può modificare il tipo o le proprietà del nodo di contesto specificato.

</dd> <dt>

<span id="ConfirmationType_TopBoundary"></span><span id="confirmationtype_topboundary"></span><span id="CONFIRMATIONTYPE_TOPBOUNDARY"></span>**ConfirmationType \_ TopBoundary**
</dt> <dd>

[**IInkAnalyzer**](iinkanalyzer.md) non eseguirà operazioni, inclusa l'aggiunta di input penna o l'unione con altri [**ContextNode,**](icontextnodes.md)che causano lo spostamento di TopBoundary oltre il limite superiore corrente. Esempio:

-   Un'applicazione analizza un set di input penna e viene identificato un elemento ParagraphNode.
-   L'applicazione conferma il valore TopBoundary di questo paragrafo.
-   L'utente dell'applicazione scrive un nuovo input penna sopra il paragrafo corrente. Quando l'analisi viene chiamata di nuovo, il nuovo input penna non verrà incorporato nel nodo del paragrafo Confermato.
-   Poiché viene confermato solo il limite superiore, ContextNode può continuare a crescere in altre direzioni. L'eliminazione dei tratti può causare lo spostamento verso il basso del limite superiore. La conversione di ContextNode può causare la modifica della posizione, ma non consentirà il merge dell'input penna aggiuntivo nella nuova posizione.

Questo confirmationType è applicabile solo ai nodi del paragrafo.

</dd> </dl>

## <a name="remarks"></a>Commenti

È possibile usare il **valore NodeTypeAndProperties** solo per i nodi di disegno di parole e input penna (vedere [**IContextNode::GetType).**](icontextnode-gettype.md) In caso contrario, **viene restituito un E \_ INVALIDARG** da [**IContextNode::Confirm.**](icontextnode-confirm.md)

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo app desktop XP Tablet PC \[ Edition\]<br/>                                                 |
| Server minimo supportato<br/> | Nessuno supportato<br/>                                                                                     |
| Intestazione<br/>                   | <dl> <dt>IACom.h (richiede anche IACom \_ i.c)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**IContextNode::Confirm**](icontextnode-confirm.md)
</dt> <dt>

[**IContextNode::IsConfirmed**](icontextnode-isconfirmed.md)
</dt> </dl>

 

 




