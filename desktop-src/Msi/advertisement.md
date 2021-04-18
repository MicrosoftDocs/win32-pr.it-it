---
description: Il Windows Installer può annunciare la disponibilità di un'applicazione a utenti o altre applicazioni senza installare effettivamente l'applicazione.
ms.assetid: 67170daa-448a-4a20-b38a-2dd36c95440f
title: Annuncio pubblicitario
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b0bb31f14fb4cd6f589e94939afdd5575df52c43
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106311067"
---
# <a name="advertisement"></a>Annuncio pubblicitario

Il Windows Installer può annunciare la disponibilità di un'applicazione a utenti o altre applicazioni senza installare effettivamente l'applicazione. Se viene annunciata un'applicazione, solo le interfacce necessarie per il caricamento e l'avvio dell'applicazione vengono presentate all'utente o ad altre applicazioni. Se un utente o un'applicazione attiva un'interfaccia annunciata, il programma di installazione procede con l'installazione dei componenti necessari, come descritto in [installazione su richiesta](installation-on-demand.md).

I due tipi di annunci pubblicitari sono assegnazione e pubblicazione. Quando l'applicazione viene assegnata all'utente, viene visualizzata un'applicazione installata a un utente. Il menu **Start** contiene i tasti di scelta rapida appropriati, vengono visualizzate le icone, i file sono associati all'applicazione e le voci del registro di sistema riflettono l'installazione dell'applicazione. Quando l'utente tenta di aprire un'applicazione assegnata, viene installata su richiesta.

Il programma di installazione supporta l'annuncio di applicazioni e funzionalità in base al sistema operativo. Il programma di installazione registra le informazioni della classe COM per le applicazioni assegnate a partire da Windows XP. Ciò consente al programma di installazione di installare l'applicazione durante la creazione di un'istanza di una classe annunciata. Per ulteriori informazioni, vedere [supporto della piattaforma](platform-support-of-advertisement.md)per gli annunci.

È possibile pubblicare un'applicazione dal server a partire da Windows Server 2003. L'applicazione pubblicata viene quindi installata tramite la relativa associazione file o il tipo MIME (Multipurpose Internet Mail Extension). La pubblicazione non popola l'interfaccia utente con alcuna icona dell'applicazione. Il sistema operativo client può installare un'applicazione pubblicata a partire da Windows XP.

 

 



