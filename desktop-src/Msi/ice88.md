---
description: ICE88 verifica che la directory a cui viene fatto riferimento nella colonna DirProperty della tabella IniFile sia presente nel pacchetto Windows Installer.
ms.assetid: 9bb253fd-e231-4016-807d-3b1068ecff68
title: ICE88
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5cb49ce6cb4363cfe89879f6e72b7ce801c063ea2b278c03dacf5cbadacddce9
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120105221"
---
# <a name="ice88"></a>ICE88

ICE88 verifica che la directory a cui viene fatto riferimento nella colonna DirProperty della tabella [IniFile](inifile-table.md) sia presente nel pacchetto Windows Installer. ICE88 restituisce un avviso se il valore DirProperty non rappresenta una proprietà nelle [](property-reference.md)tabelle Directory, AppSearch o Property, alcune proprietà della cartella di sistema o una proprietà impostata da un'azione personalizzata di tipo 51.

ICE88 analizza le tabelle e le proprietà seguenti.

-   [Tabella directory](directory-table.md)
-   [Tabella AppSearch](appsearch-table.md)
-   [Tabella delle proprietà](property-table.md)
-   [Tabella CustomAction](customaction-table.md) , in cui l'azione personalizzata è [un tipo di azione personalizzata 51](custom-action-type-51.md)
-   [**Proprietà ProgramFilesFolder**](programfilesfolder.md)
-   [**CommonFilesFolder - proprietà**](commonfilesfolder.md)
-   [**Proprietà SystemFolder**](systemfolder.md)
-   [**Proprietà ProgramFiles64Folder**](programfiles64folder.md)
-   [**CommonFiles64Folder - proprietà**](commonfiles64folder.md)
-   [**Proprietà System64Folder**](system64folder.md)

## <a name="result"></a>Risultato

ICE88 pubblica l'avviso seguente.



| Avviso ICE88                                                                                                                                                                  | Descrizione                                                                                                                                                                                                                                                                                                                                                                     |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Nella voce di tabella IniFile (IniFile=) 3 di DirProperty= 1 non è presente nelle tabelle \[ \] \[ Directory/Property/AppSearch/CA-Type51 e non è una delle proprietà del programma di \] installazione. | Per ogni record nella tabella IniFile, ICE88 legge il valore nella colonna DirProperty. ICE88 analizza il valore in [Tabella directory](directory-table.md), [](property-table.md) [Tabella AppSearch](appsearch-table.md)e Tabella delle proprietà e analizza anche l'elenco delle proprietà impostate dal programma di installazione. ICE88 invia questo avviso se non è possibile trovare il valore nell'analisi. |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Informazioni di riferimento su ICE](ice-reference.md)
</dt> </dl>

 

 



