---
title: Dialer personalizzati
description: Windows sistemi operativi 2000 e versioni successive consentono agli sviluppatori di fornire i propri dialer personalizzati che funzionano con il servizio di accesso remoto (RAS).
ms.assetid: ad94f38d-812f-4329-8055-6274a21a3242
keywords:
- Dialer personalizzati
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 69b23edd8501929181a54b1b511f365945f8e1c6277056e068cf58fb67bd26c2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117791501"
---
# <a name="custom-dialers"></a>Dialer personalizzati

Windows sistemi operativi 2000 e versioni successive consentono agli sviluppatori di fornire i propri dialer personalizzati che funzionano con il servizio di accesso remoto (RAS). Il dialer personalizzato viene implementato come una singola libreria a collegamento dinamico (DLL) che esporta i punti di ingresso seguenti:

-   [**RasCustomDial**](/windows/desktop/api/Ras/nc-ras-rascustomdialfn)
-   [**RasCustomDialDlg**](/windows/desktop/api/Rasdlg/nc-rasdlg-rascustomdialdlgfn)
-   [**RasCustomHangup**](/windows/desktop/api/Ras/nc-ras-rascustomhangupfn)
-   [**RasCustomEntryDlg**](/windows/desktop/api/Rasdlg/nc-rasdlg-rascustomentrydlgfn)
-   [**RasCustomDeleteEntryNotify**](/windows/desktop/api/Ras/nc-ras-rascustomdeleteentrynotifyfn)

La DLL di composizione personalizzata deve esportare tutti questi punti di ingresso e implementare i punti di ingresso come funzioni Unicode. Per altre informazioni su queste funzioni, vedere la pagina di riferimento per ogni funzione in Windows SDK Remote Access Service Reference (Informazioni di riferimento sul servizio di accesso remoto di Windows SDK).

Perché una connessione RAS usi il dialer personalizzato, la voce della rubrica per la connessione deve contenere il percorso della DLL di chiamata personalizzata. Usare le funzioni dell'API [**RAS RasGetEntryProperties**](/windows/desktop/api/Ras/nf-ras-rasgetentrypropertiesa) e [**RasSetEntryProperties**](/windows/desktop/api/Ras/nf-ras-rassetentrypropertiesa) per impostare questo percorso nel membro **szCustomDialDll** della [**struttura RASENTRY**](/previous-versions/windows/desktop/legacy/aa377274(v=vs.85)) per la voce della rubrica.

## <a name="updating-the-registry-for-custom-dialers"></a>Aggiornamento del Registro di sistema per i dialer personalizzati

Per consentire al sistema di stabilire una connessione che usa un dialer personalizzato, è necessario che il percorso della DLL di composizione personalizzata sia presente nel valore del Registro di sistema seguente.

```
HKEY_LOCAL_MACHINE
   System
      CurrentControlSet
         Services
            Rasman
               Parameters
                  CustomDLL<dl>
<dt>

                  Data type
</dt>
<dd>                  REG_MULTI_SZ</dd>
</dl>
```

Poiché **CustomDLL** è di tipo **REG MULTI \_ \_ SZ,** può contenere percorsi a più DLL di composizione personalizzata. È necessario impostare il percorso della DLL di composizione personalizzata in questo valore del Registro di sistema, oltre alla voce della rubrica per la connessione.

Per impostazione predefinita, questo valore del Registro di sistema è scrivibile solo da un utente con privilegi di amministratore o di sistema. Per motivi di sicurezza, non modificare le autorizzazioni per questa chiave del Registro di sistema.

## <a name="using-custom-dialers-at-system-logon"></a>Uso di dialer personalizzati all'accesso al sistema

Windows sistemi operativi 2000 e versioni successive consentono a un utente di stabilire una connessione RAS al momento dell'accesso. A tale scopo, l'utente **controlla Accesso tramite connessione** remota nella finestra di dialogo **Informazioni** di accesso . Dopo che l'utente ha fatto clic sul pulsante Ok, il sistema visualizza le connessioni disponibili.

## <a name="security-considerations"></a>Considerazioni relative alla sicurezza

Nella maggior parte dei casi, un dialer personalizzato opera con i privilegi di sicurezza dell'utente che lo richiama. Tuttavia, se il dialer personalizzato viene richiamato all'accesso, opera con privilegi di sistema. Progettare quindi il dialer personalizzato in modo che non possa essere usato per violare la sicurezza del sistema. Ad esempio, il dialer non deve presentare un'interfaccia utente che consenta all'utente l'accesso in scrittura al computer file system. Le interfacce utente che forniscono tale accesso includono  la finestra di dialogo Trova **file,** la finestra di dialogo comune Apri file e Windows **Guida.**

## <a name="custom-dialer-user-interface-must-support-idcancel"></a>I dialer Interfaccia utente devono supportare IDCANCEL

Se il dialer personalizzato visualizza un'interfaccia utente, l'interfaccia utente deve supportare i messaggi WM COMMAND in cui \_ LOWORD(*wParam*) è uguale a IDCANCEL.

 

 