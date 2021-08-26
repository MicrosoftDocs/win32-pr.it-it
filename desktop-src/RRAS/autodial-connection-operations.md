---
title: Operazioni di connessione automatica
description: Quando un tentativo di connessione a un indirizzo di rete non riesce perché l'host non è raggiungibile, il sistema cerca l'indirizzo nel database di mapping AutoDial.
ms.assetid: 343ee69e-1ff5-4107-9ddb-4245c3b4a54d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ef0f65f62121d631dcf035e641c9d0d4d89850d7673e1c47b82ff4a4889dff49
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120030501"
---
# <a name="autodial-connection-operations"></a>Operazioni di connessione automatica

Quando un tentativo di connessione a un indirizzo di rete non riesce perché l'host non è raggiungibile, il sistema cerca l'indirizzo nel database di mapping AutoDial. Se l'indirizzo si trova nel database, il sistema avvia un'operazione AutoDial per [**rasAUTODIALENTRY,**](/previous-versions/windows/desktop/legacy/aa376721(v=vs.85))se presente, che corrisponde alla località di composizione TAPI locale.

L'API RAS fornisce funzioni che consentono di impostare ed eseguire query sui parametri AutoDial che controllano le connessioni AutoDial. È possibile chiamare la [**funzione RasSetAutodialEnable**](/windows/desktop/api/Ras/nf-ras-rassetautodialenablea) per abilitare o disabilitare la funzionalità AutoDial per una località di composizione TAPI specificata. La [**funzione RasGetAutodialEnable**](/windows/desktop/api/Ras/nf-ras-rasgetautodialenablea) indica se la funzionalità AutoDial è abilitata per una località di composizione TAPI specificata. Per altre informazioni sulle località di composizione TAPI, vedere la documentazione di TAPI. È possibile chiamare la [**funzione RasSetAutodialParam**](/windows/desktop/api/Ras/nf-ras-rassetautodialparama) per impostare altri parametri di connessione AutoDial. Ad esempio, è possibile disabilitare le connessioni AutoDial per la sessione di accesso corrente. Chiamare la [**funzione RasGetAutodialParam**](/windows/desktop/api/Ras/nf-ras-rasgetautodialparama) per determinare il valore corrente dei parametri di connessione AutoDial.

Il sistema fornisce un'interfaccia utente predefinita per le operazioni di composizione automatica. È tuttavia possibile creare una libreria di collegamento dinamico (DLL) AutoDial per fornire un'interfaccia utente personalizzata per le operazioni di composizione automatica che coinvolgono voci della rubrica specificate. La DLL AutoDial deve esportare sia una versione ANSI che una versione Unicode di [**un gestore AutoDial RASADFunc.**](/windows/desktop/api/Ras/nc-ras-rasadfunca)

Per abilitare il gestore AutoDial personalizzato per una voce della rubrica, chiamare la [**funzione RasSetEntryProperties**](/windows/desktop/api/Ras/nf-ras-rassetentrypropertiesa) per impostare le proprietà per tale voce. I membri **szAutodialDll** e **szAutodialFunc** della struttura [**RASENTRY**](/previous-versions/windows/desktop/legacy/aa377274(v=vs.85)) passati **a RasSetEntryProperties** specificano il nome della DLL AutoDial e il nome della funzione [**RASADFunc,**](/windows/desktop/api/Ras/nc-ras-rasadfunca) escluso il suffisso "A" o "W".

Quando il sistema avvia un'operazione AutoDial per una voce della rubrica con un gestore AutoDial personalizzato, chiama l'oggetto [**RASADFunc specificato.**](/windows/desktop/api/Ras/nc-ras-rasadfunca) La **funzione RASADFunc** riceve un puntatore a una [**struttura RASADPARAMS**](/previous-versions/windows/desktop/legacy/aa376719(v=vs.85)) che indica la posizione e la finestra padre per la finestra dell'interfaccia utente. **RASADFunc può** avviare un thread per eseguire l'operazione di composizione personalizzata. La **funzione RASADFunc** restituisce **TRUE** per indicare che ha assunto la composizione o **FALSE** per consentire al sistema di eseguire la composizione. L'operazione di composizione personalizzata deve usare [**la funzione RasDial**](/windows/desktop/api/Ras/nf-ras-rasdiala) per eseguire la composizione effettiva. Al termine dell'operazione di composizione, l'operazione di composizione personalizzata indica l'esito positivo o negativo impostando la variabile a cui punta il parametro *lpdwRetCode* passato a [**RASADFunc**](/windows/desktop/api/Ras/nc-ras-rasadfunca).

 

 