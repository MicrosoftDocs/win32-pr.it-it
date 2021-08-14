---
title: Funzioni WNet
description: Windows Le funzioni di rete forniscono informazioni e utilità per la gestione delle risorse di rete.
ms.assetid: 8a83186f-a912-4c61-8137-1f6be1f3afd6
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 771974bcc2967ddba32439bb655173f62b8478ad367e086e620ca02825a2567f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118330786"
---
# <a name="wnet-functions"></a>Funzioni WNet

Windows Le funzioni di rete forniscono informazioni e utilità per la gestione delle risorse di rete. Le Windows di rete possono essere raggruppate nel modo seguente:

-   [Funzioni di connessione](#connection-functions)
-   [Funzioni di enumerazione](#enumeration-functions)
-   [Funzioni informative](#information-functions)
-   [Funzioni utente](#user-functions)

## <a name="connection-functions"></a>Funzioni di connessione

Chiamare le funzioni di connessione WNet seguenti per connettere un dispositivo locale a una risorsa di rete e per annullare le connessioni di rete.



| Funzione                                                                     | Descrizione                                                                                                                                                                                                                    |
|------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**MultinetGetConnectionPerformance**](/windows/win32/api/winnetwk/nf-winnetwk-multinetgetconnectionperformancea) | Restituisce informazioni sulle prestazioni previste di una connessione a una risorsa di rete.                                                                                                                                      |
| [**WNetAddConnection**](/windows/win32/api/winnetwk/nf-winnetwk-wnetaddconnectiona)                               | Connette un dispositivo locale a una risorsa di rete. Disponibile per la compatibilità con le versioni a 16 bit Windows.                                                                                                                   |
| [**WNetAddConnection2**](/windows/win32/api/winnetwk/nf-winnetwk-wnetaddconnection2a)                             | Connette un dispositivo locale a una risorsa di rete.                                                                                                                                                                                 |
| [**WNetAddConnection3**](/windows/win32/api/winnetwk/nf-winnetwk-wnetaddconnection3a)                             | Connette un dispositivo locale a una risorsa di rete. Questa funzione include un parametro in più rispetto alla funzione **WNetAddConnection2,** un handle per una finestra che il provider di rete può usare come finestra di proprietario per le finestre di dialogo. |
| [**WNetCancelConnection**](/windows/win32/api/winnetwk/nf-winnetwk-wnetcancelconnectiona)                         | Annulla una connessione di rete. Disponibile per la compatibilità con le versioni a 16 bit Windows.                                                                                                                                    |
| [**WNetCancelConnection2**](/windows/win32/api/winnetwk/nf-winnetwk-wnetcancelconnection2a)                       | Annulla una connessione di rete, offrendo la possibilità di aggiornare il profilo utente con informazioni sulle connessioni permanenti.                                                                                                  |
| [**WNetConnectionDialog**](/windows/win32/api/winnetwk/nf-winnetwk-wnetconnectiondialog)                         | Avvia una finestra di dialogo di esplorazione generale per la connessione alle risorse di rete.                                                                                                                                                      |
| [**WNetConnectionDialog1**](/windows/win32/api/winnetwk/nf-winnetwk-wnetconnectiondialog1a)                       | Avvia una finestra di dialogo di esplorazione generale per la connessione alle risorse di rete usando una [**struttura CONNECTDLGSTRUCT.**](/windows/win32/api/winnetwk/ns-winnetwk-connectdlgstructa)                                                                                  |
| [**WNetDisconnectDialog**](/windows/win32/api/winnetwk/nf-winnetwk-wnetdisconnectdialog)                         | Avvia una finestra di dialogo di esplorazione generale per la disconnessione dalle risorse di rete.                                                                                                                                                 |
| [**WNetDisconnectDialog1**](/windows/win32/api/winnetwk/nf-winnetwk-wnetdisconnectdialog1a)                       | Avvia una finestra di dialogo di esplorazione generale per la disconnessione dalle risorse di rete usando una [**struttura DISCDLGSTRUCT.**](/windows/win32/api/winnetwk/ns-winnetwk-discdlgstructa)                                                                                   |
| [**WNetGetConnection**](/windows/win32/api/winnetwk/nf-winnetwk-wnetgetconnectiona)                               | Recupera il nome della risorsa di rete associata a un dispositivo locale.                                                                                                                                                     |
| [**WNetGetUniversalName**](/windows/win32/api/winnetwk/nf-winnetwk-wnetgetuniversalnamea)                         | Quando viene specificato un percorso basato su unità per una risorsa di rete, restituisce una forma più universale del nome.                                                                                                                               |
| [**WNetRestoreConnectionW**](/windows/win32/api/winnetwk/nf-winnetwk-wnetrestoreconnectionw)                     | Ripristina la connessione a una risorsa di rete, richiedendo all'utente, se necessario, un nome e una password.                                                                                                                      |
| [**WNetUseConnection**](/windows/win32/api/winnetwk/nf-winnetwk-wnetuseconnectiona)                               | Connette un dispositivo locale a una risorsa di rete. seleziona automaticamente un dispositivo locale inutilizzato per il reindirizzamento alla risorsa di rete.                                                                                               |



 

> [!Note]  
> Le [**funzioni WNetAddConnection**](/windows/win32/api/winnetwk/nf-winnetwk-wnetaddconnectiona) e [**WNetCancelConnection**](/windows/win32/api/winnetwk/nf-winnetwk-wnetcancelconnectiona) sono supportate per la compatibilità con Windows per i gruppi di lavoro. Tuttavia, le nuove applicazioni devono [**usare WNetAddConnection2**](/windows/win32/api/winnetwk/nf-winnetwk-wnetaddconnection2a) o [**WNetAddConnection3**](/windows/win32/api/winnetwk/nf-winnetwk-wnetaddconnection3a)e [**WNetCancelConnection2**](/windows/win32/api/winnetwk/nf-winnetwk-wnetcancelconnection2a).

 

## <a name="enumeration-functions"></a>Funzioni di enumerazione

Chiamare le funzioni WNet seguenti per enumerare le risorse di rete.



| Funzione                                     | Descrizione                                                                             |
|----------------------------------------------|-----------------------------------------------------------------------------------------|
| [**WNetCloseEnum**](/windows/win32/api/winnetwk/nf-winnetwk-wnetcloseenum)       | Termina un'enumerazione di risorse di rete.                                                    |
| [**WNetEnumResource**](/windows/win32/api/winnetwk/nf-winnetwk-wnetenumresourcea) | Continua un'enumerazione delle risorse di rete avviate **dalla funzione WNetOpenEnum.** |
| [**WNetOpenEnum**](/windows/win32/api/winnetwk/nf-winnetwk-wnetopenenuma)         | Avvia un'enumerazione di risorse di rete.                                             |



 

## <a name="information-functions"></a>Funzioni informative

Chiamare le funzioni di utilità e informazioni WNet seguenti per recuperare il provider di rete e altre informazioni.



| Funzione                                                         | Descrizione                                                                                         |
|------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------|
| [**WNetGetLastError**](/windows/win32/api/winnetwk/nf-winnetwk-wnetgetlasterrora)                     | Restituisce il codice di errore più recente impostato da una funzione WNet, quello segnalato da un provider di rete.  |
| [**WNetGetNetworkInformation**](/windows/win32/api/winnetwk/nf-winnetwk-wnetgetnetworkinformationa)   | Restituisce informazioni estese su un provider di rete specifico.                                     |
| [**WNetGetProviderName**](/windows/win32/api/winnetwk/nf-winnetwk-wnetgetprovidernamea)               | Restituisce il nome del provider per un tipo specifico di rete.                                           |
| [**WNetGetResourceInformation**](/windows/win32/api/winnetwk/nf-winnetwk-wnetgetresourceinformationa) | Restituisce il provider di rete proprietario di una risorsa e ottiene informazioni sul tipo di risorsa. |
| [**WNetGetResourceParent**](/windows/win32/api/winnetwk/nf-winnetwk-wnetgetresourceparenta)           | Restituisce l'elemento padre di una risorsa di rete.                                                           |



 

## <a name="user-functions"></a>Funzioni utente

Chiamare la funzione WNet seguente per recuperare il nome dell'utente associato a un dispositivo locale.



| Funzione                           | Descrizione                                                                              |
|------------------------------------|------------------------------------------------------------------------------------------|
| [**WNetGetUser**](/windows/win32/api/winnetwk/nf-winnetwk-wnetgetusera) | Restituisce il nome utente predefinito corrente o il nome utente che ha stabilito la connessione. |



 

Molte delle funzioni WNet usano una [**struttura NETRESOURCE**](/windows/desktop/api/Winnetwk/ns-winnetwk-netresourcea) per archiviare informazioni su una risorsa di rete.

 

 