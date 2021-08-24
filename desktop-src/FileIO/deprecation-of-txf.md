---
description: Questo argomento illustra le alternative all'uso dell'API NTFS transazionale (TxF) negli scenari di utilizzo comuni.
ms.assetid: 9ee26e7e-990e-4cd3-8180-f0fcaac2b752
title: Alternative all'uso di NTFS transazionale
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4ab924c5ee4204180b891b3aad13a5809fa07671ad0e18d6ddc9ce353122ac80
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119765971"
---
# <a name="alternatives-to-using-transactional-ntfs"></a>Alternative all'uso di NTFS transazionale

-   [Contenuto](#abstract)
-   [Introduzione](#introduction)
-   [Alternative a TxF per scenario](#alternatives-to-txf-by-scenario)
-   [Applicazioni che aggiornano un singolo file con dati "di tipo documento"](#applications-updating-a-single-file-with-document-like-data)
-   [Applicazioni che eseguono aggiornamenti a più file e/o all'hive del Registro di sistema](#applications-performing-updates-to-multiple-files-andor-to-the-registry-hive)
-   [Applicazioni che gestiscono un set di dati strutturati](#applications-managing-a-set-of-structured-data)
-   [Applicazioni con transazioni che coinvolgono file in un volume NTFS locale e tabelle in un database SQL esterno](#applications-with-transactions-involving-files-on-a-local-ntfs-volume-and-tables-in-an-external-sql-database)
-   [Chiusura &'azione consigliata](/windows)

## <a name="abstract"></a>Contenuto

Microsoft consiglia vivamente agli sviluppatori di analizzare l'uso delle alternative discusse (o, in alcuni casi, di esaminare altre alternative) anziché adottare una piattaforma API che potrebbe non essere disponibile nelle versioni future di Windows.

## <a name="introduction"></a>Introduzione

TxF è stato introdotto con Windows Vista come mezzo per introdurre transazioni di file atomiche Windows. Consente agli sviluppatori Windows di avere atomicità transazionale per le operazioni sui file nelle transazioni con un singolo file, nelle transazioni che coinvolgono più file e nelle transazioni che si estendono su più origini, ad esempio il Registro di sistema (tramite TxR) e i database (ad esempio SQL). Anche se TxF è un potente set di API, l'interesse degli sviluppatori per questa piattaforma API è stato estremamente limitato a partire da Windows Vista, principalmente a causa della complessità e delle varie sfumature che gli sviluppatori devono considerare come parte dello sviluppo di applicazioni. Di conseguenza, Microsoft sta valutando la deprecazione delle API TxF in una versione futura di Windows per concentrare le attività di sviluppo e manutenzione su altre funzionalità e API che hanno più valore per la maggior parte dei clienti. La sezione successiva descrive metodi alternativi di esempio per ottenere risultati simili a quelli di TxF per diversi tipi di scenari applicativi.

## <a name="alternatives-to-txf-by-scenario"></a>Alternative a TxF per scenario

Con le limitazioni descritte in precedenza, gli sviluppatori devono esaminare le alternative a TxF per coprire scenari di applicazioni non soddisfatti da TxF. Di seguito sono descritte alcune alternative suggerite agli usi comuni di TxF che gli sviluppatori possono prendere in considerazione. Si noti che questo elenco non è completo né esaustivo.

## <a name="applications-updating-a-single-file-with-document-like-data"></a>Applicazioni che aggiornano un singolo file con dati "di tipo documento"

Molte applicazioni che gestiscono dati di tipo "documento" tendono a caricare l'intero documento in memoria, a operare su di esso e quindi a ri write-out per salvare le modifiche. L'atomicità necessaria in questo caso è che le modifiche vengono completamente applicate o non applicate affatto, perché uno stato incoerente renderebbe il file danneggiato. Un approccio comune consiste nel scrivere il documento in un nuovo file e quindi sostituire il file originale con quello nuovo. Un metodo per eseguire questa operazione è con [**l'API ReplaceFile.**](/windows/desktop/api/WinBase/nf-winbase-replacefilea)

## <a name="applications-performing-updates-to-multiple-files-andor-to-the-registry-hive"></a>Applicazioni che eseguono aggiornamenti a più file e/o all'hive del Registro di sistema

Molte applicazioni devono eseguire in modo atomico un aggiornamento a un set di file e al Registro di sistema. Questo scenario viene in genere ottenuto tramite un'applicazione del programma di installazione, ad esempio Windows programma di installazione. Per altre informazioni sul programma Windows, fare riferimento a Windows [Installer.](/windows/desktop/Msi/windows-installer-portal)

## <a name="applications-managing-a-set-of-structured-data"></a>Applicazioni che gestiscono un set di dati strutturati

Molte applicazioni gestiscono alcuni set di strutture di dati proprietari di vari tipi come mezzo per archiviare i dati. Una sfida significativa per queste applicazioni è il processo di mantenimento dell'integrità di puntatori/riferimenti interni se si verifica un errore durante un'operazione di aggiornamento. La creazione del meccanismo è effettivamente un "problema difficile", pertanto la maggior parte delle applicazioni si basa su un vero server di database per gestire il set di dati.

Per gestire i dati strutturati sono disponibili due suggerimenti:

-   Microsoft fornisce la posta in arrivo di Extensible Archiviazione Engine (ESE) in Windows per consentire alle applicazioni di eseguire operazioni transazional di aggiornamento e recupero dei dati. Per altre informazioni su Extensible Archiviazione Engine (ESE), vedere <https://msdn.microsoft.com/library/gg269259.aspx> .
-   Per le applicazioni che richiedono un provider di database più potente, affidabile e scalabile, è consigliabile che i clienti considerino l'uso della funzionalità Filestream disponibile con Microsoft SQL Server. Per altre informazioni sui SQL filestream, vedere <https://technet.microsoft.com/library/bb933993.aspx> .

## <a name="applications-with-transactions-involving-files-on-a-local-ntfs-volume-and-tables-in-an-external-sql-database"></a>Applicazioni con transazioni che coinvolgono file in un volume NTFS locale e tabelle in un database SQL esterno

Esistono classi di applicazioni che hanno esigenze di set di dati di grandi dimensioni o devono avere atomicità transazionale in un'operazione che interessa un database esterno e l'archiviazione locale. Per questo scenario, è consigliabile che gli sviluppatori considerino l'uso SQL filestream per eseguire operazioni sui file transazionali. Per altre informazioni sui SQL filestream, vedere <https://technet.microsoft.com/library/bb933993.aspx> .

## <a name="closing--recommended-action"></a>Chiusura &'azione consigliata

TxF è un set complesso e articolato di API che non vengono comunemente usate da applicazioni di terze parti. Con la possibilità che queste API non siano disponibili nelle versioni future di Windows e con il fatto che esistono strumenti alternativi più semplici per ottenere molti degli scenari per cui è stato sviluppato TxF, Microsoft consiglia vivamente agli sviluppatori di esaminare questi mezzi alternativi invece di creare una dipendenza da TxF nelle proprie applicazioni.

 

 
