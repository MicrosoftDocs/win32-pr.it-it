---
description: I servizi di telefonia supplementari sono la raccolta di tutti i servizi definiti dall'API diversi da quelli inclusi nel subset Di telefonia di base.
ms.assetid: a2a30a0d-fbfd-4317-8e3a-d1e1e8b86ae0
title: Servizi di telefonia supplementari
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9762b2d9ca74d0212170e1e87662242d3983663db024ce52018d108cc37fb883
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117760753"
---
# <a name="supplementary-telephony-services"></a>Servizi di telefonia supplementari

I servizi di telefonia supplementari sono la raccolta di tutti i servizi definiti dall'API diversi da quelli inclusi nel subset Di telefonia di base. Include tutte le cosiddette funzionalità supplementari presenti nei sistemi PBX moderni, ad esempio blocco, trasferimento, conferenza, parcheggio e così via. Tutte le funzionalità supplementari sono considerate facoltative. ovvero il provider di servizi decide quale di questi servizi esegue o non fornisce.

Un'applicazione può eseguire una query su un dispositivo linea o telefono per il set di servizi supplementari che fornisce usando funzioni come [**lineGetDevCaps**](/windows/win32/api/tapi/nf-tapi-linegetdevcaps) o [**lineGetAddressCaps.**](/windows/win32/api/tapi/nf-tapi-linegetaddresscaps) Un singolo servizio supplementare può essere costituito da più chiamate di funzione e messaggi. L'API Telefonia e non lo sviluppatore di provider di servizi definiscono il comportamento di ognuna di queste funzionalità supplementari. Un provider di servizi deve fornire un servizio di telefonia supplementare solo se può implementare il significato esatto definito dall'API. In caso contrario, la funzionalità deve essere fornita come servizio di telefonia estesa.

Come accennato nei servizi di telefonia di base, i servizi di telefonia sono considerati facoltativi. Pertanto, tutti i servizi di telefonia fanno parte della telefonia supplementare. Per un elenco delle funzioni di Telefonia supplementare, vedere Informazioni di [riferimento per le funzioni rapide TAPI.](./tapi-quick-function-reference.md)

 

 
