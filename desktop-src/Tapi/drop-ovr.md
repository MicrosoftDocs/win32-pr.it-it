---
description: L'eliminazione o la disconnessione di una sessione termina la comunicazione. L'applicazione può inviare le informazioni utente utente al momento della disconnessione, se il provider di servizi lo supporta.
ms.assetid: dc348bb2-d564-40f8-afe3-5473c5769fa4
title: Rilascia
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9a9bf3705d9b104b8816ce4b493ec6b188c5fe1c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103966568"
---
# <a name="drop"></a>Rilascia

L'eliminazione o la disconnessione di una sessione termina la comunicazione. L'applicazione può inviare le informazioni utente utente al momento della disconnessione, se il provider di servizi lo supporta.

I motivi usuali per eliminare una sessione sono che un utente ha richiesto una disconnessione o l'altra estremità della sessione è stata eliminata. Un'operazione DROP può essere chiamata anche quando TAPI offre una sessione per l'applicazione. Se il provider di servizi supporta questo, l'effetto è che l'applicazione rifiuta la chiamata.

Quando si richiama un'operazione DROP, le sessioni correlate possono anche essere interessate. Ad esempio, l'eliminazione di una chiamata di conferenza può eliminare tutti i singoli partecipanti. I messaggi di modifica dello stato vengono inviati all'applicazione per tutte le chiamate il cui stato è interessato.

In varie configurazioni Bridged o party-line quando più entità si trovano nella chiamata, un'operazione DROP potrebbe non cancellare effettivamente la chiamata. In caso di Bridge, ad esempio, la chiamata potrebbe non essere eliminata perché lo stato di altre stazioni della chiamata può governare. Al contrario, la chiamata può essere semplicemente cambiata nello stato inattivo rimanendo connesso ad altre stazioni.

In seguito a un'operazione DROP, l'identificatore di sessione e la maggior parte delle risorse associate alla sessione rimarranno utilizzabili per la maggior parte delle operazioni di query. Quando un'applicazione non richiede più queste risorse, deve [terminare la sessione](terminate-a-session-ovr.md) per evitare perdite di memoria.

**TAPI 2. x:** Vedere [**lineDrop**](/windows/win32/api/tapi/nf-tapi-linedrop).

**TAPI 3. x:** Vedere [**ITBasicCallControl::D Disconnect**](/windows/desktop/api/tapi3if/nf-tapi3if-itbasiccallcontrol-disconnect).

 

 
