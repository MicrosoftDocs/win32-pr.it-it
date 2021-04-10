---
title: Script personalizzato RAS
description: Gli sviluppatori possono creare una DLL di scripting personalizzata che risiede in un computer client RAS. Questa DLL può comunicare con il server durante il processo di creazione di una connessione.
ms.assetid: c27b8b02-6018-4441-a355-1fb890b9001c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c625f020d9dafcb352c5f1b382014f9dba189330
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "103963191"
---
# <a name="ras-custom-scripting"></a>Script personalizzato RAS

Gli sviluppatori possono creare una DLL di scripting personalizzata che risiede in un computer client RAS. Questa DLL può comunicare con il server durante il processo di creazione di una connessione.

**Windows NT:** Lo scripting personalizzato non è disponibile.

## <a name="setting-up-the-dll"></a>Configurazione della DLL

Per configurare la DLL, creare un valore con il nome **CustomScriptDllPath** nella seguente chiave del registro di sistema:

```
HKEY_LOCAL_MACHINE
   System
      CurrentControlSet
         Services
            Rasman
               Parameters
```

Questo valore deve essere di tipo **reg \_ expand \_ SZ**. Il valore deve contenere il percorso della DLL di scripting personalizzata. Per ogni computer client RAS è supportata una sola DLL di scripting personalizzato.

## <a name="interaction-between-the-server-ras-and-the-custom-scripting-dll"></a>Interazione tra server, RAS e DLL Custom-Scripting

La DLL di scripting personalizzata deve esportare un singolo punto di ingresso: [**RasCustomScriptExecute**](/windows/desktop/api/Ras/nc-ras-rascustomscriptexecutefn). RAS chiama questa funzione durante lo \_ stato interattivo RASCS del processo di connessione. Lo stato \_ interattivo RASCS è uno stato in pausa, che consente all'utente di interagire con un'interfaccia utente presentata dalla DLL di scripting personalizzato. Per ulteriori informazioni sugli stati di connessione, vedere [**RASCONNSTATE**](/previous-versions/windows/desktop/legacy/aa376727(v=vs.85)) .

RAS viene passato come parametro alla funzione [**RasCustomScriptExecute**](/windows/desktop/api/Ras/nc-ras-rascustomscriptexecutefn) :

-   Handle per la porta sul computer client utilizzato per la connessione.
-   Stringhe che identificano la Rubrica e la voce della connessione.
-   RAS passa inoltre un handle a una finestra per consentire alla DLL di presentare un'interfaccia utente.
-   Set di puntatori a funzione che la DLL può usare per comunicare con il server.

Per ulteriori informazioni su questi parametri, vedere [**RasCustomScriptExecute**](/windows/desktop/api/Ras/nc-ras-rascustomscriptexecutefn) .

RAS passa un puntatore a una struttura [**RASCUSTOMSCRIPTEXTENSIONS**](/previous-versions/windows/desktop/legacy/aa376738(v=vs.85)) come ultimo parametro a [**RasCustomScriptExecute**](/windows/desktop/api/Ras/nc-ras-rascustomscriptexecutefn). Questa struttura contiene un puntatore a una funzione di tipo [**PFNRASSETCOMMSETTINGS**](/windows/desktop/api/Ras/nc-ras-pfnrassetcommsettings). La DLL di scripting personalizzato chiama questa funzione per modificare le impostazioni di comunicazione sulla porta utilizzata dalla connessione.

RAS media l'interazione tra il server e la DLL di scripting personalizzato. In genere, il server avvia la finestra di dialogo. Ad esempio, il server può richiedere il nome utente e la password dell'utente.

Quando si usa lo scripting personalizzato per stabilire una connessione, il server non deve eseguire Windows NT 4,0 o Windows 2000.

## <a name="custom-scripting-user-interface-must-support-idcancel"></a>L'interfaccia utente di scripting personalizzata deve supportare IDCANCEL

Se il dialer personalizzato Visualizza un'interfaccia utente, l'interfaccia utente deve supportare \_ i messaggi di comando WM in cui LOWORD (*wParam*) è uguale a IDCANCEL.

## <a name="configuring-the-connection"></a>Configurazione della connessione

Il punto di ingresso di [**RasCustomScriptExecute**](/windows/desktop/api/Ras/nc-ras-rascustomscriptexecutefn) può essere richiamato da [**RasDialDlg**](/windows/desktop/api/Rasdlg/nf-rasdlg-rasdialdlga) o, in Windows XP, da [**RasDial**](/windows/desktop/api/Ras/nf-ras-rasdiala).

Per richiamare [**RasCustomScriptExecute**](/windows/desktop/api/Ras/nc-ras-rascustomscriptexecutefn) da [**RasDialDlg**](/windows/desktop/api/Rasdlg/nf-rasdlg-rasdialdlga), impostare l' \_ opzione raseo CustomScript nella voce della rubrica telefonica relativa alla connessione. Per una descrizione delle opzioni di immissione della rubrica telefonica, vedere il membro **dwfOptions** di [**RASENTRY**](/previous-versions/windows/desktop/legacy/aa377274(v=vs.85)) . Usare le funzioni [**RasGetEntryProperties**](/windows/desktop/api/Ras/nf-ras-rasgetentrypropertiesa) e [**RasSetEntryProperties**](/windows/desktop/api/Ras/nf-ras-rassetentrypropertiesa) per impostare questa opzione a livello di codice.

**Windows XP:** Per richiamare [**RasCustomScriptExecute**](/windows/desktop/api/Ras/nc-ras-rascustomscriptexecutefn) da [**RasDial**](/windows/desktop/api/Ras/nf-ras-rasdiala), la chiamata a **RasDial** deve specificare una struttura [**RASDIALEXTENSIONS**](/previous-versions/windows/desktop/legacy/aa377029(v=vs.85)) e questa struttura deve specificare il flag RDEOPT UseCustomScripting \_ . Inoltre, la voce della rubrica telefonica per la connessione deve specificare l'opzione RASEO \_ CustomScript come descritto nel paragrafo precedente.

## <a name="invoking-the-custom-scripting-dll"></a>Richiamo della DLL di scripting personalizzata

Se l'utente attiva una connessione per una voce di Rubrica con RASEO \_ CustomScript impostata, RAS richiama la dll di scripting personalizzato. In questo scenario, RAS richiama la DLL di scripting personalizzato da [**RasDialDlg**](/windows/desktop/api/Rasdlg/nf-rasdlg-rasdialdlga).

Per richiamare la DLL di scripting personalizzato a livello di codice, stabilire la connessione tramite la funzione [**RasDialDlg**](/windows/desktop/api/Rasdlg/nf-rasdlg-rasdialdlga) . In Windows XP, la funzione [**RasDial**](/windows/desktop/api/Ras/nf-ras-rasdiala) richiama anche la dll di scripting personalizzato.

 

 