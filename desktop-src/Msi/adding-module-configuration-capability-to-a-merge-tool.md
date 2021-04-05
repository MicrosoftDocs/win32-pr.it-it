---
description: Windows Installer gli sviluppatori possono creare strumenti che consentono agli utenti finali di usare moduli unione configurabili.
ms.assetid: 5857b788-f1dd-41d0-b0ee-0872494e3c2c
title: Aggiunta della funzionalità di configurazione del modulo a uno strumento di merge
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ba04d297ad93cffc553670c648577f650cd21407
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103756254"
---
# <a name="adding-module-configuration-capability-to-a-merge-tool"></a>Aggiunta della funzionalità di configurazione del modulo a uno strumento di merge

Per consentire agli utenti finali di utilizzare i moduli unione configurabili, è possibile creare strumenti di merge e configurazione per eseguire le operazioni seguenti:

-   Gli strumenti di merge devono chiamare le funzioni in Mergemod.dll versione 2,0 per unire il modulo. Non è possibile usare le versioni precedenti di Mergemod.dll per configurare i moduli unione.
-   Le applicazioni di configurazione client devono interagire con l'utente del modulo merge per raccogliere le selezioni utente per gli elementi configurabili.
-   Gli strumenti di merge devono esporre all'applicazione client le informazioni di configurazione create nel modulo merge, in modo che il client possa utilizzare tali informazioni per eseguire query sull'utente.
-   Quando uno strumento di merge rileva un elemento configurabile durante un'operazione di merge, deve chiamare lo strumento di configurazione client per le informazioni di personalizzazione ottenute dall'utente. Lo strumento di merge deve apportare le modifiche specificate al modulo merge.
-   Le applicazioni di configurazione devono consentire all'utente di fornire scelte per gli elementi configurabili, ma non è necessario che tutte le possibili scelte siano rivelate all'utente. Lo strumento di merge può utilizzare valori predefiniti per gli elementi configurabili non selezionati dall'utente.
-   Se un utente non fornisce informazioni di personalizzazione, gli strumenti di merge devono usare i valori di configurazione predefiniti specificati nel modulo merge.
-   Dopo che un utente fornisce le selezioni specifiche dello strumento di configurazione, lo strumento di merge chiama Mergemod.dll per eseguire il merge.

 

 



