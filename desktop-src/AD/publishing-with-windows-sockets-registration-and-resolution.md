---
title: Pubblicazione con la registrazione di Windows Sockets & risoluzione
description: I servizi Windows Sockets possono usare le API di registrazione e risoluzione (RnR) per pubblicare i servizi e cercare i servizi pubblicati con RnR.
ms.assetid: 95c16d0b-abbc-4407-ac31-d7de0b25bd74
ms.tgt_platform: multiple
keywords:
- Active Directory per la registrazione e la risoluzione di Windows Sockets, pubblicazione
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e722d83447bd97e3964a9a0cc85df45ffd27faba
ms.sourcegitcommit: 460af18ea55f4b12d47d5b8d4b883896e21adf00
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/04/2019
ms.locfileid: "104472091"
---
# <a name="publishing-with-windows-sockets-registration--resolution"></a>Pubblicazione con la registrazione di Windows Sockets & risoluzione

I servizi Windows Sockets possono usare le API di registrazione e risoluzione (RnR) per pubblicare i servizi e cercare i servizi pubblicati con RnR. La pubblicazione RnR viene eseguita in due passaggi. Il primo passaggio installa una classe del servizio che associa un GUID a un nome per il servizio. La classe del servizio può mantenere i dati di configurazione specifici del servizio. I servizi possono quindi essere pubblicati come istanze della classe del servizio. Al momento della pubblicazione, i client possono eseguire query nel servizio directory per le istanze di una determinata classe usando le API RnR e selezionare un'istanza a cui eseguire l'associazione. Quando una classe non è più necessaria, può essere rimossa.

 

 




