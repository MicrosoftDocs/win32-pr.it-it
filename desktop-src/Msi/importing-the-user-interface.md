---
description: Oltre alle informazioni illustrate nelle sezioni precedenti, uisample.msi contiene anche i dati per un'interfaccia utente di esempio.
ms.assetid: 7e4ae4b8-e7b2-49b3-97b7-374b69006a2f
title: Importazione dell'interfaccia utente
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2957dbec645bb85121c9748de83bc5c96ad04b05
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103879682"
---
# <a name="importing-the-user-interface"></a>Importazione dell'interfaccia utente

Oltre alle informazioni illustrate nelle sezioni precedenti, uisample.msi contiene anche i dati per un'interfaccia utente di esempio. Se è stato eseguito il merge uisample.msi in MNP2000.msi nella sezione [importazione di un database vuoto](importing-a-blank-database.md), queste informazioni sono presenti anche in MNP2000.msi. Le informazioni per l'interfaccia utente di esempio sono incluse nelle tabelle seguenti.

-   [Tabella ActionText](actiontext-table.md)
-   [Tabella binaria](binary-table.md)
-   [Tabella di controllo](control-table.md)
-   [Tabella ControlEvent](controlevent-table.md)
-   [Tabella finestra di dialogo](dialog-table.md)
-   [Tabella degli errori](error-table.md)
-   [Tabella EventMapping](eventmapping-table.md)
-   [RadioButton (tabella)](radiobutton-table.md)
-   [Tabella TextStyle](textstyle-table.md)
-   [Tabella UIText](uitext-table.md)

L'orca dell'editor di database fornito con il programma di installazione include un'opzione di anteprima della finestra di dialogo che è possibile usare per visualizzare in anteprima le finestre di dialogo dell'interfaccia utente specificata dai dati nelle tabelle precedenti.

Il pacchetto di installazione di esempio MNP2000.msi è ora pronto per la convalida del pacchetto. Eseguire sempre la convalida in un nuovo pacchetto prima di tentare di installare il pacchetto per la prima volta. Questa operazione viene illustrata in convalida dell'esempio di installazione.

Se non si desidera includere l'interfaccia utente nel pacchetto di esempio, omettere o rimuovere tutte le informazioni nelle tabelle riportate in precedenza, ad eccezione della [tabella TextStyle](textstyle-table.md) (necessaria per definire la proprietà [**DefaultUIFont**](defaultuifont.md) ). È inoltre necessario rimuovere le proprietà dell'interfaccia utente dalla [tabella delle proprietà](property-table.md). Di seguito è riportata una tabella delle proprietà di esempio per l'esempio del blocco note, senza interfaccia utente. Se si copia questo esempio, non riutilizzare i GUID visualizzati nella tabella.

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



 

Un pacchetto senza un'interfaccia utente può essere installato dalla riga di comando o da un programma. Per installare un pacchetto dalla riga di comando, usare i metodi descritti in [Opzioni della riga di comando](command-line-options.md). Per installare un pacchetto da un programma, utilizzare i metodi descritti in [utilizzo delle funzioni di installazione](using-installer-functions.md). Eseguire sempre la convalida in un nuovo pacchetto prima di tentare di installare un nuovo pacchetto per la prima volta.

[Continua](validating-an-installation-database.md)

 

 



