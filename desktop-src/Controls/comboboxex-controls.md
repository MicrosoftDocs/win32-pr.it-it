---
title: Informazioni sui controlli ComboBoxEx
description: I controlli ComboBoxEx sono controlli casella combinata che forniscono supporto nativo per le immagini degli elementi.
ms.assetid: a4b1aa79-40c4-4eff-801c-4f308d86fb35
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 993fa8db73246c62f8ceee805e767c13ffdcc15a12d0222e09f308324cc97bab
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117831837"
---
# <a name="about-comboboxex-controls"></a>Informazioni sui controlli ComboBoxEx

I controlli ComboBoxEx sono controlli casella combinata che forniscono supporto nativo per le immagini degli elementi. Per rendere facilmente accessibili le immagini degli elementi, il controllo fornisce il supporto per l'elenco di immagini. Usando questo controllo, è possibile fornire la funzionalità di una casella combinata senza dover disegnare manualmente elementi grafici.

In questo argomento sono contenute le sezioni seguenti.

-   [Creazione di controlli ComboBoxEx](#creating-comboboxex-controls)
-   [Stili del controllo ComboBoxEx](#comboboxex-control-styles)
-   [Elementi del controllo ComboBoxEx](#comboboxex-control-items)
-   [Elementi di callback](#callback-items)
-   [Elenchi di immagini del controllo ComboBoxEx](#comboboxex-control-image-lists)
-   [Informazioni sui messaggi di notifica del controllo ComboBoxEx](#about-comboboxex-control-notification-messages)
-   [Inoltro dei messaggi del controllo ComboBoxEx](#comboboxex-control-message-forwarding)

## <a name="creating-comboboxex-controls"></a>Creazione di controlli ComboBoxEx

In effetti, un controllo ComboBoxEx crea una casella combinata figlio ed esegue automaticamente le attività di disegno del proprietario in base a un elenco di immagini assegnato. Pertanto, [**lo stile CBS \_ OWNERDRAWFIXED**](combo-box-styles.md) è implicito e non è necessario usarlo durante la creazione del controllo. Poiché gli elenchi di immagini vengono utilizzati per fornire elementi grafici, non è possibile utilizzare lo stile [**CBS \_ OWNERDRAWVARIABLE.**](combo-box-styles.md)

Un controllo ComboBoxEx deve essere inizializzato chiamando la [**funzione InitCommonControlsEx,**](/windows/desktop/api/Commctrl/nf-commctrl-initcommoncontrolsex) specificando le classi ICC USEREX nella struttura \_ \_ [**INITCOMMONCONTROLSEX**](/windows/win32/api/commctrl/ns-commctrl-initcommoncontrolsex) associata.

Puoi creare un controllo ComboBoxEx usando la [**funzione CreateWindowEx**](/windows/desktop/api/winuser/nf-winuser-createwindowexa) e specificando [**WC \_ COMBOBOXEX**](common-control-window-classes.md) come classe window. La classe viene registrata quando viene chiamata [**la funzione InitCommonControlsEx**](/windows/desktop/api/Commctrl/nf-commctrl-initcommoncontrolsex) come illustrato in precedenza.

I controlli ComboBoxEx vengono creati senza un elenco di immagini predefinito. Per usare le immagini degli elementi, è necessario creare un elenco di immagini per il controllo ComboBoxEx e assegnarlo al controllo usando il [**messaggio CBEM \_ SETIMAGELIST.**](cbem-setimagelist.md) Se non si assegna un elenco di immagini al controllo ComboBoxEx, il controllo visualizza solo il testo dell'elemento.

## <a name="comboboxex-control-styles"></a>Stili del controllo ComboBoxEx

I controlli ComboBoxEx supportano solo gli stili ComboBox seguenti:

-   CBS \_ SIMPLE
-   ELENCO A DISCESA DI \_ CBS
-   ELENCO A DISCESA DI \_ CBS
-   WS \_ CHILD

Esistono anche diversi [stili estesi del controllo ComboBoxEx](comboboxex-control-extended-styles.md) usati solo da ComboBoxEx.

> [!Note]  
> In [**alcuni \_ casi,**](combo-box-styles.md) lo stile SIMPLE di CBS potrebbe non funzionare correttamente.

 

Poiché il controllo ComboBoxEx esegue automaticamente attività di disegno del proprietario in base a un elenco di immagini assegnato, lo stile [**\_ OWNERDRAWFIXED**](combo-box-styles.md) di CBS è implicito e non è necessario usarlo durante la creazione del controllo. Poiché gli elenchi di immagini vengono utilizzati per fornire elementi grafici, non è possibile utilizzare lo stile [**CBS \_ OWNERDRAWVARIABLE.**](combo-box-styles.md) Il controllo ComboBoxEx supporta anche gli stili [estesi del controllo ComboBoxEx](comboboxex-control-extended-styles.md) che forniscono funzionalità aggiuntive.

## <a name="comboboxex-control-items"></a>Elementi del controllo ComboBoxEx

I controlli ComboBoxEx gestiscono le informazioni sugli elementi usando [**una struttura COMBOBOXEXITEM.**](/windows/win32/api/commctrl/ns-commctrl-comboboxexitema) Questa struttura include membri per indici di elementi, indici di immagini (normale, stato di selezione e sovrimpressione), valori di rientro, stringhe di testo e valori specifici dell'elemento.

Il controllo ComboBoxEx consente di accedere e modificare facilmente gli elementi tramite la messaggistica. Per aggiungere o eliminare un elemento, inviare il [**messaggio CBEM \_ INSERTITEM**](cbem-insertitem.md) o [**CBEM \_ DELETEITEM.**](cbem-deleteitem.md) È possibile modificare gli elementi attualmente nel controllo usando il [**messaggio \_ CBEM SETITEM.**](cbem-setitem.md)

## <a name="callback-items"></a>Elementi di callback

I controlli ComboBoxEx supportano gli attributi degli elementi di callback. È possibile specificare un elemento come elemento di callback quando lo si aggiunge al controllo usando [**CBEM \_ INSERTITEM.**](cbem-insertitem.md) Quando si assegnano valori alla struttura [**COMBOBOXEXITEM**](/windows/win32/api/commctrl/ns-commctrl-comboboxexitema) di un elemento, è necessario specificare i valori dei flag di callback appropriati. Di seguito sono riportati **i membri della struttura COMBOBOXEXITEM** e i valori dei flag di callback corrispondenti.



| Membro             | Valore di callback      |
|--------------------|---------------------|
| **pszText**        | LPSTR \_ TEXTCALLBACK |
| **iImage**         | I \_ IMAGECALLBACK    |
| **iSelectedImage** | I \_ IMAGECALLBACK    |
| **iOverlay**       | I \_ IMAGECALLBACK    |
| **iIndent**        | I \_ INDENTCALLBACK   |



 

Il controllo richiederà informazioni sugli elementi di callback inviando codici [di notifica CBEN \_ GETDISPINFO.](cben-getdispinfo.md) Questa notifica viene inviata sotto forma di messaggio [**WM \_ NOTIFY.**](wm-notify.md) Quando l'applicazione elabora questo messaggio, deve fornire le informazioni richieste per il controllo. Se si imposta il membro **mask** della struttura [**COMBOBOXEXITEM**](/windows/win32/api/commctrl/ns-commctrl-comboboxexitema) associata su CBEIF DI SETITEM, il controllo archivierà i dati dell'elemento e non li \_ \_ richiederà di nuovo.

## <a name="comboboxex-control-image-lists"></a>Elenchi di immagini del controllo ComboBoxEx

Se vuoi che un controllo ComboBoxEx visualizza le icone con elementi, devi fornire un elenco di immagini. I controlli ComboBoxEx supportano fino a tre immagini per un elemento, una per lo stato selezionato, una per lo stato non selezionato e una per un'immagine di sovrimpressione. Assegnare un elenco di immagini esistente a un controllo ComboBoxEx usando il [**messaggio CBEM \_ SETIMAGELIST.**](cbem-setimagelist.md)

La [**struttura COMBOBOXEXITEM**](/windows/win32/api/commctrl/ns-commctrl-comboboxexitema) contiene membri che rappresentano gli indici delle immagini per ogni elenco di immagini (selezionato, non selezionato e sovrimpressione). Per ogni elemento, impostare questi membri per visualizzare le immagini desiderate. Non è necessario specificare indici di immagine per ogni tipo di immagine. È possibile combinare e associare i tipi di immagine nel modo che si desidera, ma impostare sempre il membro **mask** della struttura **COMBOBOXEXITEM** per indicare quali membri vengono usati. Il controllo ignora i membri che non sono stati contrassegnati come validi.

> [!Note]  
> Se si usa lo [**stile SIMPLE di CBS, \_**](combo-box-styles.md) le icone non vengono visualizzate.

 

## <a name="about-comboboxex-control-notification-messages"></a>Informazioni sui messaggi di notifica del controllo ComboBoxEx

Un controllo ComboBoxEx invia messaggi di notifica per segnalare le modifiche all'interno di se stesso o per richiedere informazioni sull'elemento di callback. L'elemento padre del controllo riceve tutti [**i messaggi WM \_ COMMAND**](/windows/desktop/menurc/wm-command) dalla casella combinata contenuta nel controllo ComboBoxEx. Il controllo ComboBoxEx invia le proprie notifiche usando [**messaggi WM \_ NOTIFY.**](wm-notify.md) Di conseguenza, il proprietario del controllo deve essere preparato per elaborare entrambe le forme di messaggi di notifica.

Di seguito sono riportati i codici di notifica specifici di ComboBoxEx inviati tramite messaggi [**WM \_ NOTIFY.**](wm-notify.md)



| Notifica                              | **Descrizione**                                                                                                            |
|-------------------------------------------|----------------------------------------------------------------------------------------------------------------------------|
| [CBEN \_ BEGINEDIT](cben-beginedit.md)     | Segnala che l'utente ha attivato l'elenco a discesa o ha fatto clic nella casella di modifica del controllo.                               |
| [CBEN \_ ENDEDIT](cben-endedit.md)         | Segnala che l'utente ha selezionato un elemento dall'elenco a discesa o ha terminato un'operazione di modifica all'interno della casella di modifica. |
| [CBEN \_ DELETEITEM](cben-deleteitem.md)   | Segnala che un elemento è stato eliminato.                                                                                          |
| [CBEN \_ GETDISPINFO](cben-getdispinfo.md) | Richiede informazioni sugli attributi di un elemento.                                                                           |
| [CBEN \_ INSERTITEM](cben-insertitem.md)   | Segnala che un elemento è stato inserito nel controllo .                                                                          |



 

## <a name="comboboxex-control-message-forwarding"></a>Inoltro dei messaggi del controllo ComboBoxEx

Di seguito sono riportati i messaggi della casella combinata standard che un controllo ComboBoxEx inoltra alla casella combinata figlio. Alcuni di questi messaggi possono essere elaborati dal controllo ComboBoxEx prima o dopo l'inoltro del messaggio.

-   [**CB \_ DELETESTRING**](cb-deletestring.md)
-   [**CB \_ FINDSTRINGEXACT**](cb-findstringexact.md)
-   [**CB \_ GETCOUNT**](cb-getcount.md)
-   [**CB \_ GETCURSEL**](cb-getcursel.md)
-   [**CB \_ GETDROPPEDCONTROLRECT**](cb-getdroppedcontrolrect.md)
-   [**CB \_ GETDROPPEDSTATE**](cb-getdroppedstate.md)
-   [**CB \_ GETITEMDATA**](cb-getitemdata.md)
-   [**CB \_ GETITEMHEIGHT**](cb-getitemheight.md)
-   [**CB \_ GETLBTEXT**](cb-getlbtext.md)
-   [**CB \_ GETLBTEXTLEN**](cb-getlbtextlen.md)
-   [**CB \_ GETEXTENDEDUI**](cb-getextendedui.md)
-   [**CB \_ LIMITTEXT**](cb-limittext.md)
-   [**CB \_ RESETCONTENT**](cb-resetcontent.md)
-   [**CB \_ SETCURSEL**](cb-setcursel.md)
-   [**CB \_ SETDROPPEDWIDTH**](cb-setdroppedwidth.md)
-   [**CB \_ SETEXTENDEDUI**](cb-setextendedui.md)
-   [**CB \_ SETITEMDATA**](cb-setitemdata.md)
-   [**CB \_ SETITEMHEIGHT**](cb-setitemheight.md)
-   [**CB \_ SHOWDROPDOWN**](cb-showdropdown.md)

Di seguito sono riportati i messaggi di windows che un controllo ComboBoxEx inoltra alla finestra padre:

-   [**WM \_ COMMAND**](/windows/desktop/menurc/wm-command) (include tutte le notifiche \_ CBN).
-   [**WM \_ NOTIFY**](wm-notify.md)

 

 