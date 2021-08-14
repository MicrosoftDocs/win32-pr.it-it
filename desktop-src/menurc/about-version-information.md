---
title: Informazioni sulle informazioni sulla versione
description: In questo argomento vengono illustrate le funzioni relative alle informazioni sulla versione.
ms.assetid: 63fb6c0f-11b3-4d70-b1ba-56086cb02847
keywords:
- risorse, informazioni sulla versione
- informazioni sulla versione
- aggiunta di informazioni sulla versione
- conflitti di file
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fd7b7916e77d29fa21aa6eb68e223d43a1415c36058fbe00e2d3abb9c4cae979
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117870717"
---
# <a name="about-version-information"></a>Informazioni sulle informazioni sulla versione

È possibile usare le funzioni relative alle informazioni sulla versione per determinare dove deve essere installato un file e identificare i conflitti con i file attualmente installati. Queste funzioni consentono di evitare i problemi seguenti:

-   installazione di versioni precedenti dei componenti in versioni più recenti
-   modifica della lingua in un sistema in linguaggio misto senza notifica
-   installazione di più copie di una libreria in directory diverse
-   copia di file in directory di rete condivise da più utenti

Le funzioni relative alle informazioni sulla versione consentono alle applicazioni di eseguire query su una risorsa versione per ottenere informazioni sui file e presentare le informazioni in un formato non crittografato. Queste informazioni includono lo scopo, l'autore, il numero di versione e così via del file.

È possibile aggiungere informazioni sulla versione a qualsiasi file che Windows risorse, ad esempio DLL, file eseguibili o file di tipo di carattere FON. Per aggiungere le informazioni, creare una [risorsa VERSIONINFO e](/windows/desktop/menurc/versioninfo-resource) usare il compilatore di risorse per compilare la risorsa.

 

 