---
title: Supporto per automazione interfaccia utente dei controlli standard
description: Questo argomento identifica i controlli Windows standard supportati dall'automazione interfaccia utente Microsoft. Il supporto completo viene fornito solo per i controlli della versione 6 di ComCtrl32.dll (disponibile in Windows XP e versioni successive).
ms.assetid: 4821684c-8a90-413c-8ddc-699926e3bb09
keywords:
- client, supporto di automazione interfaccia utente per i controlli standard
- client, supporto del controllo standard
- client, controlli Win32
- Automazione interfaccia utente, supporto per controlli standard
- Automazione interfaccia utente, supporto del controllo standard
- Automazione interfaccia utente, controlli Win32
- supporto per i controlli standard
- supporto del controllo standard
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ae6e384b9ee0fd72fd8a41aa3f791a5c996fe6d6
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104515535"
---
# <a name="ui-automation-support-for-standard-controls"></a>Supporto per automazione interfaccia utente dei controlli standard

Questo argomento identifica i controlli Windows standard supportati dall'automazione interfaccia utente Microsoft. Il supporto completo viene fornito solo per i controlli della versione 6 di ComCtrl32.dll (disponibile in Windows XP e versioni successive).

> [!Note]  
> Il controllo RichEdit è supportato solo per le versioni fornite con Windows Vista (in RichEd20.dll versione 3,1 e successive e MsftEdit.dll versione 4,1 e successive).

 

La tabella seguente elenca i nomi delle classi dei controlli standard supportati, insieme ai corrispondenti tipi di controllo di automazione interfaccia utente.



| Nome della classe          | Tipo di controllo        |
|---------------------|---------------------|
| Button              | Button              |
| Button              | RadioButton         |
| Pulsante              | Group               |
| Pulsante              | CheckBox            |
| Pulsante              | Hyperlink           |
| Pulsante              | SplitButton         |
| Pulsante              | CheckBox            |
| ComboBoxEx32        | ComboBox            |
| ComboBox            | ComboBox            |
| Modifica                | Documento            |
| Modifica                | Modifica                |
| SysLink             | Hyperlink           |
| Static              | Testo                |
| Static              | Immagine               |
| SysIPAddress32      | Personalizzato              |
| SysHeader32         | Header/HeaderItem   |
| SysListView32       | DataGrid            |
| SysListView32       | Elenco                |
| ListBox             | Elenco                |
| ListBox             | ListItem            |
| \#32768             | Menu                |
| \#32768             | MenuItem            |
| \_progress32 msctls  | ProgressBar         |
| RichEdit            | Documento. Vedere la nota. |
| RichEdit20A         | Documento            |
| RichEdit20W         | Documento            |
| RichEdit50W         | Documento            |
| ScrollBar           | Slider              |
| \_trackbar32 msctls  | Slider              |
| \_updown32 msctls    | Spinner             |
| \_statusbar32 msctls | StatusBar           |
| SysTabControl32     | Scheda                 |
| SysTabControl32     | TabItem             |
| ToolbarWindow32     | ToolBar             |
| ToolbarWindow32     | MenuItem            |
| ToolbarWindow32     | Pulsante              |
| ToolbarWindow32     | CheckBox            |
| ToolbarWindow32     | RadioButton         |
| ToolbarWindow32     | Separatore           |
| descrizioni comandi \_ class32   | ToolTip             |
| \#32774             | ToolTip             |
| ReBarWindow32       | Barra degli strumenti             |
| SysTreeView32       | Albero                |
| SysTreeView32       | TreeItem            |



 

I controlli elencati nella tabella seguente non sono supportati.



| Nome della classe                                    | Tipo di controllo |
|-----------------------------------------------|--------------|
| SysAnimate32                                  | Immagine        |
| SysPager                                      | Spinner      |
| SysDateTimePick32                             | Personalizzato       |
| SysMonthCal32                                 | Calendario     |
| MS \_ WINNOTE                                   | Descrizione comando      |
| VBBubble                                      | Descrizione comando      |
| ScrollBar (se usato come controllo autonomo) | Slider       |
| SuperGrid                                     | Personalizzato       |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Cenni preliminari sui tipi di controllo per l'automazione interfaccia utente](uiauto-controltypesoverview.md)
</dt> </dl>

 

 




