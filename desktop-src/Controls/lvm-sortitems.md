---
title: LVM_SORTITEMS messaggio (Commctrl.h)
description: Usa una funzione di confronto definita dall'applicazione per ordinare gli elementi di un controllo visualizzazione elenco. L'indice di ogni elemento cambia per riflettere la nuova sequenza. È possibile inviare questo messaggio in modo esplicito o usando la \_ macro SortItems di ListView.
ms.assetid: ed3d5cec-69af-49a1-9cb7-eb5da1163071
keywords:
- LVM_SORTITEMS di controllo Windows messaggio
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
ms.openlocfilehash: a245e8236995d0d595c339b322140ee53ab5f84e83f1ecbd6b8ed47293e7dc7a
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119816391"
---
# <a name="lvm_sortitems-message"></a>Messaggio \_ LVM SORTITEMS

Usa una funzione di confronto definita dall'applicazione per ordinare gli elementi di un controllo visualizzazione elenco. L'indice di ogni elemento cambia per riflettere la nuova sequenza. È possibile inviare questo messaggio in modo esplicito o usando la macro [**\_ SortItems di ListView.**](/windows/desktop/api/Commctrl/nf-commctrl-listview_sortitems)

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

Restituisce **TRUE in** caso di esito positivo oppure FALSE **in** caso contrario.

## <a name="remarks"></a>Commenti

La funzione di confronto ha il formato seguente:

``` syntax
int CALLBACK CompareFunc(LPARAM lParam1, LPARAM lParam2, LPARAM lParamSort);
```

Il *parametro lParam1* è il valore associato al primo elemento confrontato e *il parametro lParam2* è il valore associato al secondo elemento. Si tratta dei valori specificati nel membro **lParam** della struttura [**LVITEM**](/windows/win32/api/commctrl/ns-commctrl-lvitema) degli elementi quando sono stati inseriti nell'elenco. Il [**parametro \_ wParam di ListView SortItems**](/windows/desktop/api/Commctrl/nf-commctrl-listview_sortitems)viene passato alla funzione di callback come terzo parametro. 

La funzione di confronto deve restituire un valore negativo se il primo elemento deve precedere il secondo, un valore positivo se il primo elemento deve seguire il secondo oppure zero se i due elementi sono equivalenti.

> [!Note]  
> Durante il processo di ordinamento, il contenuto della visualizzazione elenco è instabile. Se la funzione di callback invia messaggi al controllo visualizzazione elenco a parte [**LVM \_ GETITEM**](lvm-getitem.md) ([**ListView \_ GetItem**](/windows/desktop/api/Commctrl/nf-commctrl-listview_getitem)), i risultati sono imprevedibili.

 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop Vista\]<br/>                                        |
| Server minimo supportato<br/> | Windows Solo app desktop di Server 2003 \[\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

 





