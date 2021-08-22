---
title: WM_COMPAREITEM messaggio (Winuser.h)
description: Inviato per determinare la posizione relativa di un nuovo elemento nell'elenco ordinato di una casella combinata o di una casella di riepilogo disegnata dal proprietario.
ms.assetid: 22882730-9fd6-4b45-a563-d7b00ed26564
keywords:
- WM_COMPAREITEM dei controlli Windows messaggio
topic_type:
- apiref
api_name:
- WM_COMPAREITEM
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 819df3c4dd36c784ef5747d4aa4cdf688b3a48dbd052254192a7c98574bbfa94
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119655771"
---
# <a name="wm_compareitem-message"></a>Messaggio \_ COMPAREITEM WM

Inviato per determinare la posizione relativa di un nuovo elemento nell'elenco ordinato di una casella combinata o di una casella di riepilogo disegnata dal proprietario. Ogni volta che l'applicazione aggiunge un nuovo elemento, il sistema invia questo messaggio al proprietario di una casella combinata o di una casella di riepilogo creata con lo stile [**CBS \_ SORT**](combo-box-styles.md) o [**LBS \_ SORT.**](list-box-styles.md)


```C++
WM_COMPAREITEM

    WPARAM wParam;
    LPARAM lParam; 
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>

Specifica l'identificatore del controllo che ha inviato il **messaggio \_ COMPAREITEM WM.**

</dd> <dt>

*lParam* 
</dt> <dd>

Puntatore a [**una struttura COMPAREITEMSTRUCT**](/windows/win32/api/winuser/ns-winuser-compareitemstruct) che contiene gli identificatori e i dati forniti dall'applicazione per due elementi nella casella combinata o di riepilogo.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Il valore restituito indica la posizione relativa dei due elementi. Può trattarsi di uno dei valori illustrati nella tabella seguente.



| Codice restituito                                                                          | Descrizione                                                  |
|--------------------------------------------------------------------------------------|--------------------------------------------------------------|
| <dl> <dt>**Valore**</dt> </dl> | Significato<br/>                                           |
| <dl> <dt>**-1**</dt> </dl>    | L'elemento 1 precede l'elemento 2 nell'ordinamento.<br/>       |
| <dl> <dt>**0**</dt> </dl>     | Gli elementi 1 e 2 sono equivalenti nell'ordinamento.<br/> |
| <dl> <dt>**1**</dt> </dl>     | L'elemento 1 segue l'elemento 2 nell'ordinamento.<br/>        |



 

## <a name="remarks"></a>Commenti

Quando il proprietario di una casella combinata o di una casella di riepilogo disegnata dal proprietario riceve questo messaggio, il proprietario restituisce un valore che indica quale degli elementi specificati dalla struttura [**COMPAREITEMSTRUCT**](/windows/win32/api/winuser/ns-winuser-compareitemstruct) verrà visualizzato prima dell'altro. In genere, il sistema invia questo messaggio più volte fino a quando non determina la posizione esatta per il nuovo elemento.

Se il messaggio viene gestito da una routine della finestra di dialogo, è necessario eseguire il cast del valore restituito desiderato in un valore **BOOL** e restituire direttamente il valore. Il valore MSGRESULT DWL \_ impostato dalla funzione [**SetWindowLong**](/windows/desktop/api/winuser/nf-winuser-setwindowlonga) viene ignorato.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop Vista\]<br/>                                                           |
| Server minimo supportato<br/> | Windows Solo app desktop di Server 2003 \[\]<br/>                                                     |
| Intestazione<br/>                   | <dl> <dt>Winuser.h (includere Windows.h)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

**Riferimento**
</dt> <dt>

[**COMPAREITEMSTRUCT**](/windows/win32/api/winuser/ns-winuser-compareitemstruct)
</dt> <dt>

**Altre risorse**
</dt> <dt>

[**Setwindowlong**](/windows/desktop/api/winuser/nf-winuser-setwindowlonga)
</dt> </dl>

 

