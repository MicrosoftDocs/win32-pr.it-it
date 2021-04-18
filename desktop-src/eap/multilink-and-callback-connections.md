---
title: Connessioni a collegamento multiplo e callback
description: Per il primo collegamento in una connessione a più collegamenti, il servizio di autenticazione imposta il flag del \_ \_ primo collegamento del flag EAP RAS \_ \_ nel membro fFlags \_ della \_ struttura di input EAP PPP.
ms.assetid: a6aee73b-43b2-43b4-a6f1-ac7b293c44ad
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: af39ebfa54469e2f44c44c800cebbfb176b33cad
ms.sourcegitcommit: c20a43b333f03175ac23823c55f3204bfe8cd243
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 11/26/2019
ms.locfileid: "106299311"
---
# <a name="multilink-and-callback-connections"></a>Connessioni a collegamento multiplo e callback

Per il primo collegamento in una connessione a più collegamenti, il servizio di autenticazione imposta il flag del \_ \_ primo collegamento del flag EAP RAS \_ \_ nel membro **fFlags** della struttura di [**\_ \_ input EAP PPP**](/windows/desktop/api/Raseapif/ns-raseapif-ppp_eap_input) . Il protocollo di autenticazione può utilizzare la presenza di questo flag per determinare se presentare un'interfaccia utente specificatamente per il primo collegamento di una connessione a più collegamenti.

Se la connessione è configurata in modo che il server richiami il computer client, il flag del \_ \_ primo collegamento del flag EAP RAS \_ \_ non verrà impostato nel callback.

Se il protocollo di autenticazione imposta il membro **fSaveConnectionData** dell' [**\_ \_ output EAP PPP**](/windows/desktop/api/Raseapif/ns-raseapif-ppp_eap_output) su **true**, i collegamenti successivi nella connessione a collegamento multiplo ricevono i nuovi dati specifici della connessione. Nel caso di dati specifici dell'utente, tuttavia, il protocollo di autenticazione continua a ottenere i dati originali specifici dell'utente anche se imposta il membro **fSaveUserData** dell' **\_ \_ output EAP PPP** su **true**.

Il protocollo di autenticazione può utilizzare un' [interfaccia utente interattiva](interactive-user-interface.md) per raccogliere dati per un particolare collegamento di una connessione a più collegamenti. In questo caso, il servizio di autenticazione rende disponibili i dati risultanti per il protocollo di autenticazione durante i collegamenti successivi. Tuttavia, questi dati non vengono mai salvati nell'archivio permanente.

 

 




