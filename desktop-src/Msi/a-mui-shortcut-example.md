---
description: Questa sezione descrive come aggiungere stringhe di risorse alla tabella dei collegamenti Windows Installer per l'uso con MUI (Multilingual User Interface).
ms.assetid: f521cfb8-32a8-4b62-b258-5b99cc3e0416
title: Esempio di collegamento MUI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0392713c1eaedabaa989baecd79478a9b329e955
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106311102"
---
# <a name="a-mui-shortcut-example"></a>Esempio di collegamento MUI

Questa sezione descrive come aggiungere stringhe di risorse alla tabella dei [collegamenti](shortcut-table.md) Windows Installer per l'uso con MUI (Multilingual User Interface).

**Windows Installer 2,0 e Windows Installer 3,0:** Non supportato. Questo esempio richiede Windows Installer 4,0.

Per informazioni sullo sviluppo di applicazioni abilitate per MUI, vedere la documentazione relativa all' [interfaccia utente multilingue (MUI)](/windows/desktop/Intl/multilingual-user-interface) .

Per aggiungere le stringhe di risorse utilizzate dalle interfacce utente multilingue di Windows Vista a un pacchetto di Windows Installer:

1.  Aggiungere le informazioni per tutti i file di lingua e indipendenti dalla lingua alla [tabella dei file](file-table.md). I file possono ad esempio essere costituiti da un file indipendente dalla lingua (msimsg.dll) e da file di lingua per l'inglese (msimsgen.dll. MUI), giapponese (msimsgja.dll. MUI) e cinese (msimsgcs.dll. MUI). Ogni file può appartenere a un altro componente. Ogni file può avere un nome file lungo e breve. Nel caso di questo esempio, è possibile aggiungere le informazioni seguenti alla [tabella file](file-table.md).

    [Tabella file](file-table.md) (parziale)

    

    | File        | Componente\_     | FileName                     |
    |-------------|-----------------|------------------------------|
    | msimsgmuija | MSIMSG \_ MUI \_ ja | msimsgja.dll\|msimsg.dll. mui |
    | msimsgmuics | MSIMSG \_ MUI \_ CS | msimsgcs.dll\|msimsg.dll. mui |
    | msimsgmuien | MSIMSG \_ MUI \_ it | msimsgen.dll\|msimsg.dll. mui |
    | msimsgdll   | MSIMSG          | msimsg.dll                   |

    

     

2.  Aggiungere informazioni alla [tabella](component-table.md) dei componenti per questi componenti. Ogni componente dispone di un identificatore GUID univoco da immettere nel campo ComponentId della tabella Component. Il file che appartiene al componente può fungere da percorso di un elemento di un componente. La directory che contiene ogni componente può essere specificata nel campo Directory \_ . È possibile aggiungere le informazioni seguenti alla tabella Component.

    [Tabella componenti](component-table.md) (parziale)

    

    | Componente       | Directory\_   | KeyPath     |
    |-----------------|---------------|-------------|
    | MSIMSG \_ MUI \_ ja | MUIFolder \_ ja | msimsgmuija |
    | MSIMSG \_ MUI \_ CS | MUIFolder \_ CS | msimsgmuics |
    | MSIMSG \_ MUI \_ it | MUIFolder \_ en | msimsgmuien |
    | MSIMSG          | MUIFolder     | msimsgdll   |

    

     

3.  Modificare la tabella di [directory](directory-table.md) in modo che i componenti vengano installati nelle directory corrette. Assicurarsi di includere le informazioni sulla directory in cui verrà installato il collegamento. Ad esempio, le informazioni seguenti potrebbero essere aggiunte alla tabella di directory di un pacchetto che installa i componenti e un collegamento situato nella directory includevano

    [Tabella directory](directory-table.md) (parziale)

    

    | Directory     | \_Padre directory | DefaultDir |
    |---------------|-------------------|------------|
    | TARGETDIR     |                   | SourceDir  |
    | MsiTest       | TARGETDIR         | MsiTest:.  |
    | MUIFolder     | MsiTest           | MUI        |
    | MUIFolder \_ CS | MUIFolder         | cs-CZ      |
    | MUIFolder \_ en | MUIFolder         | en-US      |
    | MUIFolder \_ ja | MUIFolder         | ja-JP      |
    | Includevano | TARGETDIR         | .          |

    

     

4.  Aggiungere una riga alla tabella dei [collegamenti](shortcut-table.md) per ogni collegamento. Ad esempio, la tabella dei [collegamenti](shortcut-table.md) potrebbe contenere le informazioni seguenti per due collegamenti, Quick1 e Quick2, installati nella directory DirectoryFolder. Ogni collegamento appartiene alla funzionalità specificata nel campo di destinazione. L'icona associata al tasto di scelta rapida può essere specificata nel \_ campo icona e nella tabella [Icone](icon-table.md) .

    [Tabella collegamenti](shortcut-table.md) (parziale)

    

    | Tasto di scelta rapida | Directory\_   | Componente\_ | Destinazione               | Icona             |
    |----------|---------------|-------------|----------------------|------------------|
    | Quick1   | Includevano | MSIMSG      | FeatureChild1 \_ locale | HelpFileIcon.exe |
    | Quick2   | Includevano | MSIMSG      | FeatureChild1 \_ locale | HelpFileIcon.exe |

    

     

5.  Aggiungere informazioni alla tabella della [tabella delle funzionalità](feature-table.md) per la funzionalità di cui appartiene il collegamento. Quando il collegamento viene attivato, il programma di installazione verifica che tutti i componenti appartenenti a questa funzionalità siano installati prima di avviare il file di chiave del componente specificato nella \_ colonna componente della tabella dei [collegamenti](shortcut-table.md) . Nel caso di questo esempio, è possibile aggiungere le informazioni seguenti alla tabella della tabella delle funzionalità per la \_ funzionalità locale FeatureParent1.

    [Tabella delle funzionalità](feature-table.md) (parziale)

    

    | Funzionalità               | \_Elemento padre della funzionalità       | Titolo                 | Attributi |
    |-----------------------|-----------------------|-----------------------|------------|
    | FeatureParent1 \_ locale |                       | FeatureParent1 \_ locale | 16         |
    | FeatureChild1 \_ locale  | FeatureParent1 \_ locale | FeatureParent1 \_ locale | 0          |

    

     

6.  Per ogni nuovo collegamento, aggiungere le informazioni sulla stringa di risorsa ai campi DisplayResourceDLL, DisplayResourceId, DescriptionResourceDLL e DescriptionResourceId della [tabella dei collegamenti](shortcut-table.md). I campi DisplayResourceDLL e DescriptionResourceDLL contengono la stringa di risorsa nel formato stringa [formattato](formatted.md) . La stringa formattata può utilizzare la \[ \# convenzione *FileKey* \] del formato [formattato](formatted.md) . Aggiungere gli indici di visualizzazione e descrizione per le stringhe di risorsa nei campi DisplayResourceId e DescriptionResourceId.

    [Tabella collegamenti](shortcut-table.md) (parziale)

    

    | Tasto di scelta rapida | DisplayResourceDLL | DisplayResourceId | DescriptionResourceDLL | DescriptionResourceId |
    |----------|--------------------|-------------------|------------------------|-----------------------|
    | Quick1   | \[\#msimsgdll\]    | 36                | \[\#msimsgdll\]        | 37                    |
    | Quick2   | \[\#msimsgdll\]    | 38                | \[\#msimsgdll\]        | 39                    |

    

     

7.  Dopo aver installato il pacchetto, eseguire un test per assicurarsi che l'interfaccia utente multilingue funzioni come previsto.

 

 
