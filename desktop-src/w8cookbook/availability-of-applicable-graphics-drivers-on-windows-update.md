---
title: Disponibilità dei driver grafici applicabili in Windows Update
description: La disponibilità di questi driver in Windows Update (WU) determinerà se a un utente viene automaticamente offerto un aggiornamento da Windows 7, Windows 8 o Windows 8.1 a Windows 10.
ms.assetid: 166C0FE3-CB9D-4895-91AC-6E57EC1D8B21
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 208e984199c8de63dfa49133a255865035c84bdd
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "106298105"
---
# <a name="availability-of-applicable-graphics-drivers-on-windows-update"></a>Disponibilità dei driver grafici applicabili in Windows Update

La disponibilità di questi driver in Windows Update (WU) determinerà se a un utente viene automaticamente offerto un aggiornamento da Windows 7, Windows 8 o Windows 8.1 a Windows 10. Se le analisi hardware hanno mostrato che non è disponibile alcun driver grafico in Windows Update per la scheda grafica del PC, agli utenti non è stato offerto il sistema operativo Windows 10 aggiornato. Tuttavia, gli utenti possono comunque ottenere Windows 10 attraverso altre origini ed eseguire manualmente l'aggiornamento.

Alcuni utenti non erano certi del motivo per cui l'aggiornamento non veniva offerto quando altre persone erano, anche se in preparazione aggiornamento è stato spiegato che non era disponibile alcun driver grafico per l'hardware.

Inoltre, alcuni utenti hanno forzato un aggiornamento e hanno quindi scoperto che la loro funzionalità grafica e le prestazioni sono state rilevate a causa della mancanza di un driver hardware.

## <a name="mitigations"></a>Soluzioni di prevenzione

Per attenuare questo problema, gli utenti possono installare manualmente un driver precedente, ad esempio Windows 7, Windows 8 o Windows 8.1, accedendo al sito Web IHV o OEM e scaricando un driver in modo esplicito. Questa operazione deve essere eseguita dopo l'aggiornamento e non è garantita. Non esiste alcuna soluzione supportata se un driver di grafica appropriato non è disponibile in WU. L'utente deve decidere se:

-   Rimanere nel sistema operativo precedente;
-   Accettare le limitazioni del driver software, Microsoft Basic Display Adapter (MSBDA); o
-   Acquistare una nuova scheda grafica con un driver Windows 10 supportato.

## <a name="solutions"></a>Soluzioni

È fondamentale che IHV e gli OEM carichino i driver grafici Windows 10 in WU per qualsiasi hardware che intende supportare.

Si noti che l'hardware che ha raggiunto la fine del Live (EOL) potrebbe non avere driver in WU. In questo caso non esiste alcuna soluzione: l'utente deve scegliere una delle opzioni in mitigazioni precedenti.

 

 




