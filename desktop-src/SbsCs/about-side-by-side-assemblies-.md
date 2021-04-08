---
description: Un assembly side-by-side di Windows viene descritto da manifesti.
ms.assetid: 501BBFFE-5927-4656-8EEE-1F6ECFAFEF5E
title: Informazioni sugli assembly affiancati
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e190e6428f2e366af45a4f0961ad6ea6fb3561fe
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103967398"
---
# <a name="about-side-by-side-assemblies"></a>Informazioni sugli assembly affiancati

Un assembly side-by-side di Windows viene descritto da [manifesti](manifests.md). Un assembly affiancato contiene una raccolta di risorse, ovvero un gruppo di dll, classi Windows, server COM, librerie dei tipi o interfacce, che vengono sempre fornite alle applicazioni insieme. Queste sono descritte nel manifesto dell'assembly.

In genere, un assembly affiancato è una singola DLL. Ad esempio, l'assembly Microsoft COMCTL32 è una singola DLL con un manifesto, mentre l'assembly delle librerie di runtime del sistema di sviluppo Microsoft Visual C++ contiene più file. I manifesti contengono [*metadati*](m-sbscs-gly.md) che descrivono gli assembly affiancati e le dipendenze dell'assembly side-by-side.

Gli assembly affiancati vengono usati dal sistema operativo come unità di base per la denominazione, l'associazione, il controllo delle versioni, la distribuzione e la configurazione. Ogni assembly side-by-side ha un'identità univoca. Uno degli attributi dell'identità dell'assembly è la versione. Per altre informazioni, vedere [versioni degli assembly](assembly-versions.md).

A partire da Windows XP, le applicazioni in esecuzione contemporaneamente possono utilizzare più versioni di assembly affiancati. I manifesti e il numero di versione dell'assembly vengono usati dal caricatore per determinare l'associazione corretta tra le versioni degli assembly e le applicazioni. Gli assembly affiancati e i manifesti funzionano con le applicazioni e con gestione affiancata, come illustrato nella figura seguente.

![rappresentazione di un assembly side-by-side tipico](images/sxsman.png)

Nell'esempio precedente, entrambi Comctl32.DLL versione 6,0 e Comctl32.DLL versione 5,0 sono in Assembly Cache affiancati e disponibili per le applicazioni. Quando un'applicazione chiama per caricare la DLL, il gestore affiancato determina se l'applicazione ha una dipendenza della versione descritta in un manifesto. Se non è presente alcun manifesto pertinente, il sistema carica la versione predefinita dell'assembly. Per Windows XP, la versione 5,0 di Comctl32.DLL è l'impostazione predefinita del sistema. Se il gestore affiancato rileva una dipendenza dalla versione 6,0 indicata in un manifesto, tale versione viene caricata per l'esecuzione con l'applicazione.

Diversi assembly di sistema principali vengono resi disponibili da Microsoft come assembly side-by-side. Per ulteriori informazioni, vedere [assembly affiancati di Microsoft supportati](supported-microsoft-side-by-side-assemblies.md). Gli sviluppatori di applicazioni possono inoltre creare i propri assembly affiancati. Per ulteriori informazioni, vedere [linee guida per la creazione di assembly affiancati](guidelines-for-creating-side-by-side-assemblies.md). In molti casi è possibile aggiornare le applicazioni esistenti per usare gli assembly side-by-side senza dover modificare il codice dell'applicazione.

Gli sviluppatori sono invitati a usare assembly affiancati per creare [applicazioni isolate](isolated-applications.md)e per aggiornare le applicazioni esistenti in applicazioni isolate per i motivi seguenti:

-   Gli assembly affiancati riducono la possibilità di conflitti di versione della DLL.
-   La condivisione di assembly affiancati consente l'esecuzione contemporanea di più versioni di assembly COM o Windows.
-   Le applicazioni e gli amministratori possono aggiornare la configurazione dell'assembly in base alla configurazione [globale](publisher-configuration.md) o [per applicazione](per-application-configuration.md) dopo la distribuzione. Ad esempio, un'applicazione può essere aggiornata per usare un assembly affiancato che include un aggiornamento senza dover reinstallare l'applicazione.

 

 



