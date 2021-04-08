---
description: Una patch Windows Installer (file con estensione msp) è un file usato per distribuire gli aggiornamenti alle applicazioni Windows Installer.
ms.assetid: f59736d7-0b5a-466c-ab60-f210ccccb07f
title: Pacchetti patch
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 56b4bb5b7e182c8118f5a40c45be440784b92099
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103755610"
---
# <a name="patch-packages"></a>Pacchetti patch

Una patch Windows Installer (file con estensione msp) è un file usato per distribuire gli aggiornamenti alle applicazioni Windows Installer. La patch è un pacchetto autonomo che contiene tutte le informazioni necessarie per aggiornare l'applicazione. Un pacchetto di patch (file con estensione msp) può essere molto più piccolo del pacchetto di Windows Installer (file con estensione msi) per l'intera applicazione aggiornata. Per ulteriori informazioni sulla distribuzione di aggiornamenti più piccoli alle applicazioni, vedere [riduzione delle dimensioni delle patch](reducing-patch-size.md).

Un pacchetto di patch contiene gli aggiornamenti effettivi dell'applicazione e descrive quali versioni dell'applicazione possono ricevere la patch. Le patch contengono almeno due trasformazioni di database. Una trasformazione aggiorna le informazioni nel database di installazione dell'applicazione. L'altra trasformazione aggiunge le informazioni utilizzate dal programma di installazione per l'applicazione di patch ai file. Il programma di installazione utilizza le informazioni fornite dalle trasformazioni per applicare i file di patch archiviati nel flusso di file CAB del pacchetto di patch. Un pacchetto di patch non dispone di un database come un pacchetto di installazione (file con estensione msi).

A partire da Windows Installer versione 3,0, i pacchetti di patch possono contenere informazioni che descrivono la sequenza di patch per la patch rispetto ad altri aggiornamenti nella tabella [MsiPatchSequence](msipatchsequence-table.md) e informazioni descrittive aggiuntive nella tabella [MsiPatchMetadata](msipatchmetadata-table.md) .

Gli utenti possono installare le applicazioni e gli aggiornamenti da un'immagine di amministrazione di rete. Sebbene i pacchetti di patch possano essere applicati alle installazioni amministrative, il metodo consigliato per recapitare gli aggiornamenti è quello di consentire agli utenti di installare l'applicazione originale e quindi applicare le patch all'istanza locale dell'applicazione nel computer. In questo modo gli utenti vengono sincronizzati con l'immagine amministrativa. Se viene applicata una patch all'installazione amministrativa, tutti i client dell'installazione amministrativa dovranno rimemorizzare e reinstallare l'applicazione per la ricezione dell'aggiornamento. Fino a quando un utente non memorizza nella cache e reinstalla, l'utente non è in grado di installare le installazioni su richiesta e di ripristino dall'installazione amministrativa con patch.

A partire da Windows Installer 3,0, gli utenti non amministratori possono applicare patch alle applicazioni gestite per ogni utente dopo che la patch è stata approvata come attendibile da un amministratore. Per altre informazioni su come eseguire questa operazione, vedere [applicazione di patch Per-User applicazioni gestite](patching-per-user-managed-applications.md). Un altro metodo consiste nell'usare l'applicazione di patch con privilegi minimi.

> [!Note]  
> Se è stato impostato il criterio [AllowLockdownPatch](allowlockdownpatch.md) , gli utenti non amministratori possono applicare una patch a un'applicazione esistente durante l'esecuzione di un'installazione con privilegi elevati. Questo metodo non è consigliato perché consente di applicare patch non attendibili a un'applicazione che può essere eseguita con privilegi elevati.

 

I pacchetti di patch sono costituiti dalle parti seguenti. Per ulteriori informazioni sulla costruzione di pacchetti di patch, vedere [creazione di un pacchetto di patch](creating-a-patch-package.md).

## <a name="summary-information-stream"></a>Flusso di informazioni di riepilogo

Il flusso di informazioni di riepilogo del pacchetto di patch fornisce informazioni sull'identità e lo scopo della patch.

Il flusso di informazioni di riepilogo include almeno quanto segue:

-   GUID che identifica in modo univoco la patch. Il GUID per questa patch viene aggiunto con un elenco di GUID per le patch precedenti che vengono sostituite da questa patch.
-   Elenco delimitato da punti e virgola di codici prodotto per destinazioni valide per questa patch.
-   Elenco delimitato da punti e virgola di nomi di sottoarchivi di trasformazione nell'ordine in cui devono essere elaborati.
-   Elenco di origini delimitate da punti e virgola per questa patch.

## <a name="transform-substorage"></a>Trasforma substorage

Un pacchetto di patch contiene le trasformazioni che possono aggiungere o rimuovere file, voci del registro di sistema, interfacce utente e personalizzazioni. Le trasformazioni sono incluse come sottoarchivi nel pacchetto. Un pacchetto di patch contiene due trasformazioni per ogni database di destinazione. Una trasformazione è costituita dagli aggiornamenti effettivi del database di installazione e viene generata dalle differenze tra le immagini originali e aggiornate del pacchetto di installazione. L'altra trasformazione aggiunge voci alle tabelle [patch](patch-table.md), [PacchettoPatch](patchpackage-table.md), [media](media-table.md), [InstallExecuteSequence](installexecutesequence-table.md)e [AdminExecuteSequence](adminexecutesequence-table.md) . Le informazioni contenute nell'archivio subarchiviazione lo uniscono a una specifica [**UpgradeCode**](upgradecode.md), [**ProductCode**](productcode.md), [**ProductVersion**](productversion.md)e [**ProductLanguage**](productlanguage.md). Un pacchetto di patch che può essere applicato a più destinazioni contiene più di una coppia di queste trasformazioni.

## <a name="cabinet-file-stream"></a>Flusso di file CAB

Il flusso di file cab incluso in una patch può contenere questi tipi di file:

-   Applicare patch ai file contenenti le informazioni necessarie per modificare la versione precedente del file nella nuova versione. Per aggiornare una o più versioni precedenti di un file, è possibile utilizzare un unico file di patch.
-   File aggiuntivi aggiunti all'applicazione che non sono presenti nella versione precedente.
-   Intero file di sostituzione. Nel rari casi in cui la nuova versione di un file è inferiore alla patch necessaria per aggiornare la versione precedente del file, il nuovo file può essere incluso completamente. Si tratta di nuovi file installati nelle versioni precedenti.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Creazione di un pacchetto di patch](creating-a-patch-package.md)
</dt> </dl>

 

 



