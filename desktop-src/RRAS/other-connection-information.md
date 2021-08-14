---
title: Altre informazioni di connessione
description: I membri della struttura RASDIALPARAMS possono inoltre specificare le informazioni di connessione seguenti.
ms.assetid: 95a8dd78-e424-4d0b-899a-69deb9e1b9cd
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c596dbfb160766283beb9c48a5faf4e8258dcf0361ad7a504188a29207c0500f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117789932"
---
# <a name="other-connection-information"></a>Altre informazioni di connessione

I membri della [**struttura RASDIALPARAMS**](/previous-versions/windows/desktop/legacy/aa377238(v=vs.85)) possono inoltre specificare le informazioni di connessione seguenti.

-   Numero di telefono per sostituire il numero nella voce della rubrica.
-   Numero [di telefono](callback-connections.md) di callback che il server remoto può richiamare per stabilire la connessione.
-   Nome del dominio di rete remoto in cui deve essere eseguita l'autenticazione.

Per il numero di callback e il dominio, i membri [**rasDIALPARAMS**](/previous-versions/windows/desktop/legacy/aa377238(v=vs.85)) possono indicare che RAS deve usare le informazioni nella voce della rubrica o può fornire informazioni che sostituiscono i dati della rubrica.

Un client RAS può usare il parametro *lpRasDialExtensions* della funzione [**RasDial**](/windows/desktop/api/Ras/nf-ras-rasdiala) per controllare se RAS usa un prefisso del numero di telefono o un suffisso specificato in una voce della rubrica.

 

 