---
title: Operazioni di connessione con connessione automatica
description: Quando un tentativo di connessione a un indirizzo di rete non riesce perché non è possibile raggiungere l'host, il sistema cerca l'indirizzo nel database di mapping della connessione automatica.
ms.assetid: 343ee69e-1ff5-4107-9ddb-4245c3b4a54d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 150fa8542d1724be9d60f997db7952d6df387b9b
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104399119"
---
# <a name="autodial-connection-operations"></a>Operazioni di connessione con connessione automatica

Quando un tentativo di connessione a un indirizzo di rete non riesce perché non è possibile raggiungere l'host, il sistema cerca l'indirizzo nel database di mapping della connessione automatica. Se l'indirizzo è presente nel database, il sistema avvia un'operazione di Autodial per l' [**RASAUTODIALENTRY**](/previous-versions/windows/desktop/legacy/aa376721(v=vs.85)), se presente, che corrisponde alla posizione di composizione TAPI locale.

L'API RAS fornisce funzioni che consentono di impostare ed eseguire query sui parametri di Autodial che controllano le connessioni con connessione automatica. È possibile chiamare la funzione [**RasSetAutodialEnable**](/windows/desktop/api/Ras/nf-ras-rassetautodialenablea) per abilitare o disabilitare la funzionalità di Autodial per una posizione di composizione TAPI specificata. La funzione [**RasGetAutodialEnable**](/windows/desktop/api/Ras/nf-ras-rasgetautodialenablea) indica se la funzionalità Autodial è abilitata per una posizione di composizione TAPI specificata. Per ulteriori informazioni sui percorsi di composizione TAPI, vedere la documentazione di TAPI. È possibile chiamare la funzione [**RasSetAutodialParam**](/windows/desktop/api/Ras/nf-ras-rassetautodialparama) per impostare altri parametri di connessione con connessione automatica. È ad esempio possibile disabilitare le connessioni con connessione automatica per la sessione di accesso corrente. Chiamare la funzione [**RasGetAutodialParam**](/windows/desktop/api/Ras/nf-ras-rasgetautodialparama) per determinare il valore corrente dei parametri di connessione con connessione automatica.

Il sistema fornisce un'interfaccia utente predefinita per le operazioni di composizione automatica. Tuttavia, è possibile creare una libreria di collegamento dinamico (DLL) di composizione automatica per fornire un'interfaccia utente personalizzata per le operazioni di composizione automatica che coinvolgono le voci della rubrica telefonica specificate. La DLL di Autodial deve esportare sia una versione ANSI che una versione Unicode di un gestore di Autodial [**RASADFunc**](/windows/desktop/api/Ras/nc-ras-rasadfunca) .

Per abilitare il gestore di Autodial personalizzato per una voce della rubrica telefonica, chiamare la funzione [**RasSetEntryProperties**](/windows/desktop/api/Ras/nf-ras-rassetentrypropertiesa) per impostare le proprietà per tale voce. I membri **szAutodialDll** e **SzAutodialFunc** della struttura [**RASENTRY**](/previous-versions/windows/desktop/legacy/aa377274(v=vs.85)) passata a **RasSetEntryProperties** specificano il nome della DLL di Autodial e il nome della funzione [**RASADFunc**](/windows/desktop/api/Ras/nc-ras-rasadfunca) , escluso il suffisso "A" o "W".

Quando il sistema avvia un'operazione di Autodial per una voce della rubrica telefonica con un gestore di Autodial personalizzato, chiama il [**RASADFunc**](/windows/desktop/api/Ras/nc-ras-rasadfunca)specificato. La funzione **RASADFunc** riceve un puntatore a una struttura [**RASADPARAMS**](/previous-versions/windows/desktop/legacy/aa376719(v=vs.85)) che indica la posizione e la finestra padre per la finestra dell'interfaccia utente. Il **RASADFunc** può avviare un thread per eseguire l'operazione di composizione personalizzata. La funzione **RASADFunc** restituisce **true** per indicare che è stata eseguita la chiamata o **false** per consentire al sistema di eseguire la composizione. Per eseguire la composizione effettiva, l'operazione di composizione personalizzata deve usare la funzione [**RasDial**](/windows/desktop/api/Ras/nf-ras-rasdiala) . Al termine dell'operazione di composizione, l'operazione di connessione personalizzata indica l'esito positivo o negativo impostando la variabile a cui punta il parametro *lpdwRetCode* passato a [**RASADFunc**](/windows/desktop/api/Ras/nc-ras-rasadfunca).

 

 