---
description: Le informazioni contenute in questo argomento identificano le linee guida consigliate per l'aggiornamento degli assembly mediante Windows Installer patch.
ms.assetid: 60c70d48-aae2-4ea5-a880-ac9e2c83c28c
title: Aggiornamento degli assembly
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 35b185a9943ba20c81a1fa3431dd590eb05648c9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104058353"
---
# <a name="updating-assemblies"></a>Aggiornamento degli assembly

Le informazioni contenute in questo argomento identificano le linee guida consigliate per l'aggiornamento degli assembly mediante Windows Installer patch.

Gli autori degli aggiornamenti degli assembly possono utilizzare le linee guida seguenti, applicabili a tutti i tipi di assembly:

-   Il metodo consigliato per l'aggiornamento di un assembly consiste nel modificare il nome sicuro dell'assembly nella [tabella MsiAssemblyName](msiassemblyname-table.md). La nuova versione dell'assembly può essere fornita da un nuovo componente o dallo stesso componente che fornisce la versione precedente.
-   Se la nuova versione dell'assembly viene fornita dallo stesso componente, non modificare il tipo di assembly da un assembly .NET Framework a un assembly Win32 o viceversa.
-   Se tutte le applicazioni nel sistema devono utilizzare l'assembly aggiornato, è necessario distribuire un assembly dei criteri. Un assembly di criteri può reindirizzare le applicazioni nel sistema per utilizzare la nuova versione dell'assembly. Gli assembly di criteri devono essere forniti creando un nuovo componente.
-   Per disinstallare gli aggiornamenti degli assembly è necessario Windows Installer 3,0 o versione successiva. Per altre informazioni, vedere [rimozione di patch](removing-patches.md).
-   La versione più recente dell'assembly deve contenere le stesse versioni di file o versioni successive di assembly rilasciati in precedenza.
-   Windows Installer 3,0 può servire .NET Framework e assembly Win32 mediante una sostituzione completa dei file o un aggiornamento delta più piccolo. Per altre informazioni, vedere [riduzione delle dimensioni delle patch](reducing-patch-size.md).
-   Se l'aggiornamento modifica il nome sicuro dell'assembly, la tabella [MsiPatchOldAssemblyFile](msipatcholdassemblyfile-table.md) e la tabella [MsiPatchOldAssemblyName](msipatcholdassemblyname-table.md) sono obbligatorie se per il pacchetto di patch non è presente una tabella [MsiPatchSequence](msipatchsequence-table.md) . La tabella MsiPatchOldAssemblyFile e la tabella MsiPatchOldAssemblyName non sono necessarie se il pacchetto di patch contiene informazioni di sequenziazione delle patch in una tabella MsiPatchSequence.
-   Prima di rilasciare una nuova patch, testare la patch applicando l'applicazione a tutte le patch rilasciate in precedenza.

## <a name="updating-win32-assemblies"></a>Aggiornamento degli assembly Win32

Quando si aggiornano gli assembly Win32, attenersi alle seguenti linee guida:

-   Modificare il nome sicuro del nuovo assembly specificato nella [tabella MsiAssemblyName](msiassemblyname-table.md).
-   Se si desidera che l'applicazione utilizzi sempre la nuova versione dell'assembly senza influire sulla versione dell'assembly utilizzata da altre applicazioni nel sistema, utilizzare lo stesso componente per contenere la nuova versione dell'assembly utilizzata per la versione precedente dell'assembly. Mantiene lo stesso ComponentId nella tabella dei [componenti](component-table.md) . Dopo che l'applicazione è stata applicata alla patch, esso include solo un riferimento alla nuova versione dell'assembly. La versione precedente dell'assembly può rimanere con la nuova versione nella Global Assembly Cache. Questo non influisce sulle altre applicazioni del sistema che usano la versione precedente dell'assembly. Quando si usa lo stesso componente per le versioni nuove e precedenti dell'assembly, l'aggiornamento può essere una patch Delta più piccola.
-   Se la nuova versione dell'assembly non è compatibile con tutti i sistemi in cui si desidera installare l'applicazione, è possibile installare le versioni nuove e precedenti dell'assembly come assembly side-by-side. Per installare entrambe le versioni di assembly side-by-Side, creare un nuovo componente per contenere la nuova versione dell'assembly. Il ComponentId nella tabella dei [componenti](component-table.md) per il nuovo componente deve essere diverso da quello della ComponentID del componente con la versione precedente. Dopo che l'applicazione è stata applicata a patch, include riferimenti a entrambe le versioni degli assembly. L'applicazione può quindi essere indirizzata alla versione compatibile dell'assembly da un manifesto. Quando vengono usati componenti diversi per le versioni nuove e precedenti dell'assembly, l'aggiornamento usa la sostituzione completa dei file.

## <a name="updating-net-framework-assemblies"></a>Aggiornamento di assembly .NET Framework

Usare le linee guida seguenti quando si aggiornano .NET Framework assembly.

-   Modificare il nome sicuro del nuovo assembly specificato nella [tabella MsiAssemblyName](msiassemblyname-table.md).
-   Se si desidera che l'applicazione utilizzi sempre la nuova versione dell'assembly senza influire sulla versione dell'assembly utilizzata da altre applicazioni nel sistema, modificare il nome sicuro del nuovo assembly specificato nella [tabella MsiAssemblyName](msiassemblyname-table.md)e utilizzare lo stesso componente per contenere la nuova versione dell'assembly utilizzata per la versione precedente dell'assembly. Mantiene lo stesso ComponentId nella tabella dei [componenti](component-table.md) . Dopo che l'applicazione è stata applicata alla patch, esso include solo un riferimento alla nuova versione dell'assembly. La versione precedente dell'assembly può rimanere con la nuova versione nella global assembly cache. Questo non influisce sulle altre applicazioni del sistema che usano la versione precedente dell'assembly. Quando si usa lo stesso componente per le versioni nuove e precedenti dell'assembly, l'aggiornamento può essere una patch Delta più piccola.
-   Se la nuova versione dell'assembly non è compatibile con tutti i sistemi in cui si desidera installare l'applicazione, è possibile installare le versioni nuove e precedenti dell'assembly come assembly side-by-side. Per installare entrambe le versioni di assembly side-by-Side, modificare il nome sicuro del nuovo assembly specificato nella [tabella MsiAssemblyName](msiassemblyname-table.md)e creare un nuovo componente che contenga la nuova versione dell'assembly. Il ComponentId nella tabella dei [componenti](component-table.md) per il nuovo componente deve essere diverso da quello di ComponentID del componente con la versione precedente. Dopo che l'applicazione è stata applicata a patch, include riferimenti a entrambe le versioni degli assembly. L'applicazione può quindi essere indirizzata alla versione compatibile dell'assembly da un manifesto. Quando vengono usati componenti diversi per le versioni nuove e precedenti dell'assembly, l'aggiornamento usa la sostituzione completa dei file.
-   Un aggiornamento sul posto sovrascrive la copia di un assembly .NET Framework nel Global Assembly Cache. Questo tipo di aggiornamento dell'assembly non modifica il nome sicuro dell'assembly. Viene modificato solo il valore nel campo FileVersion della [tabella MsiAssemblyName](msiassemblyname-table.md) . L'aggiornamento sul posto di un assembly di .NET Framework richiede .NET Framework 1,1 SP1 o versione successiva.
    > [!Note]  
    > Il tipo di aggiornamento sul posto sovrascrive la copia dell'assembly nella cache globale e può interrompere altre applicazioni se la nuova versione dell'assembly non è completamente compatibile con le versioni precedenti. Il metodo consigliato per l'aggiornamento di un assembly consiste nel modificare il nome sicuro dell'assembly nella [tabella MsiAssemblyName](msiassemblyname-table.md).

     

 

 



