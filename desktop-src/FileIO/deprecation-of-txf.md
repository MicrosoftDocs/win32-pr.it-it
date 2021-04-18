---
description: In questo argomento vengono illustrate le alternative all'utilizzo dell'API NTFS transazionale (TxF) negli scenari di utilizzo comuni.
ms.assetid: 9ee26e7e-990e-4cd3-8180-f0fcaac2b752
title: Alternative all'utilizzo di Transactional NTFS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cc69974f27abfba0323ea4d3f16a720e5e99e69d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106310029"
---
# <a name="alternatives-to-using-transactional-ntfs"></a>Alternative all'utilizzo di Transactional NTFS

-   [Contenuto](#abstract)
-   [Introduzione](#introduction)
-   [Alternative a TxF per scenario](#alternatives-to-txf-by-scenario)
-   [Applicazioni che aggiornano un singolo file con dati di tipo "documento"](#applications-updating-a-single-file-with-document-like-data)
-   [Applicazioni che eseguono aggiornamenti a più file e/o all'hive del registro di sistema](#applications-performing-updates-to-multiple-files-andor-to-the-registry-hive)
-   [Applicazioni che gestiscono un set di dati strutturati](#applications-managing-a-set-of-structured-data)
-   [Applicazioni con transazioni che coinvolgono file in un volume NTFS locale e tabelle in un database SQL esterno](#applications-with-transactions-involving-files-on-a-local-ntfs-volume-and-tables-in-an-external-sql-database)
-   [Chiusura & azione consigliata](/windows)

## <a name="abstract"></a>Contenuto

Microsoft consiglia vivamente agli sviluppatori di esaminare l'utilizzo delle alternative discusse (o, in alcuni casi, di analizzare altre alternative) invece di adottare una piattaforma API che potrebbe non essere disponibile nelle versioni future di Windows.

## <a name="introduction"></a>Introduzione

TxF è stato introdotto con Windows Vista come mezzo per introdurre transazioni di file atomici in Windows. Consente agli sviluppatori Windows di avere un'atomicità transazionale per le operazioni sui file in transazioni con un singolo file, in transazioni che coinvolgono più file e in transazioni che si estendono su più origini, ad esempio il registro (tramite TxR) e i database, ad esempio SQL. Sebbene TxF sia un potente set di API, l'interesse degli sviluppatori è molto limitato in questa piattaforma API, poiché Windows Vista è dovuto principalmente alla complessità e alle varie sfumature che gli sviluppatori devono considerare come parte dello sviluppo di applicazioni. Di conseguenza, Microsoft prende in considerazione la deprecazione delle API TxF in una versione futura di Windows per concentrare lo sviluppo e le attività di manutenzione su altre funzionalità e API che hanno un valore maggiore per la maggior parte dei clienti. Nella sezione successiva vengono descritti i metodi alternativi di esempio per ottenere risultati simili come TxF per diversi tipi di scenari di applicazione.

## <a name="alternatives-to-txf-by-scenario"></a>Alternative a TxF per scenario

Con le limitazioni descritte in precedenza, gli sviluppatori dovrebbero esaminare le alternative a TxF per coprire scenari di applicazione non soddisfatti da TxF. Di seguito sono illustrate alcune alternative suggerite agli usi comuni di TxF che gli sviluppatori possono prendere in considerazione. Si noti che questo elenco non è esaustivo né completo.

## <a name="applications-updating-a-single-file-with-document-like-data"></a>Applicazioni che aggiornano un singolo file con dati di tipo "documento"

Molte applicazioni che gestiscono i dati di tipo "documento" tendono a caricare l'intero documento in memoria, a operare su di esso e quindi a scriverlo di nuovo per salvare le modifiche. L'atomicità necessaria è che le modifiche siano completamente applicate o non applicate, perché uno stato incoerente renderebbe danneggiato il file. Un approccio comune consiste nel scrivere il documento in un nuovo file, quindi sostituire il file originale con quello nuovo. Un metodo per eseguire questa operazione è con l'API [**ReplaceFile**](/windows/desktop/api/WinBase/nf-winbase-replacefilea) .

## <a name="applications-performing-updates-to-multiple-files-andor-to-the-registry-hive"></a>Applicazioni che eseguono aggiornamenti a più file e/o all'hive del registro di sistema

Sono disponibili molte applicazioni che devono eseguire atomicamente un aggiornamento a un set di file e al registro di sistema. Questo scenario viene in genere eseguito tramite un'applicazione di installazione, ad esempio Windows Installer. Per ulteriori informazioni su Windows Installer, vedere [Windows Installer](/windows/desktop/Msi/windows-installer-portal).

## <a name="applications-managing-a-set-of-structured-data"></a>Applicazioni che gestiscono un set di dati strutturati

Molte applicazioni gestiscono un set di strutture di dati proprietarie di tipi diversi come mezzo per archiviare i dati. Una sfida significativa per queste applicazioni è il processo di gestione dell'integrità di puntatori/riferimenti interni se si verifica un errore durante un'operazione di aggiornamento. La creazione del meccanismo per questo è effettivamente un "problema hardware" e pertanto la maggior parte delle applicazioni si basa su un server di database reale per gestire il set di dati.

Due suggerimenti per semplificare la gestione dei dati strutturati sono:

-   Microsoft fornisce la posta in arrivo Extensible Storage Engine (ESE) in Windows per consentire alle applicazioni di eseguire operazioni di aggiornamento e recupero di dati transazionali. Per ulteriori informazioni su Extensible Storage Engine (ESE), consultare <https://msdn.microsoft.com/library/gg269259.aspx> .
-   Per le applicazioni che richiedono un provider di database più potente, affidabile e scalabile, è consigliabile che i clienti utilizzino la funzionalità FILESTREAM disponibile con Microsoft SQL Server. Per ulteriori informazioni sui flussi di dati SQL, vedere <https://technet.microsoft.com/library/bb933993.aspx> .

## <a name="applications-with-transactions-involving-files-on-a-local-ntfs-volume-and-tables-in-an-external-sql-database"></a>Applicazioni con transazioni che coinvolgono file in un volume NTFS locale e tabelle in un database SQL esterno

Esistono classi di applicazioni che hanno esigenze di set di dati di grandi dimensioni o che devono avere atomicità transazionale in un'operazione che interessa un database esterno e l'archiviazione locale. Per questo scenario, è consigliabile che gli sviluppatori utilizzino i flussi di file SQL per eseguire operazioni di file transazionali. Per ulteriori informazioni sui flussi di dati SQL, vedere <https://technet.microsoft.com/library/bb933993.aspx> .

## <a name="closing--recommended-action"></a>Chiusura & azione consigliata

TxF è un set di API complesso e sfumato che non sono comunemente usati da applicazioni di terze parti. Con la possibilità che queste API non siano disponibili nelle versioni future di Windows e il fatto che esistano metodi alternativi più semplici per realizzare molti degli scenari in cui TxF è stato sviluppato per, Microsoft consiglia vivamente agli sviluppatori di esaminare tali metodi alternativi anziché creare una dipendenza da TxF nelle proprie applicazioni.

 

 
