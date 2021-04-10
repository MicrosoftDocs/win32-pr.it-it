---
title: Altre informazioni di connessione
description: I membri della struttura RASDIALPARAMS possono inoltre specificare le informazioni di connessione seguenti.
ms.assetid: 95a8dd78-e424-4d0b-899a-69deb9e1b9cd
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ea4d006cd3cb31d5dc7229043b2a8ef169c22d76
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "103963190"
---
# <a name="other-connection-information"></a>Altre informazioni di connessione

I membri della struttura [**RASDIALPARAMS**](/previous-versions/windows/desktop/legacy/aa377238(v=vs.85)) possono inoltre specificare le informazioni di connessione seguenti.

-   Numero di telefono per l'override del numero nella voce della rubrica telefonica.
-   Numero di telefono di [callback](callback-connections.md) che il server remoto può richiamare per stabilire la connessione.
-   Nome del dominio di rete remoto in cui deve essere eseguita l'autenticazione.

Per il numero di callback e il dominio, i membri di [**RASDIALPARAMS**](/previous-versions/windows/desktop/legacy/aa377238(v=vs.85)) possono indicare che RAS deve usare le informazioni nella voce della rubrica telefonica oppure può fornire informazioni che sostituiscono i dati della rubrica telefonica.

Un client RAS può utilizzare il parametro *lpRasDialExtensions* della funzione [**RasDial**](/windows/desktop/api/Ras/nf-ras-rasdiala) per controllare se RAS utilizza un prefisso o un suffisso di numero di telefono specificato in una voce della rubrica telefonica.

 

 