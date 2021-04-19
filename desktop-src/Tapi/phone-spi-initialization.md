---
description: Come parte dell'astrazione del dispositivo telefonico definita da TSPI, TAPI e il provider di servizi devono prima essere sottoposti a un'inizializzazione di base.
ms.assetid: cd8bb328-fbd0-409c-8471-34ad4c2c8d93
title: Inizializzazione del telefono SPI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1d0c54e313c2be3846aeb604217f5324ec0d8a8d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106315272"
---
# <a name="phone-spi-initialization"></a>Inizializzazione del telefono SPI

Come parte dell'astrazione del dispositivo telefonico definita da TSPI, TAPI e il provider di servizi devono prima essere sottoposti a un'inizializzazione di base. Questa inizializzazione di base viene eseguita per le metà della linea e del telefono dell'interfaccia con lo stesso set di passaggi. Il primo di questi passaggi è la negoziazione della versione dell'interfaccia. Questa operazione viene eseguita chiamando la funzione [**TSPI \_ lineNegotiateTSPIVersion**](/windows/win32/api/tspi/nf-tspi-tspi_linenegotiatetspiversion) . Questa funzione viene in genere usata per negoziare per conto di un singolo dispositivo a linee; dispositivi linea diversi all'interno dello stesso provider di servizi possono funzionare in base a diverse versioni dell'interfaccia. TAPI passa un valore di identificatore di dispositivo riservato speciale, [**Initialize \_ Negotiation**](initialize-negotiation.md), per indicare che sta negoziando una versione di interfaccia complessiva per le funzioni di inizializzazione che interessano l'intero provider di servizi, sia per le linee che per i telefoni.

Il risultato di questa negoziazione viene passato alle procedure successive fino a quando non viene aperto un dispositivo telefonico. A questo punto, il dispositivo telefonico viene sottoposta a commit in una determinata versione dell'interfaccia. Questa versione dell'interfaccia è implicita fino alla chiusura del telefono e non deve essere passata alle funzioni successive che operano su un telefono aperto.

Dopo la negoziazione complessiva della versione dell'interfaccia, TAPI chiama la funzione [**TSPI \_ providerInit**](/windows/win32/api/tspi/nf-tspi-tspi_providerinit) . Questa funzione Inizializza il provider di servizi, assegnando anche i parametri necessari per l'operazione successiva. Questi parametri includono quanto segue:

-   *dwPermanentProviderID*: specifica l'identificatore permanente del provider di servizi da inizializzare, univoco all'interno dei provider di servizi in questo sistema.
-   *dwLineDeviceIDBase*: specifica l'identificatore di dispositivo più basso per i dispositivi linea supportati da questo provider di servizi.
-   *dwPhoneDeviceIDBase*: specifica l'identificatore di dispositivo più basso per i dispositivi telefonici supportati da questo provider di servizi. I dispositivi della classe del dispositivo telefonico telefonico sono identificati da numeri interi a partire da zero. Questo intervallo di identificatori è contiguo nell'intera gamma di dispositivi telefonici. Poiché possono essere presenti più provider di servizi che gestiscono dispositivi telefonici in un unico sistema, ogni provider di servizi ottiene una porzione contigua dell'intervallo totale. Questo parametro indica al provider di servizi il valore più basso nella parte dell'intervallo. Il provider di servizi, anziché TAPI, è responsabile del mapping di questo intervallo di variabili ai propri identificatori interni dei dispositivi. In questo modo, il fornitore del provider di servizi garantisce una flessibilità sufficiente a usare gli identificatori dei dispositivi in estensioni specifiche del dispositivo, se necessario. Poiché il provider di servizi sa quali identificatori di dispositivo vengono visualizzati in strutture di dati e parametri definiti da TAPI, può usare gli identificatori di dispositivo coerenti in strutture di dati e parametri di estensione specifici del dispositivo.
-   *dwNumLines*: specifica il numero di dispositivi linea supportati da questo provider di servizi.
-   *dwNumPhones*: specifica il numero di dispositivi telefonici supportati da questo provider di servizi.
-   *lpfnCompletionProc*: specifica la procedura chiamata dal provider di servizi per segnalare il completamento di tutte le procedure operative asincrone sui dispositivi line e Phone.

Dopo [**TSPI \_ providerInit**](/windows/win32/api/tspi/nf-tspi-tspi_providerinit), è possibile eseguire operazioni normali, ad esempio l'apertura di telefoni.

 

 
