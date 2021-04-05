---
title: Gestori di notifiche amministrative
description: Lo snap-in MMC utenti e computer di Microsoft Active Directory fornisce un meccanismo per consentire ai componenti di ricevere notifiche quando l'utente Elimina, Rinomina, sposta o modifica le proprietà di un oggetto usando lo snap-in.
ms.assetid: 49dbb995-c760-4fac-a72f-d5d94afb63c7
ms.tgt_platform: multiple
keywords:
- Gestione notifiche amministrative AD
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: baa6f48f8b56ab8e4a1d64d0fe15543bfee6c09e
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/17/2020
ms.locfileid: "103872330"
---
# <a name="administrative-notification-handlers"></a>Gestori di notifiche amministrative

Lo snap-in MMC utenti e computer di Microsoft Active Directory fornisce un meccanismo per consentire ai componenti di ricevere notifiche quando l'utente Elimina, Rinomina, sposta o modifica le proprietà di un oggetto usando lo snap-in. Il componente che riceve le notifiche è noto come "gestore notifiche".

Questa operazione è utile quando più oggetti sono collegati tra loro e devono esistere nello stesso contenitore. Se uno degli oggetti collegati viene spostato, viene fornita una notifica al gestore delle notifiche e il gestore delle notifiche può spostare gli altri oggetti collegati nella stessa cartella.

Quando si esegue una delle operazioni e si installa uno o più gestori di notifiche, nello snap-in utenti e computer verrà visualizzata una finestra di dialogo di conferma in cui sono elencati i gestori delle notifiche e una casella di controllo per ogni gestore. Se è selezionata la casella di controllo per un gestore, viene inviata una notifica al gestore. Se la casella di controllo non è selezionata, il gestore non riceve alcuna notifica.

## <a name="implementing-a-notification-handler"></a>Implementazione di un gestore notifiche

Un gestore notifiche è un oggetto COM implementato come server in-process. Il gestore delle notifiche deve implementare l'interfaccia [**IDsAdminNotifyHandler**](/windows/desktop/api/DSAdmin/nn-dsadmin-idsadminnotifyhandler) .

Quando si verifica un evento che genera una notifica, lo snap-in utenti e computer enumera i gestori delle notifiche registrati e li crea utilizzando il CLSID per il gestore. Dopo la creazione del gestore, lo snap-in chiama il metodo [**IDsAdminNotifyHandler:: Initialize**](/windows/desktop/api/DSAdmin/nf-dsadmin-idsadminnotifyhandler-initialize) . Il metodo **Initialize** fornisce lo snap-in con gli eventi che devono essere ricevuti dal gestore.

Se l'evento è un evento che deve essere inviato al gestore di notifiche, lo snap-in chiama il metodo [**IDsAdminNotifyHandler:: Begin**](/windows/desktop/api/DSAdmin/nf-dsadmin-idsadminnotifyhandler-begin) . Il metodo **Begin** fornisce il gestore con l'evento che si verifica, i dati sull'oggetto su cui si sta verificando l'evento e, a seconda dell'evento, i dati relativi all'oggetto diventerà. Il metodo **Begin** fornisce inoltre lo snap-in con il testo da visualizzare per il gestore nella finestra di dialogo di conferma.

Quando viene chiamato il metodo [**Begin**](/windows/desktop/api/DSAdmin/nf-dsadmin-idsadminnotifyhandler-begin) per ogni gestore, nello snap-in viene visualizzata la finestra di dialogo di conferma. La finestra di dialogo di conferma chiede all'utente di selezionare i gestori che riceveranno la notifica. Se l'utente preme il pulsante **No** push nella finestra di dialogo di conferma, nessuno dei gestori riceve una notifica. Se l'utente preme il pulsante **Sì** , ogni gestore selezionato nella finestra di dialogo di conferma riceve la notifica. Lo snap-in Invia la notifica al gestore chiamando il metodo [**IDsAdminNotifyHandler:: Notify**](/windows/desktop/api/DSAdmin/nf-dsadmin-idsadminnotifyhandler-notify) .

Dopo che tutti i gestori sono stati informati, lo snap-in chiama il metodo [**IDsAdminNotifyHandler:: end**](/windows/desktop/api/DSAdmin/nf-dsadmin-idsadminnotifyhandler-end) . Il metodo **end** viene sempre chiamato, anche se il metodo [**Notify**](/windows/desktop/api/DSAdmin/nf-dsadmin-idsadminnotifyhandler-notify) non viene chiamato.

## <a name="registering-a-notification-handler-in-the-windows-registry"></a>Registrazione di un gestore notifiche nel registro di sistema di Windows

Come tutti i server COM, un gestore di notifiche deve essere registrato nel registro di sistema di Windows. Il gestore viene registrato con la seguente chiave:


```C++
HKEY_CLASSES_ROOT - CLSID - <CLSID>
```



**<CLSID>** rappresentazione di stringa del CLSID come prodotto dalla funzione [**StringFromCLSID**](/windows/win32/api/combaseapi/nf-combaseapi-stringfromclsid) . Sotto la **<CLSID>** chiave è presente una chiave **InprocServer32** che identifica l'oggetto come server in-process a 32 bit. Nella chiave **InprocServer32** il percorso della dll viene specificato nel valore predefinito e il modello di Threading viene specificato nel valore **ThreadingModel** . Tutti i gestori di notifiche devono utilizzare il modello di threading dell' **Apartment** .

## <a name="registering-a-notification-handler-with-an-active-directory-server"></a>Registrazione di un gestore di notifiche con un server di Active Directory

All'interno Active Directory Domain Services la registrazione del gestore delle notifiche è specifica di un'impostazione locale. Se il gestore di notifiche si applica a tutte le impostazioni locali, è necessario registrarlo nell'oggetto **displaySpecifier** in tutti i sottocontenitori delle impostazioni locali nel contenitore DisplaySpecifiers. Se il gestore delle notifiche è localizzato per determinate impostazioni locali, viene registrato nell'oggetto **displaySpecifier** del sottocontenitore delle impostazioni locali. Per altre informazioni sul contenitore e sulle impostazioni locali di DisplaySpecifiers, vedere [identificatori di visualizzazione](display-specifiers.md) e [contenitore DisplaySpecifiers](displayspecifiers-container.md).

I gestori di notifiche sono registrati nell'attributo **dsUIAdminNotification** nel contenitore **DS-UI-default-settings** . Si tratta di un valore stringa Unicode multivalore in cui ogni valore richiede il formato seguente:


```C++
<order number>,<CLSID>
```



Il " &lt; numero di ordine &gt; " è un numero senza segno che rappresenta la posizione del gestore nella finestra di dialogo di conferma. Quando viene visualizzata la finestra di dialogo di conferma, i valori vengono ordinati usando un confronto tra il "numero di ordine" di ogni valore &lt; &gt; . Se più di un valore ha lo stesso " &lt; numero &gt; di ordine", tali gestori vengono visualizzati nell'ordine in cui vengono letti dal server Active Directory. Un oggetto non esistente, ovvero uno non usato da altri valori nella proprietà, &lt; &gt; se possibile, deve essere usato "Order Number". Non esiste alcuna posizione di inizio prescritta e i gap possono comparire nella &lt; sequenza "Numero ordine &gt; ".

" &lt; CLSID &gt; " è la rappresentazione di stringa del CLSID come prodotto dalla funzione [**StringFromCLSID**](/windows/win32/api/combaseapi/nf-combaseapi-stringfromclsid) .

 

 