---
title: Istruzioni Resource-Definition
description: Le istruzioni per la definizione delle risorse definiscono le risorse inserite dal compilatore di risorse nella risorsa. File res).
ms.assetid: f96b8c1e-8188-40b7-8eda-c13b61b8fc41
keywords:
- compilatore di risorse, istruzioni per la definizione delle risorse
- Risorsa TEXTINCLUDE
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8887c002bc3564288eb99fdb373ac26c286d1bf7
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2020
ms.locfileid: "103963071"
---
# <a name="resource-definition-statements"></a>Istruzioni Resource-Definition

Le istruzioni per la definizione delle risorse definiscono le risorse inserite dal compilatore di risorse nella risorsa. File res). Dopo l'. Il file res è collegato al file eseguibile, l'applicazione può caricare le risorse in fase di esecuzione in base alle esigenze. Tutte le istruzioni Resource associano un nome o un numero di identificazione a una determinata risorsa.

Le istruzioni per la definizione delle risorse possono essere divise nelle categorie seguenti:

-   Risorse
-   Controlli
-   Istruzioni

Nelle tabelle seguenti vengono descritte le istruzioni per la definizione delle risorse.

## <a name="resources"></a>Risorse



| Resource                                      | Descrizione                                                                                                                                                                     |
|-----------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**ACCELERATORI**](accelerators-resource.md) | Definisce i tasti di scelta rapida di menu.                                                                                                                                                  |
| [**BITMAP**](bitmap-resource.md)             | Definisce una bitmap chiamandola e specificando il nome del file che la contiene. (Per usare una particolare bitmap, l'applicazione lo richiede per nome).                          |
| [**CURSORE**](cursor-resource.md)             | Definisce un cursore o un cursore animato per denominarlo e specificare il nome del file che lo contiene. (Per usare un particolare cursore, l'applicazione lo richiede per nome).       |
| [**DIALOGO**](dialog-resource.md)             | Definisce un modello che può essere utilizzato da un'applicazione per creare finestre di dialogo.                                                                                                          |
| [**DIALOGEX**](dialogex-resource.md)         | Definisce un modello che può essere utilizzato da un'applicazione per creare finestre di dialogo.                                                                                                          |
| [**CARATTERE**](font-resource.md)                 | Specifica il nome di un file che contiene un tipo di carattere.                                                                                                                              |
| [**HTML**](html-resource.md)                 | Specifica un file HTML.                                                                                                                                                         |
| [**ICONA**](icon-resource.md)                 | Definisce un'icona o un'icona animata chiamandola e specificando il nome del file che la contiene. (Per usare una particolare icona, l'applicazione lo richiede per nome).            |
| [**MENU**](menu-resource.md)                 | Definisce l'aspetto e la funzione di un menu.                                                                                                                                  |
| [**MENUEX**](menuex-resource.md)             | Definisce l'aspetto e la funzione di un menu.                                                                                                                                  |
| [**MESSAGETABLE**](messagetable-resource.md) | Definisce una tabella messaggi chiamandola e specificando il nome del file che la contiene. Il file è un file di risorse binario generato dal compilatore di messaggi.                |
| [**POPUP**](popup-resource.md)               | Definisce una voce di menu che può contenere voci di menu e sottomenu.                                                                                                                   |
| **PLUGPLAY**                                  | Obsoleta.                                                                                                                                                                       |
| [**RCDATA**](rcdata-resource.md)             | Definisce le risorse di dati. Le risorse di dati consentono di includere dati binari nel file eseguibile.                                                                                      |
| [**UN'STRINGTABLE**](stringtable-resource.md)   | Definisce le risorse di stringa. Le risorse di tipo stringa sono stringhe Unicode o ASCII che possono essere caricate dal file eseguibile.                                                            |
| **TEXTINCLUDE**                               | Risorsa speciale interpretata da Visual C++. Per ulteriori informazioni, vedere [TN035](/cpp/mfc/tn035-using-multiple-resource-files-and-header-files-with-visual-cpp?view=vs-2019).                                        |
| **TYPELIB**                                   | Risorsa speciale utilizzata con le opzioni del linker [/TLBID](/cpp/build/reference/tlbid-specify-resource-id-for-typelib?view=vs-2019) e [/TLBOUT](/cpp/build/reference/tlbout-name-dot-tlb-file?view=vs-2019) . |
| [**Definito dall'utente**](user-defined-resource.md) | Definisce una risorsa che contiene dati specifici dell'applicazione.                                                                                                                     |
| [**VERSIONINFO**](versioninfo-resource.md)   | Definisce una risorsa di informazioni sulla versione. Contiene informazioni quali il numero di versione, il sistema operativo previsto e così via.                                                  |
| **VXD**                                       | Obsoleta.                                                                                                                                                                       |



 

Per ulteriori informazioni sulle risorse MFC predefinite, vedere [TN023](/cpp/mfc/tn023-standard-mfc-resources?view=vs-2019) e [TN024](/cpp/mfc/tn024-mfc-defined-messages-and-resources?view=vs-2019).

## <a name="controls"></a>Controlli



| Controllo                                            | Descrizione                                                                 |
|----------------------------------------------------|-----------------------------------------------------------------------------|
| [**AUTO3STATE**](auto3state-control.md)           | Crea un controllo casella di controllo automatico a tre stati.                         |
| [**CASELLA di controllo AUTOCHECKBOX**](autocheckbox-control.md)       | Crea un controllo casella di controllo automatico.                                     |
| [**RADIOBUTTON**](autoradiobutton-control.md) | Crea un controllo pulsante di opzione automatico.                                  |
| [**CASELLA**](checkbox-control.md)               | Crea un controllo casella di controllo.                                                |
| [**COMBOBOX**](combobox-control.md)               | Crea un controllo casella combinata.                                                |
| [**CONTROLLO**](control-control.md)                 | Crea un controllo definito dall'applicazione.                                     |
| [**CTEXT**](ctext-control.md)                     | Crea un controllo di testo centrato.                                            |
| [**DEFPUSHBUTTON**](defpushbutton-control.md)     | Crea un controllo pulsante predefinito.                                       |
| [**EDITTEXT**](edittext-control.md)               | Crea un controllo di modifica.                                                    |
| [**GROUPBOX**](groupbox-control.md)               | Crea un controllo casella di gruppo.                                                |
| [**ICONA**](icon-control.md)                       | Crea un controllo icona. Questo controllo è un'icona visualizzata in una finestra di dialogo. |
| [**LISTBOX**](listbox-control.md)                 | Crea un controllo casella di riepilogo.                                                 |
| [**LTEXT**](ltext-control.md)                     | Crea un controllo di testo allineato a sinistra.                                        |
| [**PUSHBOX**](pushbox-control.md)                 | Crea un controllo casella di push.                                                 |
| [**PULSANTE**](pushbutton-control.md)           | Crea un controllo pulsante di comando.                                              |
| [**RADIOBUTTON**](radiobutton-control.md)         | Crea un controllo pulsante di opzione.                                             |
| [**RTEXT**](rtext-control.md)                     | Crea un controllo allineato a destra.                                            |
| [**SCROLLBAR**](scrollbar-control.md)             | Crea un controllo barra di scorrimento.                                               |
| [**STATE3**](state3-control.md)                   | Crea un controllo casella di controllo a tre stati.                                    |



 

## <a name="statements"></a>Istruzioni



| Istruzione                                            | Descrizione                                                                                                                                                                                                                                                                                                                                                                                                                                                                                 |
|------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**DIDASCALIA**](caption-statement.md)                 | Imposta il titolo di una finestra di dialogo.                                                                                                                                                                                                                                                                                                                                                                                                                                                            |
| [**CARATTERISTICHE**](characteristics-statement.md) | Specifica le informazioni su una risorsa che può essere usata dallo strumento in grado di leggere o scrivere file di definizione delle risorse.                                                                                                                                                                                                                                                                                                                                                                           |
| [**CLASSE**](class-statement.md)                     | Imposta la classe della finestra di dialogo.                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
| [**EXSTYLE**](exstyle-statement.md)                 | Imposta lo stile della finestra estesa della finestra di dialogo.                                                                                                                                                                                                                                                                                                                                                                                                                                           |
| [**CARATTERE**](font-statement.md)                       | Imposta il tipo di carattere con cui il sistema trarrà il testo per la finestra di dialogo.                                                                                                                                                                                                                                                                                                                                                                                                                      |
| [**LINGUAGGIO**](language-statement.md)               | Imposta la lingua per tutte le risorse fino alla successiva istruzione della [**lingua**](language-statement.md) o alla fine del file. Quando l'istruzione **Language** viene visualizzata prima dell'inizio del corpo di un [**acceleratore**](accelerators-resource.md), una [**finestra di dialogo**](dialog-resource.md), un [**menu**](menu-resource.md), un [**RCDATA**](rcdata-resource.md)o una definizione di risorsa [**un'STRINGTABLE**](stringtable-resource.md) , la lingua specificata si applica solo a tale risorsa. |
| [**MENU**](menu-statement.md)                       | Imposta il menu per la finestra di dialogo.                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
| [**MENUITEM**](menuitem-statement.md)               | Definisce una voce di menu.                                                                                                                                                                                                                                                                                                                                                                                                                                                                        |
| [**STILE**](style-statement.md)                     | Imposta lo stile della finestra per la finestra di dialogo.                                                                                                                                                                                                                                                                                                                                                                                                                                                   |
| [**Versione**](version-statement.md)                 | Specifica le informazioni sulla versione per una risorsa che può essere usata dallo strumento in grado di leggere o scrivere file di definizione delle risorse.                                                                                                                                                                                                                                                                                                                                                                     |



 

 

 