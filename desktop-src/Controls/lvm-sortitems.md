---
title: Messaggio LVM_SORTITEMS (COMmctrl. h)
description: Usa una funzione di confronto definita dall'applicazione per ordinare gli elementi di un controllo di visualizzazione elenco. L'indice di ogni elemento viene modificato per riflettere la nuova sequenza. È possibile inviare questo messaggio in modo esplicito o usando la \_ macro SortItems di ListView.
ms.assetid: ed3d5cec-69af-49a1-9cb7-eb5da1163071
keywords:
- Controlli di Windows Message LVM_SORTITEMS
topic_type:
- apiref
api_name:
- LVM_SORTITEMS
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1aba6e739a15eec5e951d7c3ead04aa36a8201f7
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103965017"
---
# <a name="lvm_sortitems-message"></a>\_Messaggio SORTITEMS LVM

Usa una funzione di confronto definita dall'applicazione per ordinare gli elementi di un controllo di visualizzazione elenco. L'indice di ogni elemento viene modificato per riflettere la nuova sequenza. È possibile inviare questo messaggio in modo esplicito o usando la macro [**\_ SortItems di ListView**](/windows/desktop/api/Commctrl/nf-commctrl-listview_sortitems) .

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>

Valore definito dall'applicazione passato alla funzione di confronto.

</dd> <dt>

*lParam* 
</dt> <dd>

Puntatore alla funzione di confronto definita dall'applicazione. La funzione di confronto viene chiamata durante l'operazione di ordinamento ogni volta che è necessario confrontare l'ordine relativo di due elementi dell'elenco.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce **true** se l'operazione ha esito positivo o **false** in caso contrario.

## <a name="remarks"></a>Commenti

La funzione di confronto ha il formato seguente:

``` syntax
int CALLBACK CompareFunc(LPARAM lParam1, LPARAM lParam2, LPARAM lParamSort);
```

Il parametro *lParam1* è il valore associato al primo elemento da confrontare e il parametro *lParam2* è il valore associato al secondo elemento. Questi sono i valori specificati nel membro **lParam** della struttura [**LVITEM**](/windows/win32/api/commctrl/ns-commctrl-lvitema) degli elementi quando sono stati inseriti nell'elenco. Il parametro *wParam* di [**ListView \_ SortItems**](/windows/desktop/api/Commctrl/nf-commctrl-listview_sortitems)viene passato alla funzione di callback come terzo parametro.

La funzione di confronto deve restituire un valore negativo se il primo elemento deve precedere il secondo, un valore positivo se il primo elemento deve seguire il secondo oppure zero se i due elementi sono equivalenti.

> [!Note]  
> Durante il processo di ordinamento, il contenuto della visualizzazione elenco è instabile. Se la funzione di callback invia messaggi al controllo visualizzazione elenco oltre a [**LVM \_ GetItem**](lvm-getitem.md) ([**ListView \_ GetItem**](/windows/desktop/api/Commctrl/nf-commctrl-listview_getitem)), i risultati sono imprevedibili.

 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                        |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2003\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





