---
title: Codice di notifica PSN_WIZBACK (Prsht. h)
description: Notifica a una pagina che l'utente ha fatto clic sul pulsante indietro in una procedura guidata. Questo codice di notifica viene inviato sotto forma di messaggio di \_ notifica WM.
ms.assetid: 784f92e7-6f10-40fc-b513-bea022f13ae1
keywords:
- Controlli di Windows per il codice di notifica PSN_WIZBACK
topic_type:
- apiref
api_name:
- PSN_WIZBACK
api_location:
- Prsht.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: aed1cdd742d78473266db07899796de5a5450310
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103873290"
---
# <a name="psn_wizback-notification-code"></a>\_Codice di notifica WIZBACK PSN

Notifica a una pagina che l'utente ha fatto clic sul pulsante **indietro** in una procedura guidata. Questo codice di notifica viene inviato sotto forma di messaggio [**di \_ notifica WM**](wm-notify.md) .


```C++
PSN_WIZBACK 

    lppsn = (LPPSHNOTIFY) lParam; 
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*lParam* 
</dt> <dd>

Puntatore a una struttura [**PSHNOTIFY**](/windows/desktop/api/Prsht/ns-prsht-pshnotify) contenente informazioni sul codice di notifica. Questa struttura contiene una struttura [**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) come primo membro, **HDR**. Il membro **hwndFrom** della struttura **NMHDR** contiene l'handle per la finestra delle proprietà. Il membro **lParam** della struttura **PSHNOTIFY** non contiene informazioni.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce 0 per consentire alla procedura guidata di passare alla pagina precedente. Restituisce-1 per impedire la modifica delle pagine da parte della procedura guidata. Per visualizzare una pagina specifica, restituire il relativo identificatore di risorsa della finestra di dialogo. Se la finestra di dialogo è stata specificata con il flag [**\_ DLGINDIRECT di PSP**](/windows/desktop/api/Prsht/ns-prsht-propsheetpagea_v2) , questa notifica restituisce il puntatore al modello di finestra di dialogo.

## <a name="remarks"></a>Commenti

Per impostare il valore restituito, la routine della finestra di dialogo per la pagina deve chiamare la funzione [**SetWindowLong**](/windows/desktop/api/winuser/nf-winuser-setwindowlonga) con il valore **\_ MSGRESULT di DWL** e restituire **true**. Ad esempio:

``` syntax
case PSN_WIZBACK :
    SetWindowLong(hDlg, DWL_MSGRESULT, 0);
    break;

case PSN_WIZNEXT :
    ...
```

> [!Note]  
> La finestra delle proprietà è in corso di modifica dell'elenco di pagine quando \_ viene inviato il codice di notifica WIZBACK PSN. È possibile aggiungere, inserire o rimuovere pagine in risposta a questi codici di notifica, ma è necessario prestare particolare attenzione se si inseriscono o si rimuovono le pagine prima della pagina corrente.

 

Se si inseriscono o si rimuovono pagine prima della pagina corrente, è necessario restituire (tramite **DWL \_ MSGRESULT**) un valore diverso da zero per specificare la nuova pagina desiderata. Si noti, tuttavia, che se si inserisce o si rimuove una pagina che si trova prima della pagina corrente (con un indice più piccolo rispetto alla pagina corrente), è possibile che [PSN \_ KILLACTIVE](psn-killactive.md) venga inviato alla pagina errata.

Per questo motivo, è consigliabile che le procedure guidate che aggiungono e rimuovano le pagine in modo dinamico in risposta a [PSN \_ WIZNEXT](psn-wiznext.md) e PSN WIZBACK eseguano questa \_ operazione solo per le pagine alla fine dell'elenco. Se si desidera che la procedura guidata rimuova le pagine in modo accurato, lasciare le pagine dinamiche alla fine dell'elenco e tornare alle pagine permanenti prima di eliminarle.

Si supponga, ad esempio, che una procedura guidata sia costituita da una pagina introduttiva, una serie di pagine dinamiche e una pagina di completamento e si desidera eliminare le pagine dinamiche quando l'utente raggiunge la pagina di completamento.

1.  La procedura guidata inizierà con due pagine, "Introduction" e "complete". L'utente inizia nella pagina "Introduzione".
    1.  Introduzione (utente qui)
    2.  Completion
2.  Quando l'utente si sposta da "Introduzione", la procedura guidata aggiunge le pagine dinamiche e inserisce l'utente nella prima pagina dinamica restituendo (tramite **DWL \_ MSGRESULT**) l'identificatore della finestra di dialogo "Dynamic 1". In questo esempio sono disponibili tre pagine dinamiche.
    1.  Introduzione
    2.  Completion
    3.  Dinamica 1 (utente qui)
    4.  Dinamica 2
    5.  Dinamica 3
3.  Quando l'utente passa attraverso le pagine dinamiche a "Dynamic 3" e passa alla pagina successiva, l'applicazione deve inserire l'utente nella pagina "completamento". Anche in questo caso, questa operazione viene eseguita restituendo (tramite **DWL \_ MSGRESULT**) l'identificatore della finestra di dialogo della pagina "completamento".
    1.  Introduzione
    2.  Completamento (utente qui)
    3.  Dinamica 1
    4.  Dinamica 2
    5.  Dinamica 3
4.  L'applicazione può quindi rimuovere le tre pagine dinamiche, numerate da tre a cinque, in modo sicuro.
    1.  Introduzione
    2.  Completamento (utente qui)

Si noti che questa tecnica è necessaria solo se la procedura guidata rimuove le pagine in modo dinamico. Se la procedura guidata aggiunge pagine in modo dinamico, questo processo non è necessario.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                     |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2003\]<br/>                               |
| Intestazione<br/>                   | <dl> <dt>Prsht. h</dt> </dl> |



 

