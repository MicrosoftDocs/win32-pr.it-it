---
title: Funzioni WNet
description: Le funzioni di rete di Windows forniscono informazioni e utilità per la gestione delle risorse di rete.
ms.assetid: 8a83186f-a912-4c61-8137-1f6be1f3afd6
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 623de7adfdb57e21f01bff8b9647d6d2d175bd63
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104223991"
---
# <a name="wnet-functions"></a>Funzioni WNet

Le funzioni di rete di Windows forniscono informazioni e utilità per la gestione delle risorse di rete. Le funzioni di rete di Windows possono essere raggruppate nel modo seguente:

-   [Funzioni di connessione](#connection-functions)
-   [Funzioni di enumerazione](#enumeration-functions)
-   [Funzioni informative](#information-functions)
-   [Funzioni utente](#user-functions)

## <a name="connection-functions"></a>Funzioni di connessione

Chiamare le seguenti funzioni di connessione WNet per connettere un dispositivo locale a una risorsa di rete e per annullare le connessioni di rete.



| Funzione                                                                     | Descrizione                                                                                                                                                                                                                    |
|------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**MultinetGetConnectionPerformance**](/windows/win32/api/winnetwk/nf-winnetwk-multinetgetconnectionperformancea) | Restituisce informazioni sulle prestazioni previste di una connessione a una risorsa di rete.                                                                                                                                      |
| [**WNetAddConnection**](/windows/win32/api/winnetwk/nf-winnetwk-wnetaddconnectiona)                               | Connette un dispositivo locale a una risorsa di rete. (Fornito per la compatibilità con le versioni di Windows a 16 bit).                                                                                                                   |
| [**WNetAddConnection2**](/windows/win32/api/winnetwk/nf-winnetwk-wnetaddconnection2a)                             | Connette un dispositivo locale a una risorsa di rete.                                                                                                                                                                                 |
| [**WNetAddConnection3**](/windows/win32/api/winnetwk/nf-winnetwk-wnetaddconnection3a)                             | Connette un dispositivo locale a una risorsa di rete. Questa funzione include uno più parametri della funzione **WNetAddConnection2** , un handle per una finestra che il provider di rete può usare come finestra proprietaria per le finestre di dialogo. |
| [**WNetCancelConnection**](/windows/win32/api/winnetwk/nf-winnetwk-wnetcancelconnectiona)                         | Annulla una connessione di rete. (Fornito per la compatibilità con le versioni di Windows a 16 bit).                                                                                                                                    |
| [**WNetCancelConnection2**](/windows/win32/api/winnetwk/nf-winnetwk-wnetcancelconnection2a)                       | Annulla una connessione di rete, offrendo la possibilità di aggiornare il profilo utente con informazioni sulle connessioni permanenti.                                                                                                  |
| [**WNetConnectionDialog**](/windows/win32/api/winnetwk/nf-winnetwk-wnetconnectiondialog)                         | Avvia una finestra di dialogo di esplorazione generale per la connessione alle risorse di rete.                                                                                                                                                      |
| [**WNetConnectionDialog1**](/windows/win32/api/winnetwk/nf-winnetwk-wnetconnectiondialog1a)                       | Avvia una finestra di dialogo di esplorazione generale per la connessione alle risorse di rete, usando una struttura [**CONNECTDLGSTRUCT**](/windows/win32/api/winnetwk/ns-winnetwk-connectdlgstructa) .                                                                                  |
| [**WNetDisconnectDialog**](/windows/win32/api/winnetwk/nf-winnetwk-wnetdisconnectdialog)                         | Avvia una finestra di dialogo di esplorazione generale per la disconnessione dalle risorse di rete.                                                                                                                                                 |
| [**WNetDisconnectDialog1**](/windows/win32/api/winnetwk/nf-winnetwk-wnetdisconnectdialog1a)                       | Avvia una finestra di dialogo di esplorazione generale per la disconnessione dalle risorse di rete, usando una struttura [**DISCDLGSTRUCT**](/windows/win32/api/winnetwk/ns-winnetwk-discdlgstructa) .                                                                                   |
| [**WNetGetConnection**](/windows/win32/api/winnetwk/nf-winnetwk-wnetgetconnectiona)                               | Recupera il nome della risorsa di rete associata a un dispositivo locale.                                                                                                                                                     |
| [**WNetGetUniversalName**](/windows/win32/api/winnetwk/nf-winnetwk-wnetgetuniversalnamea)                         | Quando si specifica un percorso basato su unità per una risorsa di rete, restituisce una forma più universale del nome.                                                                                                                               |
| [**WNetRestoreConnectionW**](/windows/win32/api/winnetwk/nf-winnetwk-wnetrestoreconnectionw)                     | Ripristina la connessione a una risorsa di rete, richiedendo all'utente, se necessario, il nome e la password.                                                                                                                      |
| [**WNetUseConnection**](/windows/win32/api/winnetwk/nf-winnetwk-wnetuseconnectiona)                               | Connette un dispositivo locale a una risorsa di rete. Seleziona automaticamente un dispositivo locale non usato per il reindirizzamento alla risorsa di rete.                                                                                               |



 

> [!Note]  
> Le funzioni [**WNetAddConnection**](/windows/win32/api/winnetwk/nf-winnetwk-wnetaddconnectiona) e [**WNetCancelConnection**](/windows/win32/api/winnetwk/nf-winnetwk-wnetcancelconnectiona) sono supportate per la compatibilità con Windows per gruppi di lavoro. Tuttavia, le nuove applicazioni devono usare [**WNetAddConnection2**](/windows/win32/api/winnetwk/nf-winnetwk-wnetaddconnection2a) o [**WNetAddConnection3**](/windows/win32/api/winnetwk/nf-winnetwk-wnetaddconnection3a)e [**WNetCancelConnection2**](/windows/win32/api/winnetwk/nf-winnetwk-wnetcancelconnection2a).

 

## <a name="enumeration-functions"></a>Funzioni di enumerazione

Chiamare le funzioni WNet seguenti per enumerare le risorse di rete.



| Funzione                                     | Descrizione                                                                             |
|----------------------------------------------|-----------------------------------------------------------------------------------------|
| [**WNetCloseEnum**](/windows/win32/api/winnetwk/nf-winnetwk-wnetcloseenum)       | Termina un'enumerazione di risorse di rete.                                                    |
| [**WNetEnumResource**](/windows/win32/api/winnetwk/nf-winnetwk-wnetenumresourcea) | Continua un'enumerazione delle risorse di rete avviate dalla funzione **WNetOpenEnum** . |
| [**WNetOpenEnum**](/windows/win32/api/winnetwk/nf-winnetwk-wnetopenenuma)         | Avvia un'enumerazione delle risorse di rete.                                             |



 

## <a name="information-functions"></a>Funzioni informative

Chiamare le funzioni informative e di utilità WNet seguenti per recuperare il provider di rete e altre informazioni.



| Funzione                                                         | Descrizione                                                                                         |
|------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------|
| [**WNetGetLastError**](/windows/win32/api/winnetwk/nf-winnetwk-wnetgetlasterrora)                     | Restituisce il codice di errore più recente impostato da una funzione WNet, quella indicata da un provider di rete.  |
| [**WNetGetNetworkInformation**](/windows/win32/api/winnetwk/nf-winnetwk-wnetgetnetworkinformationa)   | Restituisce informazioni estese su un provider di rete specifico.                                     |
| [**WNetGetProviderName**](/windows/win32/api/winnetwk/nf-winnetwk-wnetgetprovidernamea)               | Restituisce il nome del provider per un tipo specifico di rete.                                           |
| [**WNetGetResourceInformation**](/windows/win32/api/winnetwk/nf-winnetwk-wnetgetresourceinformationa) | Restituisce il provider di rete che possiede una risorsa e ottiene informazioni sul tipo di risorsa. |
| [**WNetGetResourceParent**](/windows/win32/api/winnetwk/nf-winnetwk-wnetgetresourceparenta)           | Restituisce l'elemento padre di una risorsa di rete.                                                           |



 

## <a name="user-functions"></a>Funzioni utente

Chiamare la funzione WNet seguente per recuperare il nome dell'utente associato a una periferica locale.



| Funzione                           | Descrizione                                                                              |
|------------------------------------|------------------------------------------------------------------------------------------|
| [**WNetGetUser**](/windows/win32/api/winnetwk/nf-winnetwk-wnetgetusera) | Restituisce il nome utente predefinito corrente o il nome utente che ha stabilito la connessione. |



 

Molte delle funzioni WNet usano una struttura [**netresource**](/windows/desktop/api/Winnetwk/ns-winnetwk-netresourcea) per archiviare le informazioni su una risorsa di rete.

 

 