---
description: Informazioni sul controllo delle versioni TSPI. Nel corso del tempo possono essere prodotte versioni diverse di TAPI, applicazioni e provider di servizi.
ms.assetid: 994fad0e-5958-4d93-8952-9db2bbe01f44
title: Controllo delle versioni TSPI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0e0a0663a1fcc685df8643c634ec627f669aafe8
ms.sourcegitcommit: 6fc8a7419bd01787cf6a1c52c355a4a2d1aec471
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/10/2021
ms.locfileid: "111989236"
---
# <a name="tspi-versioning"></a>Controllo delle versioni TSPI

Nel corso del tempo possono essere prodotte versioni diverse di TAPI, applicazioni e provider di servizi. Queste nuove versioni possono creare nuove definizioni, ad esempio per le nuove funzionalità, nuovi membri nelle strutture di dati e nuovi campi di bit. I numeri di versione sono quindi necessari per indicare come interpretare varie strutture di dati.

Per consentire l'interoperabilità ottimale di versioni diverse di applicazioni, versioni di TAPI e versioni di provider di servizi di fornitori diversi, Microsoft Telefonia fornisce un semplice meccanismo di negoziazione della versione per le applicazioni. Esistono due diverse versioni che devono essere concordate da TAPI e dal provider di servizi di telefonia per ogni dispositivo line. Il primo è il numero di versione per l'interfaccia SPI di telefonia di base e supplementare, detta *versione dell'interfaccia TSPI.* L'altro è per le estensioni specifiche del provider, se presenti, ed è detto versione *dell'estensione*. Il formato delle strutture di dati e dei tipi di dati usati dalle funzionalità basic e supplementari di TSPI è definito dalla versione TSPI, mentre la versione dell'estensione determina il formato delle strutture di dati definite dalle estensioni specifiche del fornitore.

Questi due tipi di negoziazione della versione vengono gestiti da due procedure diverse: [**\_ lineNegotiateTSPIVersion TSPI**](/windows/win32/api/tspi/nf-tspi-tspi_linenegotiatetspiversion) viene usato per negoziare la versione dell'interfaccia TSPI e [**\_ lineNegotiateExtVersion TSPI**](/windows/win32/api/tspi/nf-tspi-tspi_linenegotiateextversion) viene usato per negoziare la versione dell'estensione. La negoziazione della versione dell'estensione può essere ignorata se le estensioni non sono disponibili. Se questi intervalli di input durante la negoziazione si sovrappongono, il provider di servizi deve restituire un valore all'interno della parte sovrapposta dell'intervallo come risultato della negoziazione. In genere, deve essere il valore più alto possibile. Se gli intervalli non si sovrappongono, le due parti non sono compatibili e la funzione restituisce un errore.

I risultati di una negoziazione indicano semplicemente che il provider di servizi è disposto a operare a un determinato numero di versione, ma non esegue il commit del provider di servizi a tale scopo. Ad esempio, TAPI può rinegoziare per determinare una versione ideale dopo aver negoziato una versione possibile. Viene eseguito il commit della versione dell'interfaccia TSPI solo quando una riga viene aperta usando la riga [**\_ TSPIApri**](/windows/win32/api/tspi/nf-tspi-tspi_lineopen) e viene chiusa fino alla chiusura del dispositivo. Il commit della versione dell'estensione viene eseguito quando viene chiamata la funzione [**\_ lineSelectExtVersion TSPI**](/windows/win32/api/tspi/nf-tspi-tspi_lineselectextversion) e non viene eseguito finché la selezione non viene annullata selezionando la versione zero dell'estensione.

La selezione della versione dell'estensione può avvenire più volte, anche mentre è in vigore una versione dell'estensione. Poiché viene eseguito il commit del provider di servizi alla versione dell'estensione, la gamma di versioni supportate si restringe esattamente a tale versione dell'estensione. Si consideri ad esempio un provider di servizi normalmente compatibile con le versioni di estensione da 1.0 a 5.5. Se la versione 3.0 è in vigore mentre un chiamante tenta di negoziare una versione nell'intervallo da 1.0 a 5.5, la negoziazione restituisce 3.0.

Poiché TAPI negozia la versione, è possibile aggiornare un provider di servizi alle nuove versioni dell'interfaccia senza richiedere l'aggiornamento anche di TAPI. Analogamente, è possibile aggiornare TAPI, ma usare comunque il provider di servizi meno recente.

 

 
