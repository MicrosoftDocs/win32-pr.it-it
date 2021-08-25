---
description: Attenersi alle linee guida seguenti quando si crea un pacchetto Windows installer a 64 bit.
ms.assetid: e7dfd188-fd4d-49d6-8cf5-c17182b697ca
title: Uso di pacchetti del programma di installazione Windows a 64 bit
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c9c3bca5c666f7a6a0f1757efca40a26b1406d4241abf7d32a066c2d7fa01b92
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119809091"
---
# <a name="using-64-bit-windows-installer-packages"></a>Uso di pacchetti del programma di installazione Windows a 64 bit

Quando si creano pacchetti di Windows a [64 bit](64-bit-windows-installer-packages.md) o applicazioni che chiamano Windows Installer per installare pacchetti a 64 bit, eseguire le operazioni seguenti:

-   Usare uno schema Windows di database del programma di installazione di 200 o versione successiva. Specificare che la versione 2.0 è la versione minima del programma di installazione necessaria per installare il pacchetto impostando la proprietà [**Riepilogo**](page-count-summary.md) conteggio pagine sul numero intero 200. Le Windows versioni precedenti del programma di installazione rifiutano i tentativi di installazione di pacchetti a 64 bit. Per i pacchetti a 64 bit nella piattaforma Arm64, lo schema del database Windows Installer deve essere 500 o superiore.
-   Nella proprietà [**Riepilogo modello**](template-summary.md) del flusso di informazioni di riepilogo del pacchetto indicare che si tratta di un pacchetto a 64 bit. Immettere "Intel64" nel campo della piattaforma della proprietà **Riepilogo** modello se il pacchetto deve essere eseguito in un processore Intel64. Immettere "x64" se il pacchetto deve essere eseguito in un processore esteso a 64 bit. Immettere "Arm64" se il pacchetto deve essere eseguito in un processore Arm64. Un pacchetto non può essere contrassegnato come che supporta  entrambe le piattaforme Intel64 e x64. Il valore della proprietà Riepilogo modello "Intel64,x64" non è valido. Un pacchetto non può essere contrassegnato come che supporta piattaforme a  32 bit e a 64 bit. I valori della proprietà Riepilogo modello "Intel,x64" o "Intel,Intel64" non sono validi.
-   Identificare ogni componente a 64 bit impostando **msidbComponentAttributes64bit** nella colonna Attributi della [tabella](component-table.md) Componente.
-   Usare istruzioni condizionali facoltative che controllano la versione del sistema operativo a 64 bit facendo riferimento alla [**proprietà VersionNT64.**](versionnt64.md) Windows Il programma di installazione imposta questa proprietà sulla versione Windows a 64 bit e lascia VersionNT64 indefinito se il sistema operativo non è a 64 bit Windows. Per altre informazioni, vedere [Uso delle proprietà nelle istruzioni condizionali](using-properties-in-conditional-statements.md).
-   Usare istruzioni condizionali facoltative che controllano il livello del processore numerico del computer facendo riferimento alla proprietà [**Intel64**](intel64.md) [**o Msix64.**](msix64.md) L Windows Installer imposta queste proprietà sul livello corrente del processore numerico del computer e lascia la proprietà **Intel64** indefinita se non si tratta di un processore basato su Itanium. Per altre informazioni, vedere [Uso delle proprietà nelle istruzioni condizionali](using-properties-in-conditional-statements.md).
-   Usare la [tabella AppSearch e](appsearch-table.md) [l'azione AppSearch](appsearch-action.md) per eseguire ricerche facoltative nel Registro di sistema per i componenti a 64 bit esistenti. Per cercare i componenti a 64 bit esistenti, includere il bit **msidbLocatorType64bit** nella colonna Tipo della [tabella RegLocator](reglocator-table.md). Per altre informazioni, vedere [Ricerca di applicazioni, file, voci del](searching-for-existing-applications-files-registry-entries-or--ini-file-entries.md) Registro di sistema o .ini proprietà Voci file esistenti
-   Ottenere i percorsi delle cartelle di sistema facendo riferimento alla proprietà [**System64Folder,**](system64folder.md)alla proprietà [**ProgramFiles64Folder**](programfiles64folder.md) e alla proprietà [**CommonFiles64Folder**](commonfiles64folder.md) per le cartelle a 64 bit e alle proprietà [**SystemFolder,**](systemfolder.md) [**ProgramFilesFolder**](programfilesfolder.md) e [**CommonFilesFolder**](commonfilesfolder.md) per le cartelle a 32 bit.
-   Verificare che l'applicazione usi il GUID corretto quando fa riferimento a un componente a 64 bit. Se sono presenti versioni a 32 bit e a 64 bit di un componente specifico, questi devono avere GUID ID componente diversi.
-   Determinare se è necessario definire nuove variabili di ambiente durante l'installazione di applicazioni a 64 bit.
-   Se è necessario installare Gestione driver ODBC a 64 bit, il componente che lo contiene deve essere denominato ODBCDriverManager64. Gestione driver ODBC deve essere creato nel pacchetto del programma di installazione e deve essere incluso un componente denominato ODBCDriverManager64. Il manager verrà installato, se necessario.
-   Verificare che l'applicazione chiami solo i servizi a 32 bit eseguiti come eseguibili. Le applicazioni non devono chiamare i servizi a 32 bit eseguiti nelle DLL.
-   Se l'applicazione installa versioni coesistenti a 32 bit e a 64 bit di un componente, verificare che l'applicazione .ini le informazioni sul file correttamente.
-   Verificare che l'applicazione appli solo patch a 32 bit a file binari a 32 bit e patch a 64 bit a file binari a 64 bit.
-   Prendere in considerazione scenari di aggiornamento futuri per le versioni a 32 bit e a 64 bit e gestire i codici di aggiornamento. Per altre informazioni, vedere [Applicazione di patch e aggiornamenti.](patching-and-upgrades.md)
-   Quando si usa [un'applicazione](bootstrapping.md) di bootstrap per installare un pacchetto di Windows [Installer a 64 bit,](64-bit-windows-installer-packages.md)compilare l'applicazione di bootstrap come applicazione a 64 bit.
-   Per [disabilitare](../winprog64/registry-reflection.md) la reflection del Registro di sistema per le chiavi del Registro di sistema interessate da un particolare componente, impostare il bit **msidbComponentAttributesDisableRegistryReflection** nel campo Attributi della [tabella Componente.](component-table.md) Potrebbe essere necessario avere copie a 32 bit e a 64 bit della stessa applicazione coesistenti. Se questo bit è impostato, Windows Installer chiama la [**funzione RegDisableReflectionKey**](/windows/win32/api/winreg/nf-winreg-regdisablereflectionkey) su ogni chiave a cui accede il componente. Questo bit è disponibile con Windows Installer versione 4.0. Questo bit viene ignorato nei sistemi a 32 bit. Questo bit viene ignorato nelle versioni a 64 bit di Windows XP e Windows 2000.

> [!Note]  
> Il valore della radice numerica del Registro di sistema restituito dal parametro *lpPathBuf* della funzione [**MsiGetComponentPath**](/windows/desktop/api/Msi/nf-msi-msigetcomponentpatha) distingue tra i componenti nei sistemi operativi a 32 bit e a 64 bit. Per altre informazioni, vedere **La funzione MsiGetComponentPath.**

 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Azioni personalizzate a 64 bit](64-bit-custom-actions.md)
</dt> </dl>

 

 
