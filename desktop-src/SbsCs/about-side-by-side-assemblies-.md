---
description: Un Windows assembly side-by-side viene descritto dai manifesti.
ms.assetid: 501BBFFE-5927-4656-8EEE-1F6ECFAFEF5E
title: Informazioni sugli assembly side-by-side
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0e38ee058965b45c3094888aa34351114aa93e595e4e8b893889daaa685410a1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119142600"
---
# <a name="about-side-by-side-assemblies"></a>Informazioni sugli assembly side-by-side

Un Windows assembly side-by-side viene descritto [dai manifesti](manifests.md). Un assembly side-by-side contiene una raccolta di risorse, ovvero un gruppo di DLL, classi Windows, server COM, librerie dei tipi o interfacce, che vengono sempre fornite insieme alle applicazioni. Queste informazioni sono descritte nel manifesto dell'assembly.

In genere, un assembly side-by-side è una singola DLL. Ad esempio, l'assembly Microsoft COMCTL32 è una singola DLL con un manifesto, mentre l'assembly delle librerie di runtime del sistema di sviluppo Microsoft Visual C++ contiene più file. I manifesti [*contengono*](m-sbscs-gly.md) metadati che descrivono gli assembly side-by-side e le dipendenze degli assembly side-by-side.

Gli assembly side-by-side vengono usati dal sistema operativo come unità fondamentali di denominazione, associazione, controllo delle versioni, distribuzione e configurazione. Ogni assembly side-by-side ha un'identità univoca. Uno degli attributi dell'identità dell'assembly è la versione. Per altre informazioni, vedere [Versioni degli assembly.](assembly-versions.md)

A partire Windows XP, le applicazioni in esecuzione contemporaneamente possono usare più versioni di assembly side-by-side. I manifesti e il numero di versione dell'assembly vengono usati dal caricatore per determinare l'associazione corretta delle versioni degli assembly alle applicazioni. Gli assembly e i manifesti side-by-side funzionano con le applicazioni e la gestione side-by-side, come illustrato nella figura seguente.

![Rappresentazione dell'assembly side-by-side tipico](images/sxsman.png)

Nell'esempio precedente, sia Comctl32.DLL versione 6.0 che Comctl32.DLL versione 5.0 sono nella Cache assembly side-by-side e disponibili per le applicazioni. Quando un'applicazione chiama per caricare la DLL, la gestione side-by-side determina se l'applicazione ha una dipendenza di versione descritta in un manifesto. Se non è presente alcun manifesto pertinente, il sistema carica la versione predefinita dell'assembly. Per Windows XP, la versione 5.0 di Comctl32.DLL è l'impostazione predefinita del sistema. Se il gestore side-by-side rileva una dipendenza dalla versione 6.0 indicata in un manifesto, tale versione viene caricata per l'esecuzione con l'applicazione.

Diversi assembly di sistema chiave vengono resi disponibili da Microsoft come assembly side-by-side. Per altre informazioni, vedere [Assembly side-by-side Microsoft supportati.](supported-microsoft-side-by-side-assemblies.md) Gli sviluppatori di applicazioni possono anche creare assembly side-by-side personalizzati. Per altre informazioni, vedere [Linee guida per la creazione di assembly side-by-side.](guidelines-for-creating-side-by-side-assemblies.md) In molti casi è possibile aggiornare le applicazioni esistenti per l'uso di assembly side-by-side senza dover modificare il codice dell'applicazione.

Gli sviluppatori sono invitati a usare assembly [](isolated-applications.md)side-by-side per creare applicazioni isolate e aggiornare le applicazioni esistenti in applicazioni isolate per i motivi seguenti:

-   Gli assembly side-by-side riducono la possibilità di conflitti di versione dll.
-   La condivisione di assembly side-by-side consente l'esecuzione di più versioni di assembly COM o Windows contemporaneamente.
-   Le applicazioni e gli amministratori possono aggiornare la configurazione degli assembly a livello [globale](publisher-configuration.md) o per ogni [applicazione dopo](per-application-configuration.md) la distribuzione. Ad esempio, un'applicazione può essere aggiornata in modo da usare un assembly side-by-side che include un aggiornamento senza dover reinstallare l'applicazione.

 

 



