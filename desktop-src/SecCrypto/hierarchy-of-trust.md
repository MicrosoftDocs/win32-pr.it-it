---
description: L'attendibilità di un certificato digitale viene stabilita usando una gerarchia di trust.
ms.assetid: 13ee08b4-9c8e-480b-b78d-9472a2d7b566
title: Gerarchia di trust
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 485c721493a93c7ea55b1993345e8168ccab319b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103884050"
---
# <a name="hierarchy-of-trust"></a>Gerarchia di trust

Per garantire l'efficacia dei [*certificati digitali*](../secgloss/c-gly.md) , gli utenti di certificati devono disporre di un elevato livello di attendibilità. Ci sono casi in cui un utente non considera attendibile l'autorità emittente di un certificato. Questo problema può verificarsi se l'utente del certificato non ha mai sentito l' [*autorità di certificazione*](../secgloss/c-gly.md) e pertanto non è in grado di accettare un certificato da tale emittente sul valore del volto. Questo problema viene risolto nel processo di certificazione da una gerarchia di trust.

Una gerarchia di trust inizia con almeno un'autorità di certificazione considerata attendibile da tutte le entità nella catena di certificati. Può trattarsi di un amministratore dell'autorità di certificazione interna o di un'azienda o un'organizzazione esterna specializzata nella verifica delle identità e nell'emissione di certificati. Questa autorità è detta [*autorità radice*](../secgloss/r-gly.md). L'autorità radice certifica quindi altre autorità di certificazione, denominate autorità di certificazione di primo livello, che possono emettere certificati e certificare anche le autorità di certificazione aggiuntive o di secondo livello. Questa situazione è illustrata nella figura seguente.

![gerarchia di trust](images/trust.png)

L'identità dell'autorità di certificazione che emette un certificato fa parte di un certificato. Questa autorità di certificazione viene chiamata autorità emittente del certificato. Quando l'emittente di un certificato è un'autorità di certificazione di livello 1 o 2, il destinatario del certificato può determinare se l'emittente del certificato è certificato come autorità di certificazione valida da un'autorità di certificazione a un livello superiore e che l'autorità di certificazione di livello superiore è certificata come autorità di certificazione valida da un'autorità di certificazione di livello superiore fino a quando non viene stabilito che esiste una catena di trust tra l'autorità di certificazione di livello più basso e la radice autorità di certificazione.

Nella figura precedente, ad esempio, è possibile verificare che \# la CA 4 sia stata certificata come autorità di certificazione dalla CA \# 1 e che \# la CA 1 sia stata certificata come autorità di certificazione dalla CA radice. Pertanto, quando viene passato un certificato da un'autorità di certificazione di livello inferiore insieme al messaggio crittografato, vengono passate informazioni su tutti i certificati nella catena di trust fino alla radice.

L'illustrazione e la descrizione appena presentate sono concettuali. Nel mondo reale, la situazione dell'autorità di certificazione è in continua evoluzione e non è stata stabilita o accettata alcuna autorità radice singola. A breve termine, le isole dell'autorità si svilupperanno come illustrato nella figura seguente.

![Isole di autorità in una gerarchia di trust](images/trust2.png)

Nel tempo, le isole radice, radice 1 e la radice 2 nell'illustrazione, potrebbero diventare CA di livello 1 a un'unica CA radice. A questo punto, la situazione avrebbe nuovamente una singola autorità radice. Resta da visualizzare solo il modo in cui l'immagine effettiva si evolverà.

 

 
