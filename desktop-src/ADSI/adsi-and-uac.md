---
title: ADSI e controllo dell'account utente
description: Windows e Windows Server hanno controllo dell'account utente, che presenta ramificazioni per le applicazioni che usano Active Directory Service Interfaces (ADSI).
ms.assetid: 0b286252-8c24-4a18-9dc6-063ca158a8ff
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ae1d0163348356f83b64522c9b05607d0d094ceb8f0ad530a798e546021433ab
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119023969"
---
# <a name="adsi-and-user-account-control"></a>ADSI e controllo dell'account utente

Windows e Windows Server hanno controllo [dell'account](/previous-versions/windows/it-pro/windows-server-2008-R2-and-2008/cc709691(v=ws.10))utente , che presenta ramificazioni per le applicazioni che usano [Active Directory Service Interfaces](active-directory-service-interfaces-adsi.md) (ADSI). In particolare, queste interfacce sono state progettate per essere eseguite da un account utente con privilegi di amministratore nel computer locale.

**Problema**

Ogni volta che un'applicazione si connette alla directory e tenta di creare un oggetto ADSI, viene verificata la ricerca delle modifiche nello schema di [Active Directory.](/windows/desktop/ADSchema/active-directory-schema) Se è stato modificato dopo l'ultima connessione, lo schema viene scaricato e archiviato in una cache nel computer locale. Nelle versioni di Windows precedenti Windows Vista, il percorso predefinito per questa cache era

`%systemroot%\SchCache\`

Tuttavia, le applicazioni eseguite da account standard (ovvero non amministratori) non avranno accesso a questa directory e, di conseguenza, le applicazioni che usano interfacce ADSI eseguite in questa modalità scariranno lo schema in ogni connessione, con un impatto sulla velocità effettiva e sulle prestazioni.

**Soluzioni**

*Utente singolo:* per risolvere questo problema, sono disponibili nuove chiavi di controllo del Registro di sistema del provider ADSI che determinano i percorsi del Registro di sistema e i percorsi dei file per gli oggetti dello [schema di Active Directory memorizzati nella](/windows/desktop/ADSchema/active-directory-schema) cache. Se la chiave del Registro di sistema

`HKEY_LOCAL_MACHINE\System\CurrentControlSet\Services\adsi\Cache\PerMachine`

è impostato su 0 (zero), ogni utente avrà un percorso di archiviazione diverso per ADSI. le chiavi del Registro di sistema verranno archiviate in

`HKEY_CURRENT_USER\Software\Microsoft\ADs\Providers\LDAP\`

e i file della cache verranno archiviati in

`%LOCALAPPDATA%\Microsoft\Windows\SchCache`

Queste impostazioni sono le impostazioni predefinite nei computer che eseguono Windows Server 2008 o Windows Vista.

*Multi-utente:* se si eseguono applicazioni ADSI in un computer con molti account utente (ad esempio, un server Web), è preferibile non avere molte copie della cache dello schema di [Active Directory](/windows/desktop/ADSchema/active-directory-schema) che utilizzano grandi quantità di spazio su disco. Impostazione della chiave del Registro di sistema

`HKEY_LOCAL_MACHINE\System\CurrentControlSet\Services\adsi\Cache\PerMachine`

se è 1 (uno), ad ADSI verrà ripristinato il comportamento precedente. tutti [gli oggetti dello schema](/windows/desktop/ADSchema/active-directory-schema) di Active Directory verranno archiviati nei percorsi precedenti. la chiave del Registro di sistema sarà in

`HKEY_LOCAL_MACHINE\Software\Microsoft\ADs\Providers\LDAP`

e il file di cache sarà in

`%systemroot%\SchCache`

In questo caso, gli account amministratore devono eseguire l'applicazione, in modo che il file di schema verrà memorizzato nella cache nella posizione globale per un uso futuro da parte degli utenti con privilegi inferiori.

 

 