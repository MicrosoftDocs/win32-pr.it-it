---
description: Il programma di installazione mantiene le informazioni sulla struttura della directory di installazione nella tabella directory.
ms.assetid: 31390138-b1d0-4f0b-9304-6e7c69e6a736
title: Specifica della struttura di directory
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 80a87880921799158559e28fed2c6dde97c9a331
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103879553"
---
# <a name="specifying-directory-structure"></a>Specifica della struttura di directory

Il programma di installazione mantiene le informazioni sulla struttura della directory di installazione nella [tabella directory](directory-table.md). Vedere il [gruppo tabelle principali](core-tables-group.md). In questa sezione è possibile aggiungere informazioni sulla struttura di directory per l'esempio del blocco note al database vuoto creato durante l' [importazione di un database vuoto](importing-a-blank-database.md). Utilizzare l'editor di database Orca fornito con l'SDK o un altro editor per aprire la tabella di directory in MNP2000.msi. Utilizzare l'editor per immettere i dati seguenti nella tabella directory vuota.

[Tabella directory](directory-table.md)



| Directory                                        | \_Padre directory                                | DefaultDir        |
|--------------------------------------------------|--------------------------------------------------|-------------------|
| [**TARGETDIR**](targetdir.md)                   |                                                  | SourceDir         |
| [**ProgramFilesFolder**](programfilesfolder.md) | [**TARGETDIR**](targetdir.md)                   | .                 |
| ARTSDIR                                          | NOTEPADDIR                                       | Arts: eventi       |
| HOLDIR                                           | MONDIno                                           | .: Festività        |
| MENUDIR                                          | NOTEPADDIR                                       | Menu              |
| MONDIno                                           | NOTEPADDIR                                       | Cancello              |
| NOTEPADDIR                                       | [**ProgramFilesFolder**](programfilesfolder.md) | Red \_ Park: blocco note |
| SPORTDIR                                         | NOTEPADDIR                                       | Sport: eventi     |



 

L'immissione di questi dati nella tabella directory specifica le strutture di directory di origine e di destinazione. Vedere la [tabella directory](directory-table.md) e [usare gli argomenti della tabella directory](using-the-directory-table.md) . Si noti che la proprietà [**targetdir**](targetdir.md) deve corrispondere al nome di una radice nella tabella di directory di ogni installazione.

[Continua](specifying-components.md)

 

 



