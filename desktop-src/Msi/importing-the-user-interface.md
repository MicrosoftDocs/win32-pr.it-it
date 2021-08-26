---
description: Oltre alle informazioni descritte nelle sezioni precedenti, uisample.msi contiene anche dati per un'interfaccia utente di esempio.
ms.assetid: 7e4ae4b8-e7b2-49b3-97b7-374b69006a2f
title: Importazione del Interfaccia utente
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2678eb2c6fb1c53f0d052c6bb1553af0f3d773b75d057969c66d74a39e499f35
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120043641"
---
# <a name="importing-the-user-interface"></a>Importazione del Interfaccia utente

Oltre alle informazioni descritte nelle sezioni precedenti, uisample.msi contiene anche dati per un'interfaccia utente di esempio. Se è stato unito uisample.msi in MNP2000.msi nella sezione Importazione di un [database](importing-a-blank-database.md)vuoto, queste informazioni sono presenti anche in MNP2000.msi. Le informazioni per l'interfaccia utente di esempio sono disponibili nelle tabelle seguenti.

-   [Tabella ActionText](actiontext-table.md)
-   [Tabella binaria](binary-table.md)
-   [Tabella di controllo](control-table.md)
-   [Tabella ControlEvent](controlevent-table.md)
-   [Tabella della finestra di dialogo](dialog-table.md)
-   [Tabella degli errori](error-table.md)
-   [Tabella EventMapping](eventmapping-table.md)
-   [Tabella RadioButton](radiobutton-table.md)
-   [Tabella TextStyle](textstyle-table.md)
-   [Tabella UIText](uitext-table.md)

L'editor di database Orca fornito con il programma di installazione include un'opzione di anteprima della finestra di dialogo che è possibile usare per visualizzare in anteprima le finestre di dialogo dell'interfaccia utente specificata dai dati nelle tabelle precedenti.

Il pacchetto di installazione di MNP2000.msi è ora pronto per la convalida del pacchetto. Eseguire sempre la convalida in un nuovo pacchetto prima di provare a installare il pacchetto per la prima volta. Questa operazione è descritta in Convalida dell'esempio di installazione.

Se non si vuole includere l'interfaccia utente nel pacchetto di esempio, omettere o rimuovere tutte le informazioni nelle tabelle illustrate in precedenza, ad eccezione della tabella [TextStyle](textstyle-table.md) (necessaria per definire la proprietà [**DefaultUIFont).**](defaultuifont.md) È anche necessario rimuovere le proprietà dell'interfaccia utente dalla [tabella delle proprietà](property-table.md). Di seguito è riportata una tabella di proprietà Blocco note esempio, senza un'interfaccia utente. Non riutilizzare i GUID visualizzati nella tabella se si copia questo esempio.

[Tabella delle proprietà](property-table.md)



| Proprietà                                   | Valore                                  |
|--------------------------------------------|----------------------------------------|
| [**DefaultUIFont**](defaultuifont.md)     | DlgFont8                               |
| [**INSTALLLEVEL**](installlevel.md)       | 3                                      |
| [**LIMITUI**](limitui.md)                 | 1                                      |
| [**Produttore**](manufacturer.md)       | Microsoft                              |
| [**ProductCode**](productcode.md)         | {18A9233C-0B34-4127-A966-C257386270BC} |
| [**ProductLanguage**](productlanguage.md) | 1033                                   |
| [**ProductName**](productname.md)         | MNP2000                                |
| [**ProductVersion**](productversion.md)   | 01.40.0000                             |
| [**UpgradeCode**](upgradecode.md)         | {908E378A-9551-4772-BF1D-5CFAF6FD9CB4} |



 

Un pacchetto senza interfaccia utente può essere installato dalla riga di comando o da un programma. Per installare un pacchetto dalla riga di comando, usare i metodi descritti in [Opzioni della riga di comando](command-line-options.md). Per installare un pacchetto da un programma, usare i metodi descritti in [Uso delle funzioni del programma di installazione](using-installer-functions.md). Eseguire sempre la convalida in un nuovo pacchetto prima di provare a installare un nuovo pacchetto per la prima volta.

[Continua](validating-an-installation-database.md)

 

 



