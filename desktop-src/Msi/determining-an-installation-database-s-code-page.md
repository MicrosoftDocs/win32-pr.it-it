---
description: Per determinare la tabella codici di un database, chiamare MsiDatabaseExport con hDatabase impostato sull'handle del database e szTableName impostato su \_ ForceCodepage.
ms.assetid: afa3fbd9-9f54-4f72-ab5d-cb0dbbd9946c
title: Determinazione della tabella codici di un database di installazione
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 89825c99e0652c0ef324c99f8906281f3c87ed58bef099886220faa6a9311583
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118637850"
---
# <a name="determining-an-installation-databases-code-page"></a>Determinazione della tabella codici di un database di installazione

Per determinare la tabella codici di un database, chiamare [**MsiDatabaseExport**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabaseexporta) con *hDatabase* impostato sull'handle del database e *szTableName* impostato su \_ ForceCodepage. Viene esportato un file di testo con estensione idt. Le prime due righe di questo file sono vuote. La terza riga è il numero della tabella codici ANSI, seguito da una scheda, seguita dal nome \_ ForceCodepage. Vedere anche [Gestione della tabella codici delle tabelle importate ed esportate](code-page-handling-of-imported-and-exported-tables.md).

Un esempio di determinazione della tabella codici tramite il metodo [**Export**](database-export.md) viene fornito in Windows Installer SDK come parte dell'utilità WiLangId.vbs. Per altre informazioni sull'uso WiLangId.vbs vedere l'argomento Relativo alla gestione del linguaggio [e della tabella codici.](manage-language-and-codepage.md)

 

 



