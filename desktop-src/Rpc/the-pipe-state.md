---
title: Stato della pipe
description: Nel server il compilatore MIDL crea una variabile di stato che coordina le procedure push, pull e alloc.
ms.assetid: 7cc59cb3-cf41-40f7-a28f-b896c319ae64
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8d12c5ef5549d89f3aee2833599f5930f2617478e66e16c3b78188eb63a40e7d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118924071"
---
# <a name="the-pipe-state"></a>Stato della pipe

Nel server il compilatore MIDL crea una variabile *di* stato che coordina le procedure push, pull e alloc. Sul lato client, lo sviluppatore deve creare la variabile *di* stato. Pertanto, la *variabile di stato* è locale per entrambi i lati, ovvero il client e il server mantengono ciascuno il proprio stato di pipe. Il codice stub del server mantiene la variabile di stato nel server. Non è consigliabile tentare di modificarne direttamente il contenuto. Il client deve inizializzare i campi nella struttura di controllo della pipe e mantenere la variabile *di* stato. Usa la variabile *di stato* per identificare dove individuare o posizionare i dati.

La variabile *di stato* client può essere semplice come un handle di file, se si trasferiscono dati da un file a un altro. Può anche essere un numero intero che punta a un elemento in una matrice. In caso contrario, è possibile definire una struttura di stato piuttosto complessa per eseguire attività aggiuntive, ad esempio il coordinamento delle routine push e pull in un \[ [parametro in](/windows/desktop/Midl/in), [out.](/windows/desktop/Midl/out-idl) \]

 

 