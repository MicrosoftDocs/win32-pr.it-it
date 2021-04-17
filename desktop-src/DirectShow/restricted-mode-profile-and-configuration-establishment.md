---
description: Creazione di profili e configurazione della modalità con restrizioni
ms.assetid: 550f5413-eaa4-4530-867e-fd9b1907cadf
title: Creazione di profili e configurazione della modalità con restrizioni
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 17a424505b3934131527f249176f9fe0984b320a
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "104401165"
---
# <a name="restricted-mode-profile-and-configuration-establishment"></a><span data-ttu-id="a46c3-103">Creazione di profili e configurazione della modalità con restrizioni</span><span class="sxs-lookup"><span data-stu-id="a46c3-103">Restricted Mode Profile and Configuration Establishment</span></span>

<span data-ttu-id="a46c3-104">A causa della varietà di tipi di dati che possono essere decodificati da DirectX VA, e le configurazioni con più decodifica supportate in DirectX VA per ognuno di questi tipi di dati (ad esempio, l'uso di buffer Bitstream rispetto alla decodifica della differenza residua del host rispetto alla decodifica IDCT basata su acceleratore con e senza crittografia di ogni tipo di buffer pertinente e così via), si ritiene che non sia possibile semplicemente specificare un GUID univoco per ogni tipo di dati univoco e la decodifica</span><span class="sxs-lookup"><span data-stu-id="a46c3-104">Due to the variety of types of data that can be decoded by DirectX VA, and the multiple decoding configurations supported within DirectX VA for each of these types of data (for example, using bitstream buffers versus host residual difference decoding versus accelerator-based IDCT with and without encryption of each relevant type of buffer, and so on), we believe it would be somewhat ungainly to simply specify a unique GUID for every unique data type and decoding configuration.</span></span> <span data-ttu-id="a46c3-105">In questo modo si creerebbe un numero elevato di GUID (ad esempio, ipoteticamente se sono stati configurati 16 profili di configurazioni di DirectX i e 16, è necessario che siano presenti 256 GUID definiti, che richiedono 4 kilobyte di memoria solo per mantenerli tutti.</span><span class="sxs-lookup"><span data-stu-id="a46c3-105">This would create a large number of GUIDs (for example, hypothetically if there were 16 profiles of DirectX VA and 16 configurations possible for each, there would need to be 256 defined GUIDs—requiring 4 kilobytes of memory just to hold them all.</span></span> <span data-ttu-id="a46c3-106">Questo problema è la parte più difficile per determinare come eseguire il mapping di DirectX VA a **IAMVideoAccelerator**, con il resto della definizione operativa per lo più piuttosto semplice.</span><span class="sxs-lookup"><span data-stu-id="a46c3-106">This issue is the most difficult part of determining how to map DirectX VA into **IAMVideoAccelerator**, with the remainder of the operational definition mostly being quite straightforward.</span></span> <span data-ttu-id="a46c3-107">Di conseguenza, viene specificato un GUID univoco solo per ogni tipo di dati (per ogni profilo in modalità limitata) e viene consentito l'associazione di un GUID aggiuntivo a ogni tipo di crittografia.</span><span class="sxs-lookup"><span data-stu-id="a46c3-107">As a result, we specify a unique GUID only for each type of data (for each restricted mode profile) and allow an additional GUID to be associated with each type of encryption.</span></span> <span data-ttu-id="a46c3-108">La configurazione della decodifica viene quindi stabilita tra il decodificatore e l'acceleratore mediante una negoziazione subordinata di livello inferiore tramite il sondaggio e le operazioni di blocco per stabilire le configurazioni per ogni tipo di funzione DirectX VA.</span><span class="sxs-lookup"><span data-stu-id="a46c3-108">The decoding configuration is then established between the decoder and accelerator by a lower-level subordinate negotiation using probing and locking operations to establish configurations for each type of DirectX VA function.</span></span>

 

 



