---
title: Voci secondarie e connessioni multilink
description: Windows NT Server 4.0 offre il supporto per le voci secondarie della rubrica, che consentono connessioni multilink. Una connessione multilink combina la larghezza di banda di più connessioni per fornire una singola connessione con una larghezza di banda superiore.
ms.assetid: 19cf6e1a-cdba-47e4-8d8f-d6030ed6f9e3
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 76cdada1e48ffc42753480a6a62fb79986d537402ad21449617359cd49df76f0
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120101801"
---
# <a name="subentries-and-multilink-connections"></a>Voci secondarie e connessioni multilink

Windows NT Server 4.0 offre il supporto per le voci secondarie della rubrica, che consentono connessioni multilink. Una connessione multilink combina la larghezza di banda di più connessioni per fornire una singola connessione con una larghezza di banda superiore.

Una voce della rubrica RAS può avere zero o più voci secondarie. La [**funzione RasGetEntryProperties**](/windows/desktop/api/Ras/nf-ras-rasgetentrypropertiesa) recupera una [**struttura RASENTRY**](/previous-versions/windows/desktop/legacy/aa377274(v=vs.85)) che include informazioni sulle voci secondarie di una voce della rubrica. Il **membro dwSubEntries** della **struttura RASENTRY** indica il numero di voci secondarie. Telefono voci di libri non hanno inizialmente voci secondarie. Per aggiungere voci secondarie a una voce di una rubrica telefonica, usare la [**funzione RasSetSubEntryProperties.**](/windows/desktop/api/Ras/nf-ras-rassetsubentrypropertiesa)

Le proprietà di ogni subentry includono un numero di telefono e il nome e il tipo del dispositivo TAPI da usare per la composizione della voce secondaria. Inoltre, una voce secondaria può includere un elenco di numeri di telefono alternativi da comporre se RAS non riesce a stabilire una connessione usando il numero primario. Le [**funzioni RasSetSubEntryProperties**](/windows/desktop/api/Ras/nf-ras-rassetsubentrypropertiesa) e [**RasGetSubEntryProperties**](/windows/desktop/api/Ras/nf-ras-rasgetsubentrypropertiesa) usano la [**struttura RASSUBENTRY**](/previous-versions/windows/desktop/legacy/aa377839(v=vs.85)) per impostare e recuperare le proprietà di una voce secondaria della rubrica specificata. Le voci secondarie sono identificate da un indice in base uno.

È possibile chiamare la [**funzione RasSetEntryProperties**](/windows/desktop/api/Ras/nf-ras-rassetentrypropertiesa) per configurare una voce RAS multilink per connettere tutte le voci secondarie quando viene chiamata per la prima volta. In alternativa, è possibile configurare una voce per fornire larghezza di banda variabile. In questo caso, RAS connette inizialmente una singola voce secondaria e quindi connette o disconnette le voci secondarie aggiuntive in base alle esigenze. Per una connessione multilink a larghezza di banda variabile, è possibile usare la struttura [**RASDIALPARAMS**](/previous-versions/windows/desktop/legacy/aa377238(v=vs.85)) per specificare la voce secondaria iniziale da connettere quando si chiama la [**funzione RasDial.**](/windows/desktop/api/Ras/nf-ras-rasdiala) Quando si usa [**la funzione RasDialDlg**](/windows/desktop/api/Rasdlg/nf-rasdlg-rasdialdlga) per connettere una voce multilink, è possibile usare la [**struttura RASDIALDLG**](/previous-versions/windows/desktop/legacy/aa377023(v=vs.85)) per specificare la voce secondaria iniziale per la connessione.

Per una connessione multilink a larghezza di banda variabile, usare la struttura [**RASENTRY**](/previous-versions/windows/desktop/legacy/aa377274(v=vs.85)) con la [**funzione RasSetEntryProperties**](/windows/desktop/api/Ras/nf-ras-rassetentrypropertiesa) per specificare i parametri per la connessione e la disconnessione delle singole voci secondarie. RAS connette una voce secondaria aggiuntiva quando la larghezza di banda usata supera una percentuale specificata della larghezza di banda disponibile per un intervallo specificato.

Se si chiama la [**funzione RasDial**](/windows/desktop/api/Ras/nf-ras-rasdiala) per stabilire una connessione multilink, è possibile specificare una funzione di callback [**RasDialFunc2**](/windows/desktop/api/Ras/nc-ras-rasdialfunc2) per ricevere notifiche sulla connessione. **RasDialFunc2** è simile alla funzione di callback [**RasDialFunc1,**](/windows/desktop/api/Ras/nc-ras-rasdialfunc1) ad eccezione del fatto che fornisce informazioni aggiuntive per una connessione multilink, ad esempio l'indice della voce secondaria che ha causato la notifica. RAS chiama la **funzione RasDialFunc2** quando si connette o disconnette una voce secondaria.

È possibile usare un handle **di connessione HRASCONN** per bloccarsi o recuperare informazioni su una connessione multilink. È possibile ottenere un handle di connessione per ognuna delle connessioni subentry che costituiscono il multilink, nonché per la connessione multilink combinata. Quando si chiama la [**funzione RasDial**](/windows/desktop/api/Ras/nf-ras-rasdiala) per stabilire una connessione multilink, **RasDial** restituisce un handle alla connessione multilink combinata. Analogamente, [**RasEnumConnections restituisce l'handle**](/windows/desktop/api/Ras/nf-ras-rasenumconnectionsa) multilink combinato quando si enumerano le connessioni. Per ottenere un handle per una delle connessioni subentry in una connessione multilink, chiamare la [**funzione RasGetSubEntryHandle.**](/windows/desktop/api/Ras/nf-ras-rasgetsubentryhandlea)

È possibile usare l'handle di connessione multilink combinato e gli handle di connessione della voce secondaria nelle funzioni [**RasHangUp**](/windows/desktop/api/Ras/nf-ras-rashangupa), [**RasGetConnectStatus**](/windows/desktop/api/Ras/nf-ras-rasgetconnectstatusa)e [**RasGetProjectionInfo.**](/previous-versions/windows/embedded/ms897107(v=msdn.10)) La **chiamata di RasHangUp** con un handle multilink combinato termina l'intera connessione. chiamandolo con un handle di subentry si blocca solo la connessione di tale voce secondaria. Analogamente, **RasGetConnectStatus** restituisce informazioni per la connessione combinata o singola, a seconda dell'handle specificato. Le informazioni di proiezione restituite da **RasGetProjectionInfo** per una voce multilink sono le stesse per ogni handle di connessione subentry come per l'handle di connessione principale.

 

 