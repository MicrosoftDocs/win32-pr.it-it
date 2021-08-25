---
title: Connessioni multilink e callback
description: Per il primo collegamento in una connessione multilink, il servizio di autenticazione imposta il flag RAS EAP FLAG FIRST LINK nel membro \_ \_ \_ \_ fFlags della struttura \_ PPP EAP \_ INPUT.
ms.assetid: a6aee73b-43b2-43b4-a6f1-ac7b293c44ad
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dfc7493550863a755a87668c96dbe0ce600d524a111b7e7300b97c307f4d30c5
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119852321"
---
# <a name="multilink-and-callback-connections"></a>Connessioni multilink e callback

Per il primo collegamento in una connessione multilink, il servizio di autenticazione imposta il flag RAS EAP FLAG FIRST LINK nel membro \_ \_ \_ \_ **fFlags** della [**struttura \_ PPP EAP \_ INPUT.**](/windows/desktop/api/Raseapif/ns-raseapif-ppp_eap_input) Il protocollo di autenticazione può utilizzare la presenza di questo flag per determinare se presentare un'interfaccia utente specifica per il primo collegamento di una connessione multilink.

Se la connessione è configurata in modo che il server chiami il computer client, il flag RAS EAP FLAG FIRST LINK non \_ verrà impostato sul \_ \_ \_ callback.

Se il protocollo di autenticazione imposta il membro **fSaveConnectionData** di [**PPP \_ EAP \_ OUTPUT**](/windows/desktop/api/Raseapif/ns-raseapif-ppp_eap_output) su **TRUE,** i collegamenti successivi nella connessione multilink ricevono i nuovi dati specifici della connessione. Nel caso di dati specifici dell'utente, tuttavia, il protocollo di autenticazione continua a ottenere i dati originali specifici dell'utente anche se imposta il membro **fSaveUserData** di **PPP \_ EAP \_ OUTPUT** su **TRUE.**

Il protocollo di autenticazione può usare [un'interfaccia utente interattiva](interactive-user-interface.md) per raccogliere dati per un particolare collegamento di una connessione multilink. In questo caso, il servizio di autenticazione rende disponibili i dati risultanti al protocollo di autenticazione durante i collegamenti successivi. Tuttavia, questi dati non vengono mai salvati in un archivio permanente.

 

 




