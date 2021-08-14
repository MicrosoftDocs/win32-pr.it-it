---
title: Controllo ComboBoxEx
description: Questa sezione contiene informazioni sugli elementi di programmazione usati con i controlli ComboBoxEx.
ms.assetid: vs|controls|~\controls\comboex\reflist.htm
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ded6ff945424f63baaf0063ce5d8897f84883d5063989aa6c7a9fb1a4f76a704
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118413464"
---
# <a name="comboboxex-control"></a>Controllo ComboBoxEx

Questa sezione contiene informazioni sugli elementi di programmazione usati con i controlli ComboBoxEx.

### <a name="overviews"></a>Cenni preliminari



| Argomento                                                | Contenuto                                                                                           |
|------------------------------------------------------|----------------------------------------------------------------------------------------------------|
| [Informazioni sui controlli ComboBoxEx](comboboxex-controls.md) | I controlli ComboBoxEx sono controlli casella combinata che forniscono supporto nativo per le immagini degli elementi.<br/> |
| [Uso dei controlli ComboBoxEx](using-comboboxex.md)    | Questa sezione contiene codice di esempio e informazioni su come usare i controlli ComboBoxEx.<br/> |



 

### <a name="messages"></a>Messaggi



| Argomento                                                   | Contenuto                                                                                                                                                                                                   |
|---------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**CBEM \_ DELETEITEM**](cbem-deleteitem.md)             | Rimuove un elemento da un controllo ComboBoxEx. <br/>                                                                                                                                                     |
| [**CBEM \_ GETCOMBOCONTROL**](cbem-getcombocontrol.md)   | Ottiene l'handle per il controllo casella combinata figlio. <br/>                                                                                                                                                |
| [**CBEM \_ GETEDITCONTROL**](cbem-geteditcontrol.md)     | Ottiene l'handle per la parte del controllo di modifica di un controllo ComboBoxEx. Un controllo ComboBoxEx usa una casella di modifica quando è impostato sullo stile elenco a discesa [**CBS. \_**](combo-box-styles.md) <br/> |
| [**CBEM \_ GETEXTENDEDSTYLE**](cbem-getextendedstyle.md) | Ottiene gli stili estesi in uso per un controllo ComboBoxEx. <br/>                                                                                                                             |
| [**CBEM \_ GETIMAGELIST**](cbem-getimagelist.md)         | Ottiene l'handle a un elenco di immagini assegnato a un controllo ComboBoxEx. <br/>                                                                                                                             |
| [**CBEM \_ GETITEM**](cbem-getitem.md)                   | Ottiene informazioni sull'elemento per un determinato elemento ComboBoxEx.<br/>                                                                                                                                              |
| [**CBEM \_ GETUNICODEFORMAT**](cbem-getunicodeformat.md) | Ottiene il flag di formato carattere UNICODE per il controllo . <br/>                                                                                                                                        |
| [**CBEM \_ HASEDITCHANGED**](cbem-haseditchanged.md)     | Determina se l'utente ha modificato il testo di un controllo di modifica ComboBoxEx.<br/>                                                                                                                  |
| [**CBEM \_ INSERTITEM**](cbem-insertitem.md)             | Inserisce un nuovo elemento in un controllo ComboBoxEx. <br/>                                                                                                                                                    |
| [**CBEM \_ KILLCOMBOFOCUS**](cbem-killcombofocus.md)     | Questo messaggio non è implementato. <br/>                                                                                                                                                               |
| [**CBEM \_ SETCOMBOFOCUS**](cbem-setcombofocus.md)       | Questo messaggio non è implementato. <br/>                                                                                                                                                               |
| [**CBEM \_ SETEXTENDEDSTYLE**](cbem-setextendedstyle.md) | Imposta gli stili estesi all'interno di un controllo ComboBoxEx. <br/>                                                                                                                                              |
| [**CBEM \_ SETIMAGELIST**](cbem-setimagelist.md)         | Imposta un elenco di immagini per un controllo ComboBoxEx. <br/>                                                                                                                                                   |
| [**CBEM \_ SETITEM**](cbem-setitem.md)                   | Imposta gli attributi per un elemento in un controllo ComboBoxEx. <br/>                                                                                                                                       |
| [**CBEM \_ SETUNICODEFORMAT**](cbem-setunicodeformat.md) | Imposta il flag di formato carattere UNICODE per il controllo . Questo messaggio consente di modificare il set di caratteri utilizzato dal controllo in fase di esecuzione anziché dover creare nuovamente il controllo. <br/>      |
| [**CBEM \_ SETWINDOWTHEME**](cbem-setwindowtheme.md)     | Imposta lo stile di visualizzazione di un controllo ComboBoxEx.<br/>                                                                                                                                                  |



 

### <a name="notifications"></a>Notifiche



| Argomento                                                      | Contenuto                                                                                                                                                                                                                                                     |
|------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [CBEN \_ BEGINEDIT](cben-beginedit.md)                      | Inviato quando l'utente attiva l'elenco a discesa o fa clic nella casella di modifica del controllo. Questo codice di notifica viene inviato sotto forma di messaggio [**WM \_ NOTIFY.**](wm-notify.md) <br/>                                                                    |
| [CBEN \_ DELETEITEM](cben-deleteitem.md)                    | Inviato quando un elemento è stato eliminato. Questo codice di notifica viene inviato sotto forma di messaggio [**WM \_ NOTIFY.**](wm-notify.md) <br/>                                                                                                                     |
| [CBEN \_ DRAGBEGIN](cben-dragbegin.md)                      | Inviato quando l'utente inizia a trascinare l'immagine dell'elemento visualizzato nella parte di modifica del controllo. Questo codice di notifica viene inviato sotto forma di messaggio [**WM \_ NOTIFY.**](wm-notify.md) <br/>                                                  |
| [CBEN \_ ENDEDIT](cben-endedit.md)                          | Inviato quando l'utente ha terminato un'operazione all'interno della casella di modifica o ha selezionato un elemento dall'elenco a discesa del controllo. Questo codice di notifica viene inviato sotto forma di messaggio [**WM \_ NOTIFY.**](wm-notify.md)<br/>                             |
| [CBEN \_ GETDISPINFO](cben-getdispinfo.md)                  | Inviato per recuperare le informazioni di visualizzazione relative a un elemento di callback. Questo codice di notifica viene inviato sotto forma di messaggio [**WM \_ NOTIFY.**](wm-notify.md) <br/>                                                                                             |
| [CBEN \_ INSERTITEM](cben-insertitem.md)                    | Inviato quando viene inserito un nuovo elemento nel controllo . Questo codice di notifica viene inviato sotto forma di messaggio [**WM \_ NOTIFY.**](wm-notify.md) <br/>                                                                                                  |
| [NM \_ SETCURSOR (ComboBoxEx)](nm-setcursor-comboboxex-.md) | Notifica alla finestra padre di un controllo ComboBoxEx che il controllo sta impostando il cursore in risposta a un [**messaggio WM \_ SETCURSOR.**](/windows/desktop/menurc/wm-setcursor) Questo codice di notifica viene inviato sotto forma di messaggio [**WM \_ NOTIFY.**](wm-notify.md) <br/> |



 

### <a name="structures"></a>Strutture



| Argomento                                    | Contenuto                                                                                                                                                                                     |
|------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**COMBOBOXEXITEM**](/windows/win32/api/commctrl/ns-commctrl-comboboxexitema) | Contiene informazioni su un elemento in un controllo ComboBoxEx.<br/>                                                                                                                       |
| [**NMCBEDRAGBEGIN**](/windows/desktop/api/Commctrl/ns-commctrl-nmcbedragbegina) | Contiene informazioni utilizzate con il [codice di notifica CBEN \_ DRAGBEGIN.](cben-dragbegin.md) <br/>                                                                                      |
| [**NMCBEENDEDIT**](/windows/desktop/api/Commctrl/ns-commctrl-nmcbeendedita)     | Contiene informazioni sulla conclusione di un'operazione di modifica all'interno di un controllo ComboBoxEx. Questa struttura viene usata con il [codice di notifica \_ ENDEDIT CBEN.](cben-endedit.md) <br/> |
| [**NMCOMBOBOXEX**](/windows/desktop/api/Commctrl/ns-commctrl-nmcomboboxexa)     | Contiene informazioni specifiche per gli elementi ComboBoxEx da usare con i codici di notifica. <br/>                                                                                               |



 

### <a name="constants"></a>Costanti



| Argomento                                                                        | Contenuto                                                                                                                  |
|------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------|
| [Stili estesi del controllo ComboBoxEx](comboboxex-control-extended-styles.md) | Supportare gli stili estesi elencati in questa sezione e la maggior parte degli stili di controllo casella combinata standard.<br/> |



 

 

