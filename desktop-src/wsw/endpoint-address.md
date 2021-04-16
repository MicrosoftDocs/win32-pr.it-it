---
title: Indirizzo endpoint
description: Un indirizzo endpoint rappresenta l'indirizzo di un servizio sulla rete.
ms.assetid: 5df9c0da-6648-42a0-ae87-06844461042a
keywords:
- Servizi Web per l'indirizzo endpoint per Windows
- WWSAPI
- WWS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 787326197bc73d57945720c34773d33b613a4aab
ms.sourcegitcommit: 5b98bf8c68922f8f03c14f793fbe17504900559c
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/12/2021
ms.locfileid: "104565182"
---
# <a name="endpoint-address"></a>Indirizzo endpoint

Un indirizzo endpoint rappresenta l'indirizzo di un servizio sulla rete. Quando si apre un [canale](channel.md), chiamando la funzione [**WsOpenChannel**](/windows/desktop/api/WebServices/nf-webservices-wsopenchannel) , è necessario fornire l'indirizzo dell'endpoint del servizio con cui comunicare, oltre a specificare il canale che si vuole aprire.


Un indirizzo endpoint è costituito da:

-   un [URL](url.md)
-   un set di intestazioni (facoltativo)
-   un set di estensioni (facoltativo)
-   [identità](endpoint-identity.md) facoltativa che rappresenta l'identità di sicurezza del servizio.

Quando un messaggio viene risolto, l'URL diventa l'intestazione "to" del messaggio. Al messaggio vengono aggiunte anche tutte le intestazioni che fanno parte dell'indirizzo endpoint.

![Diagramma che mostra le intestazioni degli indirizzi endpoint aggiunti a un messaggio.](images/endpointaddress.png)

I canali indirizzano automaticamente tutti i messaggi inviati, usando la struttura di [**\_ \_ indirizzi dell'endpoint WS**](/windows/desktop/api/WebServices/ns-webservices-ws_endpoint_address) passata a [**WsOpenChannel**](/windows/desktop/api/WebServices/nf-webservices-wsopenchannel). È anche possibile usare la funzione [**WsAddressMessage**](/windows/desktop/api/WebServices/nf-webservices-wsaddressmessage) per eseguire l'override di questo comportamento predefinito.

Quando [**l' \_ \_ Indirizzo WS endpoint**](/windows/desktop/api/WebServices/ns-webservices-ws_endpoint_address) viene passato come parametro, le funzioni [**WsOpenChannel**](/windows/desktop/api/WebServices/nf-webservices-wsopenchannel) e [**WsOpenServiceProxy**](/windows/desktop/api/WebServices/nf-webservices-wsopenserviceproxy) creano una copia del parametro **dell' \_ \_ indirizzo dell'endpoint WS** in memoria e la relativa dimensione è limitata a 65536 byte. [**WsAddressMessage**](/windows/desktop/api/WebServices/nf-webservices-wsaddressmessage) non presenta questa limitazione perché non richiede la creazione di una copia del parametro dell' **\_ \_ indirizzo dell'endpoint WS** .

Le estensioni specificate nel campo **estensioni** di [**WS \_ endpoint \_ Address**](/windows/desktop/api/WebServices/ns-webservices-ws_endpoint_address) non vengono utilizzate per indirizzare il messaggio, ma sono invece un meccanismo di estendibilità che può essere utilizzato per fornire informazioni aggiuntive (ad esempio, i metadati) sul servizio. Le estensioni comuni possono essere lette con la funzione [**WsReadEndpointAddressExtension**](/windows/desktop/api/WebServices/nf-webservices-wsreadendpointaddressextension) .

Il campo Identity facoltativo dell'indirizzo endpoint può includere, ad esempio, il nome DNS del computer in cui è in esecuzione il servizio o l'UPN dell'account di Windows con cui viene eseguito il servizio. Il campo Identity non viene utilizzato per indirizzare il messaggio, ma può essere utilizzato per ottenere un token di sicurezza per il servizio (ad esempio, per ottenere un ticket Kerberos per l'UPN di destinazione) e per verificare l'identità delle risposte al servizio (ad esempio, un'identità DNS utilizzata per i controlli nome sul certificato del servizio restituito durante SSL).

Gli indirizzi endpoint possono essere letti e scritti usando la [serializzazione](serialization.md) con il valore di enumerazione del **\_ \_ \_ tipo di indirizzo endpoint WS** da [**WS \_ Type**](/windows/desktop/api/WebServices/ne-webservices-ws_type). Nota per serializzare un indirizzo endpoint, è necessario essere a conoscenza della versione della specifica utilizzata per le intestazioni di indirizzamento, come specificato nell'enumerazione della [**\_ \_ versione WS Addressing**](/windows/desktop/api/WebServices/ne-webservices-ws_addressing_version) .

 

 




