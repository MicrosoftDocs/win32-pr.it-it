---
description: Le funzioni, le tabelle e le proprietà Windows Installer elencate in questa pagina non sono supportate da Windows Installer&\# 160; 2.0 e versioni precedenti.
ms.assetid: 850b598a-338e-4f84-8336-01e962256a08
title: Non supportato in Windows Installer 2,0
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 35ee09133af9ef611a93c2511d7b130b2175561b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103885285"
---
# <a name="not-supported-in-windows-installer-20"></a>Non supportato in Windows Installer 2,0

Le funzioni, le tabelle e le proprietà Windows Installer elencate in questa pagina non sono supportate da Windows Installer 2,0 e versioni precedenti. L'assenza di una funzionalità da questo elenco non garantisce che la funzionalità sia supportata. Vedere la documentazione principale per determinare quale versione di Windows Installer è necessaria per una determinata funzionalità. Per informazioni sulle altre versioni di Windows Installer, vedere Novità [di Windows Installer](what-s-new-in-windows-installer.md).

Windows Installer 2,0 può essere eseguito in Microsoft Windows 2000, Microsoft Windows XP o Windows Server 2003. Per un elenco di tutte le versioni di Windows Installer, vedere [versioni rilasciate di Windows Installer](released-versions-of-windows-installer.md).

Le funzionalità seguenti non sono supportate in Windows Installer 2,0 e versioni precedenti.

[Funzioni di installazione](installer-functions.md)

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

[Strutture di Windows Installer](installer-structures.md)

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

-   rimozione della patch di errore non \_ \_ \_ supportata
-   PATCH di errore \_ sconosciuta \_
-   ERRORE \_ patch \_ Nessuna \_ sequenza
-   rimozione della patch di errore non \_ \_ \_ consentita
-   ERRORE \_ \_ XML patch non valido \_
-   \_ \_ \_ prodotto annunciato gestito dalla patch di errore \_

Modalità di registrazione

-   [**\_LOGONLYONERROR INSTALLLOGMODE**](/windows/desktop/api/Msi/nf-msi-msienableloga)

[Interfaccia di automazione](automation-interface.md)

-   Proprietà dell' [ **oggetto Product**](product-object.md)

    -   [**Prodotto. UserSid**](product-usersid.md)
    -   [**Prodotto. origini**](product-sources.md)
    -   [**Prodotto. MediaDisks**](product-mediadisks.md)
    -   [**Prodotto. FeatureState**](product-featurestate.md)
    -   [**Product. Context**](product-context.md)
    -   [**Prodotto. InstallProperty**](product-installproperty.md)
    -   [**Prodotto. ProductCode**](product-productcode.md)
    -   [**Prodotto. ComponentState**](product-componentstate.md)
    -   [**Prodotto. stato**](product-state.md)
    -   [**Prodotto. SourceListInfo**](product-sourcelistinfo.md)

-   Metodi dell' [ **oggetto Product**](product-object.md)

    -   [**Prodotto. SourceListForceResolution**](product-sourcelistforceresolution.md)
    -   [**Prodotto. SourceListClearMediaDisk**](product-sourcelistclearmediadisk.md)
    -   [**Prodotto. SourceListClearAll**](product-sourcelistclearall.md)
    -   [**Prodotto. SourceListClearSource**](product-sourcelistclearsource.md)
    -   [**Prodotto. SourceListAddSource**](product-sourcelistaddsource.md)
    -   [**Prodotto. SourceListAddMediaDisk**](product-sourcelistaddmediadisk.md)

-   Proprietà dell' [ **oggetto patch**](patch-object.md)

    -   [**Patch. UserSid**](patch-usersid.md)
    -   [**Patch. state**](patch-state.md)
    -   [**Patch. Sources**](patch-sources.md)
    -   [**Patch. SourceListInfo**](patch-sourcelistinfo.md)
    -   [**Patch. ProductCode**](patch-productcode.md)
    -   [**Patch. PatchProperty**](patch-patchproperty.md)
    -   [**Patch. PatchCode**](patch-patchcode.md)
    -   [**Patch. MediaDisks**](patch-mediadisks.md)
    -   [**Patch. Context**](patch-context.md)

-   Metodi dell' [ **oggetto patch**](patch-object.md)

    -   [**Patch. SourceListForceResolution**](patch-sourcelistforceresolution.md)
    -   [**Patch. SourceListClearAll**](patch-sourcelistclearall.md)
    -   [**Patch. SourceListClearSource**](patch-sourcelistclearsource.md)
    -   [**Patch. SourceListClearMediaDisk**](patch-sourcelistclearmediadisk.md)
    -   [**Patch. SourceListAddSource**](patch-sourcelistaddsource.md)
    -   [**Patch. SourceListAddMediaDisk**](patch-sourcelistaddmediadisk.md)

-   Proprietà dell' [ **oggetto del programma di installazione**](installer-object.md)

    -   [**Programma di installazione. ProductsEx**](installer-productsex.md)
    -   [**Programma di installazione. ProductInfo**](installer-productinfo.md)
    -   [**Programma di installazione. PatchesEx**](installer-patchesex.md)

-   Metodi dell' [ **oggetto Installer**](installer-object.md)

    -   [**Programma di installazione. ApplyMultiplePatches**](installer-applymultiplepatches.md)
    -   [**Programma di installazione. ApplyPatch**](installer-applypatch.md)
    -   [**Programma di installazione. RemovePatches**](installer-removepatches.md)
    -   [**Programma di installazione. ExtractPatchXMLData**](installer-extractpatchxmldata.md)

Anche le funzionalità seguenti non sono supportate in Windows Installer versione 2.0.2600. Windows Installer versione 2.0.2600 è stata rilasciata con Windows XP e Windows 2000 Server. Le funzionalità sono disponibili a partire dalla versione Windows Installer 2.0.3790 rilasciata con Windows Server 2003. Per un elenco di tutte le versioni di Windows Installer, vedere [versioni rilasciate di Windows Installer](released-versions-of-windows-installer.md).

[Funzioni di installazione](installer-functions.md)

-   [**MsiAdvertiseProductEx**](/windows/desktop/api/Msi/nf-msi-msiadvertiseproductexa)
    -   istanza di MSIADVERTISEOPTIONS \_
-   [**MsiApplyPatch**](/windows/desktop/api/Msi/nf-msi-msiapplypatcha)
-   [**MsiGetProductInfo**](/windows/desktop/api/Msi/nf-msi-msigetproductinfoa)

[Interfaccia di automazione](automation-interface.md)

-   Metodi dell' [ **oggetto Installer**](installer-object.md)

    -   [**Programma di installazione. ApplyPatch**](installer-applypatch.md)
    -   [**Programma di installazione. ProductInfo**](installer-productinfo.md)

[Proprietà](properties.md)

-   [**MSINEWINSTANCE**](msinewinstance.md)
-   [**MSIINSTANCEGUID**](msiinstanceguid.md)
-   [**MsiNTSuiteWebServer**](msintsuitewebserver.md)

[Opzioni di esecuzione In-Script azione personalizzata](custom-action-in-script-execution-options.md)

-   [**msidbCustomActionTypeTSAware**](custom-action-in-script-execution-options.md)

[Codici errore](error-codes.md)

-   [ERRORE di \_ installazione \_ remota non \_ consentito](error-codes.md)

[Criteri del computer](machine-policies.md)

-   [DisableMSI](disablemsi.md)
-   [Criteri di TransformsSecure](transformssecure-policy.md)

[Opzioni della riga di comando](command-line-options.md)

-   [/c](command-line-options.md)
-   [/n](command-line-options.md)
-   [/Lx](command-line-options.md)

[Attributi del controllo](control-attributes.md)

-   **ImageHandle** è stato rimosso

## <a name="notes"></a>Note

Le [Opzioni del programma di installazione Standard Command-Line](standard-installer-command-line-options.md) non sono supportate da Windows Installer 2,0. Usare invece le [Opzioni della riga di comando](command-line-options.md)Windows Installer.

Quando Windows Installer 2,0 installa un pacchetto di patch, ignora le informazioni contenute nelle tabelle [MsiPatchSequence](msipatchsequence-table.md) o [MsiPatchMetadata](msipatchmetadata-table.md) . Nelle versioni successive del Windows Installer è possibile utilizzare le informazioni contenute in queste tabelle per migliorare la sequenziazione, la rimozione e l'ottimizzazione delle patch. Per informazioni sulla funzionalità di applicazione di patch migliorata in Windows Installer, vedere applicazione di [patch](patching.md).

Windows Installer 2,0 non supporta le [patch disinstallabili](uninstallable-patches.md) e l'unico metodo per rimuovere patch particolari da un'applicazione consiste nel disinstallare l'intera applicazione con patch e quindi reinstallare senza riapplicare le patch da rimuovere.

Windows Installer 2,0 non supporta la sequenziazione delle patch e installa le patch nell'ordine in cui vengono fornite al sistema quando si [installano più patch](installing-multiple-patches.md).

Windows Installer 2,0 non supporta l'utilizzo dell'applicazione di patch per il [controllo dell'account utente (UAC)](user-account-control--uac--patching.md) per abilitare patch con firma digitale che possono essere applicate da utenti non amministratori.

Windows Installer 2,0 non supporta l' [ottimizzazione della patch](patch-optimization.md). L'applicazione di patch può richiedere molto più tempo rispetto alle versioni successive di Windows Installer che aggiorna solo i file interessati dalla patch.

Windows Installer 2,0 non supporta l' [utilizzo di Windows Installer per l'inventario di prodotti e patch](inventory-products-and-patches-.md).

Windows Installer 2,0 non supporta il recupero e la modifica delle informazioni dell'elenco di origine per Windows Installer le applicazioni e le patch installate nel sistema per tutti gli utenti. Le versioni successive di Windows Installer consentono agli amministratori di gestire gli elenchi di origine e le proprietà dell'elenco di origine per le origini di rete, URL e supporti. Le versioni successive consentono agli amministratori di gestire gli elenchi di origine da un processo esterno. Per ulteriori informazioni, vedere [gestione delle origini di installazione](managing-installation-sources.md).

Windows Installer 2,0 non supporta l'installazione di più istanze di prodotti o patch senza un pacchetto di installazione separato per ogni istanza. In seguito Windows Installer versioni possono installare più istanze di un prodotto utilizzando trasformazioni del codice prodotto e un pacchetto con estensione msi o una patch. Per informazioni [, vedere installazione di più istanze di prodotti e patch](installing-multiple-instances-of-products-and-patches.md).

A partire da Windows XP con Service Pack 2 (SP2), Windows Installer possibile utilizzare i protocolli HTTP, HTTPS e FILE. Il programma di installazione non supporta i protocolli FTP e GOPHER.

 

 



