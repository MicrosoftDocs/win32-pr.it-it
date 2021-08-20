---
description: Le funzioni, le tabelle e le proprietà del programma di installazione di Windows elencate in questa pagina non sono supportate da Windows Installer&\# 160;2.0 e versioni precedenti.
ms.assetid: 850b598a-338e-4f84-8336-01e962256a08
title: Non supportato in Windows Installer 2.0
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7d244dc962e65bb017dbd5fb56c7fda644b46524df7890ede7b71bf0bdf8ad66
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120074861"
---
# <a name="not-supported-in-windows-installer-20"></a>Non supportato in Windows Installer 2.0

Le Windows installer, le tabelle e le proprietà elencate in questa pagina non sono supportate da Windows Installer 2.0 e versioni precedenti. L'assenza di una funzionalità da questo elenco non garantisce che la funzionalità sia supportata. Vedere la documentazione principale per determinare quale Windows del programma di installazione è necessaria per una particolare funzionalità. Per informazioni su altre versioni Windows Installer, vedere [Novità di Windows Installer.](what-s-new-in-windows-installer.md)

Windows Il programma di installazione 2.0 può essere eseguito in Microsoft Windows 2000, Microsoft Windows XP o Windows Server 2003. Per un elenco di tutte le versioni Windows Installer, vedere [Versioni rilasciate di Windows Installer.](released-versions-of-windows-installer.md)

Le funzionalità seguenti non sono supportate in Windows Installer 2.0 e versioni precedenti.

[Funzioni del programma di installazione](installer-functions.md)

-   [**MsiRemovePatches**](/windows/desktop/api/Msi/nf-msi-msiremovepatchesa)
-   [**MsiDeterminePatchSequence**](/windows/desktop/api/Msi/nf-msi-msideterminepatchsequencea)
-   [**MsiApplyMultiplePatches**](/windows/desktop/api/Msi/nf-msi-msiapplymultiplepatchesa)
-   [**MsiEnumPatchesEx**](/windows/desktop/api/Msi/nf-msi-msienumpatchesexa)
-   [**MsiGetPatchInfoEx**](/windows/desktop/api/Msi/nf-msi-msigetpatchinfoexa)
-   [**MsiEnumProductsEx**](/windows/desktop/api/Msi/nf-msi-msienumproductsexa)
-   [**MsiGetProductInfoEx**](/windows/desktop/api/Msi/nf-msi-msigetproductinfoexa)
-   [**MsiQueryFeatureStateEx**](/windows/desktop/api/Msi/nf-msi-msiqueryfeaturestateexa)
-   [**MsiQueryComponentState**](/windows/desktop/api/Msi/nf-msi-msiquerycomponentstatea)
-   [**MsiExtractPatchXMLData**](/windows/desktop/api/Msi/nf-msi-msiextractpatchxmldataa)
-   [**MsiDetermineApplicablePatches**](/windows/desktop/api/Msi/nf-msi-msidetermineapplicablepatchesa)
-   [**MsiSourceListEnumSources**](/windows/desktop/api/Msi/nf-msi-msisourcelistenumsourcesa)
-   [**MsiSourceListAddSourceEx**](/windows/desktop/api/Msi/nf-msi-msisourcelistaddsourceexa)
-   [**MsiSourceListClearSource**](/windows/desktop/api/Msi/nf-msi-msisourcelistclearsourcea)
-   [**MsiSourceListClearAllEx**](/windows/desktop/api/Msi/nf-msi-msisourcelistclearallexa)
-   [**MsiSourceListForceResolutionEx**](/windows/desktop/api/Msi/nf-msi-msisourcelistforceresolutionexa)
-   [**MsiSourceListGetInfo**](/windows/desktop/api/Msi/nf-msi-msisourcelistgetinfoa)
-   [**MsiSourceListSetInfo**](/windows/desktop/api/Msi/nf-msi-msisourcelistsetinfoa)
-   [**MsiSourceListEnumMediaDisks**](/windows/desktop/api/Msi/nf-msi-msisourcelistenummediadisksa)
-   [**MsiSourceListAddMediaDisk**](/windows/desktop/api/Msi/nf-msi-msisourcelistaddmediadiska)
-   [**MsiSourceListClearMediaDisk**](/windows/desktop/api/Msi/nf-msi-msisourcelistclearmediadiska)

[Windows Strutture del programma di installazione](installer-structures.md)

-   [**MSIPATCHSEQUENCEINFO**](/windows/win32/api/msi/ns-msi-msipatchsequenceinfoa)

[Tabelle di database](database-tables.md)

-   [MsiPatchCertificate](msipatchcertificate-table.md)
-   [MsiPatchSequence](msipatchsequence-table.md)
-   [MsiPatchMetadata](msipatchmetadata-table.md)

[Proprietà](properties.md)

-   [**MSIDISABLELUAPATCHING**](msidisableluapatching.md)
-   [**MSIENFORCEUPGRADECOMPONENTRULES**](msienforceupgradecomponentrules.md)
-   [**MSIPATCHREMOVE**](msipatchremove.md)
-   [**MsiPatchRemovalList**](msipatchremovallist.md)
-   [**MsiUISourceResOnly**](msiuisourceresonly.md)
-   [**MsiUIHideCancel**](msiuihidecancel.md)
-   [**MsiUIProgressOnly**](msiuiprogressonly.md)

[Criteri di sistema](system-policy.md)

-   [DisableLUAPatching](disableluapatching.md)
-   [DisablePatchUninstall](disablepatchuninstall.md)
-   [DisableFlyWeightPatching](disableflyweightpatching.md)
-   [EnforceUpgradeComponentRules](enforceupgradecomponentrules.md)
-   [MaxPatchCacheSize](maxpatchcachesize.md)

[Codici errore](error-codes.md)

-   RIMOZIONE \_ DELLA PATCH DI ERRORE NON \_ \_ SUPPORTATA
-   ERRORE \_ PATCH \_ SCONOSCIUTA
-   ERRORE \_ PATCH \_ NESSUNA \_ SEQUENZA
-   RIMOZIONE \_ PATCH DI ERRORE NON \_ \_ CONSENTITA
-   ERRORE XML \_ \_ PATCH NON \_ VALIDO
-   PATCH \_ DI ERRORE PRODOTTO ANNUNCIATO \_ \_ \_ GESTITO

Modalità di registrazione

-   [**INSTALLLOGMODE \_ LOGONLYONERROR**](/windows/desktop/api/Msi/nf-msi-msienableloga)

[Interfaccia di automazione](automation-interface.md)

-   Proprietà [ **dell'oggetto Product**](product-object.md)

    -   [**Product.UserSid**](product-usersid.md)
    -   [**Product.Sources**](product-sources.md)
    -   [**Product.MediaDisks**](product-mediadisks.md)
    -   [**Product.FeatureState**](product-featurestate.md)
    -   [**Product.Context**](product-context.md)
    -   [**Product.InstallProperty**](product-installproperty.md)
    -   [**Product.ProductCode**](product-productcode.md)
    -   [**Product.ComponentState**](product-componentstate.md)
    -   [**Product.State**](product-state.md)
    -   [**Product.SourceListInfo**](product-sourcelistinfo.md)

-   Metodi [ **dell'oggetto Product**](product-object.md)

    -   [**Product.SourceListForceResolution**](product-sourcelistforceresolution.md)
    -   [**Product.SourceListClearMediaDisk**](product-sourcelistclearmediadisk.md)
    -   [**Product.SourceListClearAll**](product-sourcelistclearall.md)
    -   [**Product.SourceListClearSource**](product-sourcelistclearsource.md)
    -   [**Product.SourceListAddSource**](product-sourcelistaddsource.md)
    -   [**Product.SourceListAddMediaDisk**](product-sourcelistaddmediadisk.md)

-   Proprietà [ **dell'oggetto Patch**](patch-object.md)

    -   [**Patch.UserSid**](patch-usersid.md)
    -   [**Patch.State**](patch-state.md)
    -   [**Patch.Sources**](patch-sources.md)
    -   [**Patch.SourceListInfo**](patch-sourcelistinfo.md)
    -   [**Patch.ProductCode**](patch-productcode.md)
    -   [**Patch.PatchProperty**](patch-patchproperty.md)
    -   [**Patch.PatchCode**](patch-patchcode.md)
    -   [**Patch.MediaDisks**](patch-mediadisks.md)
    -   [**Patch.Context**](patch-context.md)

-   Metodi [ **dell'oggetto Patch**](patch-object.md)

    -   [**Patch.SourceListForceResolution**](patch-sourcelistforceresolution.md)
    -   [**Patch.SourceListClearAll**](patch-sourcelistclearall.md)
    -   [**Patch.SourceListClearSource**](patch-sourcelistclearsource.md)
    -   [**Patch.SourceListClearMediaDisk**](patch-sourcelistclearmediadisk.md)
    -   [**Patch.SourceListAddSource**](patch-sourcelistaddsource.md)
    -   [**Patch.SourceListAddMediaDisk**](patch-sourcelistaddmediadisk.md)

-   Proprietà [ **dell'oggetto Installer**](installer-object.md)

    -   [**Installer.ProductsEx**](installer-productsex.md)
    -   [**Installer.ProductInfo**](installer-productinfo.md)
    -   [**Installer.PatchesEx**](installer-patchesex.md)

-   Metodi [ **dell'oggetto Installer**](installer-object.md)

    -   [**Installer.ApplyMultiplePatches**](installer-applymultiplepatches.md)
    -   [**Installer.ApplyPatch**](installer-applypatch.md)
    -   [**Installer.RemovePatches**](installer-removepatches.md)
    -   [**Installer.ExtractPatchXMLData**](installer-extractpatchxmldata.md)

Anche le funzionalità seguenti non sono supportate in Windows Installer versione 2.0.2600. Windows Il programma di installazione versione 2.0.2600 è stato rilasciato con Windows XP e Windows 2000 Server. Le funzionalità sono disponibili a partire da Windows Installer versione 2.0.3790 rilasciata con Windows Server 2003. Per un elenco di tutte le versioni Windows Installer, vedere [Versioni rilasciate di Windows Installer.](released-versions-of-windows-installer.md)

[Funzioni del programma di installazione](installer-functions.md)

-   [**MsiAdvertiseProductEx**](/windows/desktop/api/Msi/nf-msi-msiadvertiseproductexa)
    -   ISTANZA DI MSIADVERTISEOPTIONS \_
-   [**MsiApplyPatch**](/windows/desktop/api/Msi/nf-msi-msiapplypatcha)
-   [**MsiGetProductInfo**](/windows/desktop/api/Msi/nf-msi-msigetproductinfoa)

[Interfaccia di automazione](automation-interface.md)

-   Metodi [ **dell'oggetto Installer**](installer-object.md)

    -   [**Installer.ApplyPatch**](installer-applypatch.md)
    -   [**Installer.ProductInfo**](installer-productinfo.md)

[Proprietà](properties.md)

-   [**MSINEWINSTANCE**](msinewinstance.md)
-   [**MSIINSTANCEGUID**](msiinstanceguid.md)
-   [**MsiNTSuiteWebServer**](msintsuitewebserver.md)

[Opzioni di esecuzione In-Script azioni personalizzate](custom-action-in-script-execution-options.md)

-   [**msidbCustomActionTypeTSAware**](custom-action-in-script-execution-options.md)

[Codici errore](error-codes.md)

-   [ERRORE DURANTE \_ \_ L'INSTALLAZIONE \_ REMOTA NON CONSENTITA](error-codes.md)

[Criteri del computer](machine-policies.md)

-   [DisableMSI](disablemsi.md)
-   [TransformsSecure policy](transformssecure-policy.md)

[Opzioni della riga di comando](command-line-options.md)

-   [/c](command-line-options.md)
-   [/n](command-line-options.md)
-   [/Lx](command-line-options.md)

[Attributi del controllo](control-attributes.md)

-   **ImageHandle è** stato rimosso

## <a name="notes"></a>Note

Le [opzioni di installazione Command-Line standard](standard-installer-command-line-options.md) non sono supportate da Windows Installer 2.0. Usare invece le opzioni Windows della [riga di comando del programma di installazione di](command-line-options.md).

Quando Windows Installer 2.0 installa un pacchetto di patch, ignora le informazioni nelle tabelle [MsiPatchSequence](msipatchsequence-table.md) [o MsiPatchMetadata.](msipatchmetadata-table.md) Le versioni successive di Windows Installer possono usare le informazioni contenute in queste tabelle per migliorare la sequenziazione, la rimozione e l'ottimizzazione delle patch. Per informazioni sulle funzionalità di applicazione di patch migliorate in Windows, vedere [Applicazione di patch.](patching.md)

Windows Il programma di installazione 2.0 non supporta le [patch](uninstallable-patches.md) disinstallabili e l'unico metodo per rimuovere determinate patch da un'applicazione è disinstallare l'intera applicazione con patch e quindi reinstallarla senza riapplicare eventuali patch rimosse.

Windows Il programma di installazione 2.0 non supporta la sequenziazione delle patch e installa le patch nell'ordine in cui vengono fornite al sistema durante l'installazione di [più patch.](installing-multiple-patches.md)

Windows Il programma di installazione 2.0 non supporta l'uso dell'applicazione di patch di Controllo dell'account utente [per](user-account-control--uac--patching.md) abilitare patch con firma digitale che possono essere applicate da utenti non amministratori.

Windows Il programma di installazione 2.0 non supporta [l'ottimizzazione delle patch.](patch-optimization.md) L'applicazione di patch può richiedere molto più tempo rispetto Windows versioni successive del programma di installazione che aggiornano solo i file interessati dalla patch.

Windows Il programma di installazione 2.0 non supporta [l'uso Windows programma di installazione per l'inventario di prodotti e patch.](inventory-products-and-patches-.md)

Windows Il programma di installazione 2.0 non supporta il recupero e la modifica delle informazioni dell'elenco di origine per le applicazioni del programma di installazione di Windows e le patch installate nel sistema per tutti gli utenti. Le versioni successive di Windows installer consentono agli amministratori di gestire gli elenchi di origine e le proprietà degli elenchi di origine per le origini di rete, URL e supporti. Le versioni successive consentono agli amministratori di gestire gli elenchi di origine da un processo esterno. Per altre informazioni, vedere [Gestione delle origini di installazione.](managing-installation-sources.md)

Windows Il programma di installazione 2.0 non supporta l'installazione di più istanze di prodotti o patch senza un pacchetto di installazione separato per ogni istanza. Le Windows di installazione successive possono installare più istanze di un prodotto usando trasformazioni del codice prodotto e una .msi pacchetto o una patch. Per informazioni, [vedere Installazione di più istanze di prodotti e patch.](installing-multiple-instances-of-products-and-patches.md)

A partire Windows XP con Service Pack 2 (SP2), Windows Installer può usare i protocolli HTTP, HTTPS e FILE. Il programma di installazione non supporta i protocolli FTP e GOPHER.

 

 



