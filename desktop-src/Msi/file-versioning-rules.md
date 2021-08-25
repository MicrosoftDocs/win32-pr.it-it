---
description: La base di qualsiasi programma di installazione è l'installazione effettiva dei file.
ms.assetid: e6f6d6a5-bdb0-4866-8d2c-56313d92c94c
title: Regole di controllo delle versioni dei file
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c8dfda6a909450ba45cc213016a159bbbc8f9a54b958c7d4e37d051fd86935ad
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119828981"
---
# <a name="file-versioning-rules"></a>Regole di controllo delle versioni dei file

La base di qualsiasi programma di installazione è l'installazione effettiva dei file. Determinare se installare un file è un processo complesso. Al livello più alto, questa determinazione dipende dal fatto che il componente a cui appartiene un file sia contrassegnato per l'installazione. Dopo aver stabilito che un file deve essere copiato, il processo è complicato se nella cartella di destinazione è presente un altro file con lo stesso nome. In tali situazioni, per la determinazione è necessario un set di regole che coinvolgono le proprietà seguenti:

-   Versione
-   Data
-   Linguaggio

Il programma di installazione usa queste regole solo quando si tenta di installare un file in un percorso che contiene già un file con lo stesso nome. In questo caso, il Windows di installazione usa le regole seguenti, tutte le altre cose uguali, per determinare se eseguire l'installazione.

La versione più alta ha la priorità: tutti gli altri elementi sono uguali, il file con la versione più alta ha la priorità, anche se il file nel computer ha la versione più recente.

File con versione Win: un file con versione viene installato su un file senza versione.

Favorire la lingua del prodotto: se il file da installare ha una lingua diversa da quella del file nel computer, favorire il file con la lingua corrispondente al prodotto installato. I file indipendenti dalla lingua vengono considerati solo come un'altra lingua, quindi il prodotto da installare è di nuovo preferito.

Più lingue non corrispondenti: dopo il factoring di tutte le lingue comuni tra il file da installare e il file nel computer, tutte le lingue rimanenti sono favorite in base a ciò che è necessario per il prodotto installato.

Mantieni lingue superset: consente di mantenere il file che supporta più lingue indipendentemente dal fatto che sia già presente nel computer o che sia in fase di installazione.

I file senza versione sono dati utente: se la data modificata è successiva alla data di creazione del file nel computer, non installare il file perché le personalizzazioni utente verrebbero eliminate. Se le date Modified (Modificato) e Create (Crea) sono uguali, installare il file . Se la data di creazione è successiva alla data Modificato, il file viene considerato non modificato. Installare il file.

L'installazione di un [file complementare](companion-files.md) non dipende dalle proprie informazioni sul controllo delle versioni dei file, ma dal controllo delle versioni dell'elemento padre complementare. Nel caso di file complementari, l'installazione viene ignorata solo se il file padre ha una versione successiva. Si noti che un file che rappresenta il percorso della chiave per il relativo componente non deve essere un file complementare perché la logica di controllo delle versioni del file del percorso della chiave viene determinata dal file padre complementare.

File senza versione [](companion-files.md)Con file complementari: file senza versione associato a un file con versione che usa il meccanismo complementare abiade le regole per il file con versione. L'unica eccezione è se il file con versione nel computer e il file con versione da installare hanno la stessa versione e la stessa lingua, ma il file complementare non è presente nel computer. In questo caso viene usato il file complementare installato anche se viene usato il file con versione nel computer. Viene inoltre installato un file senza versione che usa un file complementare se la proprietà [**REINSTALLMODE**](reinstallmode.md) include le opzioni sovrascrivi le versioni precedenti ("o" o "e") e la versione del file complementare è uguale a un file già presente nel computer.

Le regole sono globali: le regole per determinare quando installare un file si trovano in un'unica posizione all'interno del programma di installazione e sono globali, vale a dire che si applicano ugualmente a tutti i file.

Per esempi del formato usato per le versioni dei file, vedere il tipo [di](version.md) dati Version. Per informazioni più specifiche, vedere [Sostituzione di file esistenti o](replacing-existing-files.md) Controllo delle versioni dei file [predefinito.](default-file-versioning.md)

 

 



