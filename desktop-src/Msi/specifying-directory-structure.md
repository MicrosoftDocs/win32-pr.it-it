---
description: Il programma di installazione mantiene le informazioni sulla struttura della directory di installazione nella tabella directory.
ms.assetid: 31390138-b1d0-4f0b-9304-6e7c69e6a736
title: Specifica della struttura di directory
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cbc71e448c03a7fdbdf9de249122246aaf0038769a1dd409551330a503be7e2b
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119627891"
---
# <a name="specifying-directory-structure"></a>Specifica della struttura di directory

Il programma di installazione mantiene le informazioni sulla struttura della directory di installazione nella [tabella directory](directory-table.md). Vedere il [gruppo Core Tables .](core-tables-group.md) In questa sezione si aggiungono informazioni sulla struttura di directory per l Blocco note di esempio al database vuoto creato in [Importazione di un database vuoto](importing-a-blank-database.md). Usare l'editor di database Orca fornito con l'SDK o un altro editor per aprire la tabella directory in MNP2000.msi. Usare l'editor per immettere i dati seguenti nella tabella Directory vuota.

[Tabella directory](directory-table.md)



| Directory                                        | Padre \_ della directory                                | DefaultDir        |
|--------------------------------------------------|--------------------------------------------------|-------------------|
| [**Targetdir**](targetdir.md)                   |                                                  | SourceDir         |
| [**Cartella ProgramFilesFolder**](programfilesfolder.md) | [**Targetdir**](targetdir.md)                   | .                 |
| ARTODIR                                          | NOTEPADDIR                                       | Arti:Eventi       |
| HOLDIR                                           | MONDIR                                           | .:Holidays        |
| MENUDIR                                          | NOTEPADDIR                                       | Menu              |
| MONDIR                                           | NOTEPADDIR                                       | Cancello              |
| NOTEPADDIR                                       | [**Cartella ProgramFilesFolder**](programfilesfolder.md) | Red \_ Park:Blocco note |
| SPORTDIR                                         | NOTEPADDIR                                       | Sport:Eventi     |



 

L'immissione di questi dati nella tabella Directory specifica le strutture di directory di origine e di destinazione. Vedere gli [argomenti Tabella directory](directory-table.md) e Uso della tabella [directory.](using-the-directory-table.md) Si noti che [**la proprietà TARGETDIR**](targetdir.md) deve essere il nome di una radice nella tabella Directory di ogni installazione.

[Continua](specifying-components.md)

 

 



