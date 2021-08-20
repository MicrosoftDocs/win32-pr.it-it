---
title: PSN_WIZNEXT di notifica (Prsht.h)
description: Notifica a una pagina che l'utente ha fatto clic sul pulsante Avanti in una procedura guidata. Questo codice di notifica viene inviato sotto forma di messaggio WM \_ NOTIFY.
ms.assetid: ff5be154-f2d1-403d-8f22-8f6cacfb66b1
keywords:
- PSN_WIZNEXT del codice di notifica Windows controlli
topic_type:
- apiref
api_name:
- PSN_WIZNEXT
api_location:
- Prsht.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: dead2de1e21631b2b8e13cb54e3ee45d5d3bc29f2234380c31ec134c3790eae7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118169631"
---
# <a name="psn_wiznext-notification-code"></a>Codice di notifica \_ PSN WIZNEXT

Notifica a una pagina che l'utente ha fatto clic sul **pulsante** Avanti in una procedura guidata. Questo codice di notifica viene inviato sotto forma di messaggio [**WM \_ NOTIFY.**](wm-notify.md)


```C++
PSN_WIZNEXT 

    lppsn = (LPPSHNOTIFY) lParam; 
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*lParam* 
</dt> <dd>

Puntatore a [**una struttura PSHNOTIFY**](/windows/desktop/api/Prsht/ns-prsht-pshnotify) che contiene informazioni sul codice di notifica. Questa struttura contiene una [**struttura NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) come primo membro, **hdr**. Il **membro hwndFrom** di questa **struttura NMHDR** contiene l'handle per la finestra delle proprietà. Il **membro lParam** della **struttura PSHNOTIFY** non contiene informazioni.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituire 0 per consentire alla procedura guidata di passare alla pagina successiva. Restituire -1 per impedire alla procedura guidata di modificare le pagine. Per visualizzare una pagina specifica, restituire l'identificatore di risorsa della finestra di dialogo. Se il dialogo è stato specificato con il flag [**\_ DLGINDIRECT PSP,**](/windows/desktop/api/Prsht/ns-prsht-propsheetpagea_v2) questa notifica restituisce il puntatore al modello di dialogo.

## <a name="remarks"></a>Commenti

Per impostare il valore restituito, la routine della finestra di dialogo per la pagina deve chiamare la [**funzione SetWindowLong**](/windows/desktop/api/winuser/nf-winuser-setwindowlonga) con il **valore \_ MSGRESULT DWL** e restituire **TRUE.** Esempio:

``` syntax
case PSN_WIZNEXT :
    SetWindowLong(hDlg, DWL_MSGRESULT, 0);
    break;

case PSN_WIZBACK :
    ...
```

> [!Note]  
> La finestra delle proprietà è in corso di modifica dell'elenco di pagine quando viene inviato il codice di notifica \_ PSN WIZNEXT. È possibile aggiungere, inserire o rimuovere pagine in risposta a questi codici di notifica, ma è necessario fare particolare attenzione se si inseriscono o rimuovono pagine prima della pagina corrente.

 

Se si inseriscono o rimuovono pagine prima della pagina corrente, è necessario restituire (tramite **DWL \_ MSGRESULT**) un valore diverso da zero per specificare la nuova pagina desiderata. Si noti, tuttavia, che se si inserisce o si rimuove una pagina che si trova prima della pagina corrente (con un indice più piccolo rispetto alla pagina corrente), [PSN \_ KILLACTIVE](psn-killactive.md) potrebbe essere inviato alla pagina errata.

Per questo motivo, è consigliabile che le procedure guidate che aggiungono e rimuovono le pagine in modo dinamico in risposta a \_ PSN WIZNEXT e [PSN \_ WIZBACK](psn-wizback.md) lo facciano solo alle pagine alla fine dell'elenco. Se si vuole che la procedura guidata rimova le pagine in modo accurato, mantenere le pagine dinamiche alla fine dell'elenco e tornare alle pagine permanenti prima di eliminarle.

Si supponga, ad esempio, che una procedura guidata sia costituita da una pagina introduttiva, da una serie di pagine dinamiche e da una pagina di completamento e che si desideri eliminare le pagine dinamiche quando l'utente raggiunge la pagina di completamento.

1.  La procedura guidata inizierà con due pagine, "Introduction" e "Completion". L'utente inizia nella pagina "Introduzione".
    1.  Introduzione (l'utente è qui)
    2.  Completion
2.  Quando l'utente si sposta da "Introduzione", la procedura guidata aggiunge le pagine dinamiche e posiziona l'utente nella prima pagina dinamica, restituisce (tramite **DWL \_ MSGRESULT)** l'identificatore della finestra di dialogo della pagina "Dynamic 1". In questo esempio sono presenti tre pagine dinamiche.
    1.  Introduzione
    2.  Completion
    3.  Dinamico 1 (l'utente è qui)
    4.  Dinamico 2
    5.  Dinamico 3
3.  Dopo che l'utente passa attraverso le pagine dinamiche a "Dynamic 3" e quindi passa alla pagina successiva, l'applicazione deve inserire l'utente nella pagina "Completion" (Completamento). Anche in questo caso, viene restituito (tramite **DWL \_ MSGRESULT)** l'identificatore della finestra di dialogo della pagina "Completion".
    1.  Introduzione
    2.  Completamento (l'utente è qui)
    3.  Dinamico 1
    4.  Dinamico 2
    5.  Dinamico 3
4.  L'applicazione può quindi rimuovere le tre pagine dinamiche (numerate da tre a cinque) in modo sicuro.
    1.  Introduzione
    2.  Completamento (l'utente è qui)

Si noti che questa tecnica è necessaria solo se la procedura guidata rimuove le pagine in modo dinamico. Se la procedura guidata aggiunge pagine solo dinamicamente, questo processo non è necessario.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop Vista\]<br/>                                     |
| Server minimo supportato<br/> | Windows Solo app desktop di Server 2003 \[\]<br/>                               |
| Intestazione<br/>                   | <dl> <dt>Prsht.h</dt> </dl> |



 

