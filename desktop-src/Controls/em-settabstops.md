---
title: Messaggio EM_SETTABSTOPS (winuser. h)
description: Il \_ messaggio SETTABSTOPS em imposta la tabulazione in un controllo di modifica su più righe.
ms.assetid: d6fe2828-4ae9-4652-ace0-2f71e146f777
keywords:
- Controlli di Windows Message EM_SETTABSTOPS
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
ms.openlocfilehash: 48d076dea415f169eff46101fd7cfe632d73d976
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104120126"
---
# <a name="em_settabstops-message"></a>\_Messaggio SETTABSTOPS em

Il **messaggio \_ SETTABSTOPS em** imposta la tabulazione in un controllo di modifica su più righe. Quando il testo viene copiato nel controllo, qualsiasi carattere di tabulazione nel testo causa la generazione dello spazio fino alla tabulazione successiva.

Questo messaggio viene elaborato solo dai controlli di modifica su più righe. Questo messaggio può essere inviato a un controllo di modifica o a un controllo Rich Edit.

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>

Numero di arresti di tabulazione contenuti nella matrice. Se questo parametro è zero, il parametro *lParam* viene ignorato e le tabulazioni predefinite vengono impostate in ogni unità del modello di finestra di dialogo 32. Se questo parametro è 1, le tabulazioni vengono impostate in ogni *n* unità modello di finestra di dialogo, dove *n* è la distanza a cui punta il parametro *lParam* . Se questo parametro è maggiore di 1, *lParam* è un puntatore a una matrice di tabulazioni.

</dd> <dt>

*lParam* 
</dt> <dd>

Puntatore a una matrice di interi senza segno che specifica le tabulazioni, nelle unità del modello di finestra di dialogo. Se il parametro *wParam* è 1, questo parametro è un puntatore a un Unsigned Integer che contiene la distanza tra tutti i punti di tabulazione, nelle unità del modello di finestra di dialogo.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se tutte le schede sono impostate, il valore restituito è **true**.

Se tutte le schede non sono impostate, il valore restituito è **false**.

## <a name="remarks"></a>Commenti

Il **messaggio \_ SETTABSTOPS em** non ridisegnato automaticamente la finestra di controllo di modifica. Se l'applicazione sta cambiando la tabulazione per il testo già presente nel controllo di modifica, deve chiamare la funzione [**InvalidateRect**](/windows/desktop/api/winuser/nf-winuser-invalidaterect) per ricreare la finestra di controllo di modifica.

I valori specificati nella matrice si trovano nelle unità dei modelli di finestra di dialogo, ovvero le unità indipendenti dal dispositivo utilizzate nei modelli di finestra di dialogo. Per convertire le misurazioni dalle unità del modello di finestra di dialogo alle unità dello schermo (pixel), usare la funzione [**MapDialogRect**](/windows/desktop/api/winuser/nf-winuser-mapdialogrect) .

**Modifica avanzata:** Supportato in Microsoft Rich Edit 3,0 e versioni successive. Un controllo Rich Edit può includere il numero massimo di interruzioni di tabulazioni specificato da MAX \_ Tab \_ stops. Per informazioni sulla compatibilità delle versioni Rich Edit con le varie versioni di sistema, vedere [informazioni sui controlli Rich Edit](about-rich-edit-controls.md).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                                           |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2003\]<br/>                                                     |
| Intestazione<br/>                   | <dl> <dt>Winuser. h (include Windows. h)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

**Altre risorse**
</dt> <dt>

[**InvalidateRect**](/windows/desktop/api/winuser/nf-winuser-invalidaterect)
</dt> <dt>

[**MapDialogRect**](/windows/desktop/api/winuser/nf-winuser-mapdialogrect)
</dt> </dl>

 

