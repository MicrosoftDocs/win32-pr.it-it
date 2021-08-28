---
title: Gestori di notifica amministrativi
description: Lo snap-in MMC di Microsoft Utenti e computer di Active Directory fornisce un meccanismo per consentire ai componenti di ricevere notifiche quando l'utente elimina, rinomina, sposta o modifica le proprietà di un oggetto usando lo snap-in.
ms.assetid: 49dbb995-c760-4fac-a72f-d5d94afb63c7
ms.tgt_platform: multiple
keywords:
- Gestori di notifica amministrativi AD
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 08d89627cdb15cc7ea15f4b56e3a6ec90eafbe6a
ms.sourcegitcommit: 61a4c522182aa1cacbf5669683d9570a3bf043b2
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/26/2021
ms.locfileid: "122879882"
---
# <a name="administrative-notification-handlers"></a>Gestori di notifica amministrativi

Lo snap-in MMC di Microsoft Utenti e computer di Active Directory fornisce un meccanismo per consentire ai componenti di ricevere notifiche quando l'utente elimina, rinomina, sposta o modifica le proprietà di un oggetto usando lo snap-in. Il componente che riceve le notifiche è noto come "gestore di notifica".

Ciò è utile quando più oggetti sono collegati tra loro e devono esistere all'interno dello stesso contenitore. Se uno degli oggetti collegati viene spostato, viene fornita una notifica al gestore di notifica e il gestore delle notifiche può spostare gli altri oggetti collegati nella stessa cartella.

Quando viene eseguita una delle operazioni e viene installato uno o più gestori di notifica, lo snap-in Utenti e computer visualizza una finestra di dialogo di conferma che elenca i gestori di notifica e una casella di controllo per ogni gestore. Se la casella di controllo per un gestore è selezionata, il gestore viene notificato. Se la casella di controllo non è selezionata, il gestore non viene informato.

## <a name="implementing-a-notification-handler"></a>Implementazione di un gestore di notifica

Un gestore di notifica è un oggetto COM implementato come server in-process. Il gestore di notifica deve implementare [**l'interfaccia IDsAdminNotifyHandler.**](/windows/desktop/api/DSAdmin/nn-dsadmin-idsadminnotifyhandler)

Quando si verifica un evento che causerà una notifica, lo snap-in Utenti e computer enumera i gestori di notifica registrati e ne crea uno usando il CLSID per il gestore. Dopo la creazione del gestore, lo snap-in chiama il [**metodo IDsAdminNotifyHandler::Initialize.**](/windows/desktop/api/DSAdmin/nf-dsadmin-idsadminnotifyhandler-initialize) Il **metodo Initialize** fornisce lo snap-in con gli eventi che il gestore deve ricevere.

Se l'evento deve essere inviato al gestore di notifica, lo snap-in chiama il metodo [**IDsAdminNotifyHandler::Begin.**](/windows/desktop/api/DSAdmin/nf-dsadmin-idsadminnotifyhandler-begin) Il **metodo Begin** fornisce al gestore l'evento che si verifica, i dati sull'oggetto su cui si sta verificando l'evento e, a seconda dell'evento, i dati su ciò che diventerà l'oggetto. Il **metodo Begin** fornisce anche lo snap-in con il testo che deve essere visualizzato per il gestore nella finestra di dialogo di conferma.

Quando viene [**chiamato il**](/windows/desktop/api/DSAdmin/nf-dsadmin-idsadminnotifyhandler-begin) metodo Begin per ogni gestore, lo snap-in visualizza la finestra di dialogo di conferma. La finestra di dialogo di conferma richiede all'utente di selezionare i gestori che riceveranno la notifica. Se l'utente preme il **pulsante** No push nella finestra di dialogo di conferma, nessuno dei gestori viene informato. Se l'utente preme **il** pulsante Sì, ognuno dei gestori selezionati nella finestra di dialogo di conferma riceve la notifica. Lo snap-in invia la notifica al gestore chiamando il [**metodo IDsAdminNotifyHandler::Notify.**](/windows/desktop/api/DSAdmin/nf-dsadmin-idsadminnotifyhandler-notify)

Dopo aver notificato tutti i gestori, lo snap-in chiama il metodo [**IDsAdminNotifyHandler::End.**](/windows/desktop/api/DSAdmin/nf-dsadmin-idsadminnotifyhandler-end) Il **metodo End** viene sempre chiamato, anche se il metodo [**Notify**](/windows/desktop/api/DSAdmin/nf-dsadmin-idsadminnotifyhandler-notify) non viene chiamato.

## <a name="registering-a-notification-handler-in-the-windows-registry"></a>Registrazione di un gestore di notifica nel Registro Windows dati

Come tutti i server COM, un gestore di notifica deve essere registrato nel registro Windows sistema. Il gestore viene registrato nella chiave seguente:


```C++
HKEY_CLASSES_ROOT - CLSID - <CLSID>
```



**&lt; CLSID &gt;** è la rappresentazione di stringa del CLSID come prodotto dalla [**funzione StringFromCLSID.**](/windows/win32/api/combaseapi/nf-combaseapi-stringfromclsid) Sotto la **&lt; chiave &gt; CLSID** è presente una chiave **InProcServer32** che identifica l'oggetto come server in-process a 32 bit. Nella chiave **InProcServer32** il percorso della DLL viene specificato nel valore predefinito e il modello di threading viene specificato nel **valore ThreadingModel.** Tutti i gestori di notifica devono usare il modello di threading **Apartment.**

## <a name="registering-a-notification-handler-with-an-active-directory-server"></a>Registrazione di un gestore di notifiche con un server Active Directory

All Active Directory Domain Services, la registrazione del gestore di notifica è specifica di un'impostazione locale. Se il gestore di notifica si applica a tutte le impostazioni locali, deve essere registrato nell'oggetto **displaySpecifier** in tutti i sottocontenitori delle impostazioni locali nel contenitore DisplaySpecifiers. Se il gestore di notifica è localizzato per determinate impostazioni locali, viene registrato nell'oggetto **displaySpecifier** nel sottocontenitore delle impostazioni locali. Per altre informazioni sul contenitore DisplaySpecifiers e sulle impostazioni locali, vedere [Identificatori di](display-specifiers.md) visualizzazione e [Contenitore DisplaySpecifiers](displayspecifiers-container.md).

I gestori di notifica vengono registrati con **l'attributo dsUIAdminNotification** nel contenitore **DS-UI-Default-Impostazioni.** Si tratta di un valore stringa Unicode multivalore in cui ogni valore richiede il formato seguente:


```C++
<order number>,<CLSID>
```



Il " &lt; numero di ordine " è un numero senza segno che rappresenta la posizione del gestore nella finestra di &gt; dialogo di conferma. Quando viene visualizzata la finestra di dialogo di conferma, i valori vengono ordinati usando un confronto del " numero di ordine" &lt; di ogni &gt; valore. Se più valori hanno lo stesso " numero di ordine ", questi gestori vengono visualizzati nell'ordine in cui vengono letti &lt; &gt; dal server Active Directory. Se possibile, è consigliabile usare un valore non esistente, non usato da altri valori nella proprietà , " &lt; order &gt; number ". Non esiste alcuna posizione iniziale prescritta e gli spazi vuoti possono essere visualizzati nella sequenza " &lt; order number &gt; ".

" &lt; CLSID " è la rappresentazione di stringa del &gt; CLSID come prodotto dalla [**funzione StringFromCLSID.**](/windows/win32/api/combaseapi/nf-combaseapi-stringfromclsid)

 

 
