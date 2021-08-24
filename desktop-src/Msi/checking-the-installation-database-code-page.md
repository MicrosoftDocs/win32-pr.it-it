---
description: Una tabella codici è una tabella interna utilizzata dal sistema operativo per eseguire il mapping di simboli (lettere, numeri e caratteri di punteggiatura) a un numero di carattere.
ms.assetid: e11193a2-2c72-43a9-8d35-fa524044e306
title: Controllo della tabella codici del database di installazione
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cedb63128d4a3b18878eba16af5e55da92403953ddf2a2c9a29c788a524ad41f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119581771"
---
# <a name="checking-the-installation-database-code-page"></a>Controllo della tabella codici del database di installazione

Una *tabella codici* è una tabella interna utilizzata dal sistema operativo per eseguire il mapping di simboli (lettere, numeri e caratteri di punteggiatura) a un numero di carattere. Diverse pagine codici forniscono il supporto per i set di caratteri usati in paesi o aree geografiche diverse. Le pagine di codice sono indicate in base al numero. Ad esempio, la tabella codici 932 rappresenta il set di caratteri giapponese e la tabella codici 950 rappresenta uno dei set di caratteri cinesi. Vedere [Localizzazione delle tabelle Error e ActionText per](localizing-the-error-and-actiontext-tables.md) un elenco di tabelle codici ASCII.

La stessa tabella codici ASCII, 1252, può essere usata per l'inglese e il francese. Non è quindi necessario reimpostare la tabella codici MNP2000.msi database (inglese) per modificare l'installazione in francese.

Per altre informazioni sull'impostazione della tabella codici, vedere [Code Page Handling (Windows Installer)](code-page-handling-windows-installer-.md).

[Continua](importing-localized-error-and-actiontext-tables.md)

 

 



