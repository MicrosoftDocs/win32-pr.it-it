---
title: Interfacce DO
description: Utilizzare le seguenti interfacce di ottimizzazione recapito per trasferire i file e monitorare i processi nella coda di trasferimento.
ms.assetid: 20203CCD-86CC-4551-BA4F-0A5999F8C956
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0359328f189c1a5b5d9649d8300dc59a80df4480
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "106299932"
---
# <a name="do-interfaces"></a>Interfacce DO

Utilizzare le seguenti interfacce di ottimizzazione recapito per trasferire i file e monitorare i processi nella coda di trasferimento.

| Interfaccia | Descrizione |
|-|-|
| [**IBackgroundCopyCallback**](ibackgroundcopycallback.md) | I client implementano l'interfaccia [**IBackgroundCopyCallback**](ibackgroundcopycallback.md) per ricevere una notifica che indica che un processo è stato completato, è stato modificato o è in errore. |
| [**IBackgroundCopyError**](ibackgroundcopyerror.md) | Recupera i dettagli di un errore del processo. |
| [**IBackgroundCopyFile**](ibackgroundcopyfile.md) | Recupera i nomi di file locali e remoti di una richiesta di trasferimento file nel processo e il relativo stato di avanzamento. |
| [**IBackgroundCopyFile2**](ibackgroundcopyfile2.md) | Specifica un nuovo nome remoto per il file e recupera l'elenco di intervalli da scaricare. |
| [**IBackgroundCopyFile5**](ibackgroundcopyfile5.md) | Fornisce i metodi get e set di proprietà generiche per le proprietà BackgroundCopyFile. |
| [**Metodo ibackgroundcopyjob**](ibackgroundcopyjob-.md) | Aggiunge file al processo, imposta il livello di priorità del processo, determina lo stato del processo e avvia e arresta il processo. |
| [**IBackgroundCopyJob5**](ibackgroundcopyjob5.md) | Esegue una query o imposta diversi comportamenti facoltativi di un processo. |
| [**IBackgroundCopyManager**](ibackgroundcopymanager.md) | Crea processi di trasferimento, recupera un oggetto enumeratore di processi nella coda e recupera singoli processi dalla coda. |
| [**IDeliveryOptimizationJob**](ideliveryoptimizationjob.md) | Usare per scaricare gli intervalli di un file. |
| [**IDeliveryOptimizationFile**](ideliveryoptimizationfile.md) | Usare per identificare lo stato di un file specifico. |
| [**IDODownload**](./do/nn-do-idodownload.md) | Utilizzato per avviare e gestire un download. |
| [**IDODownloadInternal**](./dodownloadinternal/nn-dodownloadinternal-idodownloadinternal.md) | Utilizzato per ottenere o impostare le proprietà di download estese. |
| [**IDODownloadStatusCallback**](./do/nn-do-idodownloadstatuscallback.md) | Utilizzato per ricevere notifiche relative a un download. |
| [**IDOManager**](./do/nn-do-idomanager.md) | Utilizzato per creare un nuovo download e per enumerare i download esistenti. |
| [**IEnumBackgroundCopyFiles**](ienumbackgroundcopyfiles-.md) | Enumera i file nel processo. |