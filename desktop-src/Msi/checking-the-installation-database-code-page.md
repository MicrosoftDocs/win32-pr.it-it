---
description: Una tabella codici è una tabella interna utilizzata dal sistema operativo per eseguire il mapping dei simboli (lettere, numeri e segni di punteggiatura) a un numero di caratteri.
ms.assetid: e11193a2-2c72-43a9-8d35-fa524044e306
title: Controllo della tabella codici del database di installazione
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 48ea9513ec80413e00a9f3f4c1232a06704f83e5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106310985"
---
# <a name="checking-the-installation-database-code-page"></a>Controllo della tabella codici del database di installazione

Una tabella *codici* è una tabella interna utilizzata dal sistema operativo per eseguire il mapping dei simboli (lettere, numeri e segni di punteggiatura) a un numero di caratteri. Diverse tabelle codici forniscono supporto per i set di caratteri utilizzati in diversi paesi o aree geografiche. Alle tabelle codici viene fatto riferimento in base al numero; ad esempio, la tabella codici 932 rappresenta il set di caratteri giapponese e la tabella codici 950 rappresenta uno dei set di caratteri cinesi. Vedere [localizzazione delle tabelle Error e ActionText](localizing-the-error-and-actiontext-tables.md) per un elenco di tabelle codici ASCII.

La stessa tabella codici ASCII, 1252, può essere utilizzata per l'inglese e il francese. Pertanto, non è necessario reimpostare la tabella codici per il database MNP2000.msi (Inglese) per modificare l'installazione in francese.

Per ulteriori informazioni sull'impostazione della tabella codici, vedere la pagina relativa alla [gestione della tabella codici (Windows Installer)](code-page-handling-windows-installer-.md).

[Continua](importing-localized-error-and-actiontext-tables.md)

 

 



