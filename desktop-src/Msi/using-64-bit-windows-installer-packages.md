---
description: Quando si crea un pacchetto di Windows Installer a 64 bit, attenersi alle linee guida seguenti.
ms.assetid: e7dfd188-fd4d-49d6-8cf5-c17182b697ca
title: Uso di pacchetti di Windows Installer a 64 bit
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5b46ab8a9668d816ea99bd92c2575e9ea6367352
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106314767"
---
# <a name="using-64-bit-windows-installer-packages"></a>Uso di pacchetti di Windows Installer a 64 bit

Quando si creano [pacchetti Windows Installer a 64 bit](64-bit-windows-installer-packages.md) o applicazioni che chiamano Windows Installer per installare i pacchetti a 64 bit, eseguire le operazioni seguenti:

-   Usare uno schema di database Windows Installer 200 o versione successiva. Consente di specificare che la versione 2,0 è la versione minima del programma di installazione necessario per installare il pacchetto impostando la proprietà di [**Riepilogo conteggio pagine**](page-count-summary.md) sul valore integer 200. Le versioni precedenti di Windows Installer rifiutano i tentativi di installazione dei pacchetti a 64 bit. Per i pacchetti a 64 bit nella piattaforma Arm64, lo schema del database di Windows Installer deve essere 500 o superiore.
-   Indicare nella proprietà [**Riepilogo modello**](template-summary.md) del flusso di informazioni di riepilogo del pacchetto che si tratta di un pacchetto a 64 bit. Immettere "Intel64" nel campo piattaforma della proprietà **Riepilogo modello** se il pacchetto deve essere eseguito in un processore Intel64. Immettere "x64" Se il pacchetto deve essere eseguito su un processore esteso a 64 bit. Immettere "Arm64" Se il pacchetto deve essere eseguito in un processore Arm64. Un pacchetto non può essere contrassegnato come supporto per piattaforme Intel64 e x64, il valore della proprietà di **Riepilogo del modello** "Intel64, x64" non è valido. Un pacchetto non può essere contrassegnato come supporto per piattaforme a 32 bit e a 64 bit, i valori delle proprietà di **Riepilogo dei modelli** "Intel, x64" o "Intel, Intel64" non sono validi.
-   Identificare ogni componente a 64 bit impostando **msidbComponentAttributes64bit** nella colonna Attributes della tabella [Component](component-table.md) .
-   Usare istruzioni condizionali facoltative che controllano la versione del sistema operativo a 64 bit facendo riferimento alla proprietà [**VersionNT64**](versionnt64.md) . Windows Installer imposta questa proprietà sulla versione di Windows a 64 bit e lascia VersionNT64 non definito se il sistema operativo non è Windows a 64 bit. Per ulteriori informazioni, vedere [utilizzo delle proprietà nelle istruzioni condizionali](using-properties-in-conditional-statements.md).
-   Usare istruzioni condizionali facoltative che controllano il livello di processore numerico del computer facendo riferimento alla proprietà [**Intel64**](intel64.md) o [**Msix64**](msix64.md) . Il Windows Installer imposta queste proprietà sul livello corrente del processore numerico del computer e lascia la proprietà **Intel64** non definita se non si tratta di un processore basato su Itanium. Per ulteriori informazioni, vedere [utilizzo delle proprietà nelle istruzioni condizionali](using-properties-in-conditional-statements.md).
-   Usare la [tabella AppSearch](appsearch-table.md) e l' [azione AppSearch](appsearch-action.md) per eseguire ricerche facoltative del registro di sistema per i componenti esistenti a 64 bit. Per cercare i componenti esistenti a 64 bit, includere il bit **msidbLocatorType64bit** nella colonna Type della [tabella RegLocator](reglocator-table.md). Per ulteriori informazioni, vedere [ricerca di applicazioni esistenti, file, voci del registro di sistema o proprietà dei file ini.](searching-for-existing-applications-files-registry-entries-or--ini-file-entries.md)
-   Per ottenere i percorsi delle cartelle di sistema, fare riferimento alla proprietà [**System64Folder**](system64folder.md), alla proprietà [**ProgramFiles64Folder**](programfiles64folder.md) e alla proprietà [**CommonFiles64Folder**](commonfiles64folder.md) per le cartelle a 64 bit e alla proprietà [**SystemFolder**](systemfolder.md) , alla proprietà [**ProgramFilesFolder**](programfilesfolder.md) e alla proprietà [**CommonFilesFolder**](commonfilesfolder.md) per le cartelle a 32 bit.
-   Verificare che l'applicazione utilizzi il GUID corretto quando si fa riferimento a un componente a 64 bit. Se sono presenti versioni a 32 bit e a 64 bit di un componente specifico, queste devono avere GUID ID dei componenti diversi.
-   Determinare se è necessario definire nuove variabili di ambiente quando si installano applicazioni a 64 bit.
-   Se è necessario installare una gestione driver ODBC a 64 bit, il componente che lo trasporta dovrebbe essere denominato ODBCDriverManager64. È necessario che Gestione driver ODBC sia stato creato nel pacchetto del programma di installazione e che sia incluso un componente denominato ODBCDriverManager64. Il gestore verrà installato se necessario.
-   Verificare che l'applicazione chiami solo i servizi a 32 bit che vengono eseguiti come file eseguibili. Le applicazioni non devono chiamare i servizi a 32 bit che vengono eseguiti in dll.
-   Se l'applicazione installa versioni coesistenti a 32 bit e a 64 bit di un componente, verificare che le informazioni del file ini siano condivise correttamente.
-   Verificare che l'applicazione applichi solo patch a 32 bit a file binari a 32 bit e patch a 64 bit a file binari a 64 bit.
-   Considerare gli scenari di aggiornamento futuri per le versioni a 32 bit e a 64 bit e per mantenere i codici di aggiornamento. Per ulteriori informazioni, vedere applicazione di [patch e aggiornamenti](patching-and-upgrades.md).
-   Quando si usa un'applicazione di [bootstrap](bootstrapping.md) per installare un [pacchetto di Windows Installer a 64 bit](64-bit-windows-installer-packages.md), compilare l'applicazione di bootstrap come applicazione a 64 bit.
-   Per disabilitare la [Reflection del registro](../winprog64/registry-reflection.md) di sistema per le chiavi del registro di sistema interessate da un particolare componente, impostare il bit **MsidbComponentAttributesDisableRegistryReflection** nel campo Attributes della tabella [Component](component-table.md) . Questa operazione può essere necessaria per coesistere copie a 32 bit e 64 bit della stessa applicazione. Se questo bit è impostato, il Windows Installer chiama la funzione [**RegDisableReflectionKey**](/windows/win32/api/winreg/nf-winreg-regdisablereflectionkey) su ogni chiave a cui accede il componente. Questo bit è disponibile con Windows Installer versione 4,0. Questo bit viene ignorato nei sistemi a 32 bit. Questo bit viene ignorato nelle versioni a 64 bit di Windows XP e Windows 2000.

> [!Note]  
> Il valore della radice del registro di sistema numeric restituito dal parametro *lpPathBuf* della funzione [**MsiGetComponentPath**](/windows/desktop/api/Msi/nf-msi-msigetcomponentpatha) distingue tra i componenti nei sistemi operativi a 32 bit e a 64 bit. Per altre informazioni, vedere funzione **MsiGetComponentPath** .

 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Azioni personalizzate a 64 bit](64-bit-custom-actions.md)
</dt> </dl>

 

 
