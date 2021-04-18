---
description: Un pacchetto di installazione di contiene tutte le informazioni richieste dal Windows Installer per installare o disinstallare un'applicazione o un prodotto e per eseguire l'interfaccia utente del programma di installazione.
ms.assetid: 532b3492-919f-4999-b86c-e3c210876141
title: Pacchetto di installazione
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fe5e5ff79d0c868036dd12ed533b1cd18f9f70d2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106313344"
---
# <a name="installation-package"></a>Pacchetto di installazione

Un pacchetto di installazione di contiene tutte le informazioni richieste dal Windows Installer per installare o disinstallare un'applicazione o un prodotto e per eseguire l'interfaccia utente del programma di installazione. Ogni pacchetto di installazione include un file con estensione msi contenente un database di installazione, un flusso di informazioni di riepilogo e flussi di dati per varie parti dell'installazione. Il file con estensione msi può inoltre contenere una o più trasformazioni, file di origine interni e file di origine esterni o file CAB richiesti dall'installazione.

Gli sviluppatori di applicazioni devono creare un'installazione per l'utilizzo del programma di installazione. Poiché il programma di installazione organizza le installazioni intorno al concetto di [componenti e funzionalità](components-and-features.md)e archivia tutte le informazioni sull'installazione in un database relazionale, il processo di creazione di un pacchetto di installazione comporta l'ampia gamma dei passaggi seguenti:

-   Identificare le funzionalità da presentare agli utenti.
-   Organizzare l'applicazione in componenti.
-   Inserire le informazioni nel database di installazione.
-   Convalidare il pacchetto di installazione.

Nella sezione successiva vengono descritti i componenti e le funzionalità del programma di installazione. Per ulteriori informazioni, vedere [componenti e funzionalità](components-and-features.md). La scelta delle funzionalità è generalmente determinata dalle funzionalità dell'applicazione dal punto di vista dell'utente.

È consigliabile che gli sviluppatori usino una procedura standard per la scelta dei componenti. Per altre informazioni, vedere [organizzazione di applicazioni in componenti](organizing-applications-into-components.md).

Per popolare il database di installazione, gli autori di pacchetti possono utilizzare strumenti di creazione di pacchetti di terze parti o un editor tabelle e l'SDK Windows Installer. Tutti i pacchetti di installazione devono essere convalidati per coerenza interna. Per ulteriori informazioni, vedere [convalida dei pacchetti](package-validation.md).

 

 



