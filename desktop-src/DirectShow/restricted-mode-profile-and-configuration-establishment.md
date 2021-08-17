---
description: Definizione del profilo e della configurazione in modalità con restrizioni
ms.assetid: 550f5413-eaa4-4530-867e-fd9b1907cadf
title: Definizione del profilo e della configurazione in modalità con restrizioni
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c9bb4d4bea3f42eaf897e781ccf859d094a0d0321815e7457aa6c79f96cb5ded
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119747051"
---
# <a name="restricted-mode-profile-and-configuration-establishment"></a>Definizione del profilo e della configurazione in modalità con restrizioni

A causa della varietà di tipi di dati che possono essere decodificati da DirectX VA e delle diverse configurazioni di decodifica supportate all'interno di DirectX VA per ognuno di questi tipi di dati (ad esempio, l'uso di buffer bitstream rispetto alla decodifica della differenza residua dell'host rispetto all'IDCT basato sull'acceleratore con e senza crittografia di ogni tipo pertinente di buffer e così via),  Si ritiene che sarebbe in qualche modo ingiusto specificare semplicemente un GUID univoco per ogni tipo di dati univoco e la configurazione di decodifica. In questo modo si creerebbe un numero elevato di GUID (ad esempio, ipoteticamente se fossero possibili 16 profili di DirectX VA e 16 configurazioni per ognuna, sarebbe necessario avere 256 GUID definiti, che richiedono 4 kilobyte di memoria solo per contenerli tutti. Questo problema è la parte più difficile di determinare come eseguire il mapping di DirectX VA in **IAMVideoAccelerator,** con il resto della definizione operativa per lo più piuttosto semplice. Di conseguenza, si specifica un GUID univoco solo per ogni tipo di dati (per ogni profilo in modalità limitata) e si consente l'associazione di un GUID aggiuntivo a ogni tipo di crittografia. La configurazione di decodifica viene quindi stabilita tra il decodificatore e l'acceleratore da una negoziazione subordinata di livello inferiore usando operazioni di probe e blocco per stabilire le configurazioni per ogni tipo di funzione DirectX VA.

 

 



