---
description: Modifica il tipo di conferma, che consente di controllare le modifiche apportate all'oggetto IInkAnalyzer in IContextNode.
ms.assetid: a506f27e-3909-453e-a2f3-10d4c04d78a4
title: 'Metodo IContextNode:: Confirm (IACom. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IContextNode.Confirm
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 3703bb735c0707c412b7c1e41c43819904d83ce8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106307442"
---
# <a name="icontextnodeconfirm-method"></a>Metodo IContextNode:: Confirm

Modifica il tipo di conferma, che consente di controllare le modifiche apportate all'oggetto [**IInkAnalyzer**](iinkanalyzer.md) in [**IContextNode**](icontextnode.md).

## <a name="syntax"></a>Sintassi


```C++
HRESULT Confirm(
  [in] ConfirmationType confirmedType
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*confirmedType* \[ in\]
</dt> <dd>

[**ConfirmationType**](confirmationtype.md) applicato al nodo.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Per una descrizione dei valori restituiti, vedere [classi e interfacce-analisi input penna](classes-and-interfaces---ink-analysis.md).

## <a name="remarks"></a>Commenti

Utilizzare questo metodo per consentire all'utente finale di confermare che [**IInkAnalyzer**](iinkanalyzer.md) ha analizzato correttamente i tratti. Dopo la chiamata a **IContextNode:: Confirm** , **IInkAnalyzer** non modificherà gli oggetti [**IContextNode**](icontextnode.md) per tali tratti durante un'analisi successiva.

Usare **IContextNode:: Confirm** quando l'utente ha confermato i risultati dell'analisi e non vuole che [**IInkAnalyzer**](iinkanalyzer.md) modifichi un [**IContextNode**](icontextnode.md) durante un'analisi successiva. Se, ad esempio, l'utente scrive la parola "to" e quindi l'applicazione chiama il [**Metodo IInkAnalyzer:: Analyze**](iinkanalyzer-analyze.md), l'analizzatore input penna genera un nodo InkWord con il valore "to". Se l'utente aggiunge "me" dopo "a" come una parola e l'applicazione chiama di nuovo il **Metodo IInkAnalyzer:: Analyze** , l'analizzatore di input penna potrebbe rimuovere il nodo InkWord precedente e creare un nuovo nodo InkWord con il valore "tome". Tuttavia, se dopo la prima chiamata al **Metodo IInkAnalyzer:: Analyze**, l'applicazione chiama **IContextNode:: Confirm** sul nodo InkWord per "to" con il valore [**ConfirmationType**](confirmationtype.md) **NodeTypeAndProperties**, prima che l'utente aggiunga "me", quando l'applicazione chiama il **Metodo IInkAnalyzer:: Analyze**, l'analizzatore input penna non rimuove o modifica il nodo "a". Ink Analyzer può invece riconoscere due nodi InkWord per "to" e "me".

[**IContextNode**](icontextnode.md) può confermare solo oggetti di tipo InkWord e InkDrawing (vedere [tipi di nodo di contesto](context-node-types.md)). **IContextNode:: Confirm** restituisce **E \_ INVALIDARG** quando il nodo non è un nodo foglia.

Il metodo [**IInkAnalyzer:: RemoveStroke**](iinkanalyzer-removestroke.md) e il [**Metodo IInkAnalyzer:: RemoveStrokes**](iinkanalyzer-removestrokes.md) non confermano qualsiasi nodo da cui rimuovono i dati del tratto.

[**IContextNode:: Sestrokes**](icontextnode-setstrokes.md), [**IInkAnalyzer:: SetStrokesType**](iinkanalyzer-setstrokestype.md)e [**IInkAnalyzer:: SetStrokeType**](iinkanalyzer-setstroketype.md) restituiscono **Core \_ e \_ INVALIDOPERATION** se l'oggetto [**IContextNode**](icontextnode.md) è già confermato.

[**IContextNode:: ReparentStrokeByIdToNode**](icontextnode-reparentstrokebyidtonode.md) restituisce un errore se il nodo di origine o di destinazione è confermato.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Solo app desktop Windows XP Tablet PC Edition \[\]<br/>                                                 |
| Server minimo supportato<br/> | Nessuno supportato<br/>                                                                                     |
| Intestazione<br/>                   | <dl> <dt>IACom. h (richiede anche IACom \_ i. c)</dt> </dl> |
| DLL<br/>                      | <dl> <dt>IACom.dll</dt> </dl>                          |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**IContextNode**](icontextnode.md)
</dt> <dt>

[**IContextNode:: deconfirmed**](icontextnode-isconfirmed.md)
</dt> <dt>

[Riferimento all'analisi dell'input penna](ink-analysis-reference.md)
</dt> </dl>

 

 




