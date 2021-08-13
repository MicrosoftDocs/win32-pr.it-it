---
description: Un pacchetto di installazione contiene tutte le informazioni richieste dal Windows installer per installare o disinstallare un'applicazione o un prodotto ed eseguire l'interfaccia utente di installazione.
ms.assetid: 532b3492-919f-4999-b86c-e3c210876141
title: Pacchetto di installazione
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 61daf878a7933353382a52acd9a7172e87b97b14cdf41a047279360342ca768b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118633821"
---
# <a name="installation-package"></a>Pacchetto di installazione

Un pacchetto di installazione contiene tutte le informazioni richieste dal Windows installer per installare o disinstallare un'applicazione o un prodotto ed eseguire l'interfaccia utente di installazione. Ogni pacchetto di installazione include un file .msi, contenente un database di installazione, un flusso di informazioni di riepilogo e flussi di dati per varie parti dell'installazione. Il .msi può contenere anche una o più trasformazioni, file di origine interni e file di origine esterni o file cab richiesti dall'installazione.

Gli sviluppatori di applicazioni devono creare un'installazione per usare il programma di installazione. Poiché il programma di installazione organizza [](components-and-features.md)le installazioni in base al concetto di componenti e funzionalità e archivia tutte le informazioni sull'installazione in un database relazionale, il processo di creazione di un pacchetto di installazione comporta in generale i passaggi seguenti:

-   Identificare le funzionalità da presentare agli utenti.
-   Organizzare l'applicazione in componenti.
-   Popolare il database di installazione con informazioni.
-   Convalidare il pacchetto di installazione.

La sezione successiva illustra i componenti e le funzionalità del programma di installazione. Per altre informazioni, vedere [Componenti e funzionalità](components-and-features.md). La scelta delle funzionalità è comunemente determinata dalla funzionalità dell'applicazione dal punto di vista dell'utente.

È consigliabile che gli sviluppatori usino una procedura standard per la scelta dei componenti. Per altre informazioni, vedere [Organizzazione di applicazioni in componenti](organizing-applications-into-components.md).

Gli autori di pacchetti possono usare strumenti di creazione di pacchetti di terze parti o un editor di tabelle e Windows Installer SDK per popolare il database di installazione. Tutti i pacchetti di installazione devono essere convalidati per garantire la coerenza interna. Per altre informazioni, vedere [Convalida dei pacchetti](package-validation.md).

 

 



