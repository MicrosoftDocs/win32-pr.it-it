---
title: Linee guida per applicazioni e servizi
description: Per ridurre il numero di riavvii del sistema durante l'installazione e la manutenzione di applicazioni in Windows Vista o Windows Server 2008, è necessario osservare le linee guida seguenti per abilitare l'arresto pulito e il riavvio dell'applicazione o del servizio.
ms.assetid: d0b9344f-05c6-4054-90b9-86942df50b3d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d1d4aa10da60ca5019a723ec996532ac5b60fdbfcdb7c322ff07ecbf8681f37b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119010159"
---
# <a name="guidelines-for-applications-and-services"></a>Linee guida per applicazioni e servizi

Per ridurre il numero di riavvii del sistema durante l'installazione e la manutenzione di applicazioni in Windows Vista o Windows Server 2008, è necessario osservare le linee guida seguenti per abilitare l'arresto pulito e il riavvio dell'applicazione o del servizio.

-   Le applicazioni e i servizi devono essere pronti per essere arrestati e riavviati dal sistema quando è necessario installare un aggiornamento. In genere, quando viene installato un aggiornamento, un'applicazione o un servizio deve essere arrestato perché attualmente contiene un file interessato in uso. Tutte le applicazioni o i servizi che possono contenere un file in uso durante un aggiornamento devono essere pronti per l'arresto pulito.
-   Le applicazioni devono salvare i dati utente e le informazioni sullo stato necessari dopo un riavvio e devono rispettare le linee guida descritte nella sezione Linee guida [per le applicazioni](guidelines-for-applications.md).
-   I servizi devono rispettare le linee guida descritte nella sezione [Linee guida per i servizi](guidelines-for-services.md).
-   Gestione riavvio non arresta i [servizi di sistema critici.](critical-system-services.md) Pertanto, questi servizi devono limitare il numero di DLL da cui dipendono.

 

 




