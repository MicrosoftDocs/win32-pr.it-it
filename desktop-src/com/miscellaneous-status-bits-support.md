---
title: Supporto BITS di stato vario
description: Supporto BITS di stato vario
ms.assetid: 3f967371-3d5a-4948-9008-6f4c3052bf07
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4c281b52283796d67c476e8ee00383436bc2235a
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104044034"
---
# <a name="miscellaneous-status-bits-support"></a>Supporto BITS di stato vario

I contenitori di controlli ActiveX devono riconoscere e supportare i seguenti bit di stato di OLEMISC \_ .



| Bit di stato                           | Necessaria?      | Commenti                                                                                                                                                                                                                                                                                                |
|--------------------------------------|----------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| ACTIVATEWHENVISIBLE<br/>       | Sì<br/> |                                                                                                                                                                                                                                                                                                         |
| IGNOREACTIVATEWHENVISIBLE<br/> | No<br/>  | Necessaria per il supporto di controlli inattivi e senza finestra. Il bit IGNOREACTIVATEWHENVISIBLE è per i contenitori che ospitano controlli inattivi e senza finestra. Il bit IGNOREACTIVATEWHENVISIBLE è stato introdotto come parte della specifica ActiveX Controls 96. per ulteriori informazioni, vedere questa documentazione.<br/> |
| INSIDEOUT<br/>                 | No<br/>  | Non viene in genere utilizzato con i controlli ActiveX, bensì con incorporamenti di documenti composti. Si noti che questo bit è contrario a una documentazione dell'SDK che indica che questo bit deve essere impostato in modo da impostare il bit ACTIVATEWHENVISIBLE.<br/>                                                                             |
| INVISIBLEATRUNTIME<br/>        | Sì<br/> | Definisce un controllo che deve essere visibile in fase di progettazione, ma invisibile in fase di esecuzione.<br/>                                                                                                                                                                                                       |
| ALWAYSRUN<br/>                 | Sì<br/> |                                                                                                                                                                                                                                                                                                         |
| ACTSLIKEBUTTON<br/>            | No<br/>  | Il supporto in genere è obbligatorio anche se non è necessario per i contenitori di stile del documento.<br/>                                                                                                                                                                                                    |
| ACTSLIKELABEL<br/>             | No<br/>  | Il supporto in genere è obbligatorio anche se non è necessario per i contenitori di stile del documento.<br/>                                                                                                                                                                                                    |
| NOUIACTIVATE<br/>              | Sì<br/> |                                                                                                                                                                                                                                                                                                         |
| REGOLABILE<br/>                 | No<br/>  |                                                                                                                                                                                                                                                                                                         |
| SIMPLEFRAME<br/>               | No<br/>  | Vedere il contenuto di un [sito con frame semplice](simple-frame-site-containment.md)<br/>                                                                                                                                                                                                                       |
| SETCLIENTSITEFIRST<br/>        | No<br/>  | Il supporto per questo bit è consigliato ma non obbligatorio.<br/>                                                                                                                                                                                                                                       |
| IMEMODE<br/>                   | No<br/>  |                                                                                                                                                                                                                                                                                                         |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Contenitori](containers.md)
</dt> </dl>

 

 





