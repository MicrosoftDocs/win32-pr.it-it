---
title: Messaggio LB_SETTABSTOPS (winuser. h)
description: Imposta le posizioni di interruzione di tabulazione in una casella di riepilogo.
ms.assetid: b96b974e-b1e6-4361-98bb-4dc21c752690
keywords:
- Controlli di Windows Message LB_SETTABSTOPS
topic_type:
- apiref
api_name:
- LB_SETTABSTOPS
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f21927aaf82624242e8d42ef4a7459f1e36cdf74
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103874333"
---
# <a name="lb_settabstops-message"></a>\_Messaggio SETTABSTOPS lb

Imposta le posizioni di interruzione di tabulazione in una casella di riepilogo.

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>

Specifica il numero di arresti tabulari.

</dd> <dt>

*lParam* 
</dt> <dd>

Puntatore al primo membro di una matrice di numeri interi contenenti le tabulazioni. I numeri interi rappresentano il numero di trimestri della larghezza media dei caratteri per il tipo di carattere selezionato nella casella di riepilogo. Ad esempio, una tabulazione di 4 viene posizionata a 1,0 unità di caratteri e una tabulazione di 6 viene posizionata a 1,5 unità di caratteri medie. Tuttavia, se la casella di riepilogo fa parte di una finestra di dialogo, i numeri interi si trovano in unità modello di finestra di dialogo. Le tabulazioni devono essere ordinate in ordine crescente. le schede con le versioni precedenti non sono consentite.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se tutte le schede specificate sono impostate, il valore restituito è **true**; in caso contrario, è **false**.

## <a name="remarks"></a>Commenti

Per rispondere al messaggio **lb \_ SETTABSTOPS** , è necessario che la casella di riepilogo sia stata creata con lo stile [**\_ USETABSTOPS lbs**](list-box-styles.md) .

Se *wParam* è 0 e *lParam* è **null**, la tabulazione predefinita è due unità modello di finestra di dialogo. Se *wParam* è 1, la casella di riepilogo disporrà di tabulazioni separate dalla distanza specificata da *lParam*.

Se *lParam* punta a più di un valore singolo, viene impostata una tabulazione per ogni valore in *lParam*, fino al numero specificato da *wParam*.

I valori specificati da *lParam* si trovano nelle unità dei modelli di finestra di dialogo, ovvero le unità indipendenti dal dispositivo utilizzate nei modelli di finestra di dialogo. Per convertire le misurazioni dalle unità del modello di finestra di dialogo alle unità dello schermo (pixel), usare la funzione [**MapDialogRect**](/windows/desktop/api/winuser/nf-winuser-mapdialogrect) .

Windows 95/Windows 98/Windows Millennium Edition (Windows Me): il buffer a cui punta *lParam* deve risiedere nella memoria scrivibile, anche se il messaggio non modifica la matrice.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                                           |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2003\]<br/>                                                     |
| Intestazione<br/>                   | <dl> <dt>Winuser. h (include Windows. h)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**MapDialogRect**](/windows/desktop/api/winuser/nf-winuser-mapdialogrect)
</dt> </dl>

 

