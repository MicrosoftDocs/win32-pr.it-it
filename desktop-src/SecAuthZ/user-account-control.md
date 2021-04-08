---
description: Consente agli utenti di eseguire attività comuni come non amministratori, denominati utenti standard e come amministratori senza dover cambiare utenti, disconnettersi o utilizzare Run As.
ms.assetid: 8a7ba726-c2a6-4b7b-b664-3c6fcfbfb221
title: Controllo dell'account utente (autorizzazione)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: be7f3cd8f31dda8f1b15145bc4003fc9ede8782c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103968222"
---
# <a name="user-account-control-authorization"></a>Controllo dell'account utente (autorizzazione)

Il controllo dell'account utente consente agli utenti di eseguire attività comuni come utenti non amministratori, detti utenti standard e come amministratori senza dover cambiare utente, disconnettersi o utilizzare **Esegui come**. Il comportamento del controllo dell'account utente per l'impostazione "non notifica mai" non consente più di disabilitare UAC. L'impostazione "mai notifica" fornisce un token di divisione e eleva sempre automaticamente il privilegio richiesto. Questa sottigliezza può causare problemi di compatibilità con l'app. È comunque possibile disabilitare il controllo dell'account utente usando criteri di gruppo o impostando manualmente la chiave del registro di sistema.

**Windows server 2008 R2, Windows 7, Windows server 2008 e Windows Vista:** L'impostazione "non notifica mai" Disabilita il controllo dell'account utente.

Se, ad esempio, si eseguono i passaggi seguenti per modificare l'impostazione "non notificare mai", si ottengono risultati diversi quando si tenta di creare un file in una cartella che richiede privilegi elevati. Il comportamento di Windows 8 consiste nel negare l'accesso. Il comportamento di Windows 7 consente di creare il file di File.txt.

1.  Toccare o fare clic su **Avvia**. Nella casella di ricerca digitare "modifica impostazioni di controllo dell'account utente".
2.  Toccare o fare clic su **Modifica impostazioni di controllo dell'account utente** per aprirlo.
3.  Spostare il dispositivo di scorrimento su **non notificare mai**.
4.  Toccare o fare clic su **OK**.
5.  Riavviare il computer.
6.  Toccare o fare clic su **Start** , quindi su **Esegui**. Nella casella **Apri** digitare "Cmd.exe". Si noti che il titolo della finestra non contiene la stringa "Administrator".
7.  Digitare "Echo >% windir% \\ system32 \\File.txt".

UAC è stato aggiunto in Windows Server 2008 e Windows Vista. Un account utente standard è sinonimo di un account utente in Windows XP. Gli account utente che sono membri del gruppo Administrators locale eseguiranno la maggior parte delle applicazioni come utente standard.

Per informazioni su UAC, vedere gli argomenti seguenti.



| Argomento                                                                                                                                        | Descrizione                                                                                                                                   |
|----------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------|
| [Linee guida per il controllo dell'account utente nello sviluppo dell'interfaccia utente](https://msdn.microsoft.com/library/aa511445(l=en-us,v=MSDN.10).aspx)<br/> | Informazioni generali sul controllo dell'account utente.<br/>                                                                                                     |
| [Sviluppo di applicazioni che richiedono privilegi di amministratore](developing-applications-that-require-administrator-privilege.md)<br/>  | Modelli per lo sviluppo di applicazioni che eseguono operazioni che richiedono privilegi amministrativi, ma che vengono eseguite come utente standard.<br/> |
| [Riferimento all'autorizzazione](authorization-reference.md)<br/>                                                                            | Informazioni dettagliate sulle funzioni di autorizzazione, le interfacce, le strutture e altri elementi di programmazione.<br/>                        |



 

 

 




