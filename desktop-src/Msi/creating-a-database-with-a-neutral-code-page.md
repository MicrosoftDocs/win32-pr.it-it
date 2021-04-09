---
description: L'approccio consigliato per la gestione delle tabelle codici consiste nel creare un database di base neutro che contenga solo caratteri che possono essere convertiti in qualsiasi tabella codici.
ms.assetid: 8ded41a6-6e5b-4a39-b783-e2b9f83eaed4
title: Creazione di un database con una tabella codici neutra
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 08639b6ab3521f183a2dab46dfd257121b28bae0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104050160"
---
# <a name="creating-a-database-with-a-neutral-code-page"></a>Creazione di un database con una tabella codici neutra

L'approccio consigliato per la gestione delle tabelle codici consiste nel creare un database di base neutro che contenga solo caratteri che possono essere convertiti in qualsiasi tabella codici. Il database può quindi essere impostato sulla tabella codici della localizzazione e le informazioni di localizzazione possono essere aggiunte come descritto in [localizzazione di un pacchetto di Windows Installer](localizing-a-windows-installer-package.md).

Per creare un database neutro, evitare i caratteri estesi che non appartengono al set di caratteri ASCII e quindi richiedere una tabella codici speciale. Ad esempio, il segno di copyright, il © e il segno di marchio registrato,, non sono caratteri ASCII e richiedono una tabella codici ANSI speciale per la visualizzazione corretta. Usare invece (c) e (r), perché questi caratteri possono essere convertiti o trasformati in simboli per la versione in lingua inglese. Questo database neutro può quindi essere localizzato impostando la relativa tabella codici e aggiungendo le informazioni di localizzazione mediante la modifica della tabella oppure importando i file di archivio di testo.

 

 



