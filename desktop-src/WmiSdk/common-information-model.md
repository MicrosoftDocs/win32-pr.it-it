---
description: Common Information Model (CIM) è un modello dati estensibile e orientato a oggetti che contiene informazioni relative a diverse parti di un'azienda.
ms.assetid: 3e619cb7-18a9-40ff-82fe-c10eb5090a93
ms.tgt_platform: multiple
title: Common Information Model
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5d095dfb7f05b7637ac027e6ea02eeba2e10e12845670aebd635e50e8c3265fa
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119131643"
---
# <a name="common-information-model"></a>Common Information Model

Common Information Model (CIM) è un modello dati estensibile e orientato a oggetti che contiene informazioni relative a diverse parti di un'azienda. [CIM è](https://www.dmtf.org/standards/cim) uno standard multipiattaforma gestito dalla Distributed Management Task Force[(DMTF).](https://www.dmtf.org/) Grazie a WMI, uno sviluppatore può utilizzare CIM per creare classi che rappresentino unità disco rigido, applicazioni, router di rete e persino tecnologie definite dall'utente, come un climatizzatore installato in rete. Mediante la visualizzazione e la modifica di una classe CIM, un responsabile può controllare diversi aspetti dell'azienda. Ad esempio, può eseguire una query nell'istanza di una classe CIM che rappresenta una workstation desktop e quindi eseguire uno script per modificare l'istanza della workstation CIM. WMI converte ogni modifica alla classe CIM della workstation in una modifica alla workstation effettiva.

CIM è un modello di programmazione indipendente dal linguaggio che usa tecniche orientate a oggetti per descrivere un'azienda. Usando tre livelli di ereditarietà padre/figlio, CIM può descrivere aspetti generali e specifici di un'azienda. Il CIM usa anche una tecnica denominata "associazione" per collegare tra loro diverse parti del modello Enterprise e usa schemi per distinguere ambienti di gestione diversi.

CIM è progettato per presentare una visualizzazione coerente degli oggetti logici e fisici in un ambiente di gestione. CIM rappresenta gli oggetti gestiti usando un costrutto orientato a oggetti denominato "classe". Analogamente a una classe C++ o COM, una classe CIM può includere proprietà per descrivere i dati e i metodi per descrivere il comportamento. Analogamente a un set di classi COM, il CIM non è associato ad alcuna piattaforma. TUTTAVIA, WMI include un'estensione al CIM che descrive le piattaforme del Windows microsoft.

Cim definisce tre livelli di classi:

-   Core

    Le classi di base rappresentano oggetti gestiti che si applicano a tutte le aree di gestione. Queste classi forniscono un vocabolario di base per l'analisi e la descrizione dei sistemi gestiti. Le [**\_ \_ classi Parameters**](--parameters.md) e [**\_ \_ SystemSecurity**](--systemsecurity.md) sono esempi di classi di base.

-   Comuni

    Le classi comuni rappresentano oggetti gestiti che si applicano ad aree di gestione specifiche. Tuttavia, le classi comuni sono indipendenti da una particolare implementazione o tecnologia. Le classi comuni sono un'estensione delle classi principali. La [**classe CIM \_ UnitaryComputerSystem**](/windows/desktop/CIMWin32Prov/cim-unitarycomputersystem) è un esempio di classe comune.

-   Extended

    Le classi estese rappresentano oggetti gestiti che sono aggiunte specifiche della tecnologia alle classi comuni. Una classe estesa si applica in genere a una piattaforma specifica, ad esempio UNIX o all'ambiente Microsoft Win32. La [**classe \_ ComputerSystem Win32**](/windows/desktop/CIMWin32Prov/win32-computersystem) è un esempio di classe estesa.

Uno sviluppatore può derivare una classe da un'altra classe. Una classe derivata rappresenta un caso speciale della classe padre ed eredita tutte le proprietà e i metodi dell'elemento padre. Ad esempio, [**Win32 \_ ComputerSystem**](/windows/desktop/CIMWin32Prov/win32-computersystem) eredita da [**CIM \_ UnitaryComputerSystem**](/windows/desktop/CIMWin32Prov/cim-unitarycomputersystem). Le relazioni di ereditarietà possono essere determinate usando le proprietà di sistema **\_ \_ Derivation**, **\_ \_ Dinastia** e **\_ \_ SuperClasse**. La proprietà di sistema **\_ \_ Derivation** è una matrice di stringhe che elenca l'intera catena di ereditarietà fino alla classe radice e include la classe radice, inclusa anche in **\_ \_ e**. La proprietà di sistema **\_ \_ SuperClass** mostra l'elemento padre immediato della classe corrente.

WMI supporta anche le associazioni. Un'associazione è una relazione tra due o più classi WMI diverse. Ad esempio, una workstation in esecuzione ha in genere un processore. La classe di associazione WMI [Win32 \_ ComputerSystemProcessor](/windows/desktop/CIMWin32Prov/win32-computersystemprocessor) associa la classe di workstation [**Win32 \_ ComputerSystem**](/windows/desktop/CIMWin32Prov/win32-computersystem) alla classe processore [**Win32 \_ Processor**](/windows/desktop/CIMWin32Prov/win32-processor). Tuttavia, una classe di associazione non deve associare due classi dipendenti. In realtà, lo scopo principale di una classe di associazione è mostrare le relazioni tra le classi che non dipendono necessariamente l'una dall'altra. Per altre informazioni, vedere [Dichiarazione di una classe di associazione](declaring-an-association-class.md).

Infine, WMI supporta il concetto di schemi. Nel contesto di WMI, uno schema è un gruppo di classi che descrivono un particolare ambiente di gestione. Microsoft Windows Software Development Kit (SDK) usa due schemi: lo schema CIM e lo schema Win32. I nomi delle classi dello schema CIM iniziano con [CIM \_](cimclas.md)e i nomi delle classi dello schema Win32 iniziano con [**\_ Win32**](/windows/desktop/CIMWin32Prov/win32-provider). Lo schema CIM contiene le definizioni per le classi core e comuni, mentre lo schema Win32 contiene le definizioni per le classi estese comuni all'ambiente Win32. Tuttavia, un fornitore di terze parti può creare i propri schemi per descrivere i requisiti specifici del fornitore. Poiché gli schemi sono progettati per essere infinitamente estendibili, uno sviluppatore può sempre aggiungere nuove classi per descrivere nuovi oggetti gestiti in un ambiente esistente. Per semplicità, tuttavia, la maggior parte dei fornitori sceglie di creare schemi che ereditano proprietà dagli schemi CIM o Win32.

 

 
