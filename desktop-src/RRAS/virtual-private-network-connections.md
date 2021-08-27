---
title: Connessioni di rete privata virtuale
description: Il servizio di accesso remoto (RAS) supporta le connessioni di rete privata virtuale (VPN), oltre alle connessioni di accesso remoto convenzionali che usano Point-to-Point Protocol (PPP).
ms.assetid: c1195ebb-3107-4429-bc67-b64577d66268
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4fc532d0873a5c3cb4a50552ca267a8a88b305ad855a1588338786881b3af04e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120024781"
---
# <a name="virtual-private-network-connections"></a>Connessioni di rete privata virtuale

Il servizio di accesso remoto (RAS) supporta le connessioni di rete privata virtuale (VPN), oltre alle connessioni di accesso remoto convenzionali che usano Point-to-Point Protocol (PPP). In una connessione VPN i pacchetti VPN vengono incapsulati in pacchetti IP e inviati attraverso una rete IP, ad esempio Internet. Pertanto, l'accesso a una rete IP è un requisito per stabilire una connessione VPN. Se il computer client ha una connessione sempre attiva a una rete IP, ad esempio una connessione a una LAN IP, il client può stabilire la connessione VPN usando una singola chiamata alla funzione [**RasDial.**](/windows/desktop/api/Ras/nf-ras-rasdiala)

Se il computer client non ha una connessione sempre attiva a una rete IP, sono necessarie due chiamate a [**RasDial**](/windows/desktop/api/Ras/nf-ras-rasdiala) per stabilire la connessione VPN. La prima chiamata stabilisce una connessione remota alla rete IP. la seconda chiamata stabilisce la connessione VPN.

Il **membro szLocalPhoneNumber** della struttura [**RASENTRY**](/previous-versions/windows/desktop/legacy/aa377274(v=vs.85)) per la connessione VPN deve contenere il nome DNS o l'indirizzo IP del server VPN di destinazione.

Ogni connessione richiede una voce [separata per la rubrica.](ras-phone-books.md) La prima chiamata a [**RasDial**](/windows/desktop/api/Ras/nf-ras-rasdiala) specifica la voce della rubrica per la rete IP. La seconda chiamata specifica la voce della rubrica per la VPN.

La [**funzione RasDial**](/windows/desktop/api/Ras/nf-ras-rasdiala) accetta un puntatore a una [**struttura RASDIALPARAMS**](/previous-versions/windows/desktop/legacy/aa377238(v=vs.85)) come parametro. Questa struttura specifica le credenziali di autenticazione da usare per la rete specificata dalla voce della rubrica. Le credenziali necessarie per accedere alla rete IP sono in genere diverse da quelle per la VPN. La prima chiamata a **RasDial deve** specificare le credenziali per la rete IP. La seconda chiamata deve specificare le credenziali per la VPN.

Se la [**funzione RasDial**](/windows/desktop/api/Ras/nf-ras-rasdiala) ha esito positivo, restituisce un handle per la connessione. Usare questo handle in una chiamata a [**RasHangUp**](/windows/desktop/api/Ras/nf-ras-rashangupa) per terminare la connessione.

Nello scenario precedente, le due chiamate a [**RasDial**](/windows/desktop/api/Ras/nf-ras-rasdiala) restituiscono handle di connessione separati per la rete IP e la VPN. La [**chiamata di RasHangUp**](/windows/desktop/api/Ras/nf-ras-rashangupa) con l'handle per la connessione VPN termina la connessione VPN, ma lascia intatta la connessione alla rete IP.

 

 