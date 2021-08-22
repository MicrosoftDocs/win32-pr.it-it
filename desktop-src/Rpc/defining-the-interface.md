---
title: Definizione dell'interfaccia
description: Una definizione di interfaccia è una specifica formale del modo in cui un'applicazione client e un'applicazione server comunicano tra loro.
ms.assetid: 709ca498-4da3-4e6f-bb12-333a407b74c2
keywords:
- RPC Remote Procedure Call , attività, definizione dell'interfaccia
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 654c6690e6980e659df8a68652aec59b296b7d88543eca02605f489a2c3a909c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118930806"
---
# <a name="defining-the-interface"></a>Definizione dell'interfaccia

Una definizione di interfaccia è una specifica formale del modo in cui un'applicazione client e un'applicazione server comunicano tra loro. L'interfaccia definisce il modo in cui il client e il server si riconoscono tra loro, le procedure remote che l'applicazione client può chiamare e i tipi di dati per i parametri e i valori restituiti di tali procedure. Specifica inoltre la modalità di trasmissione dei dati tra client e server.

Questa interfaccia viene definita nel Microsoft Interface Definition Language (MIDL), costituito da definizioni in linguaggio C, arricchite con parole chiave, denominate attributi, che descrivono come i dati vengono trasmessi in rete.

Il file di definizione dell'interfaccia (IDL) contiene definizioni di tipi, attributi e prototipi di funzione che descrivono la modalità di trasmissione dei dati in rete. Il file di configurazione dell'applicazione (ACF) contiene attributi che configurano l'applicazione per un particolare ambiente operativo senza influire sulle caratteristiche di rete.

 

 




