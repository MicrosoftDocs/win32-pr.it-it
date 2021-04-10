---
title: Messaggio LVM_SORTITEMSEX (COMmctrl. h)
description: Usa una funzione di confronto definita dall'applicazione per ordinare gli elementi di un controllo di visualizzazione elenco. L'indice di ogni elemento viene modificato per riflettere la nuova sequenza. È possibile inviare questo messaggio in modo esplicito o usando la \_ macro SortItemsEx di ListView.
ms.assetid: eab2f6f5-68fd-4cb6-acf4-cb267ee40fdc
keywords:
- Controlli di Windows Message LVM_SORTITEMSEX
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
ms.openlocfilehash: 99e524b00cb5ff1260eb68e7d86e185e5ae60c75
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104047931"
---
# <a name="lvm_sortitemsex-message"></a>\_Messaggio SORTITEMSEX LVM

Usa una funzione di confronto definita dall'applicazione per ordinare gli elementi di un controllo di visualizzazione elenco. L'indice di ogni elemento viene modificato per riflettere la nuova sequenza. È possibile inviare questo messaggio in modo esplicito o usando la macro [**\_ SortItemsEx di ListView**](/windows/desktop/api/Commctrl/nf-commctrl-listview_sortitemsex) .

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

Restituisce **true** se l'operazione ha esito positivo o **false** in caso contrario.

## <a name="remarks"></a>Commenti

La funzione di confronto ha il formato seguente:

``` syntax
int CALLBACK CompareFunc(LPARAM lParam1, LPARAM lParam2, LPARAM lParamSort);  
```

Questo messaggio è simile a [**LVM \_ SORTITEMS**](lvm-sortitems.md), eccetto il tipo di informazioni passate alla funzione di confronto. Con **LVM \_ SORTITEMSEX**, *lParam1* è l'indice corrente del primo elemento e *lParam2* è l'indice corrente del secondo elemento. Se necessario, è possibile inviare un messaggio [**LVM \_ GETITEMTEXT**](lvm-getitemtext.md) per recuperare altre informazioni su un elemento.

La funzione di confronto deve restituire un valore negativo se il primo elemento deve precedere il secondo, un valore positivo se il primo elemento deve seguire il secondo oppure zero se i due elementi sono equivalenti.

> [!Note]  
> Durante il processo di ordinamento, il contenuto della visualizzazione elenco è instabile. Se la funzione di callback invia messaggi al controllo visualizzazione elenco oltre a [**LVM \_ GetItem**](lvm-getitem.md) ([**ListView \_ GetItem**](/windows/desktop/api/Commctrl/nf-commctrl-listview_getitem)), i risultati sono imprevedibili.

 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                        |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2003\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





