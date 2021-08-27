---
title: Supporto dei bit di stato vari
description: Supporto dei bit di stato vari
ms.assetid: 3f967371-3d5a-4948-9008-6f4c3052bf07
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6d491e4f9ab3e41cf42510beeeb037e3b58e80a5f02ebe8e86e8bb07f3be5cb2
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120096921"
---
# <a name="miscellaneous-status-bits-support"></a>Supporto dei bit di stato vari

ActiveX I contenitori di controllo devono riconoscere e supportare i bit di stato OLEMISC \_ seguenti.



| Bit di stato                           | Necessaria?      | Commenti                                                                                                                                                                                                                                                                                                |
|--------------------------------------|----------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| ACTIVATEWHENVISIBLE<br/>       | Sì<br/> |                                                                                                                                                                                                                                                                                                         |
| IGNOREACTIVATEWHENVISIBLE<br/> | No<br/>  | Necessario per il supporto dei controlli inattivi e senza finestra. Il bit IGNOREACTIVATEWHENVISIBLE è per i contenitori che ospitano controlli inattivi e senza finestra. Il bit IGNOREACTIVATEWHENVISIBLE è stato introdotto come parte della specifica ActiveX Controls 96. Per altri dettagli, vedere questa documentazione.<br/> |
| INSIDEOUT<br/>                 | No<br/>  | Non usato in genere con i ActiveX ma con gli incorporamenti di documenti composti. Si noti che questa operazione è contraria ad alcune documentazione dell'SDK che indica che questo bit deve essere impostato per il bit ACTIVATEWHENVISIBLE da impostare.<br/>                                                                             |
| INVISIBLEATRUNTIME<br/>        | Sì<br/> | Designa un controllo che deve essere visibile in fase di progettazione, ma invisibile in fase di esecuzione.<br/>                                                                                                                                                                                                       |
| ALWAYSRUN<br/>                 | Sì<br/> |                                                                                                                                                                                                                                                                                                         |
| ACTSLIKEBUTTON<br/>            | No<br/>  | Il supporto è in genere obbligatorio anche se non è necessario per i contenitori in stile documento.<br/>                                                                                                                                                                                                    |
| ACTSLIKELABEL<br/>             | No<br/>  | Il supporto è in genere obbligatorio anche se non è necessario per i contenitori in stile documento.<br/>                                                                                                                                                                                                    |
| NOUIACTIVATE<br/>              | Sì<br/> |                                                                                                                                                                                                                                                                                                         |
| ALLINEABILE<br/>                 | No<br/>  |                                                                                                                                                                                                                                                                                                         |
| SIMPLEFRAME<br/>               | No<br/>  | Vedere [Simple Frame Site Containment](simple-frame-site-containment.md)<br/>                                                                                                                                                                                                                       |
| SETCLIENTSITEFIRST<br/>        | No<br/>  | Il supporto per questo bit è consigliato ma non obbligatorio.<br/>                                                                                                                                                                                                                                       |
| Imemode<br/>                   | No<br/>  |                                                                                                                                                                                                                                                                                                         |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Contenitori](containers.md)
</dt> </dl>

 

 





