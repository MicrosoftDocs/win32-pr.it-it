---
title: Evoluzione dei file System
description: Prima che i computer venissero sviluppati per funzionare su sistemi operativi su disco, ogni computer era progettato per eseguire un'unica applicazione proprietaria, che aveva un controllo completo ed esclusivo dell'intero computer.
ms.assetid: 46d497b5-c325-4395-8512-1ed4b88441de
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7dc34dc699488b5952d52dfd13f49ea63aaa85aa
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "106298123"
---
# <a name="the-evolution-of-file-systems"></a>Evoluzione dei file System

Prima che i computer venissero sviluppati per funzionare su sistemi operativi su disco, ogni computer era progettato per eseguire un'unica applicazione proprietaria, che aveva un controllo completo ed esclusivo dell'intero computer. L'applicazione scrive i dati persistenti direttamente in un disco o in un tamburo inviando i comandi direttamente al controller del disco. L'applicazione è stata responsabile della gestione dei percorsi assoluti dei dati sul disco, assicurandosi che non sovrascriva i dati già esistenti. Poiché una sola applicazione era in esecuzione nel computer in qualsiasi momento, questa attività non era troppo complessa.

L'avvento dei sistemi informatici che potevano eseguire più di un'applicazione richiedeva un meccanismo per garantire che le applicazioni non scrivessero i dati degli altri. Gli sviluppatori di applicazioni hanno risolto questo problema adottando un unico standard per distinguere i settori del disco in uso da quelli che erano gratuiti, definendoli di conseguenza. Nel tempo questi standard si uniscono a un sistema operativo su disco, che fornisce vari servizi alle applicazioni, incluso un file system per la gestione dell'archiviazione permanente. Con l'avvento di una file system, le applicazioni non devono più gestire direttamente il supporto di archiviazione fisica. Al contrario, hanno semplicemente detto al file system di scrivere blocchi di dati sul disco e lasciare che i file system si preoccupino di come farlo. Inoltre, il file system le applicazioni consentite di creare gerarchie di dati tramite un'astrazione nota come una directory. Una directory potrebbe contenere non solo file ma altre directory, che a loro volta potrebbero contenere i propri file e directory e così via.

Il file system ha fornito un unico livello di riferimento indiretto tra le applicazioni e il disco e il risultato è che ogni applicazione ha visualizzato un file come un singolo flusso contiguo di byte sul disco, anche se il file system stava effettivamente archiviando il file in settori non contigui. Il riferimento indiretto per le applicazioni ha liberato la necessità di tenere traccia della posizione assoluta dei dati in un dispositivo di archiviazione.

Attualmente, praticamente tutte le API di sistema per l'input e l'output di file forniscono applicazioni per la scrittura di informazioni in un file flat. Le applicazioni visualizzano questo file come un singolo flusso di byte che può aumentare fino a quando il disco non è pieno. Per un lungo periodo di tempo queste API sono sufficienti per le applicazioni per archiviare le informazioni persistenti. Le applicazioni hanno innovazioni significative nel modo in cui si occupano di un unico flusso di informazioni per fornire funzionalità come i salvataggi "veloci" incrementali.

Tuttavia, in un mondo di oggetti componente, l'archiviazione dei dati in un singolo file flat non è più efficiente. Così come i file System sono emersi dalla necessità per più applicazioni di condividere lo stesso supporto di archiviazione, ora, gli oggetti componente richiedono un sistema che consenta loro di condividere l'archiviazione all'interno del framework concettuale di un singolo file. Anche se è possibile archiviare gli oggetti separati usando l'archiviazione file flat convenzionale, se uno degli oggetti aumenta di dimensione o se si aggiunge semplicemente un altro oggetto, è necessario caricare l'intero file in memoria, inserire il nuovo oggetto e salvare l'intero file. Questo processo può richiedere molto tempo.

La soluzione fornita da COM consiste nell'implementazione di un secondo livello di riferimento indiretto: un file system all'interno di un file. Per l'archiviazione file flat è necessario che un'ampia sequenza di byte contigui sul disco venga modificata tramite un singolo handle di file con un unico puntatore di ricerca. Al contrario, l'archiviazione strutturata COM definisce come trattare una singola entità di file system come raccolta strutturata di due tipi di oggetti, ovvero archivi e flussi, che fungono da directory e file.

 

 




