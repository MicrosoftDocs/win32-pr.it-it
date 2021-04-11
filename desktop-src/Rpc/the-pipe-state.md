---
title: Stato della pipe
description: Sul server, il compilatore MIDL crea una variabile di stato che coordina le procedure push, pull e allocazione.
ms.assetid: 7cc59cb3-cf41-40f7-a28f-b896c319ae64
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a6d7ec8af1907c98b7cf2098f4979dac62ef573a
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104118055"
---
# <a name="the-pipe-state"></a>Stato della pipe

Sul server, il compilatore MIDL crea una variabile di *stato* che coordina le procedure push, pull e allocazione. Sul lato client, lo sviluppatore deve creare la variabile di *stato* . La variabile di *stato* è quindi locale a entrambi i lati, ovvero il client e il server mantengono il proprio stato di pipe. Il codice stub del server mantiene la variabile di stato nel server. Non tentare di modificare direttamente il contenuto. Il client deve inizializzare i campi nella struttura del controllo pipe e mantenerne la variabile di *stato* . Usa la variabile di *stato* per identificare dove individuare o inserire i dati.

La variabile di *stato* del client può essere semplice come un handle di file, se si trasferiscono dati da un file a un altro. Può anche essere un numero intero che punta a un elemento in una matrice. In alternativa, è possibile definire una struttura di stato piuttosto complessa per eseguire attività aggiuntive, ad esempio il coordinamento delle routine push e pull \[ [in un](/windows/desktop/Midl/in)parametro [out](/windows/desktop/Midl/out-idl) \] .

 

 