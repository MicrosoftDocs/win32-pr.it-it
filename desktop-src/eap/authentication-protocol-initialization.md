---
title: Inizializzazione del protocollo di autenticazione
description: La connessione protetta EAP viene inizializzata tra il client e il server in modo analogo ai client RAS e wireless (802.1 X).
ms.assetid: 1cd5bfc9-2ba3-477c-9bbb-73578a5623c2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 856bd173ef617fb272460f874fa1d2087322c8b4
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2020
ms.locfileid: "104398933"
---
# <a name="authentication-protocol-initialization"></a>Inizializzazione del protocollo di autenticazione

La connessione protetta EAP viene inizializzata tra il client e il server in modo analogo ai client RAS e wireless (802.1 X).

## <a name="client"></a>Client

Quando il client tenta di stabilire la connessione, il servizio di autenticazione ottiene le [informazioni sull'identità](obtaining-identity-information.md) per l'utente. Se il valore **RAS \_ EAP \_ valueName \_ Invoke \_ NAMEDLG** è presente nel registro di sistema per questo protocollo di autenticazione e questo valore è impostato su zero, il servizio di autenticazione chiama [**RasEapGetIdentity**](/previous-versions/windows/desktop/api/Raseapif/nf-raseapif-raseapgetidentity). Questa funzione Visualizza in genere un'interfaccia utente che consente alle informazioni di identità di essere di un tipo specifico per il protocollo di autenticazione; ad esempio, un certificato o un ID numerico. Se **RAS \_ EAP \_ valueName \_ Invoke \_ NAMEDLG** non è presente o è impostato su uno, il servizio di autenticazione Visualizza la finestra di dialogo del nome utente di sistema standard.

Una volta ottenute le informazioni di identità per l'utente, il servizio di autenticazione chiama l'implementazione del protocollo di autenticazione di [**RasEapBegin**](/previous-versions/windows/desktop/legacy/aa363520(v=vs.85)). Questa chiamata consente al protocollo di autenticazione di allocare e inizializzare un buffer di lavoro che il servizio passa alle chiamate successive a [**RasEapMakeMessage**](/previous-versions/windows/desktop/legacy/aa363532(v=vs.85)) e [**RasEapEnd**](/previous-versions/windows/desktop/legacy/aa363521(v=vs.85)). Il buffer di lavoro è opaco per il servizio e non accede mai al contenuto del buffer di lavoro. Se il protocollo di autenticazione crea un buffer di lavoro distinto per ogni sessione EAP, il buffer di lavoro è di tipo sessione e thread-safe. Poiché il protocollo di autenticazione alloca la memoria per il buffer di lavoro, il protocollo di autenticazione deve liberare anche questa memoria tramite la funzione [**RasEapFreeMemory**](/previous-versions/windows/desktop/api/Raseapif/nf-raseapif-raseapfreememory) .

Nella chiamata a [**RasEapBegin**](/previous-versions/windows/desktop/legacy/aa363520(v=vs.85)), il servizio passa anche una struttura [**di \_ \_ input EAP PPP**](/windows/desktop/api/Raseapif/ns-raseapif-ppp_eap_input) che contiene i puntatori alle informazioni di configurazione per la connessione e le informazioni sull'identità per l'utente. Il servizio passa sempre un valore per il membro **pszIdentity** dell' **\_ \_ input EAP di PPP**. Tuttavia, il membro **pszPassword** dell' [**\_ \_ input EAP PPP**](/windows/desktop/api/Raseapif/ns-raseapif-ppp_eap_input) può essere **null**.

All'interno della struttura di [**\_ \_ input EAP PPP**](/windows/desktop/api/Raseapif/ns-raseapif-ppp_eap_input) , il membro **fAuthenticator** indica se il protocollo di autenticazione viene richiamato per l'autenticazione (sul client) o come autenticatore (sul server).

## <a name="server"></a>Server

Sul server, il membro **bInitialID** dell' [**\_ \_ input EAP PPP**](/windows/desktop/api/Raseapif/ns-raseapif-ppp_eap_input) specifica l'ID utilizzato dal server per il primo pacchetto EAP. Il server incrementa questo ID per i pacchetti successivi.

Inoltre, nel server, il puntatore **pUserAttributes** nell' [**\_ \_ input EAP PPP**](/windows/desktop/api/Raseapif/ns-raseapif-ppp_eap_input) punta a una matrice di attributi del tipo di [**\_ \_ attributo di \_ autenticazione RAS**](/windows/win32/api/raseapif/ne-raseapif-ras_auth_attribute_type) . Si tratta di attributi per l'utente ottenuti dal client.

Se la chiamata [**RasEapBegin**](/previous-versions/windows/desktop/legacy/aa363520(v=vs.85)) restituisce un valore diverso da **nessun \_ errore**, la sessione viene disconnessa. L'errore restituito viene registrato (sul server) o visualizzato all'utente (sul client).

 

 