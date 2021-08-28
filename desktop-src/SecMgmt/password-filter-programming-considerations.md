---
description: Vengono illustrate le considerazioni per l'implementazione delle funzioni di esportazione del filtro password.
ms.assetid: ec7c1e7e-844a-43d4-b756-02bc1062d7b8
title: Considerazioni sulla programmazione del filtro password
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7e9270a08c51b4b3e6b07923ad9461dc2e2dd418c3be1f1a181c07f940d71ba7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119005089"
---
# <a name="password-filter-programming-considerations"></a>Considerazioni sulla programmazione del filtro password

Quando si implementano [*le funzioni di*](/windows/desktop/SecGloss/p-gly) esportazione del filtro password, tenere presenti le considerazioni seguenti:

-   Quando si lavora con password [*in testo non crittografato,*](/windows/desktop/SecGloss/p-gly) è necessario fare attenzione. L'invio di password in testo non crittografato sulle reti potrebbe compromettere la sicurezza. Gli "sniffer" di rete possono controllare facilmente il traffico delle password in testo non crittografato.
-   Cancellare tutta la memoria usata per archiviare le password chiamando la [**funzione SecureZeroMemory**](/previous-versions/windows/desktop/legacy/aa366877(v=vs.85)) prima di liberare memoria.
-   Tutti i buffer passati nelle routine di notifica della password e filtro devono essere considerati di sola lettura. La scrittura di dati in questi buffer può causare un comportamento instabile.
-   Tutte le routine di notifica e filtro delle password devono essere thread-safe. Usare sezioni critiche o altre tecniche di programmazione sincrone per proteggere i dati, se necessario.
-   La notifica delle password e il filtro vengono esersi solo nel computer che ospita l'account.
-   Tutti i controller di dominio sono scrivibili, pertanto i pacchetti di filtro delle password devono essere presenti in tutti i controller di dominio.

    **Windows NT 4.0:** La notifica sugli account di dominio viene inviata solo nel controller di dominio primario. Oltre al controller di dominio primario, i pacchetti di filtro password devono essere installati in tutti i controller di dominio di backup per consentire la continuazione delle notifiche in caso di modifiche al ruolo del server.

-   Tutte le DLL del filtro password vengono eseguite nel [*contesto di sicurezza dell'account*](/windows/desktop/SecGloss/s-gly) di sistema locale.



| Per informazioni su                                                                                                                     | Vedere                                                                                                      |
|-------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------|
| Come installare e registrare la DLL del [*filtro*](/windows/desktop/SecGloss/p-gly) password. | [Installazione e registrazione di una DLL filtro password](installing-and-registering-a-password-filter-dll.md) |
| DLL del filtro delle password fornita da Microsoft.                                                                                            | [Imposizione delle password complessa e Passfilt.dll](strong-password-enforcement-and-passfilt-dll.md)         |
| Funzioni di esportazione implementate da una DLL di filtro delle password.                                                                                    | [Funzioni di filtro password](management-functions.md)                          |



 

 

 
