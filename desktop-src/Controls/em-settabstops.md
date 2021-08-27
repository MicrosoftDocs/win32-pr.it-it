---
title: EM_SETTABSTOPS messaggio (Winuser.h)
description: Il messaggio EM \_ SETTABSTOPS imposta i tabulazioni in un controllo di modifica su più righe.
ms.assetid: d6fe2828-4ae9-4652-ace0-2f71e146f777
keywords:
- EM_SETTABSTOPS controlli Windows messaggio
topic_type:
- apiref
api_name:
- EM_SETTABSTOPS
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c2bf8285bbc8830f784b6cf2cf6671634bf4339a418c163bc3962150d6cb6674
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120048081"
---
# <a name="em_settabstops-message"></a>Messaggio \_ EM SETTABSTOPS

Il **messaggio EM \_ SETTABSTOPS** imposta i tabulazioni in un controllo di modifica su più righe. Quando il testo viene copiato nel controllo, qualsiasi carattere di tabulazione nel testo causa la generazione di spazio fino alla tabulazione successiva.

Questo messaggio viene elaborato solo da controlli di modifica su più righe. È possibile inviare questo messaggio a un controllo di modifica o a un controllo Rich Edit.

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>

Numero di tabulazioni contenute nella matrice. Se questo parametro è zero, il *parametro lParam* viene ignorato e le tabulazioni predefinite vengono impostate ogni 32 unità del modello di finestra di dialogo. Se questo parametro è 1, le tabulazioni vengono impostate ogni *n* unità del modello di dialogo, dove *n* è la distanza a cui punta *il parametro lParam.* Se questo parametro è maggiore di 1, *lParam è* un puntatore a una matrice di tabulazioni.

</dd> <dt>

*lParam* 
</dt> <dd>

Puntatore a una matrice di interi senza segno che specificano i tabulazioni, in unità del modello di finestra di dialogo. Se il *parametro wParam* è 1, questo parametro è un puntatore a un intero senza segno contenente la distanza tra tutte le tabulazioni, in unità del modello di finestra di dialogo.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se tutte le schede sono impostate, il valore restituito è **TRUE.**

Se tutte le schede non sono impostate, il valore restituito è **FALSE.**

## <a name="remarks"></a>Commenti

Il **messaggio EM \_ SETTABSTOPS** non ridisegna automaticamente la finestra di controllo di modifica. Se l'applicazione modifica le tabulazioni per il testo già presente nel controllo di modifica, deve chiamare la funzione [**InvalidateRect**](/windows/desktop/api/winuser/nf-winuser-invalidaterect) per ridisegnare la finestra del controllo di modifica.

I valori specificati nella matrice sono in unità del modello di finestra di dialogo, ovvero le unità indipendenti dal dispositivo usate nei modelli di finestra di dialogo. Per convertire le misurazioni dalle unità del modello di finestra di dialogo alle unità dello schermo (pixel), usare la [**funzione MapDialogRect.**](/windows/desktop/api/winuser/nf-winuser-mapdialogrect)

**Rich Edit:** Supportato in Microsoft Rich Edit 3.0 e versioni successive. Un controllo Rich Edit può avere il numero massimo di tabulazioni specificato da MAX \_ TAB \_ STOPS. Per informazioni sulla compatibilità delle versioni rich edit con le varie versioni di sistema, vedere [Informazioni sui controlli Rich Edit.](about-rich-edit-controls.md)

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop Vista\]<br/>                                                           |
| Server minimo supportato<br/> | Windows Solo app desktop di Server 2003 \[\]<br/>                                                     |
| Intestazione<br/>                   | <dl> <dt>Winuser.h (includere Windows.h)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

**Altre risorse**
</dt> <dt>

[**InvalidateRect**](/windows/desktop/api/winuser/nf-winuser-invalidaterect)
</dt> <dt>

[**MapDialogRect**](/windows/desktop/api/winuser/nf-winuser-mapdialogrect)
</dt> </dl>

 

