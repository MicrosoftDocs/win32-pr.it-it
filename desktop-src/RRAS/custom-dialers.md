---
title: Dialer personalizzati
description: I sistemi operativi Windows 2000 e versioni successive consentono agli sviluppatori di fornire i propri dialers personalizzati che funzionano con il servizio di accesso remoto (RAS).
ms.assetid: ad94f38d-812f-4329-8055-6274a21a3242
keywords:
- Dialer personalizzati
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 35293de408a2a0faa146b93f9b5d5ebccf447acc
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104223973"
---
# <a name="custom-dialers"></a>Dialer personalizzati

I sistemi operativi Windows 2000 e versioni successive consentono agli sviluppatori di fornire i propri dialers personalizzati che funzionano con il servizio di accesso remoto (RAS). Il dialer personalizzato viene implementato come una singola libreria di collegamento dinamico (DLL) che esporta i punti di ingresso seguenti:

-   [**RasCustomDial**](/windows/desktop/api/Ras/nc-ras-rascustomdialfn)
-   [**RasCustomDialDlg**](/windows/desktop/api/Rasdlg/nc-rasdlg-rascustomdialdlgfn)
-   [**RasCustomHangup**](/windows/desktop/api/Ras/nc-ras-rascustomhangupfn)
-   [**RasCustomEntryDlg**](/windows/desktop/api/Rasdlg/nc-rasdlg-rascustomentrydlgfn)
-   [**RasCustomDeleteEntryNotify**](/windows/desktop/api/Ras/nc-ras-rascustomdeleteentrynotifyfn)

La DLL di connessione personalizzata deve esportare tutti questi punti di ingresso e deve implementare i punti di ingresso come funzioni Unicode. Per ulteriori informazioni su queste funzioni, vedere la pagina di riferimento per ogni funzione nel riferimento al servizio Windows SDK Remote Access.

Per consentire a una connessione RAS di utilizzare il dialer personalizzato, è necessario che la voce del libro telefonico per la connessione contenga il percorso della DLL di composizione personalizzata. Usare le funzioni API RAS [**RasGetEntryProperties**](/windows/desktop/api/Ras/nf-ras-rasgetentrypropertiesa) e [**RasSetEntryProperties**](/windows/desktop/api/Ras/nf-ras-rassetentrypropertiesa) per impostare questo percorso nel membro **szCustomDialDll** della struttura [**RASENTRY**](/previous-versions/windows/desktop/legacy/aa377274(v=vs.85)) per la voce della rubrica telefonica.

## <a name="updating-the-registry-for-custom-dialers"></a>Aggiornamento del registro di sistema per i dialer personalizzati

Per consentire al sistema di comporre una connessione che utilizza un dialer personalizzato, è necessario che il percorso della DLL della connessione personalizzata esista nel seguente valore del registro di sistema.

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
<dd>                  REG_MULTI_SZ</dd>
</dl>
```

Poiché **CustomDLL** è di tipo **reg \_ multi \_ SZ**, può mantenere i percorsi di più DLL di composizione personalizzata. È necessario impostare il percorso della DLL di composizione personalizzata in questo valore del registro di sistema, oltre alla voce della Rubrica per la connessione.

Per impostazione predefinita, questo valore del registro di sistema è scrivibile solo da un utente con privilegi di amministratore o di sistema. Per motivi di sicurezza, non modificare le autorizzazioni per questa chiave del registro di sistema.

## <a name="using-custom-dialers-at-system-logon"></a>Uso di dialer personalizzati all'accesso al sistema

I sistemi operativi Windows 2000 e versioni successive consentono a un utente di stabilire una connessione RAS al momento dell'accesso. A tale scopo, l'utente controlla l' **accesso tramite la rete remota** nella finestra di dialogo **informazioni di accesso** . Quando l'utente fa clic sul pulsante OK, il sistema Visualizza le connessioni disponibili.

## <a name="security-considerations"></a>Considerazioni relative alla sicurezza

Nella maggior parte dei casi, un dialer personalizzato opera con i privilegi di sicurezza dell'utente che lo richiama. Tuttavia, se il dialer personalizzato viene richiamato al momento dell'accesso, agisce con i privilegi di sistema. Pertanto, progettare il dialer personalizzato in modo che non possa essere utilizzato per violare la sicurezza del sistema. Il dialer, ad esempio, non deve presentare un'interfaccia utente che consente all'utente di accedere in scrittura al file system del computer. Le interfacce utente che forniscono tali accessi includono la finestra di dialogo **Trova file** , la finestra di dialogo **file-Apri** comune e la **Guida** di Windows.

## <a name="custom-dialer-user-interface-must-support-idcancel"></a>L'interfaccia utente del dialer personalizzato deve supportare IDCANCEL

Se il dialer personalizzato Visualizza un'interfaccia utente, l'interfaccia utente deve supportare \_ i messaggi di comando WM in cui LOWORD (*wParam*) è uguale a IDCANCEL.

 

 