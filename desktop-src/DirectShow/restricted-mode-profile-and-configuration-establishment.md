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
# <a name="restricted-mode-profile-and-configuration-establishment"></a>Creazione di profili e configurazione della modalità con restrizioni

A causa della varietà di tipi di dati che possono essere decodificati da DirectX VA, e le configurazioni con più decodifica supportate in DirectX VA per ognuno di questi tipi di dati (ad esempio, l'uso di buffer Bitstream rispetto alla decodifica della differenza residua del host rispetto alla decodifica IDCT basata su acceleratore con e senza crittografia di ogni tipo di buffer pertinente e così via), si ritiene che non sia possibile semplicemente specificare un GUID univoco per ogni tipo di dati univoco e la decodifica In questo modo si creerebbe un numero elevato di GUID (ad esempio, ipoteticamente se sono stati configurati 16 profili di configurazioni di DirectX i e 16, è necessario che siano presenti 256 GUID definiti, che richiedono 4 kilobyte di memoria solo per mantenerli tutti. Questo problema è la parte più difficile per determinare come eseguire il mapping di DirectX VA a **IAMVideoAccelerator**, con il resto della definizione operativa per lo più piuttosto semplice. Di conseguenza, viene specificato un GUID univoco solo per ogni tipo di dati (per ogni profilo in modalità limitata) e viene consentito l'associazione di un GUID aggiuntivo a ogni tipo di crittografia. La configurazione della decodifica viene quindi stabilita tra il decodificatore e l'acceleratore mediante una negoziazione subordinata di livello inferiore tramite il sondaggio e le operazioni di blocco per stabilire le configurazioni per ogni tipo di funzione DirectX VA.

 

 



