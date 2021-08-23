---
description: Il Windows programma di installazione può annunciare la disponibilità di un'applicazione agli utenti o ad altre applicazioni senza installare effettivamente l'applicazione.
ms.assetid: 67170daa-448a-4a20-b38a-2dd36c95440f
title: Annuncio pubblicitario
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d71f9d60eb1d709f0b956719593e2d7158ba8ef2bc17994945302474a02b695a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119066371"
---
# <a name="advertisement"></a>Annuncio pubblicitario

Il Windows programma di installazione può annunciare la disponibilità di un'applicazione agli utenti o ad altre applicazioni senza installare effettivamente l'applicazione. Se un'applicazione viene annunciata, solo le interfacce necessarie per il caricamento e l'avvio dell'applicazione vengono presentate all'utente o ad altre applicazioni. Se un utente o un'applicazione attiva un'interfaccia annunciata, il programma di installazione procede all'installazione dei componenti necessari come descritto in [Installazione su richiesta.](installation-on-demand.md)

I due tipi di annunci pubblicitari sono l'assegnazione e la pubblicazione. Un'applicazione viene visualizzata come installata a un utente quando l'applicazione viene assegnata all'utente. Il menu **Start** contiene i collegamenti appropriati, vengono visualizzate le icone, i file sono associati all'applicazione e le voci del Registro di sistema riflettono l'installazione dell'applicazione. Quando l'utente tenta di aprire un'applicazione assegnata, questa viene installata su richiesta.

Il programma di installazione supporta l'annuncio di applicazioni e funzionalità in base al sistema operativo. Il programma di installazione registra le informazioni sulla classe COM per le applicazioni assegnate a partire da Windows XP. In questo modo il programma di installazione può installare l'applicazione al momento della creazione di un'istanza di una classe annunciata. Per altre informazioni, vedere [Platform Support of Advertisement](platform-support-of-advertisement.md).

È possibile pubblicare un'applicazione dal server a partire Windows Server 2003. L'applicazione pubblicata viene quindi installata tramite l'associazione di file o il tipo MIME (Multipurpose Internet Mail Extension). La pubblicazione non popola l'interfaccia utente con alcuna delle icone dell'applicazione. Il sistema operativo client può installare un'applicazione pubblicata a partire da Windows XP.

 

 



