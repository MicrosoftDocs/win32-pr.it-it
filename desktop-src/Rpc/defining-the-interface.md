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
# <a name="defining-the-interface"></a><span data-ttu-id="fee58-104">Definizione dell'interfaccia</span><span class="sxs-lookup"><span data-stu-id="fee58-104">Defining the Interface</span></span>

<span data-ttu-id="fee58-105">Una definizione di interfaccia è una specifica formale per il modo in cui un'applicazione client e un'applicazione server comunicano tra loro.</span><span class="sxs-lookup"><span data-stu-id="fee58-105">An interface definition is a formal specification for how a client application and a server application communicate with each other.</span></span> <span data-ttu-id="fee58-106">L'interfaccia definisce il modo in cui il client e il server si riconoscono reciprocamente, le procedure remote che l'applicazione client può chiamare e i tipi di dati per i parametri e i valori restituiti di tali procedure.</span><span class="sxs-lookup"><span data-stu-id="fee58-106">The interface defines how the client and server recognize each other, the remote procedures that the client application can call, and the data types for those procedures' parameters and return values.</span></span> <span data-ttu-id="fee58-107">Specifica anche la modalità di trasmissione dei dati tra client e server.</span><span class="sxs-lookup"><span data-stu-id="fee58-107">It also specifies how the data is transmitted between client and server.</span></span>

<span data-ttu-id="fee58-108">Questa interfaccia viene definita nel Microsoft Interface Definition Language (MIDL), che è costituita da definizioni del linguaggio C ampliate con parole chiave, denominate attributi, che descrivono la modalità di trasmissione dei dati in rete.</span><span class="sxs-lookup"><span data-stu-id="fee58-108">You define this interface in the Microsoft Interface Definition Language (MIDL) which consists of C-language definitions augmented with keywords, called attributes, which describe how the data is transmitted over the network.</span></span>

<span data-ttu-id="fee58-109">Il file di definizione dell'interfaccia (IDL) contiene le definizioni dei tipi, gli attributi e i prototipi di funzione che descrivono il modo in cui i dati vengono trasmessi in rete.</span><span class="sxs-lookup"><span data-stu-id="fee58-109">The interface definition (IDL) file contains type definitions, attributes and function prototypes that describe how data is transmitted on the network.</span></span> <span data-ttu-id="fee58-110">Il file di configurazione dell'applicazione (ACF) contiene attributi che configurano l'applicazione per un particolare ambiente operativo senza influire sulle caratteristiche di rete.</span><span class="sxs-lookup"><span data-stu-id="fee58-110">The application configuration (ACF) file contains attributes that configure your application for a particular operating environment without affecting its network characteristics.</span></span>

 

 




