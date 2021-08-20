---
description: Le informazioni contenute in questo argomento identificano le linee guida consigliate per l'aggiornamento degli assembly Windows patch del programma di installazione.
ms.assetid: 60c70d48-aae2-4ea5-a880-ac9e2c83c28c
title: Aggiornamento degli assembly
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a65467613206f3736f35852a919432b11a6761860bd0db22c6da2600c159ef0f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118141624"
---
# <a name="updating-assemblies"></a>Aggiornamento degli assembly

Le informazioni contenute in questo argomento identificano le linee guida consigliate per l'aggiornamento degli assembly Windows patch del programma di installazione.

Gli autori degli aggiornamenti degli assembly possono usare le linee guida seguenti, applicabili a tutti i tipi di assembly:

-   Il metodo consigliato per l'aggiornamento di un assembly è la modifica del nome sicuro dell'assembly nella [tabella MsiAssemblyName](msiassemblyname-table.md). La nuova versione dell'assembly può essere fornita da un nuovo componente o dallo stesso componente che fornisce la versione precedente.
-   Se la nuova versione dell'assembly viene fornita dallo stesso componente, non modificare il tipo di assembly da un assembly .NET Framework a un assembly Win32 o viceversa.
-   Se tutte le applicazioni nel sistema devono usare l'assembly aggiornato, è necessario distribuire un assembly dei criteri. Un assembly di criteri può reindirizzare le applicazioni nel sistema per usare la nuova versione dell'assembly. Gli assembly dei criteri devono essere forniti creando un nuovo componente.
-   Windows Il programma di installazione 3.0 o versione successiva è necessario per disinstallare gli aggiornamenti degli assembly. Per altre informazioni, vedere [Rimozione di patch.](removing-patches.md)
-   La versione più recente dell'assembly deve contenere la stessa versione o versioni successive dei file degli assembly rilasciati in precedenza.
-   Windows Il programma di installazione 3.0 può .NET Framework e gli assembly Win32 tramite una sostituzione completa dei file o un aggiornamento differenziale più piccolo. Per altre informazioni, vedere Riduzione [delle dimensioni delle patch.](reducing-patch-size.md)
-   Se l'aggiornamento modifica il nome sicuro dell'assembly, la tabella [MsiPatchOldAssemblyFile](msipatcholdassemblyfile-table.md) e la tabella [MsiPatchOldAssemblyName](msipatcholdassemblyname-table.md) sono necessarie se il pacchetto di patch non dispone di una tabella [MsiPatchSequence.](msipatchsequence-table.md) La tabella MsiPatchOldAssemblyFile e la tabella MsiPatchOldAssemblyName non sono necessarie se il pacchetto patch contiene informazioni di sequenziazione delle patch in una tabella MsiPatchSequence.
-   Prima di rilasciare una nuova patch, testarla applicandola con tutte le patch rilasciate in precedenza.

## <a name="updating-win32-assemblies"></a>Aggiornamento di assembly Win32

Quando si aggiornano assembly Win32, usare le linee guida seguenti:

-   Modificare il nome sicuro del nuovo assembly specificato nella [tabella MsiAssemblyName](msiassemblyname-table.md).
-   Se si vuole che l'applicazione usi sempre la nuova versione dell'assembly senza influire sulla versione dell'assembly usata da altre applicazioni nel sistema, usare lo stesso componente per contenere la nuova versione dell'assembly usata per la versione precedente dell'assembly. Mantenere lo stesso ComponentId nella [tabella Component.](component-table.md) Dopo l'applicazione di patch, l'applicazione contiene solo un riferimento alla nuova versione dell'assembly. La versione precedente dell'assembly può rimanere con la nuova versione nella Global Assembly Cache. Ciò non influisce sulle altre applicazioni nel sistema che usano la versione precedente dell'assembly. Quando lo stesso componente viene usato sia per le versioni nuove che per le versioni precedenti dell'assembly, l'aggiornamento può essere una patch delta più piccola.
-   Se la nuova versione dell'assembly non è compatibile con tutti i sistemi in cui si vuole installare l'applicazione, è possibile installare le versioni nuove e precedenti dell'assembly come assembly side-by-side. Per installare entrambe le versioni degli assembly side-by-side, creare un nuovo componente che contenga la nuova versione dell'assembly. ComponentId nella tabella [Component](component-table.md) per il nuovo componente deve essere diverso da ComponentId del componente con la versione precedente. Dopo l'applicazione di patch, l'applicazione contiene riferimenti a entrambe le versioni dell'assembly. L'applicazione può quindi essere indirizzata alla versione compatibile dell'assembly da un manifesto. Quando vengono usati componenti diversi per le versioni nuove e precedenti dell'assembly, l'aggiornamento usa la sostituzione completa dei file.

## <a name="updating-net-framework-assemblies"></a>Aggiornamento .NET Framework assembly

Usare le linee guida seguenti quando si aggiornano .NET Framework assembly.

-   Modificare il nome sicuro del nuovo assembly specificato nella [tabella MsiAssemblyName](msiassemblyname-table.md).
-   Se si vuole che l'applicazione usi sempre la nuova versione dell'assembly senza influire sulla versione dell'assembly usata da altre applicazioni nel sistema, modificare il nome sicuro del nuovo assembly specificato nella tabella [MsiAssemblyName](msiassemblyname-table.md)e usare lo stesso componente per contenere la nuova versione dell'assembly usata per la versione precedente dell'assembly. Mantenere lo stesso ComponentId nella [tabella Component.](component-table.md) Dopo l'applicazione di patch, l'applicazione contiene solo un riferimento alla nuova versione dell'assembly. La versione precedente dell'assembly può rimanere con la nuova versione nella cache globale. Ciò non influisce sulle altre applicazioni nel sistema che usano la versione precedente dell'assembly. Quando lo stesso componente viene usato sia per le versioni nuove che per le versioni precedenti dell'assembly, l'aggiornamento può essere una patch delta più piccola.
-   Se la nuova versione dell'assembly non è compatibile con tutti i sistemi in cui si vuole installare l'applicazione, è possibile installare le versioni nuove e precedenti dell'assembly come assembly side-by-side. Per installare entrambe le versioni degli assembly side-by-side, modificare il nome sicuro del nuovo assembly specificato nella tabella [MsiAssemblyName](msiassemblyname-table.md)e creare un nuovo componente che contenga la nuova versione dell'assembly. ComponentId nella tabella [Component](component-table.md) per il nuovo componente deve essere diverso da ComponentId del componente con la versione precedente. Dopo l'applicazione di patch, l'applicazione contiene riferimenti a entrambe le versioni dell'assembly. L'applicazione può quindi essere indirizzata alla versione compatibile dell'assembly da un manifesto. Quando vengono usati componenti diversi per le versioni nuove e precedenti dell'assembly, l'aggiornamento usa la sostituzione completa dei file.
-   Un aggiornamento sul posto sovrascrive la copia di un .NET Framework assembly nella Global Assembly Cache. Questo tipo di aggiornamento dell'assembly non modifica il nome sicuro dell'assembly. Viene modificato solo il valore nel campo FileVersion [della tabella MsiAssemblyName.](msiassemblyname-table.md) L'aggiornamento sul posto di un assembly .NET Framework richiede .NET Framework 1.1 SP1 o versione successiva.
    > [!Note]  
    > Il tipo di aggiornamento sul posto sovrascrive la copia dell'assembly nella global cache e può interrompere altre applicazioni se la nuova versione dell'assembly non è completamente compatibile con le versioni precedenti. Il metodo consigliato per l'aggiornamento di un assembly è la modifica del nome sicuro dell'assembly nella [tabella MsiAssemblyName](msiassemblyname-table.md).

     

 

 



