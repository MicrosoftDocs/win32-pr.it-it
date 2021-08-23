---
description: La disinstallazione di una patch dipende dalla modalità di creazione della patch, dalla versione del programma di installazione di Windows usata per installare la patch e dalle modifiche apportate dalla patch all'applicazione.
ms.assetid: 95a5365c-e2ae-4e35-9aeb-67d04e67c7df
title: Patch disinstallabili
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a9a3abea369a09dd51e995ba28dcab1463032bb6e5dec9648d3eae39be4cbf21
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119527641"
---
# <a name="uninstallable-patches"></a>Patch disinstallabili

La disinstallazione di una patch dipende dalla modalità di creazione della patch, dalla versione del programma di installazione di Windows usata per installare la patch e dalle modifiche apportate dalla patch all'applicazione. Se una patch non è disinstallabile, l'unico modo per rimuoverla è disinstallare l'intera applicazione e reinstallarla senza applicare la patch da rimuovere.

È possibile chiamare per la disinstallazione delle patch applicate con il programma di installazione di Windows versione 3.0 usando le opzioni della riga di comando [,](command-line-options.md)la funzione [**MsiRemovePatches**](/windows/desktop/api/Msi/nf-msi-msiremovepatchesa) o il metodo [**RemovePatches**](installer-removepatches.md) come descritto nella sezione Disinstallazione [delle patch.](uninstalling-patches.md) Il Windows installer verifica che ognuna delle patch elencate per la rimozione nella [**proprietà MSIPATCHREMOVE**](msipatchremove.md) sia disinstallabile. Se l'utente non dispone dei privilegi per rimuovere la patch, la patch è sconosciuta per il prodotto, i criteri di patch impediscono la rimozione o la patch è stata contrassegnata come non disinstallabile, il programma di installazione restituisce un errore che indica una transazione di installazione non riuscita.

**Windows Installer 2.0:** Non supportato. Le patch applicate usando una versione di Windows installer precedente Windows Installer 3.0 non sono disinstallabili.

## <a name="patches-that-are-not-uninstallable"></a>Patch non disinstallabili

Una patch (file con estensione msp) applicata a un'applicazione installata non è disinstallabile nei casi seguenti. L'unico metodo per rimuovere una patch non disinstallabile è disinstallare l'applicazione con patch e quindi reinstallare l'applicazione senza riapplicare la patch. In questo caso, è necessario riapplicare le patch che non si desidera rimuovere dall'applicazione.

-   Le patch applicate usando una versione di Windows installer inferiore a Windows Installer 3.0 non sono disinstallabili.
-   Le patch applicate alle applicazioni installate in un computer in cui è stato impostato il criterio [DisablePatchUninstall](disablepatchuninstall.md) da un amministratore non sono disinstallabili. Dopo aver [impostato i](machine-policies.md)criteri del computer, non è possibile disinstallare patch nel computer, anche da un amministratore.
-   Le patch che non dispongono di [una tabella MsiPatchMetadata](msipatchmetadata-table.md) nel database non sono disinstallabili.
-   Le patch che non includono la riga seguente nella tabella [MsiPatchMetadata](msipatchmetadata-table.md) non sono disinstallabili. La patch non è disinstallabile per altri valori di Company, Property e Value.

    | Company | Proprietà     | Valore |
    |---------|--------------|-------|
    | {Null}  | AllowRemoval | 1     |

    

     

-   La patch è stata applicata a un'applicazione installata in un contesto per cui l'utente ha privilegi insufficienti per disinstallare le patch. Le parole "Non consentite" nella tabella seguente indicano che un amministratore o un utente non amministratore non può disinstallare le patch dalle applicazioni con patch installate in questo contesto. La parola "Consentito" in questa tabella indica che i privilegi non impediscono a un amministratore o a un utente non amministratore di disinstallare le patch, tuttavia per uno qualsiasi degli altri motivi illustrati in questa sezione potrebbe comunque non essere possibile disinstallare la patch.

    | Contesto di installazione dell'applicazione        | Disinstallazione della patch da parte dell'amministratore | Disinstallazione della patch non da parte dell'amministratore                                                                                                                                                                                                                                                                             |
    |-----------------------------------------|----------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
    | Per-Machine                             | Consentito                          | In genere non consentito L'unica eccezione è se la patch è stata applicata usando l'applicazione di patch (LUA). Una patch contrassegnata come patch LUA è disinstallabile da amministratori o non amministratori. L'applicazione di patch LUA è disponibile solo per i pacchetti installati per computer dai supporti e richiede una creazione speciale.<br/> |
    | Per-User non gestito per l'utente corrente   | Consentito                          | Consentito                                                                                                                                                                                                                                                                                                          |
    | Per-User non gestito per utenti diversi | Non consentito                      | Non consentito                                                                                                                                                                                                                                                                                                      |
    | Per-User gestito per l'utente corrente       | Consentito                          | Non consentito                                                                                                                                                                                                                                                                                                      |
    | Per-User gestito per un utente diverso     | Non consentito                      | Non consentito                                                                                                                                                                                                                                                                                                      |

    

     

-   Un [aggiornamento importante](major-upgrades.md) applicato da una patch non è disinstallabile. Gli aggiornamenti principali di un'applicazione devono essere eseguiti installando l'applicazione aggiornata (.msi file) anziché una patch.
-   Le patch applicate a un'installazione amministrativa non sono disinstallabili. Non è consigliabile applicare patch alle installazioni amministrative. Il set corrente di patch deve essere applicato nel computer dell'utente dopo che l'utente ha installato l'applicazione dall'immagine amministrativa. Ciò può impedire che [il codice del](package-codes.md) pacchetto memorizzato nella cache nel computer dell'utente diventi diverso dal codice del pacchetto nell'installazione amministrativa. Se il codice del pacchetto memorizzato nella cache del computer dell'utente diventa diverso da quello dell'installazione amministrativa, reinstallare l'applicazione dall'installazione amministrativa e quindi applicare patch al computer client.
-   Quando una patch aggiunge nuovo contenuto a una delle tabelle nell'elenco seguente, Windows programma di installazione contrassegna la patch come non disinstallabile. Una patch disinstallabile può aggiungere nuovi file, assembly, voci del Registro di sistema, componenti o funzionalità a un'installazione aggiungendo nuove righe alle tabelle di database non incluse in questo elenco.

    -   [Appid](appid-table.md)
    -   [BindImage](bindimage-table.md)
    -   [Classe](class-table.md)
    -   [Complus](complus-table.md)
    -   [CreateFolder](createfolder-table.md)
    -   [DuplicateFile](duplicatefile-table.md)
    -   [Environment](environment-table.md)
    -   [Estensione](extension-table.md)
    -   [Font](font-table.md)
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
    -   [Progid](progid-table.md)
    -   [PublishComponent](publishcomponent-table.md)
    -   [RemoveIniFile](removeinifile-table.md)
    -   [SelfReg](selfreg-table.md)
    -   [ServiceControl](servicecontrol-table.md)
    -   [ServiceInstall](serviceinstall-table.md)
    -   [Typelib](typelib-table.md)
    -   [Verbo](verb-table.md)
    -   [!Note]  
        > Se una patch aggiunge nuovo contenuto alle tabelle [RemoveFile](removefile-table.md) o [RemoveRegistry,](removeregistry-table.md) Windows Installer non contrassegna la patch come non disinstallabile. Tuttavia, la patch non è disinstallabile a meno che la risorsa per rimuovere il nuovo contenuto non esista già nel pacchetto di installazione originale. Ad esempio, se la patch aggiunge una nuova riga alla tabella RemoveFile, il file rimosso non può essere ripristinato disinstallando la patch se il file è esterno alla [tabella File](file-table.md). Il file deve essere stato creato nella tabella File del pacchetto originale e le patch applicate per la disinstallazione della patch.

         

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Sequenziazione delle patch](sequencing-patches.md)
</dt> <dt>

[Rimozione di patch](removing-patches.md)
</dt> <dt>

[Disinstallazione delle patch](uninstalling-patches.md)
</dt> <dt>

[Azioni personalizzate di disinstallazione patch](patch-uninstall-custom-actions.md)
</dt> <dt>

[**MSIPATCHREMOVE**](msipatchremove.md)
</dt> <dt>

[**MsiEnumapplicationsEx**](/windows/desktop/api/Msi/nf-msi-msienumproductsexa)
</dt> <dt>

[**MsiGetPatchInfoEx**](/windows/desktop/api/Msi/nf-msi-msigetpatchinfoexa)
</dt> <dt>

[**MsiRemovePatches**](/windows/desktop/api/Msi/nf-msi-msiremovepatchesa)
</dt> </dl>

 

 




