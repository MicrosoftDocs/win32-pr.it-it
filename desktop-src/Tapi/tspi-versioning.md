---
description: Nel tempo è possibile che vengano generate versioni diverse di TAPI, applicazioni e provider di servizi.
ms.assetid: 994fad0e-5958-4d93-8952-9db2bbe01f44
title: Controllo delle versioni di TSPI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dfe405a629ddc64f76535b33554509b1a6fca81d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104526814"
---
# <a name="tspi-versioning"></a>Controllo delle versioni di TSPI

Nel tempo è possibile che vengano generate versioni diverse di TAPI, applicazioni e provider di servizi. Queste nuove versioni possono creare nuove definizioni, ad esempio per nuove funzionalità, nuovi membri nelle strutture di dati e nuovi campi di bit. I numeri di versione sono pertanto necessari per indicare come interpretare diverse strutture di dati.

Per consentire l'interoperabilità ottimale di versioni diverse di applicazioni, versioni di TAPI e versioni di provider di servizi da fornitori diversi, la telefonia Microsoft fornisce un meccanismo di negoziazione della versione semplice per le applicazioni. Ci sono due versioni diverse che devono essere concordate da TAPI e dal provider di servizi di telefonia per ogni dispositivo line. Il primo è il numero di versione per la telefonia SPI di base e supplementare, denominata versione dell' *interfaccia TSPI*. L'altro è per le estensioni specifiche del provider, se presente, e viene indicato come *versione dell'estensione*. Il formato delle strutture di dati e dei tipi di dati usati dalle funzionalità di base e supplementare di TSPI è definito dalla versione TSPI, mentre la versione dell'estensione determina il formato delle strutture di dati definite dalle estensioni specifiche del fornitore.

Questi due tipi di negoziazione della versione vengono gestiti da due procedure diverse: [**TSPI \_ lineNegotiateTSPIVersion**](/windows/win32/api/tspi/nf-tspi-tspi_linenegotiatetspiversion) viene usato per negoziare la versione dell'interfaccia TSPI e [**TSPI \_ lineNegotiateExtVersion**](/windows/win32/api/tspi/nf-tspi-tspi_linenegotiateextversion) viene usato per negoziare la versione dell'estensione. La negoziazione della versione dell'estensione può essere ignorata se non si desiderano le estensioni. Se questi intervalli di input durante la negoziazione si sovrappongono, il provider di servizi deve restituire un valore all'interno della parte sovrapposta dell'intervallo come risultato della negoziazione. In genere, deve essere il valore massimo possibile. Se gli intervalli non si sovrappongono, le due entità sono incompatibili e la funzione restituisce un errore.

I risultati di una negoziazione indicano semplicemente che il provider di servizi è disposto a funzionare con un determinato numero di versione, ma non esegue il commit del provider di servizi. Ad esempio, è possibile rinegoziare TAPI per determinare una versione ideale dopo aver negoziato una versione possibile. Viene eseguito il commit della versione dell'interfaccia TSPI solo quando viene aperta una riga con [**TSPI \_ lineOpen**](/windows/win32/api/tspi/nf-tspi-tspi_lineopen) e viene mantenuta fino alla chiusura del dispositivo. Viene eseguito il commit della versione dell'estensione quando viene chiamata la funzione [**TSPI \_ lineSelectExtVersion**](/windows/win32/api/tspi/nf-tspi-tspi_lineselectextversion) , che rimane in attesa fino a quando la selezione non viene annullata selezionando versione dell'estensione zero.

La selezione della versione dell'estensione può essere eseguita più volte, incluso mentre è attiva una versione di estensione. Poiché viene eseguito il commit del provider di servizi nella versione dell'estensione, il relativo intervallo di versioni supportate viene ridotto esattamente a tale versione dell'estensione. Si consideri, ad esempio, un provider di servizi normalmente compatibile con le versioni di estensione da 1,0 a 5,5. Se è attiva la versione 3,0 mentre un chiamante tenta di negoziare una versione nell'intervallo compreso tra 1,0 e 5,5, la negoziazione restituisce 3,0.

Poiché TAPI negozia la versione, è possibile aggiornare un provider di servizi a nuove versioni dell'interfaccia senza che sia necessario aggiornare anche TAPI. Analogamente, è possibile aggiornare TAPI, ma continuare a usare il provider di servizi meno recente.

 

 
