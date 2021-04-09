---
title: ADSI e controllo dell'account utente
description: Windows e Windows Server hanno il controllo dell'account utente, che include le ramificazioni per le applicazioni che utilizzano ADSI (Active Directory Service Interfaces).
ms.assetid: 0b286252-8c24-4a18-9dc6-063ca158a8ff
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f36fc88169a8710228a3bf70283aaccd4b4ac42e
ms.sourcegitcommit: b0ebdefc3dcd5c04bede94091833aa1015a2f95c
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/21/2020
ms.locfileid: "104047356"
---
# <a name="adsi-and-user-account-control"></a>ADSI e controllo dell'account utente

Windows e Windows Server hanno il [controllo dell'account utente](/previous-versions/windows/it-pro/windows-server-2008-R2-and-2008/cc709691(v=ws.10)), che include le ramificazioni per le applicazioni che utilizzano ADSI ( [Active Directory Service Interfaces](active-directory-service-interfaces-adsi.md) ). In particolare, queste interfacce sono state progettate per essere eseguite da un account utente con privilegi di amministratore nel computer locale.

**Problema**

Ogni volta che un'applicazione si connette alla directory e tenta di creare un oggetto ADSI, viene verificata la presenza di modifiche nello [Schema Active Directory](/windows/desktop/ADSchema/active-directory-schema) . Se è stato modificato dopo l'ultima connessione, lo schema viene scaricato e archiviato in una cache nel computer locale. Nelle versioni di Windows precedenti a Windows Vista, il percorso predefinito per questa cache era

`%systemroot%\SchCache\`

Tuttavia, le applicazioni eseguite da account standard, ovvero non amministratori, non avranno accesso a questa directory e, di conseguenza, le applicazioni che utilizzano le interfacce ADSI eseguite in questa modalità scaricheranno lo schema in ogni connessione, che influirà sulla velocità effettiva e sulle prestazioni.

**Soluzioni**

*Utente singolo* : per risolvere questo problema, sono disponibili nuove chiavi di controllo del registro di sistema del provider ADSI che determinano i percorsi del registro di sistema e i percorsi dei file per gli oggetti [dello schema di Active Directory](/windows/desktop/ADSchema/active-directory-schema) memorizzati Se la chiave del registro di sistema

`HKEY_LOCAL_MACHINE\System\CurrentControlSet\Services\adsi\Cache\PerMachine`

è impostato su 0 (zero), ogni utente avrà un percorso di archiviazione diverso per ADSI. le chiavi del registro di sistema verranno archiviate in

`HKEY_CURRENT_USER\Software\Microsoft\ADs\Providers\LDAP\`

e i file di cache verranno archiviati in

`%LOCALAPPDATA%\Microsoft\Windows\SchCache`

Queste impostazioni sono le impostazioni predefinite dei computer che eseguono Windows Server 2008 o Windows Vista.

*Multiutente* : se si eseguono applicazioni ADSI in un computer con molti account utente (ad esempio, un server Web), è preferibile non avere molte copie della [Active Directory cache dello schema](/windows/desktop/ADSchema/active-directory-schema) usando grandi quantità di spazio su disco. Impostazione della chiave del registro di sistema

`HKEY_LOCAL_MACHINE\System\CurrentControlSet\Services\adsi\Cache\PerMachine`

a 1 (uno) verrà ripristinato il comportamento precedente di ADSI. tutti gli oggetti [dello Schema Active Directory](/windows/desktop/ADSchema/active-directory-schema) verranno archiviati nei percorsi precedenti. la chiave del registro di sistema sarà in

`HKEY_LOCAL_MACHINE\Software\Microsoft\ADs\Providers\LDAP`

e il file di cache sarà in

`%systemroot%\SchCache`

In questo caso, gli account amministratore devono eseguire l'applicazione, il che comporterà la memorizzazione nella cache del file di schema nel percorso globale per un uso futuro da parte degli utenti con privilegi minori.

 

 