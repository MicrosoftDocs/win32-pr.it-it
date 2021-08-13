---
description: Questa sezione descrive come aggiungere stringhe di risorse alla tabella Windows collegamento del programma di installazione per l'uso con le interfacce utente multilingue (MUI).
ms.assetid: f521cfb8-32a8-4b62-b258-5b99cc3e0416
title: Esempio di collegamento MUI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b3b38f674a63e854fbcd4439229c5aded5b0efe6cfc17d3e475f8a52f30db949
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118640288"
---
# <a name="a-mui-shortcut-example"></a>Esempio di collegamento MUI

Questa sezione descrive come aggiungere stringhe di risorse alla tabella Windows [collegamento](shortcut-table.md) del programma di installazione per l'uso con le interfacce utente multilingue (MUI).

**Windows Installer 2.0 e Windows Installer 3.0:** Non supportato. Questo esempio richiede Windows Installer 4.0.

Per informazioni su [come sviluppare applicazioni abilitate per MUI,](/windows/desktop/Intl/multilingual-user-interface) vedere la documentazione di interfaccia utente multilingue (MUI).

Per aggiungere le stringhe di risorsa usate da Windows multilingue di Vista a un pacchetto Windows Installer:

1.  Aggiungere le informazioni per tutti i file indipendenti dalla lingua e alla tabella [file](file-table.md). Ad esempio, i file possono essere costituiti da un file indipendente dalla lingua (msimsg.dll) e da file di lingua per l'inglese (msimsgen.dll.mui), il giapponese (msimsgja.dll.mui) e il cinese (msimsgcs.dll.mui). Ogni file può appartenere a un componente diverso. Ogni file può avere un nome di file lungo e breve. Nel caso di questo esempio, è possibile aggiungere le informazioni seguenti alla [tabella file](file-table.md).

    [Tabella file](file-table.md) (parziale)

    

    | File        | Componente\_     | FileName                     |
    |-------------|-----------------|------------------------------|
    | msimsgmuija | MSIMSG \_ MUI \_ JA | msimsgja.dll\|msimsg.dll.mui |
    | msimsgmuics | MSIMSG \_ MUI \_ CS | msimsgcs.dll\|msimsg.dll.mui |
    | msimsgmuien | MSIMSG \_ MUI \_ EN | msimsgen.dll\|msimsg.dll.mui |
    | msimsgdll   | MSIMSG          | msimsg.dll                   |

    

     

2.  Aggiungere informazioni alla tabella [Componente per](component-table.md) questi componenti. Ogni componente ha un identificatore GUID univoco che deve essere immesso nel campo ComponentId della tabella Component. Il file appartenente al componente può fungere da KeyPath per tale componente. La directory che contiene ogni componente può essere specificata nel campo \_ Directory. Le informazioni seguenti possono essere aggiunte alla tabella Component.

    [Tabella dei componenti](component-table.md) (parziale)

    

    | Componente       | Directory\_   | KeyPath     |
    |-----------------|---------------|-------------|
    | MSIMSG \_ MUI \_ JA | MUIFolder \_ JA | msimsgmuija |
    | MSIMSG \_ MUI \_ CS | MUIFolder \_ CS | msimsgmuics |
    | MSIMSG \_ MUI \_ EN | MUIFolder \_ EN | msimsgmuien |
    | MSIMSG          | MUIFolder     | msimsgdll   |

    

     

3.  Modificare la [tabella Directory](directory-table.md) in modo che i componenti siano installati nelle directory corrette. Assicurarsi di includere informazioni sulla directory in cui verrà installato il collegamento. Ad esempio, le informazioni seguenti potrebbero essere aggiunte alla tabella Directory di un pacchetto che installa i componenti e un collegamento che si trova nella directory DesktopFolder.

    [Tabella directory](directory-table.md) (parziale)

    

    | Directory     | Directory \_ Parent | DefaultDir |
    |---------------|-------------------|------------|
    | Targetdir     |                   | SourceDir  |
    | MsiTest       | Targetdir         | MsiTest:.  |
    | MUIFolder     | MsiTest           | Mui        |
    | MUIFolder \_ CS | MUIFolder         | cs-CZ      |
    | MUIFolder \_ EN | MUIFolder         | en-US      |
    | MUIFolder \_ JA | MUIFolder         | ja-JP      |
    | Cartella Desktop | Targetdir         | .          |

    

     

4.  Aggiungere una riga alla tabella [Collegamento](shortcut-table.md) per ogni collegamento. Ad esempio, la [tabella Collegamento](shortcut-table.md) potrebbe contenere le informazioni seguenti per due collegamenti, Quick1 e Quick2, installati nella directory DirectoryFolder. Ogni collegamento appartiene alla funzionalità specificata nel campo Destinazione. L'icona associata al collegamento può essere specificata nel campo \_ Icona e nella [tabella](icon-table.md) Icona.

    [Tabella dei collegamenti](shortcut-table.md) (parziale)

    

    | Tasto di scelta rapida | Directory\_   | Componente\_ | Destinazione               | Icona             |
    |----------|---------------|-------------|----------------------|------------------|
    | Rapida1   | Cartella Desktop | MSIMSG      | FeatureChild1 \_ Local | HelpFileIcon.exe |
    | Rapida2   | Cartella Desktop | MSIMSG      | FeatureChild1 \_ Local | HelpFileIcon.exe |

    

     

5.  Aggiungere informazioni alla tabella [tabella delle funzionalità](feature-table.md) per l'appartenenza al collegamento di proprietà della funzionalità. Quando il collegamento viene attivato, il programma di installazione verifica che tutti i componenti appartenenti a questa funzionalità siano installati prima di avviare il file di chiave del componente specificato nella colonna Componente della tabella \_ [Collegamento.](shortcut-table.md) Nel caso di questo esempio, è possibile aggiungere le informazioni seguenti alla tabella Tabella delle funzionalità per la funzionalità Locale \_ FeatureParent1.

    [Tabella delle funzionalità](feature-table.md) (parziale)

    

    | Funzionalità               | Elemento padre \_ della funzionalità       | Title                 | Attributi |
    |-----------------------|-----------------------|-----------------------|------------|
    | Elemento FeatureParent1 \_ locale |                       | Elemento FeatureParent1 \_ locale | 16         |
    | FeatureChild1 \_ Local  | Elemento FeatureParent1 \_ locale | Elemento FeatureParent1 \_ locale | 0          |

    

     

6.  Per ogni nuovo collegamento, aggiungere le informazioni sulla stringa di risorsa nei campi DisplayResourceDLL, DisplayResourceId, DescriptionResourceDLL e DescriptionResourceId della tabella [Shortcut](shortcut-table.md). I campi DisplayResourceDLL e DescriptionResourceDLL contengono la stringa di risorsa nel [formato stringa](formatted.md) formattata. La stringa formattata può usare la \[ \# *convenzione filekey* \] del formato [formattato.](formatted.md) Aggiungere gli indici di visualizzazione e descrizione per le stringhe di risorsa nei campi DisplayResourceId e DescriptionResourceId.

    [Tabella dei collegamenti](shortcut-table.md) (parziale)

    

    | Tasto di scelta rapida | DisplayResourceDLL | DisplayResourceId | DescrizioneResourceDLL | DescriptionResourceId |
    |----------|--------------------|-------------------|------------------------|-----------------------|
    | Rapida1   | \[\#msimsgdll\]    | 36                | \[\#msimsgdll\]        | 37                    |
    | Rapida2   | \[\#msimsgdll\]    | 38                | \[\#msimsgdll\]        | 39                    |

    

     

7.  Dopo aver installato il pacchetto, testare per assicurarsi che il interfaccia utente multilingue funzioni come previsto.

 

 
