---
description: Modifica il tipo di conferma, che controlla cosa può cambiare l'oggetto IInkAnalyzer su IContextNode.
ms.assetid: a506f27e-3909-453e-a2f3-10d4c04d78a4
title: Metodo IContextNode::Confirm (IACom.h)
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
ms.openlocfilehash: 248eb78f364f7e938d78846c3e830cc170587961b81dfedcc046e10c59e4fd18
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120008451"
---
# <a name="icontextnodeconfirm-method"></a>Metodo IContextNode::Confirm

Modifica il tipo di conferma, che controlla cosa può cambiare [**l'oggetto IInkAnalyzer**](iinkanalyzer.md) sull'oggetto [**IContextNode.**](icontextnode.md)

## <a name="syntax"></a>Sintassi


```C++
HRESULT Confirm(
  [in] ConfirmationType confirmedType
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*confirmedType* \[ Pollici\]
</dt> <dd>

[**ConfirmationType**](confirmationtype.md) applicato al nodo.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Per una descrizione dei valori restituiti, vedere [Classi e interfacce - Analisi input penna](classes-and-interfaces---ink-analysis.md).

## <a name="remarks"></a>Commenti

Usare questo metodo per consentire all'utente finale di verificare che [**IInkAnalyzer**](iinkanalyzer.md) abbia analizzato correttamente i tratti. Dopo **la chiamata di IContextNode::Confirm,** **IInkAnalyzer** non modificherà gli oggetti [**IContextNode**](icontextnode.md) per tali tratti durante un'analisi successiva.

Usare **IContextNode::Confirm** quando l'utente ha confermato i risultati dell'analisi e non vuole che [**IInkAnalyzer**](iinkanalyzer.md) cambi [**un IContextNode**](icontextnode.md) durante un'analisi successiva. Ad esempio, se l'utente scrive la parola "in" e quindi l'applicazione chiama il metodo [**IInkAnalyzer::Analyze**](iinkanalyzer-analyze.md), l'analizzatore input penna genera un nodo InkWord con il valore "to". Se l'utente aggiunge "me" dopo "to" come parola e l'applicazione chiama nuovamente il metodo **IInkAnalyzer::Analyze,** l'analizzatore input penna può rimuovere il nodo InkWord precedente e creare un nuovo nodo InkWord con il valore "tome". Tuttavia, se dopo la prima chiamata al metodo **IInkAnalyzer::Analyze** l'applicazione chiama **IContextNode::Confirm** nel nodo InkWord per "to" con il valore **NodeTypeAndProperties** di [**ConfirmationType**](confirmationtype.md) , prima che l'utente asci il nodo "me", quando l'applicazione chiama il metodo **IInkAnalyzer::Analyze**, l'analizzatore input penna non rimuove o modifica il nodo "to". L'analizzatore dell'input penna può invece riconoscere due nodi InkWord per "to" e "me".

[**IContextNode può**](icontextnode.md) confermare solo oggetti di tipo InkWord e InkDrawing (vedere [Tipi di nodo di contesto](context-node-types.md)). **IContextNode::Confirm restituisce** **E \_ INVALIDARG** quando il nodo non è un nodo foglia.

[**IInkAnalyzer::RemoveStroke Method**](iinkanalyzer-removestroke.md) e [**IInkAnalyzer::RemoveStrokes Method**](iinkanalyzer-removestrokes.md) annullano la conferma di qualsiasi nodo da cui rimuovono i dati del tratto.

[**IContextNode::SetStrokes**](icontextnode-setstrokes.md), [**IInkAnalyzer::SetStrokesType**](iinkanalyzer-setstrokestype.md)e [**IInkAnalyzer::SetStrokeType**](iinkanalyzer-setstroketype.md) restituiscono **CORE E \_ \_ INVALIDOPERATION** se l'oggetto [**IContextNode**](icontextnode.md) è già confermato.

[**IContextNode::ReparentStrokeByIdToNode**](icontextnode-reparentstrokebyidtonode.md) restituisce un errore se viene confermato il nodo di origine o di destinazione.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo app desktop tablet PC Edition \[ XP\]<br/>                                                 |
| Server minimo supportato<br/> | Nessuno supportato<br/>                                                                                     |
| Intestazione<br/>                   | <dl> <dt>IACom.h (richiede anche IACom \_ i.c)</dt> </dl> |
| DLL<br/>                      | <dl> <dt>IACom.dll</dt> </dl>                          |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**IContextNode**](icontextnode.md)
</dt> <dt>

[**IContextNode::IsConfirmed**](icontextnode-isconfirmed.md)
</dt> <dt>

[Informazioni di riferimento per l'analisi dell'input penna](ink-analysis-reference.md)
</dt> </dl>

 

 




