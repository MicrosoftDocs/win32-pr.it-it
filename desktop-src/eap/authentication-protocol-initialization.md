---
title: Inizializzazione del protocollo di autenticazione
description: La connessione protetta EAP viene inizializzata tra il client e il server in modo simile per i client RAS e wireless (802.1X).
ms.assetid: 1cd5bfc9-2ba3-477c-9bbb-73578a5623c2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e5d53643718f747e1f39aaf68393f92a0577455041ec765ca19bea710f2c3aca
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118984461"
---
# <a name="authentication-protocol-initialization"></a>Inizializzazione del protocollo di autenticazione

La connessione protetta EAP viene inizializzata tra il client e il server in modo simile per i client RAS e wireless (802.1X).

## <a name="client"></a>Client

Quando il client tenta di stabilire la connessione, il servizio di autenticazione ottiene le [informazioni di identità](obtaining-identity-information.md) per l'utente. Se il **valore RAS \_ EAP \_ VALUENAME INVOKE \_ \_ NAMEDLG** è presente nel Registro di sistema per questo protocollo di autenticazione e questo valore è impostato su zero, il servizio di autenticazione chiama [**RasEapGetIdentity**](/previous-versions/windows/desktop/api/Raseapif/nf-raseapif-raseapgetidentity). Questa funzione visualizza in genere un'interfaccia utente che consente alle informazioni sull'identità di essere di un tipo specifico del protocollo di autenticazione. ad esempio un certificato o un ID numerico. Se **RAS \_ EAP \_ VALUENAME INVOKE \_ \_ NAMEDLG** non è presente o è impostato su uno, il servizio di autenticazione visualizza la finestra di dialogo del nome utente del sistema standard.

Dopo che il servizio di autenticazione ha ottenuto le informazioni di identità per l'utente, chiama l'implementazione del protocollo di autenticazione [**di RasEapBegin**](/previous-versions/windows/desktop/legacy/aa363520(v=vs.85)). Questa chiamata consente al protocollo di autenticazione di allocare e inizializzare un buffer di lavoro che il servizio passa alle chiamate successive a [**RasEapMakeMessage**](/previous-versions/windows/desktop/legacy/aa363532(v=vs.85)) [**e RasEapEnd.**](/previous-versions/windows/desktop/legacy/aa363521(v=vs.85)) Il buffer di lavoro è opaco per il servizio e non accede mai al contenuto del buffer di lavoro. Se il protocollo di autenticazione crea un buffer di lavoro distinto per ogni sessione EAP, il buffer di lavoro è sessione e thread-safe. Poiché il protocollo di autenticazione alloca la memoria per il buffer di lavoro, anche il protocollo di autenticazione deve liberare questa memoria usando la [**funzione RasEapFreeMemory.**](/previous-versions/windows/desktop/api/Raseapif/nf-raseapif-raseapfreememory)

Nella chiamata a [**RasEapBegin**](/previous-versions/windows/desktop/legacy/aa363520(v=vs.85))il servizio passa anche una struttura [**\_ PPP EAP \_ INPUT**](/windows/desktop/api/Raseapif/ns-raseapif-ppp_eap_input) che contiene puntatori alle informazioni di configurazione per la connessione e le informazioni sull'identità per l'utente. Il servizio passa sempre un valore per il membro **pszIdentity** di **PPP \_ EAP \_ INPUT**. Tuttavia, il **membro pszPassword** di [**PPP \_ EAP \_ INPUT**](/windows/desktop/api/Raseapif/ns-raseapif-ppp_eap_input) può essere **NULL.**

All'interno della struttura [**\_ PPP EAP \_ INPUT,**](/windows/desktop/api/Raseapif/ns-raseapif-ppp_eap_input) il membro **fAuthenticator** indica se il protocollo di autenticazione viene richiamato per essere autenticato (nel client) o come autenticatore (nel server).

## <a name="server"></a>Server

Nel server il **membro bInitialID** di [**PPP \_ EAP \_ INPUT**](/windows/desktop/api/Raseapif/ns-raseapif-ppp_eap_input) specifica l'ID utilizzato dal server per il primo pacchetto EAP. Il server incrementa questo ID per i pacchetti successivi.

Anche nel server, il **puntatore pUserAttributes** in [**PPP \_ EAP \_ INPUT**](/windows/desktop/api/Raseapif/ns-raseapif-ppp_eap_input) punta a una matrice di attributi del tipo [**RAS \_ AUTH \_ ATTRIBUTE \_ TYPE.**](/windows/win32/api/raseapif/ne-raseapif-ras_auth_attribute_type) Si tratta di attributi per l'utente ottenuti dal client.

Se la [**chiamata RasEapBegin**](/previous-versions/windows/desktop/legacy/aa363520(v=vs.85)) restituisce un valore diverso da **NO \_ ERROR,** la sessione viene disconnessa. L'errore restituito viene registrato (nel server) o visualizzato all'utente (nel client).

 

 