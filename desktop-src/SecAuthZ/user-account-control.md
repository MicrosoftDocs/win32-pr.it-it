---
description: Consente agli utenti di eseguire attività comuni come utenti non amministratori, denominati utenti standard, e come amministratori senza dover cambiare utente, disconnettersi o usare RunAs.
ms.assetid: 8a7ba726-c2a6-4b7b-b664-3c6fcfbfb221
title: Controllo dell'account utente (autorizzazione)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: da0092ed5d8de1c141ba4ee2ea31a498bd6954ba8401aafeb08e6a69b8d130f3
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119906831"
---
# <a name="user-account-control-authorization"></a>Controllo dell'account utente (autorizzazione)

Controllo dell'account utente consente agli utenti di eseguire attività comuni come utenti non amministratori, denominati utenti standard, e come amministratori senza dover cambiare utente, disconnettersi o usare **RunAs.** Il comportamento del controllo dell'account utente per l'impostazione "Non notificare mai" non disabilita più il controllo dell'account utente. L'impostazione "Non notificare mai" fornisce un token di divisione e eleva sempre automaticamente i privilegi necessari. Questa sottigliezza può causare problemi di compatibilità dell'app. È comunque possibile disabilitare controllo dell'account utente usando Criteri di gruppo o impostando manualmente la chiave del Registro di sistema.

**Windows Server 2008 R2, Windows 7, Windows Server 2008 e Windows Vista:** L'impostazione "Non notificare mai" disabilita il controllo dell'account utente.

Ad esempio, se si esegue la procedura seguente per modificare l'impostazione "Non notificare mai", si ottengono risultati diversi quando si tenta di creare un file in una cartella che richiede privilegi elevati. Il Windows 8 comportamento è negare l'accesso. Il Windows 7 consente di creare il file File.txt file.

1.  Toccare o fare clic **su Avvia**. Nella casella di ricerca digitare "Modificare le impostazioni di Controllo account utente".
2.  Toccare o fare clic **su Modifica impostazioni di Controllo account utente** per aprirlo.
3.  Spostare il dispositivo di scorrimento su **Non notificare mai**.
4.  Toccare o fare clic **su OK.**
5.  Riavviare il computer.
6.  Toccare o fare clic **su Start** e quindi **su Esegui**. Nella casella **Apri** digitare "Cmd.exe". Si noti che il titolo della finestra non contiene la stringa "Administrator".
7.  Digitare "echo > %windir% \\ system32 \\File.txt".

Il controllo dell'account utente è stato aggiunto in Windows Server 2008 e Windows Vista. Un account utente standard è sinonimo di un account utente in Windows XP. Gli account utente membri del gruppo Administrators locale eseguiranno la maggior parte delle applicazioni come utente standard.

Per informazioni sul controllo dell'account utente, vedere gli argomenti seguenti.



| Argomento                                                                                                                                        | Descrizione                                                                                                                                   |
|----------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------|
| [Linee guida per il controllo dell'account utente nello sviluppo dell'interfaccia utente](https://msdn.microsoft.com/library/aa511445(l=en-us,v=MSDN.10).aspx)<br/> | Informazioni generali sul controllo dell'account utente.<br/>                                                                                                     |
| [Sviluppo di applicazioni che richiedono privilegi di amministratore](developing-applications-that-require-administrator-privilege.md)<br/>  | Modelli per lo sviluppo di applicazioni che eseguono operazioni che richiedono privilegi amministrativi, ma che vengono eseguite come utente standard.<br/> |
| [Informazioni di riferimento sulle autorizzazioni](authorization-reference.md)<br/>                                                                            | Informazioni dettagliate su funzioni di autorizzazione, interfacce, strutture e altri elementi di programmazione.<br/>                        |



 

 

 




