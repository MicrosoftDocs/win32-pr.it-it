---
description: Per generare un pacchetto di patch, è consigliabile utilizzare uno strumento per la creazione di patch, ad esempio Msimsp.exe e Patchwiz.dll.
ms.assetid: aca3bbd2-440a-405f-bddc-5f9cc831b811
title: Patchwiz.dll
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c6dc1135a9e2c09bb8a96e041f77bae39f0057ea
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104234025"
---
# <a name="patchwizdll"></a>Patchwiz.dll

Per generare un pacchetto di patch, è consigliabile utilizzare uno strumento per la creazione di patch, ad esempio [Msimsp.exe](msimsp-exe.md) e Patchwiz.dll. Patchwiz.dll versione 4,0 è compatibile con i pacchetti e le patch creati usando le versioni precedenti del Patchwiz.dll. Lo strumento Patchwiz.dll è disponibile solo nei [componenti Windows SDK per Windows Installer sviluppatori](platform-sdk-components-for-windows-installer-developers.md).

Patchwiz.dll versione 4,0 include una nuova funzione, [UiCreatePatchPackageEx (Patchwiz.dll)](uicreatepatchpackageex--patchwiz-dll-.md), che estende la funzionalità di [UiCreatePatchPackage (Patchwiz.dll)](uicreatepatchpackage-patchwiz-dll-.md). Queste funzioni accettano un file delle proprietà di creazione della patch (file con estensione PCP) e generano un [pacchetto di patch](patch-packages.md)del programma di installazione.

Il file con estensione PCP è un file di database binario con lo stesso formato di un database di Windows Installer (file con estensione msi), ma con uno schema di database diverso. È pertanto possibile creare un file con estensione PCP utilizzando gli stessi strumenti utilizzati per un database del programma di installazione.

È possibile creare un file con estensione PCP usando un editor di tabelle, ad esempio [Orca.exe](orca-exe.md) per immettere le informazioni nel database vuoto. PCP fornito con Windows Installer SDK, template. PCP. Per ulteriori informazioni, vedere [un esempio di patch per l'aggiornamento di piccole dimensioni](a-small-update-patching-example.md).

Le tabelle di database seguenti sono necessarie in ogni file. PCP:

-   [Tabella Properties (Patchwiz.dll)](properties-table-patchwiz-dll-.md)
-   [Tabella ImageFamilies (Patchwiz.dll)](imagefamilies-table-patchwiz-dll-.md)
-   [Tabella UpgradedImages (Patchwiz.dll)](upgradedimages-table-patchwiz-dll-.md)
-   [Tabella TargetImages (Patchwiz.dll)](targetimages-table-patchwiz-dll-.md)

Le tabelle di database seguenti sono facoltative:

-   [\_Tabella UpgradedFiles OptionalData (Patchwiz.dll)](upgradedfiles-optionaldata-table-patchwiz-dll-.md)
-   [Tabella FamilyFileRanges (Patchwiz.dll)](familyfileranges-table-patchwiz-dll-.md)
-   [\_Tabella TargetFiles OptionalData (Patchwiz.dll)](targetfiles-optionaldata-table-patchwiz-dll-.md)
-   [Tabella ExternalFiles (Patchwiz.dll)](externalfiles-table-patchwiz-dll-.md)
-   [Tabella UpgradedFilesToIgnore (Patchwiz.dll)](upgradedfilestoignore-table-patchwiz-dll-.md)

La tabella seguente è obbligatoria nei file. PCP con MinimumRequiredMsiVersion uguale a 300 nella tabella [Properties](properties-table-patchwiz-dll-.md) .

-   [Tabella PatchMetadata (Patchwiz.dll)](patchmetadata-table--patchwiz-dll-.md)

> [!Note]  
> La tabella è facoltativa se MinimumRequiredMsiVersion non è uguale a 300.

 

La versione di Patchwiz.dll rilasciata con Windows Installer 3,0 è in grado di generare automaticamente informazioni di sequenziazione delle patch e di aggiungerle alla [tabella MsiPatchSequence](msipatchsequence-table.md) di una nuova patch. La [tabella PatchSequence](patchsequence-table--patchwiz-dll-.md) può essere utilizzata per aggiungere manualmente le informazioni di sequenziazione della patch alla tabella MsiPatchSequence. Per ulteriori informazioni, vedere [generazione di informazioni sulla sequenza di patch](generating-patch-sequence-information---patchwiz-dll-.md).

A partire da Patchwiz.dll versione 2,0, è possibile aumentare la velocità della creazione di patch successiva usando [patch Information Caching (Patchwiz.dll)](patch-information-caching-patchwiz-dll-.md).

L'uso di simboli pubblici per i file binari di destinazione e di aggiornamento delle immagini può ridurre le dimensioni di una dimensione di circa una metà. Per ulteriori informazioni, vedere [utilizzo di simboli per ridurre le dimensioni della patch binaria](using-symbols-to-reduce-binary-patch-size.md).

È possibile specificare che alcune aree del file di destinazione vengano mantenute da sovrascrivere durante l'applicazione di patch e che le informazioni contenute in tali aree vengano mantenute. Per ulteriori informazioni, vedere applicazione [di patch alle aree selezionate di un file](patching-selected-regions-of-a-file.md).

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Versioni rilasciate, strumenti e ridistribuibili](released-versions-tools-and-redistributables.md)
</dt> </dl>

 

 



