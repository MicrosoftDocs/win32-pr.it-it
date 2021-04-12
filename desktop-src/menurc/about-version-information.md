---
title: Informazioni sulle versioni
description: In questo argomento vengono illustrate le funzioni delle informazioni sulla versione.
ms.assetid: 63fb6c0f-11b3-4d70-b1ba-56086cb02847
keywords:
- risorse, informazioni sulla versione
- informazioni sulla versione
- aggiunta di informazioni sulla versione
- conflitti di file
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 25bf5c0914ba28b9a5178f99a94f83f57ac99550
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2020
ms.locfileid: "104398920"
---
# <a name="about-version-information"></a>Informazioni sulle versioni

È possibile utilizzare le funzioni di informazioni sulla versione per determinare la posizione in cui deve essere installato un file e identificare i conflitti con i file attualmente installati. Queste funzioni consentono di evitare i problemi seguenti:

-   installazione di versioni precedenti dei componenti rispetto a versioni più recenti
-   modifica della lingua in un sistema con linguaggio misto senza notifica
-   installazione di più copie di una raccolta in directory diverse
-   copia di file in directory di rete condivise da più utenti

Le funzioni di informazioni sulla versione consentono alle applicazioni di eseguire query su una risorsa di versione per ottenere informazioni sui file e presentare le informazioni in un formato non crittografato. Queste informazioni includono lo scopo, l'autore, il numero di versione e così via del file.

È possibile aggiungere informazioni sulla versione a tutti i file che possono avere risorse di Windows, ad esempio le dll, i file eseguibili o i file del tipo di carattere fon. Per aggiungere le informazioni, creare una [risorsa VERSIONINFO](/windows/desktop/menurc/versioninfo-resource) e usare il compilatore di risorse per compilare la risorsa.

 

 