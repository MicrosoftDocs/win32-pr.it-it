---
title: Scripting personalizzato RAS
description: Gli sviluppatori possono creare una DLL di scripting personalizzata che risiede in un computer client RAS. Questa DLL può comunicare con il server durante il processo di definizione di una connessione.
ms.assetid: c27b8b02-6018-4441-a355-1fb890b9001c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 66ac0bd83b8d7c48ee8b0468d89a70d19a5e5e6555b9a8bc8ac86d66c8cd666e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119673281"
---
# <a name="ras-custom-scripting"></a>Scripting personalizzato RAS

Gli sviluppatori possono creare una DLL di scripting personalizzata che risiede in un computer client RAS. Questa DLL può comunicare con il server durante il processo di definizione di una connessione.

**Windows NT:** Lo scripting personalizzato non è disponibile.

## <a name="setting-up-the-dll"></a>Configurazione della DLL

Per configurare la DLL, creare un valore con il nome **CustomScriptDllPath** nella chiave del Registro di sistema seguente:

```
HKEY_LOCAL_MACHINE
   System
      CurrentControlSet
         Services
            Rasman
               Parameters
```

Questo valore deve essere di tipo **REG \_ EXPAND \_ SZ**. Il valore deve contenere il percorso della DLL di scripting personalizzata. Per ogni computer client RAS è supportata una sola DLL di scripting personalizzata.

## <a name="interaction-between-the-server-ras-and-the-custom-scripting-dll"></a>Interazione tra il server, RAS e la DLL Custom-Scripting

La DLL di scripting personalizzata deve esportare un singolo punto di ingresso: [**RasCustomScriptExecute**](/windows/desktop/api/Ras/nc-ras-rascustomscriptexecutefn). RAS chiama questa funzione durante lo stato RASCS \_ Interactive del processo di connessione. Lo stato interattivo RASCS è uno stato sospeso, che consente all'utente di interagire con un'interfaccia utente \_ presentata dalla DLL di scripting personalizzata. Per altre informazioni sugli stati di connessione, vedere [**RASCONNSTATE.**](/previous-versions/windows/desktop/legacy/aa376727(v=vs.85))

RAS passerà come parametri alla [**funzione RasCustomScriptExecute:**](/windows/desktop/api/Ras/nc-ras-rascustomscriptexecutefn)

-   Handle della porta nel computer client utilizzato per la connessione.
-   Stringhe che identificano la rubrica e la voce per la connessione.
-   RAS passa anche un handle a una finestra per consentire alla DLL di presentare un'interfaccia utente.
-   Set di puntatori a funzione che la DLL può usare per comunicare con il server.

Per altre informazioni su questi parametri, vedere [**RasCustomScriptExecute.**](/windows/desktop/api/Ras/nc-ras-rascustomscriptexecutefn)

RAS passa un puntatore a [**una struttura RASCUSTOMSCRIPTEXTENSIONS**](/previous-versions/windows/desktop/legacy/aa376738(v=vs.85)) come ultimo parametro [**a RasCustomScriptExecute**](/windows/desktop/api/Ras/nc-ras-rascustomscriptexecutefn). Questa struttura contiene un puntatore a una funzione di [**tipo PFNRASSETCOMMSETTINGS**](/windows/desktop/api/Ras/nc-ras-pfnrassetcommsettings). La DLL di scripting personalizzato chiama questa funzione per modificare le impostazioni di comunicazione sulla porta usata dalla connessione.

RAS media l'interazione tra il server e la DLL di scripting personalizzata. In genere, il server avvia la finestra di dialogo. Ad esempio, il server può richiedere il nome utente e la password dell'utente.

Quando si usa lo scripting personalizzato per stabilire una connessione, il server non deve eseguire Windows NT 4.0 o Windows 2000.

## <a name="custom-scripting-user-interface-must-support-idcancel"></a>La creazione di script Interfaccia utente deve supportare IDCANCEL

Se il dialer personalizzato visualizza un'interfaccia utente, l'interfaccia utente deve supportare i messaggi WM COMMAND in cui \_ LOWORD(*wParam*) è uguale a IDCANCEL.

## <a name="configuring-the-connection"></a>Configurazione della connessione

Il punto di ingresso [**RasCustomScriptExecute**](/windows/desktop/api/Ras/nc-ras-rascustomscriptexecutefn) può essere richiamato da [**RasDialDlg**](/windows/desktop/api/Rasdlg/nf-rasdlg-rasdialdlga) o, Windows XP, da [**RasDial**](/windows/desktop/api/Ras/nf-ras-rasdiala).

Per richiamare [**RasCustomScriptExecute**](/windows/desktop/api/Ras/nc-ras-rascustomscriptexecutefn) da [**RasDialDlg,**](/windows/desktop/api/Rasdlg/nf-rasdlg-rasdialdlga)impostare l'opzione RASEO CustomScript nella \_ voce della rubrica telefonica per la connessione. Per una descrizione delle opzioni di immissione della rubrica telefonica, vedere il membro **dwfOptions** di [**RASENTRY.**](/previous-versions/windows/desktop/legacy/aa377274(v=vs.85)) Usare le [**funzioni RasGetEntryProperties**](/windows/desktop/api/Ras/nf-ras-rasgetentrypropertiesa) e [**RasSetEntryProperties**](/windows/desktop/api/Ras/nf-ras-rassetentrypropertiesa) per impostare questa opzione a livello di codice.

**Windows XP:** Per richiamare [**RasCustomScriptExecute**](/windows/desktop/api/Ras/nc-ras-rascustomscriptexecutefn) da [**RasDial,**](/windows/desktop/api/Ras/nf-ras-rasdiala)la chiamata a **RasDial** deve specificare una struttura [**RASDIALEXTENSIONS**](/previous-versions/windows/desktop/legacy/aa377029(v=vs.85)) e questa struttura deve specificare il flag RDEOPT \_ UseCustomScripting. Inoltre, la voce della rubrica telefonica per la connessione deve specificare l'opzione \_ RASEO CustomScript come descritto nel paragrafo precedente.

## <a name="invoking-the-custom-scripting-dll"></a>Chiamata della DLL di scripting personalizzata

Se l'utente attiva una connessione per una voce della rubrica telefonica con l'opzione \_ CustomScript RASEO impostata, RAS richiama la DLL di scripting personalizzato. In questo scenario, RAS richiama la DLL di scripting personalizzata da [**RasDialDlg**](/windows/desktop/api/Rasdlg/nf-rasdlg-rasdialdlga).

Per richiamare la DLL di scripting personalizzata a livello di codice, stabilire la connessione usando la [**funzione RasDialDlg.**](/windows/desktop/api/Rasdlg/nf-rasdlg-rasdialdlga) In Windows XP, la [**funzione RasDial**](/windows/desktop/api/Ras/nf-ras-rasdiala) richiama anche la DLL di scripting personalizzata.

 

 