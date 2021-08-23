---
description: Windows Gli sviluppatori del programma di installazione possono creare strumenti che consentono agli utenti finali di usare moduli unione configurabili.
ms.assetid: 5857b788-f1dd-41d0-b0ee-0872494e3c2c
title: Aggiunta della funzionalità di configurazione del modulo a uno strumento di unione
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cb20645d4a66b09ffa95e34f04e9057bd0a8c57e645be652d8ea8cd595ddd6cb
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119252101"
---
# <a name="adding-module-configuration-capability-to-a-merge-tool"></a>Aggiunta della funzionalità di configurazione del modulo a uno strumento di unione

Per consentire agli utenti finali di usare moduli unione configurabili, è possibile creare strumenti di unione e configurazione per eseguire le operazioni seguenti:

-   Gli strumenti di merge devono chiamare le funzioni Mergemod.dll versione 2.0 per unire il modulo. Le versioni precedenti di Mergemod.dll possono essere usate per configurare i moduli unione.
-   Le applicazioni di configurazione client devono interagire con l'utente del modulo unione per raccogliere le selezioni utente per gli elementi configurabili.
-   Gli strumenti di unione devono esporre le informazioni di configurazione scritte nel modulo di merge all'applicazione client in modo che il client possa usare queste informazioni per eseguire query sull'utente.
-   Quando uno strumento di unione rileva un elemento configurabile durante un'unione, deve chiamare lo strumento di configurazione client per le informazioni di personalizzazione ottenute dall'utente. Lo strumento di unione deve apportare le modifiche specificate al modulo unione.
-   Le applicazioni di configurazione devono consentire all'utente di fornire opzioni per gli elementi configurabili, ma non è necessario che tutte le scelte possibili siano rivelate all'utente. Lo strumento di unione può usare i valori predefiniti per gli elementi configurabili che l'utente non seleziona.
-   Se un utente non fornisce informazioni di personalizzazione, gli strumenti di unione devono usare i valori di configurazione predefiniti specificati nel modulo unione.
-   Dopo che un utente ha selezionato lo strumento di configurazione, lo strumento di merge chiama Mergemod.dll per eseguire l'unione.

 

 



