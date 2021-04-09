---
title: Risoluzione dei nomi per DLL e provider di servizi
description: I paragrafi seguenti descrivono come il WS2 \_32.dll e i provider dello spazio dei nomi implementano i servizi di risoluzione dei nomi supportati dall'API Winsock.
ms.assetid: 25fcb1c2-2d28-41a0-9124-05608f22420f
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b527f0849eb441ab7bc8d096c0198d703f2ce337
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103966677"
---
# <a name="name-resolution-for-dll-and-service-providers"></a>Risoluzione dei nomi per DLL e provider di servizi

I paragrafi seguenti descrivono come il WS2 \_32.dll e i provider dello spazio dei nomi implementano i servizi di risoluzione dei nomi supportati dall'API Winsock.

## <a name="ws2_32dll-functionality-for-name-resolution"></a>WS2 \_32.dll funzionalità per la risoluzione dei nomi

Il \_32.dll WS2 gestisce la registrazione e il caricamento delle richieste delle singole DLL del provider dello spazio dei nomi. Inoltre, è responsabile del routing delle operazioni dello spazio dei nomi da un'applicazione Windows Sockets 2 al set appropriato di provider dello spazio dei nomi. Questo mapping è regolato dal valore dei parametri dello spazio dei nomi e dell'identificatore del provider di servizi presenti nelle singole funzioni API. Come regola generale, quando si fa riferimento a un provider dello spazio dei nomi specifico, l'operazione viene indirizzata solo a un provider identificato. Se l'identificatore del provider dello spazio dei nomi è null ma viene fatto riferimento a un determinato spazio dei nomi, l'operazione viene indirizzata a tutti i provider dello spazio dei nomi che supportano lo spazio dei nomi identificato. Se l'identificatore del provider dello spazio dei nomi è null e l'identificatore dello spazio dei nomi viene fornito come NS \_ All, l'operazione viene instradata a tutti i provider dello spazio dei nomi attivi.

Nell'ambito dell'avvio di una query per uno o più provider di servizi, WS2 \_32.dll alloca un oggetto per tenere traccia dello stato in corso della query. Un handle opaco che rappresenta questo oggetto viene restituito all'applicazione che ha avviato la query. L'applicazione fornisce questo handle come parametro ogni volta che viene chiamata ripetutamente una funzione dell'interfaccia dell'applicazione per recuperare l'unità di dati successiva risultante dalla query.

In risposta a queste chiamate di routine dell'interfaccia dell'applicazione, il \_32.dll WS2 utilizza le informazioni archiviate nell'oggetto per effettuare chiamate corrispondenti ai provider dello spazio dei nomi necessari per la query. WS2 \_32.dll aggiorna le informazioni nel relativo oggetto quando si verifica ogni chiamata successiva dell'interfaccia dell'applicazione in modo che le chiamate corrispondenti ai provider dello spazio dei nomi vengano eseguite correttamente attraverso tutti i provider dello spazio dei nomi necessari per la query.

## <a name="namespace-provider-functionality"></a>Funzionalità del provider dello spazio dei nomi

Ogni provider dello spazio dei nomi è responsabile del mapping del set di funzioni visualizzate nella risoluzione dei nomi di Windows Sockets 2 per le transazioni appropriate con lo spazio dei nomi supportato. In alcuni casi, si tratta principalmente di eseguire il mapping di SPI a qualsiasi interfaccia nativa esistente per lo spazio dei nomi. In altri, il provider dello spazio dei nomi deve eseguire transazioni con il provider dello spazio dei nomi sulla rete. Alcuni provider dello spazio dei nomi eseguiranno le chiamate all'API di Windows Sockets, mentre altre utilizzeranno interfacce private per gli stack di trasporto associati.

 

 



