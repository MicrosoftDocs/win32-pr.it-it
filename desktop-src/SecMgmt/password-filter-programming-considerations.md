---
description: Vengono illustrate le considerazioni per l'implementazione delle funzioni di esportazione del filtro delle password.
ms.assetid: ec7c1e7e-844a-43d4-b756-02bc1062d7b8
title: Considerazioni sulla programmazione del filtro password
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9ad13a52f66c29142248ca07179d8692887b1acb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106306435"
---
# <a name="password-filter-programming-considerations"></a>Considerazioni sulla programmazione del filtro password

Quando si implementano le funzioni di esportazione del [*filtro delle password*](/windows/desktop/SecGloss/p-gly) , tenere presenti le considerazioni seguenti:

-   Prestare particolare attenzione quando si utilizzano password in [*testo non crittografato*](/windows/desktop/SecGloss/p-gly) . L'invio di password in testo non crittografato attraverso le reti potrebbe compromettere I "sniffer" della rete possono controllare facilmente il traffico delle password in testo non crittografato.
-   Cancellare tutta la memoria usata per archiviare le password chiamando la funzione [**SecureZeroMemory**](/previous-versions/windows/desktop/legacy/aa366877(v=vs.85)) prima di liberare la memoria.
-   Tutti i buffer passati nelle routine di notifica e filtro delle password devono essere considerati di sola lettura. La scrittura di dati in questi buffer può causare un comportamento instabile.
-   Tutte le routine di notifica e filtro della password devono essere thread-safe. Usare sezioni critiche o altre tecniche di programmazione sincrona per proteggere i dati laddove appropriato.
-   La notifica e il filtro delle password avvengono solo nel computer che ospita l'account.
-   Tutti i controller di dominio sono scrivibili, quindi i pacchetti di filtro password devono essere presenti in tutti i controller di dominio.

    **Domini di Windows NT 4,0:** La notifica sugli account di dominio si verifica solo sul controller di dominio primario. Oltre al controller di dominio primario, i pacchetti di filtro password devono essere installati in tutti i controller di dominio di backup per consentire la continuazione delle notifiche in caso di modifiche al ruolo del server.

-   Tutte le dll del filtro password vengono eseguite nel [*contesto di sicurezza*](/windows/desktop/SecGloss/s-gly) dell'account di sistema locale.



| Per informazioni su                                                                                                                     | Vedere                                                                                                      |
|-------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------|
| Come installare e registrare la propria DLL di [*filtro password*](/windows/desktop/SecGloss/p-gly) . | [Installazione e registrazione di una DLL di filtro password](installing-and-registering-a-password-filter-dll.md) |
| DLL di filtro password fornita da Microsoft.                                                                                            | [Imposizione avanzata delle password e Passfilt.dll](strong-password-enforcement-and-passfilt-dll.md)         |
| Esporta le funzioni implementate da una DLL di filtro password.                                                                                    | [Funzioni di filtro password](management-functions.md)                          |



 

 

 
