---
title: Definizione dell'interfaccia
description: Una definizione di interfaccia è una specifica formale per il modo in cui un'applicazione client e un'applicazione server comunicano tra loro.
ms.assetid: 709ca498-4da3-4e6f-bb12-333a407b74c2
keywords:
- RPC (Remote Procedure Call), attività, definizione dell'interfaccia
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8c9f447847eeca39258b96ba129c46b3f7bcf054
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104044397"
---
# <a name="defining-the-interface"></a>Definizione dell'interfaccia

Una definizione di interfaccia è una specifica formale per il modo in cui un'applicazione client e un'applicazione server comunicano tra loro. L'interfaccia definisce il modo in cui il client e il server si riconoscono reciprocamente, le procedure remote che l'applicazione client può chiamare e i tipi di dati per i parametri e i valori restituiti di tali procedure. Specifica anche la modalità di trasmissione dei dati tra client e server.

Questa interfaccia viene definita nel Microsoft Interface Definition Language (MIDL), che è costituita da definizioni del linguaggio C ampliate con parole chiave, denominate attributi, che descrivono la modalità di trasmissione dei dati in rete.

Il file di definizione dell'interfaccia (IDL) contiene le definizioni dei tipi, gli attributi e i prototipi di funzione che descrivono il modo in cui i dati vengono trasmessi in rete. Il file di configurazione dell'applicazione (ACF) contiene attributi che configurano l'applicazione per un particolare ambiente operativo senza influire sulle caratteristiche di rete.

 

 




