---
description: ICE88 verifica che la directory a cui viene fatto riferimento nella colonna DirProperty della tabella IniFile esista nel pacchetto di Windows Installer.
ms.assetid: 9bb253fd-e231-4016-807d-3b1068ecff68
title: ICE88
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0f59197259f8e5e1831c055618a85854d9f7c427
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103884330"
---
# <a name="ice88"></a>ICE88

ICE88 verifica che la directory a cui viene fatto riferimento nella colonna DirProperty della [tabella inifile](inifile-table.md) esista nel pacchetto di Windows Installer. ICE88 genera un avviso se il valore DirProperty non rappresenta una proprietà nella directory, AppSearch, o nelle tabelle delle proprietà, in determinate [proprietà della cartella di sistema](property-reference.md)o in una proprietà impostata da un'azione personalizzata di tipo 51.

ICE88 analizza le seguenti tabelle e proprietà.

-   [Tabella directory](directory-table.md)
-   [Tabella AppSearch](appsearch-table.md)
-   [Tabella delle proprietà](property-table.md)
-   [Tabella CustomAction](customaction-table.md) , in cui l'azione personalizzata è un [tipo di azione personalizzata 51](custom-action-type-51.md)
-   [**Proprietà ProgramFilesFolder**](programfilesfolder.md)
-   [**Proprietà CommonFilesFolder**](commonfilesfolder.md)
-   [**Proprietà SystemFolder**](systemfolder.md)
-   [**Proprietà ProgramFiles64Folder**](programfiles64folder.md)
-   [**Proprietà CommonFiles64Folder**](commonfiles64folder.md)
-   [**Proprietà System64Folder**](system64folder.md)

## <a name="result"></a>Risultato

ICE88 invia il seguente avviso.



| Avviso di ICE88                                                                                                                                                                  | Descrizione                                                                                                                                                                                                                                                                                                                                                                     |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Nella voce della tabella IniFile (IniFile =) \[ 3 \] DirProperty = \[ 1 \] non è disponibile nelle tabelle directory/Property/AppSearch/CA-Type51 e non è una delle proprietà del programma di installazione. | Per ogni record nella tabella IniFile, ICE88 legge il valore nella colonna DirProperty. ICE88 analizza il valore nella tabella di [directory](directory-table.md), nella tabella [AppSearch](appsearch-table.md)e nella [tabella delle proprietà](property-table.md) e analizza anche l'elenco delle proprietà impostate dal programma di installazione. ICE88 Invia questo avviso se il valore non è stato trovato nell'analisi. |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Riferimento ghiaccio](ice-reference.md)
</dt> </dl>

 

 



