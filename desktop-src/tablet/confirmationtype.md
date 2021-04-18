---
description: Specifica il tipo di conferma che può verificarsi in un oggetto IContextNode.
ms.assetid: 5c906548-dbf5-4448-b248-070bd43b054e
title: Enumerazione ConfirmationType (IACom. h)
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
ms.openlocfilehash: 2c43971c6ccf44513c11e46d4bc5db86d973d7f2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106305686"
---
# <a name="confirmationtype-enumeration"></a>Enumerazione ConfirmationType

Specifica il tipo di conferma che può verificarsi in un oggetto [**IContextNode**](icontextnode.md) .

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

Non viene applicata alcuna conferma. [**IInkAnalyzer**](iinkanalyzer.md) è libero di modificare un nodo di contesto o uno qualsiasi dei relativi discendenti in base alle esigenze.

</dd> <dt>

<span id="ConfirmationType_NodeTypeAndProperties"></span><span id="confirmationtype_nodetypeandproperties"></span><span id="CONFIRMATIONTYPE_NODETYPEANDPROPERTIES"></span>**\_NodeTypeAndProperties ConfirmationType**
</dt> <dd>

[**IInkAnalyzer**](iinkanalyzer.md) non è in grado di modificare il tipo o qualsiasi proprietà del nodo di contesto specificato.

</dd> <dt>

<span id="ConfirmationType_TopBoundary"></span><span id="confirmationtype_topboundary"></span><span id="CONFIRMATIONTYPE_TOPBOUNDARY"></span>**ConfirmationType in \_ uscita**
</dt> <dd>

Il [**IInkAnalyzer**](iinkanalyzer.md) non eseguirà operazioni, tra cui l'aggiunta di input penna o l'Unione con altri [**ContextNode**](icontextnodes.md), che fanno sì che il bordo superiore venga spostato oltre il limite superiore corrente. Ad esempio:

-   Un'applicazione analizza un set di input penna e viene identificato un ParagraphNode.
-   L'applicazione conferma il delimitatore di questo paragrafo.
-   L'utente dell'applicazione scrive nuovo input penna sopra il paragrafo corrente. Quando l'analisi viene chiamata nuovamente, il nuovo input penna non verrà incorporato nel nodo di paragrafo confermato.
-   Poiché viene confermato solo il limite superiore, l'oggetto ContextNode può continuare ad aumentare in altre direzioni. L'eliminazione dei tratti può causare lo spostamento del limite superiore. La conversione dell'oggetto ContextNode può causare la modifica della posizione, ma non consente l'Unione di input penna aggiuntivi nella nuova posizione.

Questo ConfirmationType è applicabile solo ai nodi di paragrafo.

</dd> </dl>

## <a name="remarks"></a>Commenti

È possibile usare il valore **NodeTypeAndProperties** solo per i nodi input penna e di disegno input penna (vedere [**IContextNode:: GetType**](icontextnode-gettype.md)). In caso contrario, viene restituito un **E \_ INVALIDARG** da [**IContextNode:: Confirm**](icontextnode-confirm.md).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Solo app desktop Windows XP Tablet PC Edition \[\]<br/>                                                 |
| Server minimo supportato<br/> | Nessuno supportato<br/>                                                                                     |
| Intestazione<br/>                   | <dl> <dt>IACom. h (richiede anche IACom \_ i. c)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**IContextNode:: Confirm**](icontextnode-confirm.md)
</dt> <dt>

[**IContextNode:: deconfirmed**](icontextnode-isconfirmed.md)
</dt> </dl>

 

 




