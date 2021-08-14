---
title: Resource-Definition istruzioni
description: Le istruzioni di definizione delle risorse definiscono le risorse che il compilatore di risorse inserisce nella risorsa (. Res) file.
ms.assetid: f96b8c1e-8188-40b7-8eda-c13b61b8fc41
keywords:
- compilatore di risorse, istruzioni di definizione delle risorse
- Risorsa TEXTINCLUDE
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4937eb9d5fb9bba7b174aa9543be8b3f2eb41c90c6bc20a72650114f57fb4fa8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117869907"
---
# <a name="resource-definition-statements"></a>Resource-Definition istruzioni

Le istruzioni di definizione delle risorse definiscono le risorse che il compilatore di risorse inserisce nella risorsa (. Res) file. Dopo l'oggetto . Il file Res è collegato al file eseguibile. L'applicazione può caricare le risorse in fase di esecuzione in base alle esigenze. Tutte le istruzioni di risorsa associano un nome o un numero di identificazione a una determinata risorsa.

Le istruzioni di definizione delle risorse possono essere suddivise nelle categorie seguenti:

-   Risorse
-   Controlli
-   Istruzioni

Le tabelle seguenti descrivono le istruzioni di definizione delle risorse.

## <a name="resources"></a>Risorse



| Resource                                      | Descrizione                                                                                                                                                                     |
|-----------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Acceleratori**](accelerators-resource.md) | Definisce i tasti di scelta rapida del menu.                                                                                                                                                  |
| [**Bitmap**](bitmap-resource.md)             | Definisce una bitmap assegnando un nome e specificando il nome del file che la contiene. Per usare una particolare bitmap, l'applicazione la richiede in base al nome.                          |
| [**Cursore**](cursor-resource.md)             | Definisce un cursore o un cursore animato assegnandogli un nome e specificando il nome del file che lo contiene. Per usare un cursore specifico, l'applicazione lo richiede in base al nome.       |
| [**Dialogo**](dialog-resource.md)             | Definisce un modello che un'applicazione può usare per creare finestre di dialogo.                                                                                                          |
| [**DIALOGEX**](dialogex-resource.md)         | Definisce un modello che un'applicazione può usare per creare finestre di dialogo.                                                                                                          |
| [**Carattere**](font-resource.md)                 | Specifica il nome di un file che contiene un tipo di carattere.                                                                                                                              |
| [**HTML**](html-resource.md)                 | Specifica un file HTML.                                                                                                                                                         |
| [**Icona**](icon-resource.md)                 | Definisce un'icona o un'icona animata assegnando un nome e specificando il nome del file che la contiene. Per usare una particolare icona, l'applicazione la richiede in base al nome.            |
| [**Menu**](menu-resource.md)                 | Definisce l'aspetto e la funzione di un menu.                                                                                                                                  |
| [**MENUEX**](menuex-resource.md)             | Definisce l'aspetto e la funzione di un menu.                                                                                                                                  |
| [**MESSAGETABLE**](messagetable-resource.md) | Definisce una tabella dei messaggi denominarla e specificando il nome del file che la contiene. Il file è un file di risorse binario generato dal compilatore di messaggi.                |
| [**Popup**](popup-resource.md)               | Definisce una voce di menu che può contenere voci di menu e sottomenu.                                                                                                                   |
| **PLUGPLAY**                                  | Obsoleta.                                                                                                                                                                       |
| [**RCDATA**](rcdata-resource.md)             | Definisce le risorse dati. Le risorse dati consentono di includere dati binari nel file eseguibile.                                                                                      |
| [**Stringtable**](stringtable-resource.md)   | Definisce le risorse stringa. Le risorse stringa sono stringhe Unicode o ASCII che possono essere caricate dal file eseguibile.                                                            |
| **TEXTINCLUDE**                               | Risorsa speciale interpretata da Visual C++. Per altre informazioni, vedere [TN035](/cpp/mfc/tn035-using-multiple-resource-files-and-header-files-with-visual-cpp?view=vs-2019).                                        |
| **TYPELIB**                                   | Risorsa speciale usata con le opzioni del linker [/TLBID](/cpp/build/reference/tlbid-specify-resource-id-for-typelib?view=vs-2019) e [/TLBOUT.](/cpp/build/reference/tlbout-name-dot-tlb-file?view=vs-2019) |
| [**Definito dall'utente**](user-defined-resource.md) | Definisce una risorsa che contiene dati specifici dell'applicazione.                                                                                                                     |
| [**VERSIONINFO**](versioninfo-resource.md)   | Definisce una risorsa di informazioni sulla versione. Contiene informazioni quali il numero di versione, il sistema operativo previsto e così via.                                                  |
| **Vxd**                                       | Obsoleta.                                                                                                                                                                       |



 

Per altre informazioni sulle risorse MFC predefinite, vedere [TN023](/cpp/mfc/tn023-standard-mfc-resources?view=vs-2019) e [TN024.](/cpp/mfc/tn024-mfc-defined-messages-and-resources?view=vs-2019)

## <a name="controls"></a>Controlli



| Controllo                                            | Descrizione                                                                 |
|----------------------------------------------------|-----------------------------------------------------------------------------|
| [**AUTO3STATE**](auto3state-control.md)           | Crea un controllo casella di controllo a tre stati automatico.                         |
| [**AUTOCHECKBOX**](autocheckbox-control.md)       | Crea un controllo casella di controllo automatico.                                     |
| [**AUTORADIOBUTTON**](autoradiobutton-control.md) | Crea un controllo pulsante di opzione automatico.                                  |
| [**Casella**](checkbox-control.md)               | Crea un controllo casella di controllo.                                                |
| [**Combobox**](combobox-control.md)               | Crea un controllo casella combinata.                                                |
| [**Controllo**](control-control.md)                 | Crea un controllo definito dall'applicazione.                                     |
| [**CTEXT**](ctext-control.md)                     | Crea un controllo di testo centrato.                                            |
| [**DEFPUSHBUTTON**](defpushbutton-control.md)     | Crea un controllo pulsante di comando predefinito.                                       |
| [**EDITTEXT**](edittext-control.md)               | Crea un controllo di modifica.                                                    |
| [**Groupbox**](groupbox-control.md)               | Crea un controllo casella di gruppo.                                                |
| [**Icona**](icon-control.md)                       | Crea un controllo icona. Questo controllo è un'icona visualizzata in una finestra di dialogo. |
| [**Listbox**](listbox-control.md)                 | Crea un controllo casella di riepilogo.                                                 |
| [**LTEXT**](ltext-control.md)                     | Crea un controllo testo allineato a sinistra.                                        |
| [**PUSHBOX**](pushbox-control.md)                 | Crea un controllo casella di push.                                                 |
| [**Pulsante**](pushbutton-control.md)           | Crea un controllo pulsante di push.                                              |
| [**Radiobutton**](radiobutton-control.md)         | Crea un controllo pulsante di opzione.                                             |
| [**Rtext**](rtext-control.md)                     | Crea un controllo allineato a destra.                                            |
| [**Scrollbar**](scrollbar-control.md)             | Crea un controllo barra di scorrimento.                                               |
| [**STATE3**](state3-control.md)                   | Crea un controllo casella di controllo a tre stati.                                    |



 

## <a name="statements"></a>Istruzioni



| Istruzione                                            | Descrizione                                                                                                                                                                                                                                                                                                                                                                                                                                                                                 |
|------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Didascalia**](caption-statement.md)                 | Imposta il titolo di una finestra di dialogo.                                                                                                                                                                                                                                                                                                                                                                                                                                                            |
| [**Caratteristiche**](characteristics-statement.md) | Specifica informazioni su una risorsa che può essere usata dallo strumento che può leggere o scrivere file di definizione delle risorse.                                                                                                                                                                                                                                                                                                                                                                           |
| [**Classe**](class-statement.md)                     | Imposta la classe della finestra di dialogo.                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
| [**EXSTYLE**](exstyle-statement.md)                 | Imposta lo stile della finestra estesa della finestra di dialogo.                                                                                                                                                                                                                                                                                                                                                                                                                                           |
| [**Carattere**](font-statement.md)                       | Imposta il tipo di carattere con cui il sistema disegna il testo per la finestra di dialogo.                                                                                                                                                                                                                                                                                                                                                                                                                      |
| [**Lingua**](language-statement.md)               | Imposta la lingua per tutte le risorse fino all'istruzione [**LANGUAGE**](language-statement.md) successiva o alla fine del file. Quando **l'istruzione LANGUAGE** viene visualizzata prima dell'inizio del corpo di una definizione di risorsa [**ACCELERATORS**](accelerators-resource.md), [**DIALOG**](dialog-resource.md), [**MENU**](menu-resource.md), [**RCDATA**](rcdata-resource.md)o [**STRINGTABLE,**](stringtable-resource.md) il linguaggio specificato si applica solo a tale risorsa. |
| [**Menu**](menu-statement.md)                       | Imposta il menu per la finestra di dialogo.                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
| [**Menuitem**](menuitem-statement.md)               | Definisce una voce di menu.                                                                                                                                                                                                                                                                                                                                                                                                                                                                        |
| [**Stile**](style-statement.md)                     | Imposta lo stile della finestra per la finestra di dialogo.                                                                                                                                                                                                                                                                                                                                                                                                                                                   |
| [**Versione**](version-statement.md)                 | Specifica le informazioni sulla versione per una risorsa che può essere usata dallo strumento che può leggere o scrivere file di definizione delle risorse.                                                                                                                                                                                                                                                                                                                                                                     |



 

 

 