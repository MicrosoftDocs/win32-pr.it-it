---
description: Per determinare la tabella codici di un database, chiamare MsiDatabaseExport con hDatabase impostato sull'handle del database e szTableName impostato su \_ ForceCodepage.
ms.assetid: afa3fbd9-9f54-4f72-ab5d-cb0dbbd9946c
title: Determinazione della tabella codici di un database di installazione
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 212978cbce0e73ae495a0ed10ea9070cce6bd374
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103882993"
---
# <a name="determining-an-installation-databases-code-page"></a>Determinazione della tabella codici di un database di installazione

Per determinare la tabella codici di un database, chiamare [**MsiDatabaseExport**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabaseexporta) con *hDatabase* impostato sull'handle del database e *szTableName* impostato su \_ ForceCodepage. Viene esportato un file di testo con estensione IDT. Le prime due righe del file sono vuote. La terza riga è il numero di tabella codici ANSI, seguito da una scheda, seguito dal nome \_ ForceCodepage. Vedere anche [gestione della tabella codici per le tabelle importate ed esportate](code-page-handling-of-imported-and-exported-tables.md).

Un esempio di determinazione della tabella codici tramite il [**Metodo Export**](database-export.md) viene fornito nel Windows Installer SDK come parte del WiLangId.vbs di utilità. Per ulteriori informazioni sull'utilizzo di WiLangId.vbs, vedere l'argomento relativo alla [gestione della lingua e](manage-language-and-codepage.md)della tabella codici.

 

 



