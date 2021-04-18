---
description: ICE91 pubblica un avviso se un file, un file con estensione ini o un file di collegamento è installato in una directory solo per singolo utente.
ms.assetid: 1834d841-b1d9-4646-8057-a41dd88310b6
title: ICE91
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 91f5723369c21894817dacbc1755430a31f17199
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106316272"
---
# <a name="ice91"></a>ICE91

ICE91 pubblica un avviso se un file, un file con estensione ini o un file di collegamento è installato in una directory solo per singolo utente. Questi avvisi sono innocui se il pacchetto viene usato solo per l'installazione nel contesto di [installazione](installation-context.md) per utente e mai usato per le installazioni per computer.

I file, i file con estensione ini o i collegamenti nelle directory solo per utente vengono installati nel profilo di un utente specifico. Anche se l'utente imposta la proprietà [**ALLUSERS**](allusers.md) per le installazioni per computer, i file, i file ini o i collegamenti nelle directory solo per singolo utente non vengono copiati nel profilo "tutti gli utenti" e non sono disponibili ad altri utenti. Le directory solo per utente non variano in base alla proprietà **ALLUSERS** . Di seguito è riportato un elenco delle directory solo per utente:

-   CartellaDatiApp
-   FavoritesFolder
-   NetHoodFolder
-   PersonalFolder
-   PrintHoodFolder
-   RecentFolder
-   SendToFolder
-   MyPicturesFolder
-   LocalAppDataFolder

## <a name="result"></a>Risultato

ICE91 invia gli avvisi seguenti.



| Avviso di ICE91                                                                                                                                                                                                                            | Descrizione                                                                                                                                |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------|
| Il file ' \[ 1 \] ' verrà installato nella directory per utente ' \[ 2 \] ' che non varia in base al valore di [**ALLUSERS**](allusers.md) . Il file non verrà copiato nel profilo di ogni utente anche se si desidera un'installazione per computer.     | Il file viene installato in una directory solo per singolo utente. Non viene installato nel profilo di ogni utente durante un'installazione per computer.      |
| Il IniFile ' \[ 1 \] ' verrà installato nella directory per utente ' \[ 2 \] ' che non varia in base al valore di [**ALLUSERS**](allusers.md) . Il file non verrà copiato nel profilo di ogni utente anche se si desidera un'installazione per computer.  | Il file ini viene installato in una directory solo per singolo utente. Non viene installato nel profilo di ogni utente durante un'installazione per computer. |
| Il collegamento ' \[ 1 \] ' verrà installato nella directory per utente ' \[ 2 \] ' che non varia in base al valore di [**ALLUSERS**](allusers.md) . Il file non verrà copiato nel profilo di ogni utente anche se si desidera un'installazione per computer. | Il collegamento viene installato in una directory solo per singolo utente. Non viene installato nel profilo di ogni utente durante un'installazione per computer.  |



 

## <a name="example"></a>Esempio

ICE91 segnala gli avvisi seguenti per l'esempio:

``` syntax
The file 'File1' will be installed to the per user directory 'MyPicturesFolder' that does not vary based on ALLUSERS value. This file won't be copied to each user's profile even if a per machine installation is desired.

The IniFile 'IniFile1' will be installed to the per user directory 'MyIniDir' that does not vary based on ALLUSERS value. This file won't be copied to each user's profile even if a per machine installation is desired.

The shortcut 'Shortcut1' will be installed to the per user directory 'MyShortcutDir' that does not vary based on ALLUSERS value. This file won't be copied to each user's profile even if a per machine installation is desired.
```

[Tabella file](file-table.md) (parziale)



| File  | Componente\_ |
|-------|-------------|
| File1 | C1          |



 

[Tabella componenti](component-table.md) (parziale) (parziale) (parziale) (parziale)



| Componente | Directory\_ |
|-----------|-------------|
| C1        | MyDir       |



 

[Tabella IniFile](inifile-table.md)



| IniFile  | DirProperty |
|----------|-------------|
| IniFile1 | MyIniDir    |



 

[Tabella di collegamento](shortcut-table.md)



| Tasto di scelta rapida  | Directory\_   |
|-----------|---------------|
| Shortcut1 | MyShortcutDir |



 

[Tabella directory](directory-table.md)



| Directory     | \_Padre directory  |
|---------------|--------------------|
| MyDir         | FavoritesFolder    |
| MyIniDir      | LocalAppDataFolder |
| MyShortcutDir | PersonalFolder     |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Riferimento ghiaccio](ice-reference.md)
</dt> </dl>

 

 



