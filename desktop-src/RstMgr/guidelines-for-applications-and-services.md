---
title: Linee guida per le applicazioni e i servizi
description: Per ridurre il numero di riavvii del sistema durante l'installazione e la manutenzione di applicazioni in Windows Vista o Windows Server 2008, è necessario osservare le linee guida seguenti per consentire l'arresto corretto e riavviato dell'applicazione o del servizio.
ms.assetid: d0b9344f-05c6-4054-90b9-86942df50b3d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: eaf2963c03432a8b016f01316b79b387754f1459
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "106297945"
---
# <a name="guidelines-for-applications-and-services"></a>Linee guida per le applicazioni e i servizi

Per ridurre il numero di riavvii del sistema durante l'installazione e la manutenzione di applicazioni in Windows Vista o Windows Server 2008, è necessario osservare le linee guida seguenti per consentire l'arresto corretto e riavviato dell'applicazione o del servizio.

-   Le applicazioni e i servizi devono essere preparati per essere arrestati e riavviati dal sistema quando è necessario installare un aggiornamento. In genere, quando viene installato un aggiornamento, è necessario arrestare un'applicazione o un servizio perché attualmente è in uso un file interessato. Tutte le applicazioni o i servizi che possono contenere un file in uso durante un aggiornamento devono essere preparati per l'arresto corretto.
-   Le applicazioni devono salvare i dati utente e le informazioni sullo stato necessarie dopo un riavvio e rispettare le linee guida descritte nella sezione [linee guida per le applicazioni](guidelines-for-applications.md).
-   I servizi devono rispettare le linee guida descritte nella sezione [linee guida per i servizi di](guidelines-for-services.md).
-   Gestione riavvio non arresta i [servizi di sistema critici](critical-system-services.md). Pertanto, questi servizi devono limitare il numero di dll da cui dipendono.

 

 




