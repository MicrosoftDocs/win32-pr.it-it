---
description: Elenco di alcuni dei possibili codici restituiti per metodi e funzioni.
ms.assetid: 391b56a1-d0aa-4d35-8dba-cf7de66513d8
title: S_PRESENT
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d6cd860fcc8268bf2b63a9498b9960da359ca210
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/26/2021
ms.locfileid: "107999338"
---
# <a name="s_present"></a>S \_ PRESENT

Elenco di alcuni dei possibili codici restituiti per metodi e funzioni.



| \#Definire                  | Descrizione                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
|---------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| S \_ OK                     | Il dispositivo viene eseguito normalmente e può essere usato per il rendering.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
| S \_ PRESENTE \_ OCCLUDED      | L'area della presentazione è occlusa. Occlusione significa che la finestra di presentazione è ridotta a icona o che un altro dispositivo è entrato nella modalità schermo intero sullo stesso monitor della finestra di presentazione e la finestra di presentazione è completamente su tale monitor. L'occlusione non si verifica se l'area client è coperta da un'altra finestra.<br/> Le applicazioni occluded possono continuare il rendering e tutte le chiamate avranno esito positivo, ma la finestra di presentazione occlusa non verrà aggiornata. Preferibilmente, l'applicazione deve interrompere il rendering nella finestra di presentazione usando il dispositivo e continuare a chiamare [**CheckDeviceState**](/windows/desktop/api/d3d9/nf-d3d9-idirect3ddevice9ex-checkdevicestate) fino a quando non viene restituito S OK o \_ S PRESENT MODE \_ \_ \_ CHANGED.<br/> |
| MODALITÀ S \_ \_ PRESENT \_ MODIFICATA | La modalità di visualizzazione del desktop è stata modificata. L'applicazione può continuare il rendering, ma potrebbe esserci una conversione/estensione del colore. Selezionare un formato di buffer nascosto simile alla modalità di visualizzazione corrente e chiamare Reset per ricreare le catene di scambio. Il dispositivo lascia questo stato dopo la chiamata a Reset.                                                                                                                                                                                                                                                                                                                                                                                                                 |



 

Altri codici di errore sono contenuti in [D3DERR](d3derr.md).

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Costanti Direct3D](dx9-graphics-reference-d3d-constants.md)
</dt> </dl>

 

 




