---
title: Evoluzione dei file system
description: Prima che i computer fossero sviluppati per funzionare nei sistemi operativi su disco, ogni computer era progettato per eseguire una singola applicazione proprietaria, che aveva il controllo completo ed esclusivo dell'intero computer.
ms.assetid: 46d497b5-c325-4395-8512-1ed4b88441de
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 35a619328da91e2d1387690b005984fa62c7b1439183b53188b11ffc4ba0565d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117959582"
---
# <a name="the-evolution-of-file-systems"></a>Evoluzione dei file system

Prima che i computer fossero sviluppati per funzionare nei sistemi operativi su disco, ogni computer era progettato per eseguire una singola applicazione proprietaria, che aveva il controllo completo ed esclusivo dell'intero computer. L'applicazione scriverà i dati persistenti direttamente in un disco, o a un disco, inviando i comandi direttamente al controller del disco. L'applicazione era responsabile della gestione delle posizioni assolute dei dati sul disco, assicurando che non sovrascriveva i dati già esistenti. Poiché nel computer era in esecuzione una sola applicazione alla volta, questa attività non era troppo difficile.

L'avvento dei sistemi informatici che potevano eseguire più di un'applicazione richiedeva un meccanismo per garantire che le applicazioni non scriveva i dati reciproci. Gli sviluppatori di applicazioni hanno risolto questo problema adottando un singolo standard per distinguere i settori del disco in uso da quelli gratuiti contrassegnandoli di conseguenza. Nel tempo, questi standard si sono uniti per diventare un sistema operativo su disco, che ha fornito vari servizi alle applicazioni, incluso un file system per la gestione dell'archiviazione permanente. Con l'avvento di un file system, le applicazioni non dovevano più gestire direttamente il supporto di archiviazione fisico. Al contrario, hanno semplicemente file system scrivere blocchi di dati sul disco e lasciare che il file system si preoccupa di come eseguire questa operazione. Inoltre, il file system alle applicazioni di creare gerarchie di dati tramite un'astrazione nota come directory. Una directory può contenere non solo file, ma anche altre directory, che a loro volta possono contenere i propri file e directory e così via.

Il file system ha fornito un singolo livello di riferimento indiretto tra le applicazioni e il disco e il risultato è che ogni applicazione vede un file come un singolo flusso contiguo di byte sul disco anche se il file system archivia effettivamente il file in settori non contigui. Il riferimento indiretto ha liberato le applicazioni dalla necessità di tenere traccia della posizione assoluta dei dati in un dispositivo di archiviazione.

Attualmente, praticamente tutte le API di sistema per l'input e l'output dei file forniscono applicazioni per la scrittura di informazioni in un file flat. Le applicazioni vedono questo file come un singolo flusso di byte che può aumentare fino a quando il disco non è pieno. Per molto tempo queste API sono state sufficienti per le applicazioni per archiviare le informazioni persistenti. Le applicazioni hanno apportato innovazioni significative nel modo in cui si occupano di un singolo flusso di informazioni per offrire funzionalità come i risparmi incrementali "veloci".

Tuttavia, in un mondo di oggetti componente, l'archiviazione dei dati in un singolo file flat non è più efficiente. Proprio come i file system non hanno richiesto a più applicazioni di condividere lo stesso supporto di archiviazione, ora gli oggetti componente richiedono un sistema che consenta loro di condividere l'archiviazione all'interno del framework concettuale di un singolo file. Anche se è possibile archiviare gli oggetti separati usando l'archiviazione convenzionale di file flat, se le dimensioni di uno degli oggetti aumentano o se si aggiunge semplicemente un altro oggetto, diventa necessario caricare l'intero file in memoria, inserire il nuovo oggetto e quindi salvare l'intero file. Questo processo può richiedere molto tempo.

La soluzione fornita da COM consiste nell'implementare un secondo livello di riferimento indiretto: un file system all'interno di un file. L'archiviazione file flat richiede che una sequenza contigua di byte di grandi dimensioni sul disco sia manipolata tramite un singolo handle di file con un singolo puntatore di ricerca. Al contrario, l'archiviazione strutturata COM definisce come trattare una singola entità file system come una raccolta strutturata di due tipi di oggetti, archivi e flussi, che fungono da directory e file.

 

 




