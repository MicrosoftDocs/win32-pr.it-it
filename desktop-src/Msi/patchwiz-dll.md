---
description: Per generare un pacchetto di patch, è consigliabile usare uno strumento di creazione delle patch, ad esempio Msimsp.exe e Patchwiz.dll.
ms.assetid: aca3bbd2-440a-405f-bddc-5f9cc831b811
title: Patchwiz.dll
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0de7a099a95eb6b42341b7f440f15fadb42e6a5ea8bbf69ff4d61b1fcaa28d21
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120129171"
---
# <a name="patchwizdll"></a>Patchwiz.dll

Per generare un pacchetto di patch, è consigliabile usare uno strumento di creazione delle patch, ad esempioMsimsp.exe[ e ](msimsp-exe.md) Patchwiz.dll. Patchwiz.dll versione 4.0 è compatibile con i pacchetti e le patch creati con versioni precedenti del Patchwiz.dll. Lo Patchwiz.dll è disponibile solo nei componenti dell'SDK Windows [per Windows programma di installazione.](platform-sdk-components-for-windows-installer-developers.md)

Patchwiz.dll versione 4.0 include una nuova funzione, [UiCreatePatchPackageEx (Patchwiz.dll),](uicreatepatchpackageex--patchwiz-dll-.md)che estende la funzionalità di [UiCreatePatchPackage (Patchwiz.dll).](uicreatepatchpackage-patchwiz-dll-.md) Queste funzioni accettano un file delle proprietà di creazione della patch (file con estensione pcp) e generano un pacchetto [patch del programma di installazione.](patch-packages.md)

Il file con estensione pcp è un file di database binario con lo stesso formato di un database Windows Installer (file .msi), ma con uno schema di database diverso. È quindi possibile creare un file con estensione pcp usando gli stessi strumenti usati per un database del programma di installazione.

È possibile creare un file con estensione pcp usando un editor di tabelle, ad esempio [Orca.exe,](orca-exe.md) per immettere informazioni nel database con estensione pcp vuoto fornito con Windows Installer SDK, Template.pcp. Per altre informazioni, vedere [A Small Update Patching Example](a-small-update-patching-example.md).

In ogni file con estensione pcp sono necessarie le tabelle di database seguenti:

-   [Tabella Delle proprietà (Patchwiz.dll)](properties-table-patchwiz-dll-.md)
-   [Tabella ImageFamilies (Patchwiz.dll)](imagefamilies-table-patchwiz-dll-.md)
-   [Tabella UpgradedImages (Patchwiz.dll)](upgradedimages-table-patchwiz-dll-.md)
-   [Tabella TargetImages (Patchwiz.dll)](targetimages-table-patchwiz-dll-.md)

Le tabelle di database seguenti sono facoltative:

-   [Tabella OptionalData di UpgradedFiles \_ (Patchwiz.dll)](upgradedfiles-optionaldata-table-patchwiz-dll-.md)
-   [Tabella FamilyFileRanges (Patchwiz.dll)](familyfileranges-table-patchwiz-dll-.md)
-   [Tabella TargetFiles \_ OptionalData (Patchwiz.dll)](targetfiles-optionaldata-table-patchwiz-dll-.md)
-   [Tabella ExternalFiles (Patchwiz.dll)](externalfiles-table-patchwiz-dll-.md)
-   [Tabella UpgradedFilesToIgnore (Patchwiz.dll)](upgradedfilestoignore-table-patchwiz-dll-.md)

La tabella seguente è obbligatoria nei file con estensione pcp con minimumRequiredMsiVersion uguale a 300 nella [tabella](properties-table-patchwiz-dll-.md) Properties.

-   [Tabella PatchMetadata (Patchwiz.dll)](patchmetadata-table--patchwiz-dll-.md)

> [!Note]  
> La tabella è facoltativa se MinimumRequiredMsiVersion non è uguale a 300.

 

La versione di Patchwiz.dll rilasciata con Windows Installer 3.0 può generare automaticamente le informazioni di sequenziazione delle patch e aggiungerle alla tabella [MsiPatchSequence](msipatchsequence-table.md) di una nuova patch. La [tabella PatchSequence può](patchsequence-table--patchwiz-dll-.md) essere usata per aggiungere manualmente le informazioni di sequenziazione delle patch nella tabella MsiPatchSequence. Per altre informazioni, vedere [Generazione di informazioni sulla sequenza di patch](generating-patch-sequence-information---patchwiz-dll-.md).

A partire Patchwiz.dll versione 2.0, è possibile aumentare la velocità di creazione successiva delle patch usando Patch [Information Caching (Patchwiz.dll)](patch-information-caching-patchwiz-dll-.md).

L'uso di simboli pubblici per i file binari delle immagini di destinazione e di aggiornamento può ridurre le dimensioni delle patch binarie di circa la metà. Per altre informazioni, vedere [Uso di simboli per ridurre le dimensioni delle patch binarie.](using-symbols-to-reduce-binary-patch-size.md)

È possibile specificare che determinate aree del file di destinazione non vengano sovrascritte durante l'applicazione di patch e che le informazioni in tali aree vengano mantenute. Per altre informazioni, vedere [Applicazione di patch alle aree selezionate di un file](patching-selected-regions-of-a-file.md).

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Versioni rilasciate, strumenti e ridistribuibili](released-versions-tools-and-redistributables.md)
</dt> </dl>

 

 



