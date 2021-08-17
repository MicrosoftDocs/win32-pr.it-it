---
title: LVM_SORTITEMSEX messaggio (Commctrl.h)
description: Usa una funzione di confronto definita dall'applicazione per ordinare gli elementi di un controllo visualizzazione elenco. L'indice di ogni elemento cambia per riflettere la nuova sequenza. È possibile inviare questo messaggio in modo esplicito o usando la \_ macro SortItemsEx di ListView.
ms.assetid: eab2f6f5-68fd-4cb6-acf4-cb267ee40fdc
keywords:
- LVM_SORTITEMSEX dei controlli Windows messaggio
topic_type:
- apiref
api_name:
- LVM_SORTITEMSEX
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ef492ff11980e764b33942f54c0732a64e799a94dde0e3d872ef0cb7bfb66c0a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118170367"
---
# <a name="lvm_sortitemsex-message"></a>Messaggio \_ LVM SORTITEMSEX

Usa una funzione di confronto definita dall'applicazione per ordinare gli elementi di un controllo visualizzazione elenco. L'indice di ogni elemento cambia per riflettere la nuova sequenza. È possibile inviare questo messaggio in modo esplicito o usando la macro [**\_ SortItemsEx di ListView.**](/windows/desktop/api/Commctrl/nf-commctrl-listview_sortitemsex)

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>

Valore definito dall'applicazione passato alla funzione di confronto.

</dd> <dt>

*lParam* 
</dt> <dd>

Puntatore a una funzione di confronto definita dall'applicazione. Viene chiamato durante l'operazione di ordinamento ogni volta che è necessario confrontare l'ordine relativo di due elementi dell'elenco.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce **TRUE in** caso di esito positivo oppure FALSE **in** caso contrario.

## <a name="remarks"></a>Commenti

La funzione di confronto ha il formato seguente:

``` syntax
int CALLBACK CompareFunc(LPARAM lParam1, LPARAM lParam2, LPARAM lParamSort);  
```

Questo messaggio è simile a [**LVM \_ SORTITEMS,**](lvm-sortitems.md)ad eccezione del tipo di informazioni passate alla funzione di confronto. Con **LVM \_ SORTITEMSEX**, *lParam1* è l'indice corrente del primo elemento e *lParam2* è l'indice corrente del secondo elemento. È possibile inviare un [**messaggio LVM \_ GETITEMTEXT**](lvm-getitemtext.md) per recuperare altre informazioni su un elemento, se necessario.

La funzione di confronto deve restituire un valore negativo se il primo elemento deve precedere il secondo, un valore positivo se il primo elemento deve seguire il secondo oppure zero se i due elementi sono equivalenti.

> [!Note]  
> Durante il processo di ordinamento, il contenuto della visualizzazione elenco è instabile. Se la funzione di callback invia messaggi al controllo visualizzazione elenco a parte [**LVM \_ GETITEM**](lvm-getitem.md) ([**ListView \_ GetItem**](/windows/desktop/api/Commctrl/nf-commctrl-listview_getitem)), i risultati sono imprevedibili.

 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop Vista\]<br/>                                        |
| Server minimo supportato<br/> | Windows Solo app desktop di Server 2003 \[\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

 





