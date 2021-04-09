---
title: Controllo ComboBoxEx
description: Questa sezione contiene informazioni sugli elementi di programmazione usati con i controlli ComboBoxEx.
ms.assetid: vs|controls|~\controls\comboex\reflist.htm
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7d5a926ccf2f9f5b5bb68e040731d6b9d8e37ee8
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/09/2021
ms.locfileid: "103969119"
---
# <a name="comboboxex-control"></a>Controllo ComboBoxEx

Questa sezione contiene informazioni sugli elementi di programmazione usati con i controlli ComboBoxEx.

### <a name="overviews"></a>Cenni preliminari



| Argomento                                                | Contenuto                                                                                           |
|------------------------------------------------------|----------------------------------------------------------------------------------------------------|
| [Informazioni sui controlli ComboBoxEx](comboboxex-controls.md) | I controlli ComboBoxEx sono controlli casella combinata che forniscono il supporto nativo per le immagini di elementi.<br/> |
| [Uso di controlli ComboBoxEx](using-comboboxex.md)    | Questa sezione contiene il codice di esempio e le informazioni su come usare i controlli ComboBoxEx.<br/> |



 

### <a name="messages"></a>Messaggi



| Argomento                                                   | Contenuto                                                                                                                                                                                                   |
|---------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**\_DeleteItem CBEM**](cbem-deleteitem.md)             | Rimuove un elemento da un controllo ComboBoxEx. <br/>                                                                                                                                                     |
| [**\_GETCOMBOCONTROL CBEM**](cbem-getcombocontrol.md)   | Ottiene l'handle per il controllo casella combinata figlio. <br/>                                                                                                                                                |
| [**\_GETEDITCONTROL CBEM**](cbem-geteditcontrol.md)     | Ottiene l'handle per la parte del controllo di modifica di un controllo ComboBoxEx. Un controllo ComboBoxEx usa una casella di modifica quando è impostata sullo stile [**a \_ discesa CBS**](combo-box-styles.md) . <br/> |
| [**\_GETEXTENDEDSTYLE CBEM**](cbem-getextendedstyle.md) | Ottiene gli stili estesi utilizzati per un controllo ComboBoxEx. <br/>                                                                                                                             |
| [**CBEM \_ GETimages**](cbem-getimagelist.md)         | Ottiene l'handle per un elenco di immagini assegnato a un controllo ComboBoxEx. <br/>                                                                                                                             |
| [**GetItem CBEM \_**](cbem-getitem.md)                   | Ottiene le informazioni sugli elementi per un elemento ComboBoxEx specificato.<br/>                                                                                                                                              |
| [**\_GETUNICODEFORMAT CBEM**](cbem-getunicodeformat.md) | Ottiene il flag del formato carattere UNICODE per il controllo. <br/>                                                                                                                                        |
| [**\_HASEDITCHANGED CBEM**](cbem-haseditchanged.md)     | Determina se l'utente ha modificato il testo di un controllo di modifica ComboBoxEx.<br/>                                                                                                                  |
| [**CBEM \_ INSERTITEM**](cbem-insertitem.md)             | Inserisce un nuovo elemento in un controllo ComboBoxEx. <br/>                                                                                                                                                    |
| [**\_KILLCOMBOFOCUS CBEM**](cbem-killcombofocus.md)     | Questo messaggio non è implementato. <br/>                                                                                                                                                               |
| [**\_SETCOMBOFOCUS CBEM**](cbem-setcombofocus.md)       | Questo messaggio non è implementato. <br/>                                                                                                                                                               |
| [**\_SETEXTENDEDSTYLE CBEM**](cbem-setextendedstyle.md) | Imposta gli stili estesi in un controllo ComboBoxEx. <br/>                                                                                                                                              |
| [**CBEM \_**](cbem-setimagelist.md)         | Imposta un elenco di immagini per un controllo ComboBoxEx. <br/>                                                                                                                                                   |
| [**CBEM ( \_ elemento)**](cbem-setitem.md)                   | Imposta gli attributi per un elemento in un controllo ComboBoxEx. <br/>                                                                                                                                       |
| [**\_SETUNICODEFORMAT CBEM**](cbem-setunicodeformat.md) | Imposta il flag di formato carattere UNICODE per il controllo. Questo messaggio consente di modificare il set di caratteri utilizzato dal controllo in fase di esecuzione anziché dover ricreare il controllo. <br/>      |
| [**\_SETWINDOWTHEME CBEM**](cbem-setwindowtheme.md)     | Imposta lo stile di visualizzazione di un controllo ComboBoxEx.<br/>                                                                                                                                                  |



 

### <a name="notifications"></a>Notifiche



| Argomento                                                      | Contenuto                                                                                                                                                                                                                                                     |
|------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [\_BEGINEDIT CBEN](cben-beginedit.md)                      | Inviato quando l'utente attiva l'elenco a discesa o fa clic nella casella di modifica del controllo. Questo codice di notifica viene inviato sotto forma di messaggio [**di \_ notifica WM**](wm-notify.md) . <br/>                                                                    |
| [\_DeleteItem CBEN](cben-deleteitem.md)                    | Inviato quando un elemento è stato eliminato. Questo codice di notifica viene inviato sotto forma di messaggio [**di \_ notifica WM**](wm-notify.md) . <br/>                                                                                                                     |
| [\_DRAGBEGIN CBEN](cben-dragbegin.md)                      | Inviato quando l'utente inizia a trascinare l'immagine dell'elemento visualizzato nella parte di modifica del controllo. Questo codice di notifica viene inviato sotto forma di messaggio [**di \_ notifica WM**](wm-notify.md) . <br/>                                                  |
| [\_ENDEDIT CBEN](cben-endedit.md)                          | Inviato quando l'utente ha concluso un'operazione all'interno della casella di modifica o ha selezionato un elemento dall'elenco a discesa del controllo. Questo codice di notifica viene inviato sotto forma di messaggio [**di \_ notifica WM**](wm-notify.md) .<br/>                             |
| [\_GETDISPINFO CBEN](cben-getdispinfo.md)                  | Inviato per recuperare le informazioni di visualizzazione relative a un elemento di callback. Questo codice di notifica viene inviato sotto forma di messaggio [**di \_ notifica WM**](wm-notify.md) . <br/>                                                                                             |
| [CBEN \_ INSERTITEM](cben-insertitem.md)                    | Inviato quando un nuovo elemento è stato inserito nel controllo. Questo codice di notifica viene inviato sotto forma di messaggio [**di \_ notifica WM**](wm-notify.md) . <br/>                                                                                                  |
| [\_Cursore Nm (ComboBoxEx)](nm-setcursor-comboboxex-.md) | Notifica alla finestra padre di un controllo ComboBoxEx che il controllo sta impostando il cursore in risposta a un messaggio del [**\_ cursore WM**](/windows/desktop/menurc/wm-setcursor) . Questo codice di notifica viene inviato sotto forma di messaggio [**di \_ notifica WM**](wm-notify.md) . <br/> |



 

### <a name="structures"></a>Strutture



| Argomento                                    | Contenuto                                                                                                                                                                                     |
|------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**COMBOBOXEXITEM**](/windows/win32/api/commctrl/ns-commctrl-comboboxexitema) | Contiene informazioni su un elemento in un controllo ComboBoxEx.<br/>                                                                                                                       |
| [**NMCBEDRAGBEGIN**](/windows/desktop/api/Commctrl/ns-commctrl-nmcbedragbegina) | Contiene informazioni usate con il codice di notifica [ \_ DRAGBEGIN di CBEN](cben-dragbegin.md) . <br/>                                                                                      |
| [**NMCBEENDEDIT**](/windows/desktop/api/Commctrl/ns-commctrl-nmcbeendedita)     | Contiene informazioni sulla conclusione di un'operazione di modifica all'interno di un controllo ComboBoxEx. Questa struttura viene utilizzata con il codice di notifica di [CBEN \_ ENDEDIT](cben-endedit.md) . <br/> |
| [**NMCOMBOBOXEX**](/windows/desktop/api/Commctrl/ns-commctrl-nmcomboboxexa)     | Contiene informazioni specifiche per gli elementi ComboBoxEx da utilizzare con i codici di notifica. <br/>                                                                                               |



 

### <a name="constants"></a>Costanti



| Argomento                                                                        | Contenuto                                                                                                                  |
|------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------|
| [Stili estesi del controllo ComboBoxEx](comboboxex-control-extended-styles.md) | Supportare gli stili estesi elencati in questa sezione, nonché la maggior parte degli stili standard del controllo casella combinata.<br/> |



 

 

