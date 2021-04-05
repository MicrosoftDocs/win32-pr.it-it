---
title: Informazioni sui controlli ComboBoxEx
description: I controlli ComboBoxEx sono controlli casella combinata che forniscono il supporto nativo per le immagini di elementi.
ms.assetid: a4b1aa79-40c4-4eff-801c-4f308d86fb35
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 427abef015474047d1842d13e5fb40640d0406c5
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/21/2020
ms.locfileid: "103873030"
---
# <a name="about-comboboxex-controls"></a>Informazioni sui controlli ComboBoxEx

I controlli ComboBoxEx sono controlli casella combinata che forniscono il supporto nativo per le immagini di elementi. Per rendere facilmente accessibili le immagini degli elementi, il controllo fornisce supporto per l'elenco immagini. Utilizzando questo controllo, è possibile fornire la funzionalità di una casella combinata senza dover tracciare manualmente la grafica dell'elemento.

In questo argomento sono contenute le sezioni seguenti.

-   [Creazione di controlli ComboBoxEx](#creating-comboboxex-controls)
-   [Stili del controllo ComboBoxEx](#comboboxex-control-styles)
-   [Elementi di controllo ComboBoxEx](#comboboxex-control-items)
-   [Elementi di callback](#callback-items)
-   [Elenchi di immagini del controllo ComboBoxEx](#comboboxex-control-image-lists)
-   [Informazioni sui messaggi di notifica del controllo ComboBoxEx](#about-comboboxex-control-notification-messages)
-   [ComboBoxEx controllo di invio messaggi](#comboboxex-control-message-forwarding)

## <a name="creating-comboboxex-controls"></a>Creazione di controlli ComboBoxEx

In realtà, un controllo ComboBoxEx crea una casella combinata figlio ed esegue Owner Draw attività in base a un elenco di immagini assegnato. Di conseguenza, lo stile [**\_ OwnerDrawFixed CBS**](combo-box-styles.md) è implicito e non è necessario usarlo durante la creazione del controllo. Poiché gli elenchi di immagini vengono usati per fornire elementi grafici, lo stile [**\_ OwnerDrawVariable CBS**](combo-box-styles.md) non può essere usato.

È necessario inizializzare un controllo ComboBoxEx chiamando la funzione [**InitCommonControlsEx**](/windows/desktop/api/Commctrl/nf-commctrl-initcommoncontrolsex) , specificando le \_ classi USEREX ICC \_ nella struttura [**InitCommonControlsEx**](/windows/win32/api/commctrl/ns-commctrl-initcommoncontrolsex) associata.

È possibile creare un controllo ComboBoxEx usando la funzione [**CreateWindowEx**](/windows/desktop/api/winuser/nf-winuser-createwindowexa) e specificando [**WC \_ ComboBoxEx**](common-control-window-classes.md) come classe della finestra. La classe viene registrata quando viene chiamata la funzione [**InitCommonControlsEx**](/windows/desktop/api/Commctrl/nf-commctrl-initcommoncontrolsex) come illustrato in precedenza.

I controlli ComboBoxEx vengono creati senza un elenco di immagini predefinito. Per usare le immagini degli elementi, è necessario creare un elenco di immagini per il controllo ComboBoxEx e assegnarlo al controllo usando il messaggio CBEM dell'elenco di immagini. [**\_**](cbem-setimagelist.md) Se non si assegna un elenco di immagini al controllo ComboBoxEx, il controllo Visualizza solo il testo dell'elemento.

## <a name="comboboxex-control-styles"></a>Stili del controllo ComboBoxEx

I controlli ComboBoxEx supportano solo gli stili ComboBox seguenti:

-   \_semplice CBS
-   \_elenco a discesa CBS
-   \_DropDownList CBS
-   WS \_ figlio

Sono disponibili anche diversi [stili estesi del controllo ComboBoxEx](comboboxex-control-extended-styles.md) che vengono usati solo da ComboBoxEx.

> [!Note]  
> In alcuni casi, lo stile [**\_ semplice CBS**](combo-box-styles.md) potrebbe non funzionare correttamente.

 

Poiché il controllo ComboBoxEx esegue automaticamente le attività Owner Draw in base a un elenco di immagini assegnato, lo stile [**\_ OwnerDrawFixed CBS**](combo-box-styles.md) è implicito e non è necessario usarlo durante la creazione del controllo. Poiché gli elenchi di immagini vengono usati per fornire elementi grafici, lo stile [**\_ OwnerDrawVariable CBS**](combo-box-styles.md) non può essere usato. Il controllo ComboBoxEx supporta anche gli [stili estesi del controllo ComboBoxEx](comboboxex-control-extended-styles.md) che forniscono funzionalità aggiuntive.

## <a name="comboboxex-control-items"></a>Elementi di controllo ComboBoxEx

I controlli ComboBoxEx gestiscono le informazioni sugli elementi usando una struttura [**COMBOBOXEXITEM**](/windows/win32/api/commctrl/ns-commctrl-comboboxexitema) . Questa struttura include i membri per gli indici degli elementi, gli indici delle immagini (normale, lo stato di selezione e la sovrapposizione), i valori di rientro, le stringhe di testo e i valori specifici dell'elemento.

Il controllo ComboBoxEx consente di accedere e modificare facilmente gli elementi attraverso la messaggistica. Per aggiungere o eliminare un elemento, inviare il messaggio [**CBEM \_ INSERTITEM**](cbem-insertitem.md) o [**CBEM \_ DeleteItem**](cbem-deleteitem.md) . È possibile modificare gli elementi attualmente presenti nel controllo utilizzando [**il \_ messaggio CBEM**](cbem-setitem.md) .

## <a name="callback-items"></a>Elementi di callback

I controlli ComboBoxEx supportano gli attributi degli elementi di callback. È possibile specificare un elemento come elemento di callback quando lo si aggiunge al controllo utilizzando [**CBEM \_ INSERTITEM**](cbem-insertitem.md). Quando si assegnano valori alla struttura [**COMBOBOXEXITEM**](/windows/win32/api/commctrl/ns-commctrl-comboboxexitema) di un elemento, è necessario specificare i valori dei flag di callback appropriati. Di seguito sono riportati i membri della struttura **COMBOBOXEXITEM** e i valori dei flag di callback corrispondenti.



| Membro             | Valore callback      |
|--------------------|---------------------|
| **pszText**        | \_TEXTCALLBACK LPSTR |
| **iImage**         | \_IMAGECALLBACK    |
| **iSelectedImage** | \_IMAGECALLBACK    |
| **iOverlay**       | \_IMAGECALLBACK    |
| **iIndent**        | \_INDENTCALLBACK   |



 

Il controllo richiederà informazioni sugli elementi di callback inviando i codici di notifica di [CBEN \_ GETDISPINFO](cben-getdispinfo.md) . Questa notifica viene inviata sotto forma di messaggio di [**\_ notifica WM**](wm-notify.md) . Quando l'applicazione elabora il messaggio, deve fornire le informazioni richieste per il controllo. Se si imposta il membro **mask** della struttura [**COMBOBOXEXITEM**](/windows/win32/api/commctrl/ns-commctrl-comboboxexitema) associata su CBEIF \_ di \_ SetItem, il controllo archivia i dati dell'elemento e non ne richiederà nuovamente la richiesta.

## <a name="comboboxex-control-image-lists"></a>Elenchi di immagini del controllo ComboBoxEx

Se si vuole che un controllo ComboBoxEx visualizzi le icone con gli elementi, è necessario fornire un elenco di immagini. I controlli ComboBoxEx supportano fino a tre immagini per un elemento, uno per lo stato selezionato, uno per lo stato non selezionato e uno per un'immagine sovrapposta. Assegnare un elenco di immagini esistente a un controllo ComboBoxEx usando il messaggio CBEM dell'elenco di immagini. [**\_**](cbem-setimagelist.md)

La struttura [**COMBOBOXEXITEM**](/windows/win32/api/commctrl/ns-commctrl-comboboxexitema) contiene membri che rappresentano gli indici delle immagini per ogni elenco di immagini (selezionato, non selezionato e sovrapposto). Per ogni elemento, impostare i membri in modo da visualizzare le immagini desiderate. Non è necessario specificare gli indici delle immagini per ogni tipo di immagine. È possibile combinare e abbinare i tipi di immagine nel modo desiderato, ma impostare sempre il membro **mask** della struttura **COMBOBOXEXITEM** per indicare i membri da usare. Il controllo Ignora i membri che non sono stati contrassegnati come validi.

> [!Note]  
> Se si usa lo [**stile \_ semplice CBS**](combo-box-styles.md) , le icone non vengono visualizzate.

 

## <a name="about-comboboxex-control-notification-messages"></a>Informazioni sui messaggi di notifica del controllo ComboBoxEx

Un controllo ComboBoxEx invia messaggi di notifica per segnalare le modifiche all'interno o per richiedere informazioni sull'elemento di callback. L'elemento padre del controllo riceve tutti i messaggi di [**\_ comando WM**](/windows/desktop/menurc/wm-command) dalla casella combinata contenuta nel controllo ComboBoxEx. Il controllo ComboBoxEx Invia notifiche personalizzate usando i messaggi di [**\_ notifica WM**](wm-notify.md) . Di conseguenza, il proprietario del controllo deve essere preparato per elaborare entrambe le forme di messaggi di notifica.

Di seguito sono riportati i codici di notifica specifici di ComboBoxEx inviati tramite i messaggi di [**\_ notifica WM**](wm-notify.md) .



| Notifica                              | **Descrizione**                                                                                                            |
|-------------------------------------------|----------------------------------------------------------------------------------------------------------------------------|
| [\_BEGINEDIT CBEN](cben-beginedit.md)     | Segnala che l'utente ha attivato l'elenco a discesa o ha fatto clic nella casella di modifica del controllo.                               |
| [\_ENDEDIT CBEN](cben-endedit.md)         | Segnala che l'utente ha selezionato un elemento dall'elenco a discesa o ha concluso un'operazione di modifica all'interno della casella di modifica. |
| [\_DeleteItem CBEN](cben-deleteitem.md)   | Segnala che un elemento è stato eliminato.                                                                                          |
| [\_GETDISPINFO CBEN](cben-getdispinfo.md) | Richiede informazioni sugli attributi di un elemento.                                                                           |
| [CBEN \_ INSERTITEM](cben-insertitem.md)   | Segnala che un elemento è stato inserito nel controllo.                                                                          |



 

## <a name="comboboxex-control-message-forwarding"></a>ComboBoxEx controllo di invio messaggi

Di seguito sono riportati i messaggi della casella combinata standard che un controllo ComboBoxEx invia alla relativa casella combinata figlio. Alcuni di questi messaggi possono essere elaborati dal controllo ComboBoxEx prima o dopo l'invio del messaggio.

-   [**CB \_ DELETESTRING**](cb-deletestring.md)
-   [**CB \_ FindExactString**](cb-findstringexact.md)
-   [**CONTEGGIO di CB \_**](cb-getcount.md)
-   [**CB \_ GETcursel**](cb-getcursel.md)
-   [**CB \_ GETDROPPEDCONTROLRECT**](cb-getdroppedcontrolrect.md)
-   [**CB \_ GETDROPPEDSTATE**](cb-getdroppedstate.md)
-   [**CB \_ GETITEMDATA**](cb-getitemdata.md)
-   [**CB \_ GETITEMHEIGHT**](cb-getitemheight.md)
-   [**CB \_ GETLBTEXT**](cb-getlbtext.md)
-   [**CB \_ GETLBTEXTLEN**](cb-getlbtextlen.md)
-   [**CB \_ GETEXTENDEDUI**](cb-getextendedui.md)
-   [**CB \_ LIMITTEXT**](cb-limittext.md)
-   [**CB \_ ResetContent**](cb-resetcontent.md)
-   [**\_CAcursel CB**](cb-setcursel.md)
-   [**CB \_ SETDROPPEDWIDTH**](cb-setdroppedwidth.md)
-   [**CB \_ SETEXTENDEDUI**](cb-setextendedui.md)
-   [**CB \_ SETITEMDATA**](cb-setitemdata.md)
-   [**CB \_ SETITEMHEIGHT**](cb-setitemheight.md)
-   [**CB \_ SHOWDROPDOWN**](cb-showdropdown.md)

Di seguito sono riportati i messaggi di Windows che un controllo ComboBoxEx invia alla relativa finestra padre:

-   [**WM \_ (Incluse**](/windows/desktop/menurc/wm-command) tutte le \_ notifiche CBN).
-   [**\_notifica WM**](wm-notify.md)

 

 