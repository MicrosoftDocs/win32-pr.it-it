---
description: L'area di notifica è una parte della barra delle applicazioni che fornisce un'origine temporanea per le notifiche e lo stato.
ms.assetid: D37E2BF7-1887-4780-81AD-85B2117321E4
title: Notifiche e area di notifica
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 89af1d0b8af0b41674f79325f0eeb389cbc8f2c1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104344141"
---
# <a name="notifications-and-the-notification-area"></a>Notifiche e area di notifica

L'area di notifica è una parte della barra delle applicazioni che fornisce un'origine temporanea per le notifiche e lo stato. Può anche essere usato per visualizzare le icone per le funzionalità di sistema e di programma che non hanno presenza sul desktop, ad esempio il livello di batteria, il controllo del volume e lo stato della rete. L'area di notifica è nota storicamente come area di stato o barra di sistema.

In questo argomento sono incluse le sezioni seguenti:

-   [Linee guida per le notifiche e l'area di notifica](#notification-and-notification-area-guidelines)
-   [Creazione e visualizzazione di una notifica](#notifications-and-the-notification-area)
    -   [Aggiungere un'icona di notifica](#add-a-notification-icon)
    -   [Definire la versione di NOTIFYICONDATA](#define-the-notifyicondata-version)
    -   [Definire l'aspetto e il contenuto della notifica](#define-the-notification-look-and-contents)
    -   [Verificare lo stato utente](#check-the-user-status)
    -   [Visualizza la notifica](#display-the-notification)
    -   [Rimozione di un'icona](#removing-an-icon)
-   [Esempio SDK](#sdk-sample)
-   [Argomenti correlati](#related-topics)

## <a name="notification-and-notification-area-guidelines"></a>Linee guida per le notifiche e l'area di notifica

Vedere le sezioni [notifiche](../uxguide/mess-notif.md) e [area di notifica](../uxguide/winenv-notification.md) delle linee guida sull'interazione dell'esperienza utente di Windows per le procedure consigliate per l'uso delle notifiche e dell'area di notifica. L'obiettivo è fornire il vantaggio dell'utente tramite l'uso appropriato delle notifiche, senza irritare o distrazione.

L'area di notifica non è destinata a informazioni critiche che devono essere eseguite immediatamente. Non è inoltre concepito per l'accesso rapido a programmi o comandi. A partire da Windows 7, gran parte di queste funzionalità viene eseguita in modo ottimale tramite il pulsante della barra delle applicazioni di un'applicazione.

Windows 7 consente a un utente di disattivare tutte le notifiche da un'applicazione, se scelgono, in modo da consentirne la progettazione e l'utilizzo in modo che l'utente possa continuare a visualizzarle. Le notifiche sono un'interruzione; Assicurarsi che valga la pena.

In Windows 7 è stato introdotto il concetto di "tempo di inquieto". Il tempo di attesa è definito come prima ora dopo che un nuovo utente accede al proprio account per la prima volta o per la prima volta dopo un aggiornamento del sistema operativo o un'installazione pulita. Questo tempo è accantonato per consentire all'utente di esplorare e acquisire familiarità con il nuovo ambiente senza la distrazione delle notifiche. Durante questo periodo, la maggior parte delle notifiche non deve essere inviata o visualizzata. Le eccezioni includono il feedback che l'utente si aspetta di vedere in risposta a un'azione dell'utente, ad esempio quando inserisce un dispositivo USB o stampa un documento. Le specifiche dell'API relative al tempo di indisponibilità sono descritte più avanti in questo argomento.

## <a name="creating-and-displaying-a-notification"></a>Creazione e visualizzazione di una notifica

Le sezioni rimanenti di questo argomento illustrano la procedura di base da seguire per visualizzare una notifica dall'applicazione all'utente.

1.  [Aggiungere un'icona di notifica](#add-a-notification-icon)
2.  [Definire la versione di NOTIFYICONDATA](#define-the-notifyicondata-version)
3.  [Definire l'aspetto e il contenuto della notifica](#define-the-notification-look-and-contents)
4.  [Verificare lo stato utente](#check-the-user-status)
5.  [Visualizza la notifica](#display-the-notification)
6.  [Rimozione di un'icona](#removing-an-icon)

### <a name="add-a-notification-icon"></a>Aggiungere un'icona di notifica

Per visualizzare una notifica, è necessario disporre di un'icona nell'area di notifica. In alcuni casi, ad esempio Microsoft Communicator o il livello di batteria, tale icona sarà già presente. In molti altri casi, tuttavia, verrà aggiunta un'icona all'area di notifica solo se è necessario per visualizzare la notifica. In entrambi i casi, questa operazione viene eseguita utilizzando la funzione [**\_ NotifyIcon della shell**](/windows/desktop/api/Shellapi/nf-shellapi-shell_notifyicona) . **Shell \_ di NotifyIcon** consente di aggiungere, modificare o eliminare un'icona nell'area di notifica.

![area di notifica contenente tre icone](images/taskbar/notificationareaicons.png)

Quando un'icona viene aggiunta all'area di notifica in Windows 7, viene aggiunta alla sezione overflow dell'area di notifica per impostazione predefinita. Quest'area contiene icone dell'area di notifica attive, ma non visibili nell'area di notifica. Solo l'utente può alzare di livello un'icona dall'overflow all'area di notifica, sebbene in determinate circostanze il sistema possa promuovere temporaneamente un'icona nell'area di notifica come anteprima breve (in un minuto).

> [!Note]  
> L'utente deve avere la parola finale sulle icone che desidera visualizzare nell'area di notifica. Prima di installare un'icona non temporanea nell'area di notifica, all'utente viene richiesta l'autorizzazione. È anche necessario specificare l'opzione (normalmente se il menu di scelta rapida) per rimuovere l'icona dall'area di notifica.

 

La struttura [**NOTIFYICONDATA**](/windows/desktop/api/Shellapi/ns-shellapi-notifyicondataa) inviata nella chiamata a [**Shell \_ NotifyIcon**](/windows/desktop/api/Shellapi/nf-shellapi-shell_notifyicona) contiene informazioni che specificano sia l'icona dell'area di notifica che la notifica stessa. Di seguito sono riportati gli elementi specifici dell'icona dell'area di notifica, che possono essere impostati tramite **NOTIFYICONDATA**.

-   Risorsa da cui viene acquisita l'icona.
-   Identificatore univoco per l'icona.
-   Stile della descrizione comando dell'icona.
-   Stato dell'icona (nascosto, condiviso o entrambi) nell'area di notifica.
-   Handle di una finestra dell'applicazione associata all'icona.
-   Identificatore del messaggio di callback che consente all'icona di comunicare gli eventi che si verificano all'interno del rettangolo di delimitazione dell'icona e la notifica dell'aerostato con la finestra dell'applicazione associata. Il rettangolo di delimitazione dell'icona può essere recuperato tramite la [**Shell \_ NotifyIconGetRect**](/windows/desktop/api/Shellapi/nf-shellapi-shell_notifyicongetrect).

Ogni icona nell'area di notifica può essere identificata in due modi:

-   GUID con cui l'icona viene dichiarata nel registro di sistema. Questo è il metodo preferito in Windows 7 e versioni successive.
-   Handle di una finestra associata all'icona dell'area di notifica, oltre a un identificatore di icona definito dall'applicazione. Questo metodo viene utilizzato in Windows Vista e versioni precedenti.

Le icone nell'area di notifica possono avere una descrizione comando. La descrizione comando può essere una descrizione comando standard (scelta consigliata) o un'interfaccia utente popup disegnata dall'applicazione. Sebbene non sia necessario, è consigliabile usare una descrizione comando.

Le icone dell'area di notifica devono essere compatibili con i valori DPI alti. Un'applicazione deve fornire sia un'icona di pixel 16x16 che un'icona 32x32 nel file di risorse, quindi usare [**LoadIconMetric**](/windows/win32/api/commctrl/nf-commctrl-loadiconmetric) per assicurarsi che l'icona corretta venga caricata e ridimensionata in modo appropriato.

L'applicazione responsabile dell'icona dell'area di notifica deve gestire un clic del mouse per l'icona. Quando un utente fa clic con il pulsante destro del mouse sull'icona, deve visualizzare un menu di scelta rapida normale. Tuttavia, il risultato di un solo clic con il pulsante sinistro del mouse può variare in funzione dell'icona. Dovrebbe visualizzare le informazioni che l'utente dovrebbe visualizzare nel formato più adatto al contenuto, ovvero una finestra popup, una finestra di dialogo o la finestra del programma. Ad esempio, potrebbe visualizzare il testo di stato per un'icona di stato o un dispositivo di scorrimento per il controllo volume.

La posizione di una finestra popup o di una finestra di dialogo risultante dal clic deve essere posizionata vicino alla coordinata del clic nell'area di notifica. Usare [**CalculatePopupWindowPosition**](/windows/win32/api/winuser/nf-winuser-calculatepopupwindowposition) per determinarne la posizione.

L'icona può essere aggiunta all'area di notifica senza visualizzare una notifica definendo solo i membri specifici dell'icona di [**NOTIFYICONDATA**](/windows/desktop/api/Shellapi/ns-shellapi-notifyicondataa) (sopra illustrata) e chiamando l'oggetto [**\_ NotifyIcon della shell**](/windows/desktop/api/Shellapi/nf-shellapi-shell_notifyicona) come illustrato di seguito:


```
NOTIFYICONDATA nid = {};
// Do NOT set the NIF_INFO flag.
...                    
Shell_NotifyIcon(NIM_ADD, &nid);
```



È anche possibile aggiungere l'icona all'area di notifica e visualizzare una notifica tutti in una sola chiamata all'oggetto [**\_ NotifyIcon della shell**](/windows/desktop/api/Shellapi/nf-shellapi-shell_notifyicona). A tale scopo, continuare con le istruzioni riportate in questo argomento.

### <a name="define-the-notifyicondata-version"></a>Definire la versione di NOTIFYICONDATA

Con l'avanzamento di Windows, la struttura [**NOTIFYICONDATA**](/windows/desktop/api/Shellapi/ns-shellapi-notifyicondataa) è stata espansa in modo da includere più membri per definire più funzionalità. Le costanti vengono usate per dichiarare la versione di **NOTIFYICONDATA** da usare con l'icona dell'area di notifica, in modo da consentire la compatibilità con le versioni precedenti. A meno che non esista un motivo valido per eseguire altre operazioni, è consigliabile utilizzare la versione di NOTIFYICON \_ versione \_ 4, introdotta in Windows Vista. Questa versione fornisce le funzionalità complete disponibili, tra cui la possibilità di identificare l'icona dell'area di notifica anche se un GUID registrato, un meccanismo di callback superiore e un'accessibilità migliore.

Impostare la versione tramite le chiamate seguenti:


```
NOTIFYICONDATA nid = {};
... 
nid.uVersion = NOTIFYICON_VERSION_4;
// Add the icon
Shell_NotifyIcon(NIM_ADD, &nid);
// Set the version
Shell_NotifyIcon(NIM_SETVERSION, &nid);
```



Si noti che questa chiamata a [**Shell \_ NotifyIcon**](/windows/desktop/api/Shellapi/nf-shellapi-shell_notifyicona) non visualizza una notifica.

### <a name="define-the-notification-look-and-contents"></a>Definire l'aspetto e il contenuto della notifica

Una notifica è un tipo speciale di controllo ToolTip a fumetti. Contiene un titolo, un testo del corpo e un'icona. Analogamente a una finestra, presenta un pulsante **Chiudi** nell'angolo superiore destro. Contiene inoltre un pulsante **Opzioni** che consente di aprire l'elemento icone area di notifica nel pannello di controllo, che consente all'utente di visualizzare o nascondere l'icona o di visualizzare solo le notifiche senza un'icona.

![screenshot del fumetto di notifica che indica che l'alimentazione della batteria è insufficiente](images/taskbar/notificationballoon.png)

La struttura [**NOTIFYICONDATA**](/windows/desktop/api/Shellapi/ns-shellapi-notifyicondataa) inviata nella chiamata a [**Shell \_ NotifyIcon**](/windows/desktop/api/Shellapi/nf-shellapi-shell_notifyicona) contiene informazioni che specificano l'icona dell'area di notifica e il fumetto di notifica. Di seguito sono riportati gli elementi specifici della notifica che possono essere impostati tramite **NOTIFYICONDATA**.

-   Icona da visualizzare nel fumetto di notifica, specificato dal tipo di notifica. È possibile specificare le dimensioni dell'icona, nonché le icone personalizzate.
-   Titolo della notifica. Questo titolo deve avere una lunghezza massima di 48 caratteri in inglese (per adattarsi alla localizzazione). Il titolo è la prima riga della notifica e viene impostato con l'uso della dimensione del carattere, del colore e del peso.
-   Testo da utilizzare nel corpo della notifica. Questo testo deve essere costituito da un massimo di 200 caratteri in inglese (per adattarsi alla localizzazione).
-   Indica se la notifica deve essere eliminata se non può essere visualizzata immediatamente.
-   Timeout per la notifica. Questa impostazione viene ignorata in Windows Vista e nei sistemi successivi a favore di un'impostazione di timeout di accessibilità a livello di sistema.
-   Indica se la notifica deve rispettare l'ora non interattiva, impostata tramite il flag di ora di NIIF rispetto al valore di [**\_ \_ quiet \_**](/windows/desktop/api/Shellapi/ns-shellapi-notifyicondataa) .

> [!Note]  
> Le interfacce [**IUserNotification**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iusernotification) e [**IUserNotification2**](/windows/desktop/api/Shobjidl/nn-shobjidl-iusernotification2) sono wrapper Component Object Model (com) per l' [**oggetto \_ NotifyIcon della shell**](/windows/desktop/api/Shellapi/nf-shellapi-shell_notifyicona). Al momento, tuttavia, non forniscono la funzionalità NOTIFYICON completa della \_ versione \_ 4 disponibile direttamente tramite l' **oggetto \_ NotifyIcon della shell** , incluso l'utilizzo di un GUID per identificare l'icona dell'area di notifica.

 

### <a name="check-the-user-status"></a>Verificare lo stato utente

Il sistema utilizza la funzione [**SHQueryUserNotificationState**](/windows/desktop/api/Shellapi/nf-shellapi-shqueryusernotificationstate) per verificare se l'utente si trova in un tempo di attesa, distante dal computer o in uno stato non interrompebile, ad esempio la modalità presentazione. Indica se il sistema Visualizza la notifica dipende da questo stato.

> [!Note]  
> Se l'applicazione usa un metodo di notifica personalizzato che non usa la [**Shell \_ NotifyIcon**](/windows/desktop/api/Shellapi/nf-shellapi-shell_notifyicona), [**IUserNotification**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iusernotification)o [**IUserNotification2**](/windows/desktop/api/Shobjidl/nn-shobjidl-iusernotification2), deve sempre chiamare in modo esplicito [**SHQueryUserNotificationState**](/windows/desktop/api/Shellapi/nf-shellapi-shqueryusernotificationstate) per determinare se deve visualizzare l'interfaccia utente di notifica in quel momento.

 

Le notifiche inviate quando l'utente è distante vengono accodate per la visualizzazione, ma poiché non è possibile sapere quando l'utente restituisce o se la notifica sarà ancora valida in quel momento, è possibile inviare nuovamente la notifica in un secondo momento.

Le notifiche inviate durante l'intervallo di tempo silenzioso vengono ignorate. Le linee guida di progettazione chiedono che tutte le notifiche siano ignorabili. Non devono richiedere un'azione immediata da un utente. Pertanto, nessuna notifica è così importante che debba eseguire l'override del tempo di attesa.

### <a name="display-the-notification"></a>Visualizza la notifica

Dopo aver impostato la versione [**NOTIFYICONDATA**](/windows/desktop/api/Shellapi/ns-shellapi-notifyicondataa) e definito la notifica in una struttura **NOTIFYICONDATA** , chiamare la [**Shell \_ NotifyIcon**](/windows/desktop/api/Shellapi/nf-shellapi-shell_notifyicona) per visualizzare l'icona.

-   Se l'icona dell'area di notifica non è presente, chiamare la [**Shell \_ NotifyIcon**](/windows/desktop/api/Shellapi/nf-shellapi-shell_notifyicona) per aggiungere l'icona. Eseguire questa operazione per icone temporanee e non temporanee.
    ```
    NOTIFYICONDATA nid = {};
    ...                    
    Shell_NotifyIcon(NIM_ADD, &nid);
    ```

    

-   Se l'icona dell'area di notifica è già presente, chiamare la [**Shell \_ NotifyIcon**](/windows/desktop/api/Shellapi/nf-shellapi-shell_notifyicona) per modificare l'icona.
    ```
    NOTIFYICONDATA nid = {};
    ...                    
    Shell_NotifyIcon(NIM_MODIFY, &nid);
    ```

    

Il codice seguente illustra un esempio di impostazione dei dati di [**NOTIFYICONDATA**](/windows/desktop/api/Shellapi/ns-shellapi-notifyicondataa) e l'invio tramite l'oggetto [**\_ NotifyIcon della shell**](/windows/desktop/api/Shellapi/nf-shellapi-shell_notifyicona). Si noti che questo esempio identifica l'icona di notifica tramite un GUID (scelta consigliata in Windows 7).


```
// Declare NOTIFYICONDATA details. 
    // Error handling is omitted here for brevity. Do not omit it in your code.
    
    NOTIFYICONDATA nid = {};
    nid.cbSize = sizeof(nid);
    nid.hWnd = hWnd;
    nid.uFlags = NIF_ICON | NIF_TIP | NIF_GUID;
    
    // Note: This is an example GUID only and should not be used.
    // Normally, you should use a GUID-generating tool to provide the value to
    // assign to guidItem.
    static const GUID myGUID = 
    {0x23977b55, 0x10e0, 0x4041, {0xb8, 0x62, 0xb1, 0x95, 0x41, 0x96, 0x36, 0x69}};
    nid.guidItem = myGUID;
    
    nid.guidItem = guid;
    
    // This text will be shown as the icon's tooltip.
    StringCchCopy(nid.szTip, ARRAYSIZE(nid.szTip), L"Test application");
    
    // Load the icon for high DPI.
    LoadIconMetric(hInst, MAKEINTRESOURCE(IDI_SMALL), LIM_SMALL, &(nid.hIcon));
    
    // Show the notification.
    Shell_NotifyIcon(NIM_ADD, &nid) ? S_OK : E_FAIL;
```



### <a name="removing-an-icon"></a>Rimozione di un'icona

Per rimuovere un'icona (ad esempio, quando è stata aggiunta temporaneamente l'icona per trasmettere una notifica, chiamare la [**Shell \_ NotifyIcon**](/windows/desktop/api/Shellapi/nf-shellapi-shell_notifyicona)come illustrato di seguito. In questa chiamata è necessaria solo una struttura [**NOTIFYICONDATA**](/windows/desktop/api/Shellapi/ns-shellapi-notifyicondataa) minima che identifichi l'icona.


```
NOTIFYICONDATA nid = {};
...                    
Shell_NotifyIcon(NIM_DELETE, &nid);
```



> [!Note]  
> Quando un'applicazione viene disinstallata, l'icona dell'area di notifica può ancora apparire all'utente come opzione nella pagina icone area di notifica nel pannello di controllo per un massimo di sette giorni. Tuttavia, le modifiche apportate non avranno alcun effetto.

 

## <a name="sdk-sample"></a>Esempio SDK

Vedere l'esempio di esempio di [NotificationIcon](samples-notificationicon.md) in Windows Software Development Kit (SDK) per un esempio completo dell'uso di [**\_ NotifyIcon della shell**](/windows/desktop/api/Shellapi/nf-shellapi-shell_notifyicona).

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**NotifyIcon della shell \_**](/windows/desktop/api/Shellapi/nf-shellapi-shell_notifyicona)
</dt> <dt>

[**\_NotifyIconGetRect Shell**](/windows/desktop/api/Shellapi/nf-shellapi-shell_notifyicongetrect)
</dt> <dt>

[**NOTIFYICONDATA**](/windows/desktop/api/Shellapi/ns-shellapi-notifyicondataa)
</dt> <dt>

[**SHQueryUserNotificationState**](/windows/desktop/api/Shellapi/nf-shellapi-shqueryusernotificationstate)
</dt> <dt>

[**IUserNotification**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iusernotification)
</dt> <dt>

[**IUserNotification2**](/windows/desktop/api/Shobjidl/nn-shobjidl-iusernotification2)
</dt> <dt>

[Barra delle applicazioni](taskbar.md)
</dt> <dt>

[Estensioni della barra delle applicazioni](taskbar-extensions.md)
</dt> </dl>

 

 
