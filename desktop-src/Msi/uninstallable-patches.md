---
description: Il fatto che una patch possa essere disinstallata dipende dalla modalità di creazione della patch, dalla versione di Windows Installer usata per installare la patch e dalle modifiche apportate dalla patch all'applicazione.
ms.assetid: 95a5365c-e2ae-4e35-9aeb-67d04e67c7df
title: Patch disinstallabili
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6ad46d85318378ed81d2278d3ea1290152723704
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104524888"
---
# <a name="uninstallable-patches"></a>Patch disinstallabili

Il fatto che una patch possa essere disinstallata dipende dalla modalità di creazione della patch, dalla versione di Windows Installer usata per installare la patch e dalle modifiche apportate dalla patch all'applicazione. Se una patch non è disinstallabile, l'unico modo per rimuovere la patch è disinstallare l'intera applicazione e reinstallare senza applicare la patch da rimuovere.

È possibile chiamare per la disinstallazione delle patch applicate con Windows Installer versione 3,0 usando le [Opzioni della riga di comando](command-line-options.md), la funzione [**MsiRemovePatches**](/windows/desktop/api/Msi/nf-msi-msiremovepatchesa) o il [**Metodo RemovePatches**](installer-removepatches.md) come descritto nella sezione [Disinstallazione delle patch](uninstalling-patches.md) . Il Windows Installer verifica che ciascuna delle patch elencate per la rimozione nella proprietà [**MSIPATCHREMOVE**](msipatchremove.md) sia disinstallabile. Se l'utente non dispone dei privilegi necessari per rimuovere la patch, la patch non è nota per il prodotto, il criterio patch impedisce la rimozione o la patch è stata contrassegnata come non disinstallabile, il programma di installazione restituisce un errore che indica una transazione di installazione non riuscita.

**Windows Installer 2,0:** Non supportato. Le patch applicate con una versione di Windows Installer precedente alla Windows Installer 3,0 non sono disinstallabili.

## <a name="patches-that-are-not-uninstallable"></a>Patch non disinstallabili

Nei casi seguenti non è possibile disinstallare una patch (file con estensione msp) applicata a un'applicazione installata. L'unico metodo per rimuovere una patch non disinstallabile consiste nel disinstallare l'applicazione con patch, quindi reinstallare l'applicazione senza riapplicare la patch. In questo caso, è necessario riapplicare le patch che non si desidera rimuovere dall'applicazione.

-   Le patch applicate con una versione di Windows Installer inferiore a Windows Installer 3,0 non sono disinstallabili.
-   Le patch applicate alle applicazioni installate in un computer in cui è stato impostato il criterio [DisablePatchUninstall](disablepatchuninstall.md) da un amministratore non possono essere disinstallate. Quando è stato impostato questo [criterio computer](machine-policies.md), non è possibile disinstallare alcuna patch nel computer, neanche da un amministratore.
-   Le patch che non dispongono di una tabella [MsiPatchMetadata](msipatchmetadata-table.md) nel database non sono disinstallabili.
-   Le patch che non includono la riga seguente nella tabella [MsiPatchMetadata](msipatchmetadata-table.md) non sono disinstallabili. La patch non è disinstallabile per altri valori di Company, Property e value.

    | Company | Proprietà     | Valore |
    |---------|--------------|-------|
    | Null  | AllowRemoval | 1     |

    

     

-   La patch è stata applicata a un'applicazione installata in un contesto per il quale l'utente non dispone di privilegi sufficienti per la disinstallazione delle patch. Le parole "non consentite" nella tabella seguente indicano che un amministratore o un utente non amministratore non è in grado di disinstallare patch da applicazioni con patch installate in questo contesto. La parola "Allowed" in questa tabella indica che i privilegi non impediscono a un amministratore o a un utente non amministratore di disinstallare le patch. Tuttavia, per gli altri motivi illustrati in questa sezione, potrebbe non essere possibile disinstallare la patch.

    | Contesto di installazione dell'applicazione        | Disinstallazione dell'amministratore della patch | Disinstallazione patch non amministratore                                                                                                                                                                                                                                                                             |
    |-----------------------------------------|----------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
    | Per-Machine                             | Consentito                          | In genere non è consentito l'unica eccezione se la patch è stata applicata con l'applicazione di patch (LUA). Una patch contrassegnata come patch LUA può essere disinstallata da amministratori o non amministratori. L'applicazione di patch LUA è disponibile solo per i pacchetti installati per computer dal supporto e richiede la creazione speciale.<br/> |
    | Per-User non gestito per l'utente corrente   | Consentito                          | Consentito                                                                                                                                                                                                                                                                                                          |
    | Per-User non gestito per un utente diverso | Non consentito                      | Non consentito                                                                                                                                                                                                                                                                                                      |
    | Per-User gestito per l'utente corrente       | Consentito                          | Non consentito                                                                                                                                                                                                                                                                                                      |
    | Per-User gestiti per un utente diverso     | Non consentito                      | Non consentito                                                                                                                                                                                                                                                                                                      |

    

     

-   Un [aggiornamento principale](major-upgrades.md) applicato da una patch non è disinstallabile. Per eseguire gli aggiornamenti principali di un'applicazione, è necessario installare l'applicazione aggiornata (file con estensione msi) anziché una patch.
-   Le patch applicate a un'installazione amministrativa non sono disinstallabili. L'applicazione di patch alle installazioni amministrative non è consigliata. Il set corrente di patch deve essere applicato nel computer dell'utente dopo che l'utente ha installato l'applicazione dall'immagine amministrativa. Ciò può impedire che il [codice del pacchetto](package-codes.md) memorizzato nella cache del computer dell'utente diventi diverso dal codice del pacchetto nell'installazione amministrativa. Se il codice del pacchetto memorizzato nella cache nel computer dell'utente è diverso da quello dell'installazione amministrativa, reinstallare l'applicazione dall'installazione amministrativa, quindi applicare una patch al computer client.
-   Quando una patch aggiunge nuovo contenuto a una delle tabelle nell'elenco seguente, Windows Installer contrassegna la patch come non disinstallabile. Una patch non installabile può aggiungere nuovi file, assembly, voci del registro di sistema, componenti o funzionalità a un'installazione aggiungendo nuove righe a tabelle di database non incluse in questo elenco.

    -   [AppId](appid-table.md)
    -   [Azione BindImage sul](bindimage-table.md)
    -   [Classe](class-table.md)
    -   [ComPlus](complus-table.md)
    -   [CreateFolder](createfolder-table.md)
    -   [DuplicateFile](duplicatefile-table.md)
    -   [Environment](environment-table.md)
    -   [Estensione](extension-table.md)
    -   [Carattere](font-table.md)
    -   [IniFile](inifile-table.md)
    -   [IsolatedComponent](isolatedcomponent-table.md)
    -   [LockPermissions](lockpermissions-table.md)
    -   [MsiLockPermissionsEx](msilockpermissionsex-table.md)
    -   [MIME](mime-table.md)
    -   [MoveFile](movefile-table.md)
    -   [MsiServiceConfig](msiserviceconfig-table.md)
    -   [MsiServiceConfigFailureActions](msiserviceconfigfailureactions-table.md)
    -   [ODBCAttribute](odbcattribute-table.md)
    -   [ODBCDataSource](odbcdatasource-table.md)
    -   [ODBCDriver](odbcdriver-table.md)
    -   [ODBCSourceAttribute](odbcsourceattribute-table.md)
    -   [ODBCTranslator](odbctranslator-table.md)
    -   [ProgId](progid-table.md)
    -   [PublishComponent](publishcomponent-table.md)
    -   [RemoveIniFile](removeinifile-table.md)
    -   [SelfReg](selfreg-table.md)
    -   [ServiceControl](servicecontrol-table.md)
    -   [ServiceInstall](serviceinstall-table.md)
    -   [TypeLib](typelib-table.md)
    -   [Verbo](verb-table.md)
    -   [!Note]  
        > Se una patch aggiunge nuovo contenuto alle tabelle [RemoveFile](removefile-table.md) o [RemoveRegistry](removeregistry-table.md) , Windows Installer non contrassegna la patch come non disinstallabile. Tuttavia, la patch non è disinstallabile, a meno che la risorsa per rimuovere il nuovo contenuto non esista già nel pacchetto di installazione originale. Se, ad esempio, la patch aggiunge una nuova riga alla tabella RemoveFile, non sarà possibile ripristinare il file rimosso eseguendo la disinstallazione della patch se il file è esterno alla [tabella dei file](file-table.md). È necessario che il file sia stato creato nella tabella dei file del pacchetto originale più le patch applicate affinché la patch sia disinstallabile.

         

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Sequenza di patch](sequencing-patches.md)
</dt> <dt>

[Rimozione di patch](removing-patches.md)
</dt> <dt>

[Disinstallazione di patch](uninstalling-patches.md)
</dt> <dt>

[Patch disinstallare azioni personalizzate](patch-uninstall-custom-actions.md)
</dt> <dt>

[**MSIPATCHREMOVE**](msipatchremove.md)
</dt> <dt>

[**MsiEnumapplicationsEx**](/windows/desktop/api/Msi/nf-msi-msienumproductsexa)
</dt> <dt>

[**MsiGetPatchInfoEx**](/windows/desktop/api/Msi/nf-msi-msigetpatchinfoexa)
</dt> <dt>

[**MsiRemovePatches**](/windows/desktop/api/Msi/nf-msi-msiremovepatchesa)
</dt> </dl>

 

 




