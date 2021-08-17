---
description: L'approccio consigliato per la gestione delle tabelle codici consiste nel creare un database di base neutro contenente solo caratteri che possono essere tradotti in qualsiasi tabella codici.
ms.assetid: 8ded41a6-6e5b-4a39-b783-e2b9f83eaed4
title: Creazione di un database con una tabella codici neutra
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 72e9283378d003adf3069e2feb505fab36c9a379de4deb2a767d10559d547e8b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118379416"
---
# <a name="creating-a-database-with-a-neutral-code-page"></a>Creazione di un database con una tabella codici neutra

L'approccio consigliato per la gestione delle tabelle codici consiste nel creare un database di base neutro contenente solo caratteri che possono essere tradotti in qualsiasi tabella codici. Il database può quindi essere impostato sulla tabella codici della localizzazione e le informazioni sulla localizzazione possono essere aggiunte come descritto in Localizzazione di un pacchetto Windows [installer](localizing-a-windows-installer-package.md).

Per creare un database neutro, evitare caratteri estesi che non appartengono al set di caratteri ASCII e pertanto richiedono una tabella codici speciale. Ad esempio, il segno di copyright, © e il segno del marchio registrato, , non sono caratteri ASCII e richiedono una tabella codici ANSI speciale per la corretta visualizzazione. Usare invece (c) e (r), perché questi caratteri possono essere tradotti o trasformati nei simboli per la versione in lingua inglese. Questo database neutro può quindi essere localizzato impostandone la tabella codici e aggiungendo informazioni di localizzazione tramite la modifica della tabella o importando file di archivio di testo.

 

 



