---
description: Common Information Model (CIM) è un modello dati estensibile e orientato a oggetti che contiene informazioni relative a diverse parti di un'azienda.
ms.assetid: 3e619cb7-18a9-40ff-82fe-c10eb5090a93
ms.tgt_platform: multiple
title: Common Information Model
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e53e4e2dc06e03a1f19b5b47ba0b94d7a866a5e4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104057957"
---
# <a name="common-information-model"></a>Common Information Model

Common Information Model (CIM) è un modello dati estensibile e orientato a oggetti che contiene informazioni relative a diverse parti di un'azienda. [CIM](https://www.dmtf.org/standards/cim) è uno standard multipiattaforma gestito da Distributed Management Task Force ([DMTF](https://www.dmtf.org/)). Grazie a WMI, uno sviluppatore può utilizzare CIM per creare classi che rappresentino unità disco rigido, applicazioni, router di rete e persino tecnologie definite dall'utente, come un climatizzatore installato in rete. Mediante la visualizzazione e la modifica di una classe CIM, un responsabile può controllare diversi aspetti dell'azienda. Ad esempio, può eseguire una query nell'istanza di una classe CIM che rappresenta una workstation desktop e quindi eseguire uno script per modificare l'istanza della workstation CIM. WMI converte ogni modifica alla classe CIM della workstation in una modifica alla workstation effettiva.

CIM è un modello di programmazione indipendente dal linguaggio che usa tecniche orientate a oggetti per descrivere un'azienda. Utilizzando tre livelli di ereditarietà padre/figlio, il CIM può descrivere aspetti generali e specifici di un'azienda. CIM usa anche una tecnica denominata "Association" per collegare diverse parti del modello Enterprise e usa gli schemi per distinguere gli ambienti di gestione diversi.

CIM è progettato per presentare una visualizzazione coerente di oggetti logici e fisici in un ambiente di gestione. Il CIM rappresenta oggetti gestiti usando un costrutto orientato a oggetti denominato "class". Analogamente a una classe C++ o COM, una classe CIM può includere proprietà per descrivere i dati e i metodi per descrivere il comportamento. Analogamente a un set di classi COM, il CIM non è associato ad alcuna piattaforma. WMI, tuttavia, include un'estensione del CIM che descrive le piattaforme del sistema operativo Microsoft Windows.

Il CIM definisce tre livelli di classi:

-   Core

    Le classi principali rappresentano oggetti gestiti che si applicano a tutte le aree di gestione. Queste classi forniscono un vocabolario di base per l'analisi e la descrizione dei sistemi gestiti. I [**\_ \_ parametri**](--parameters.md) e le classi [**\_ \_ SystemSecurity**](--systemsecurity.md) sono esempi di classi principali.

-   Comuni

    Le classi comuni rappresentano oggetti gestiti che si applicano a aree di gestione specifiche. Tuttavia, le classi comuni sono indipendenti da un'implementazione o una tecnologia particolare. Le classi comuni sono un'estensione delle classi principali. La classe [**CIM \_ UnitaryComputerSystem**](/windows/desktop/CIMWin32Prov/cim-unitarycomputersystem) è un esempio di classe comune.

-   Extended

    Le classi estese rappresentano oggetti gestiti che sono aggiunte specifiche della tecnologia alle classi comuni. Una classe estesa si applica in genere a una piattaforma specifica, ad esempio UNIX o l'ambiente Microsoft Win32. La classe [**Win32 \_ ComputerSystem**](/windows/desktop/CIMWin32Prov/win32-computersystem) è un esempio di classe estesa.

Uno sviluppatore può derivare una classe da un'altra classe. Una classe derivata rappresenta un caso speciale della classe padre ed eredita tutte le proprietà e i metodi dell'elemento padre. Ad esempio, [**Win32 \_ ComputerSystem**](/windows/desktop/CIMWin32Prov/win32-computersystem) eredita da [**CIM \_ UnitaryComputerSystem**](/windows/desktop/CIMWin32Prov/cim-unitarycomputersystem). Le relazioni di ereditarietà possono essere determinate usando le proprietà di sistema **\_ \_ derivazione**, **\_ \_ dinastia** e **\_ \_ superclasse**. La proprietà del sistema di **\_ \_ derivazione** è una matrice di stringhe che elenca l'intera catena di ereditarietà fino alla classe radice, inclusa anche in **\_ \_ Dynasty**. La proprietà di sistema **\_ \_ superclass** Mostra l'elemento padre diretto della classe corrente.

WMI supporta inoltre le associazioni. Un'associazione è una relazione tra due o più classi WMI diverse. Una workstation in esecuzione, ad esempio, ha in genere un processore. La classe di associazione WMI [Win32 \_ ComputerSystemProcessor](/windows/desktop/CIMWin32Prov/win32-computersystemprocessor) associa la classe workstation [**Win32 \_ ComputerSystem**](/windows/desktop/CIMWin32Prov/win32-computersystem) al [**\_ processore Win32**](/windows/desktop/CIMWin32Prov/win32-processor)della classe Processor. Tuttavia, una classe di associazione non deve associare due classi dipendenti. Infatti, lo scopo principale di una classe di associazione è mostrare le relazioni tra le classi che non sono necessariamente dipendenti tra loro. Per ulteriori informazioni, vedere [dichiarazione di una classe di associazione](declaring-an-association-class.md).

Infine, WMI supporta il concetto di schemi. Nel contesto di WMI, uno schema è un gruppo di classi che descrivono un particolare ambiente di gestione. Il Software Development Kit (SDK) di Microsoft Windows utilizza due schemi: lo schema CIM e lo schema Win32. I nomi delle classi dello schema CIM iniziano con [CIM \_](cimclas.md)e i nomi delle classi dello schema Win32 iniziano con [**Win32 \_**](/windows/desktop/CIMWin32Prov/win32-provider). Nello schema CIM sono contenute le definizioni per le classi di base e comuni, mentre lo schema Win32 contiene le definizioni per le classi estese comuni all'ambiente Win32. Tuttavia, un fornitore di terze parti può creare schemi personalizzati per descrivere i requisiti specifici del fornitore. Poiché gli schemi sono progettati per essere illimitatamente estendibili, uno sviluppatore può sempre aggiungere nuove classi per descrivere nuovi oggetti gestiti in un ambiente esistente. Per semplicità, tuttavia, la maggior parte dei fornitori sceglie di creare schemi che ereditano proprietà dagli schemi CIM o Win32.

 

 
