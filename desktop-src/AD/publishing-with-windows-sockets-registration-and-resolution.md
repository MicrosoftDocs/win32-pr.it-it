---
title: Pubblicazione con Windows di registrazione dei socket & risoluzione
description: Windows I servizi socket possono usare le API di registrazione e risoluzione (RnR) per pubblicare i servizi e cercare i servizi pubblicati con RnR.
ms.assetid: 95c16d0b-abbc-4407-ac31-d7de0b25bd74
ms.tgt_platform: multiple
keywords:
- Windows Registrazione e risoluzione dei socket ad , pubblicazione
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4a071a37d1d017e4c034f3eaab175889fdfcd1789d9f48aeac2c2943dfc8b4f1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118184925"
---
# <a name="publishing-with-windows-sockets-registration--resolution"></a>Pubblicazione con Windows di registrazione dei socket & risoluzione

Windows I servizi socket possono usare le API di registrazione e risoluzione (RnR) per pubblicare i servizi e cercare i servizi pubblicati con RnR. La pubblicazione di RnR avviene in due passaggi. Il primo passaggio installa una classe del servizio che associa un GUID a un nome per il servizio. La classe del servizio può contenere dati di configurazione specifici del servizio. I servizi possono quindi pubblicarsi come istanze della classe di servizio. Quando vengono pubblicati, i client possono eseguire query sul servizio directory per le istanze di una determinata classe usando le API RnR e selezionare un'istanza a cui eseguire l'associazione. Quando una classe non è più necessaria, può essere rimossa.

 

 




