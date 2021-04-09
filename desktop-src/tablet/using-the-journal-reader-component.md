---
description: Il componente lettore note Microsoft Windows Journal fornisce l'accesso in lettura a livello di codice ai file nel formato journal.
ms.assetid: 85dcda59-2972-48e3-a9f5-5cce0b60a1f1
title: Utilizzo del componente Reader Journal
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 48fd098db4ce1c0c92a5ded76b0950e264aa2a73
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103966649"
---
# <a name="using-the-journal-reader-component"></a>Utilizzo del componente Reader Journal

Il componente lettore note Microsoft Windows Journal fornisce l'accesso in lettura a livello di codice ai file nel formato journal.

## <a name="component-overview"></a>Panoramica sui componenti

File journal con estensione JNT. Questo componente semplice accetta un flusso contenente un file con estensione JNT e restituisce un flusso contenente il contenuto del file in formato XML. Il codice XML restituito dal componente è conforme allo schema del lettore di note del journal. Questo schema è documentato in [Journal Reader Schema Reference](journal-reader-schema-reference.md).

Il componente non offre la possibilità di scrivere file con estensione JNT.

Il componente è disponibile nelle versioni gestite e non gestite. Il componente non gestito è disponibile nella libreria a collegamento dinamico (DLL) di journal.dll. La versione gestita è nell'assembly Microsoft.Ink.Journal.dll (per la ridistribuzione a Windows XP Tablet PC Edition o Windows Vista) o Microsoft.Ink.dll.

> [!IMPORTANT]
>
> A partire da Windows 10, versione 1607, journal.dll non è incluso nel sistema operativo Windows. Tale libreria deve essere considerata deprecata o obsoleta e non deve essere utilizzata.

 

### <a name="assembly-changes-of-note"></a>Modifiche all'assembly della nota

È importante tenere presente alcune modifiche apportate all'assembly contenente il componente Reader note Journal che si è verificato tra la versione rilasciata in combinazione con la versione 1,7 del kit per sviluppatori di Tablet e la versione fornita nel sistema operativo Windows Vista.

La versione 1,7 del componente Reader, che può essere ridistribuita in Windows XP o Windows Vista, è contenuta in un assembly denominato Microsoft.Ink.Journal.dll. Il componente Reader è incluso in Windows Vista, ma è stato integrato nell'assembly di base Microsoft.Ink.dll. Ciò significa che le applicazioni che usano l'assembly 1,7 devono ridistribuire l'assembly con la relativa configurazione.

## <a name="using-the-component"></a>Utilizzo del componente

Il componente Reader note Journal è utile per estrarre i dati di input penna e altre informazioni sul file da un file journal.

### <a name="com"></a>COM

Il componente COM Journal note Reader si trova nel file Journal.dll, che viene installato e registrato quando si scarica e si esegue il file di installazione Journal note Reader.

Il componente COM non supporta l'interfaccia [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) .

### <a name="managed"></a>Gestita

Il componente del Journal note Reader gestito si trova nell'assembly Microsoft.Ink.JournalReader.dll. Questo assembly viene installato e registrato nella Global Assembly Cache quando si esegue il file di installazione Journal note Reader.

Aggiungere un riferimento all'assembly per utilizzarlo nel progetto gestito.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Interfaccia IJournalReader**](ijournalreader.md)
</dt> <dt>

[Riferimento allo schema del lettore Journal](journal-reader-schema-reference.md)
</dt> </dl>

 

 
