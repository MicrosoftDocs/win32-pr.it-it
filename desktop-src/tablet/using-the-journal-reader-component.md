---
description: Il componente Microsoft Windows Journal Note Reader fornisce l'accesso in lettura a livello di codice ai file in formato Journal.
ms.assetid: 85dcda59-2972-48e3-a9f5-5cce0b60a1f1
title: Utilizzo del componente lettore journal
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 41559ac31ff081ecb810b0fe6e82ce1107ed87dae897cc7e6b8be4569e9b78f4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118449192"
---
# <a name="using-the-journal-reader-component"></a>Utilizzo del componente lettore journal

Il componente Microsoft Windows Journal Note Reader fornisce l'accesso in lettura a livello di codice ai file in formato Journal.

## <a name="component-overview"></a>Cenni preliminari sui componenti

I file journal hanno l'estensione jnt. Questo componente semplice accetta un flusso contenente un file con estensione jnt e restituisce un flusso contenente il contenuto del file in formato XML. Il codice XML restituito dal componente è conforme allo schema journal note reader. Questo schema è documentato in Journal Reader Schema Reference (Informazioni [di riferimento sullo schema del lettore journal).](journal-reader-schema-reference.md)

Il componente non consente di scrivere file con estensione jnt.

Il componente è disponibile nelle versioni non gestite e gestite. Il componente non gestito è disponibile nella journal.dll di collegamento dinamico (DLL). La versione gestita si trova nell'assembly Microsoft.Ink.Journal.dll (per la ridistribuzione a Windows XP Tablet PC Edition o Windows Vista) o Microsoft.Ink.dll.

> [!IMPORTANT]
>
> A partire Windows 10 versione 1607, journal.dll non è incluso nel Windows operativo. Tale libreria deve essere considerata deprecata o obsoleta e non deve essere usata.

 

### <a name="assembly-changes-of-note"></a>Modifiche all'assembly della nota

È importante tenere presenti alcune modifiche all'assembly contenente il componente Journal Note Reader che si sono verificate tra la versione rilasciata in combinazione con la versione 1.7 di Tablet Developers Kit e la versione fornita nel sistema operativo Windows Vista.

La versione 1.7 del componente reader, che può essere ridistribuito in Windows XP o Windows Vista, è contenuta in un assembly denominato Microsoft.Ink.Journal.dll. Il componente lettore viene fornito in Windows Vista, ma è stato integrato nell'assembly Microsoft.Ink.dll core. Ciò significa che le applicazioni che usano l'assembly 1.7 devono ridistribuire l'assembly con la relativa configurazione.

## <a name="using-the-component"></a>Uso del componente

Il componente Lettore note journal è utile per estrarre i dati dell'input penna e altre informazioni sul file da un file journal.

### <a name="com"></a>COM

Il componente COM Journal Note Reader si trova nel file Journal.dll, che viene installato e registrato quando si scarica ed esegue il file di installazione journal note reader.

Il componente COM non supporta [**l'interfaccia IDispatch.**](/windows/win32/api/oaidl/nn-oaidl-idispatch)

### <a name="managed"></a>Gestita

Il componente gestito Journal Note Reader si trova nellMicrosoft.Ink.JournalReader.dll assembly. Questo assembly viene installato e registrato nella Global Assembly Cache quando si esegue il file di installazione journal note reader.

Aggiungere un riferimento all'assembly per usarlo nel progetto gestito.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Interfaccia IJournalReader**](ijournalreader.md)
</dt> <dt>

[Informazioni di riferimento sullo schema del lettore journal](journal-reader-schema-reference.md)
</dt> </dl>

 

 
