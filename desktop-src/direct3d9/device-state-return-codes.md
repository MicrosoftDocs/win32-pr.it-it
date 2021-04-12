---
description: Elenco di alcuni dei possibili codici restituiti per i metodi e le funzioni.
ms.assetid: 391b56a1-d0aa-4d35-8dba-cf7de66513d8
title: S_PRESENT
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a4146a65e9092dcd3fed261c127e84fe8552128a
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "104225376"
---
# <a name="s_present"></a>S \_ presente

Elenco di alcuni dei possibili codici restituiti per i metodi e le funzioni.



|                           |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                         |
|---------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| \#definire                  | Descrizione                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
| \_OK                     | Il dispositivo è in esecuzione normalmente e può essere usato per il rendering.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
| S \_ presente \_ nascosto      | L'area di presentazione è nascosto. L'occlusione indica che la finestra di presentazione è ridotta a icona o che un altro dispositivo è entrato in modalità schermo intero sullo stesso monitor della finestra di presentazione e la finestra di presentazione è completamente su tale monitoraggio. L'occlusione non verrà eseguita se l'area client è coperta da un'altra finestra.<br/> Le applicazioni non riuscite possono continuare il rendering e tutte le chiamate riusciranno, ma la finestra di presentazione non verrà aggiornata. Preferibilmente, l'applicazione deve arrestare il rendering nella finestra di presentazione usando il dispositivo e continuando a chiamare [**CheckDeviceState**](/windows/desktop/api/d3d9/nf-d3d9-idirect3ddevice9ex-checkdevicestate) fino a quando non viene \_ modificata la modalità presente di S OK o s \_ \_ \_ .<br/> |
| \_modalità presente \_ S \_ modificata | La modalità di visualizzazione del desktop è stata modificata. L'applicazione può continuare il rendering, ma è possibile che la conversione o l'allungamento dei colori sia sufficiente. Selezionare un formato di buffer nascosto simile alla modalità di visualizzazione corrente e chiamare Reset per ricreare le catene di scambio. Il dispositivo lascerà questo stato dopo la chiamata di reset.                                                                                                                                                                                                                                                                                                                                                                                                                 |



 

Altri codici di errore sono contenuti in [D3DERR](d3derr.md).

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Costanti Direct3D](dx9-graphics-reference-d3d-constants.md)
</dt> </dl>

 

 




