---
title: Disponibilità dei driver di grafica applicabili in Windows Update
description: La disponibilità di questi driver in Windows Update (WU) determinerà se a un utente viene offerto automaticamente un aggiornamento da Windows 7, Windows 8 o Windows 8.1 a Windows 10.
ms.assetid: 166C0FE3-CB9D-4895-91AC-6E57EC1D8B21
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 906894f317a86d851501e913e3c9491dc1f83336f7f80eefa660ee43d3510b18
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119935431"
---
# <a name="availability-of-applicable-graphics-drivers-on-windows-update"></a>Disponibilità dei driver di grafica applicabili in Windows Update

La disponibilità di questi driver in Windows Update (WU) determinerà se a un utente viene offerto automaticamente un aggiornamento da Windows 7, Windows 8 o Windows 8.1 a Windows 10. Se le analisi hardware hanno mostrato che non era disponibile alcun driver di grafica Windows Update per la scheda grafica nel PC, agli utenti non è stato offerto il sistema operativo Windows 10 aggiornato. Tuttavia, gli utenti possono comunque ottenere Windows 10 tramite altre origini ed eseguire manualmente l'aggiornamento.

Alcuni utenti non erano certi del motivo per cui non venivano offerti l'aggiornamento quando altri utenti lo erano, anche se il Gestione spazio aggiornamenti spiegava che non era disponibile alcun driver di grafica per l'hardware.

Inoltre, alcuni utenti forzavano un aggiornamento e quindi trovavano che le funzionalità grafiche e le prestazioni subivano a causa della mancanza di un driver hardware.

## <a name="mitigations"></a>Soluzioni di prevenzione

Per attenuare questo problema, gli utenti possono installare manualmente un driver meno recente, ad esempio da Windows 7, Windows 8 o Windows 8.1, dal sito Web IHV o OEM e scaricando un driver in modo esplicito. Questa operazione deve essere eseguita dopo l'aggiornamento e non è garantito il funzionamento. Non esiste alcuna soluzione supportata se non è disponibile un driver di grafica appropriato in WU. L'utente deve decidere se:

-   Rimanere nel sistema operativo precedente;
-   Accettare le limitazioni del driver software, Microsoft Basic Display Adapter (MSBDA); O
-   Acquistare una nuova scheda grafica con un driver di Windows 10 supportato.

## <a name="solutions"></a>Soluzioni

È fondamentale che gli IHV e gli OEM carichino i driver di grafica Windows 10 in WU per qualsiasi hardware che intendono supportare.

Si noti che l'hardware che ha raggiunto end-of-live (EOL) potrebbe non avere driver in WU. In questo caso non esiste alcuna soluzione: l'utente deve scegliere una delle opzioni in Mitigazioni precedenti.

 

 




