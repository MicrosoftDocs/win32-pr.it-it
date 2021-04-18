---
description: Alla base di qualsiasi programma di installazione è presente l'installazione effettiva dei file.
ms.assetid: e6f6d6a5-bdb0-4866-8d2c-56313d92c94c
title: Regole di controllo delle versioni dei file
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 67c6f8e59b4f15774f898217690dbb1c4d57b1bf
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106309475"
---
# <a name="file-versioning-rules"></a>Regole di controllo delle versioni dei file

Alla base di qualsiasi programma di installazione è presente l'installazione effettiva dei file. Determinare se installare un file è un processo complesso. Al livello più alto, questa decisione dipende dal fatto che il componente a cui appartiene un file sia contrassegnato per l'installazione. Una volta determinato che un file deve essere copiato, il processo è complesso se nella cartella di destinazione esiste un altro file con lo stesso nome. In tali situazioni, per eseguire la determinazione è necessario un set di regole che includa le proprietà seguenti:

-   Versione
-   Data
-   Linguaggio

Il programma di installazione utilizza queste regole solo quando si tenta di installare un file in un percorso che contiene già un file con lo stesso nome. In questo caso, il Windows Installer utilizza le regole seguenti, tutte le altre sono uguali, per determinare se installare.

WINS con la versione più recente: tutti gli altri elementi sono uguali, il file con la versione più alta prevale, anche se il file nel computer ha la versione più recente.

Win con versione file: un file con versione viene installato su un file non con versione.

Favorisce la lingua del prodotto: se il file da installare ha una lingua diversa da quella del computer, predilige il file con la lingua corrispondente al prodotto in fase di installazione. I file indipendenti dalla lingua vengono considerati come un altro linguaggio, in modo che il prodotto da installare venga nuovamente favorito.

Mancata corrispondenza di più lingue: dopo aver fattorizzato le lingue comuni tra il file in fase di installazione e il file nel computer, le lingue rimanenti vengono favorite in base a quanto richiesto dal prodotto da installare.

Mantieni lingue superset: consente di mantenere il file che supporta più lingue, indipendentemente dal fatto che sia già presente nel computer o sia in fase di installazione.

I file senza versione sono dati utente: se la data di modifica è successiva alla data di creazione del file nel computer, non installare il file perché le personalizzazioni degli utenti verranno eliminate. Se le date modificate e create sono le stesse, installare il file. Se la data di creazione è successiva alla data di modifica, il file viene considerato non modificato, installare il file.

L'installazione di un [file complementare](companion-files.md) dipende non dalle informazioni relative al controllo delle versioni dei file, bensì al controllo delle versioni del padre complementare. Nel caso di file complementari, l'installazione viene ignorata solo se la versione del file padre è superiore. Si noti che un file che rappresenta il percorso della chiave per il componente non deve essere un file complementare, perché ciò comporta la logica di controllo delle versioni del file del percorso della chiave determinata dal file padre complementare.

File senza versione che usano [file complementari](companion-files.md): un file senza versione associato a un file con versione che usa il meccanismo complementare rispetta le regole per il file con versione. L'unica eccezione è rappresentata dal fatto che il file con versione nel computer e il file con versione installato hanno la stessa versione e la stessa lingua, ma il file complementare non è presente nel computer. In questo caso, il file complementare installato viene utilizzato anche se viene utilizzato il file con versione nel computer. Inoltre, viene installato un file senza versione che utilizza un file complementare se la proprietà [**REINSTALLMODE**](reinstallmode.md) include le opzioni Sovrascrivi versioni precedenti ("o" o "e") e la versione del file complementare è uguale a un file già presente nel computer.

Le regole sono globali: le regole per determinare quando installare un file si trovano in un'unica posizione all'interno del programma di installazione e sono globali, vale a dire che si applicano ugualmente a tutti i file.

Per esempi del formato utilizzato per le versioni dei file, vedere il tipo di dati [Version](version.md) . Per informazioni più specifiche, vedere [sostituzione di file esistenti](replacing-existing-files.md) o [controllo delle versioni dei file predefiniti](default-file-versioning.md).

 

 



