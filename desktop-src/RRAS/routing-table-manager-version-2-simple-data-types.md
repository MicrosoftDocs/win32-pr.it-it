---
title: Tipi di dati semplici di Routing Table Manager versione 2
description: L'API RTMv2 definisce diversi tipi di dati semplici. Nella tabella seguente sono elencati questi tipi di dati.
ms.assetid: e935518e-b8d8-47fb-b2b2-c9750c2b540e
keywords:
- Servizio Routing e accesso remoto RRAS, gestione tabelle di routing versione 2, tipi di dati semplici
- Gestione tabelle di routing versione 2 RRAS, tipi di dati semplici
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b6dbd7530799c1c7e1702e0384d51b37a77dda0d
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103712088"
---
# <a name="routing-table-manager-version-2-simple-data-types"></a>Tipi di dati semplici di Routing Table Manager versione 2

L'API RTMv2 definisce diversi tipi di dati semplici. Nella tabella seguente sono elencati questi tipi di dati.



| Tipo di dati                                                                                                                                                                                                                                                                                                                   | Descrizione                                                                                                                                      | Typedef              |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------|----------------------|
| \_ID Vista RTM \_ , \* \_ ID vista \_ PRTM                                                                                                                                                                                                                                                                                             | Identifica una visualizzazione specifica.                                                                                                                    | INT                  |
| \_ \_ set di viste DWORD RTM \* , \_ set di viste PRTM \_                                                                                                                                                                                                                                                                                     | Identifica un set di visualizzazioni; espressa come maschera.                                                                                                  | DWORD                |
| \_handle di entità RTM \_ , handle di \* \_ entità PRTM \_ , handle di \_ destinazione RTM \_ , handle di \* \_ destinazione PRTM \_ , handle di \_ route RTM \_ , handle di \* \_ Route PRTM \_ , \_ \_ handle di NEXTHOP RTM, handle PRTM \* \_ NEXTHOP \_ , handle di \_ enumerazione RTM \_ , handle di \* \_ enumerazione PRTM \_ , \_ \_ handle elenco route RTM, handle \_ \* elenco Route PRTM \_ \_ \_ \_ \_ \* \_ \_ , handle di notifica RTM, gestione notifiche PRTM | Handle che puntano a dati RTMv2.                                                                                                                  | HANDLE               |
| \_ \_ \_ tipo di metodo di entità RTM, \* tipo di \_ metodo di entità PRTM \_ \_                                                                                                                                                                                                                                                                     | Identifica i metodi esportati da un client registrato.                                                                                              | DWORD                |
| \_ \_ metodo di esportazione entità RTM \_ , \* \_ metodo di esportazione entità PRTM \_ \_                                                                                                                                                                                                                                                                 | Specifica il prototipo comune per i metodi client.                                                                                               | \_\_Metodo Entity     |
| \_ \_ flag di modifica della route RTM \_ , \* flag di modifica della \_ Route PRTM \_ \_                                                                                                                                                                                                                                                                     | Flag di input e di output utilizzati per specificare lo stato quando viene aggiunta o aggiornata una route.                                                               | DWORD                |
| \_ \_ flag di modifica NEXTHOP RTM \_ , \* \_ flag di modifica PRTM NEXTHOP \_ \_                                                                                                                                                                                                                                                                 | Flag di output utilizzati per specificare lo stato quando viene aggiunto un hop successivo.                                                                                 | DWORD                |
| \_ \_ flag di corrispondenza RTM \* , \_ flag di corrispondenza PRTM \_                                                                                                                                                                                                                                                                                     | Flag di input utilizzati per specificare i criteri per la corrispondenza delle route nella tabella di routing.                                                                  | DWORD                |
| \_flag enum RTM \_ , \* \_ flag enum \_ PRTM                                                                                                                                                                                                                                                                                       | Identifica le enumerazioni.                                                                                                                         | DWORD                |
| \_ \_ flag di notifica RTM \* , \_ flag di notifica PRTM \_                                                                                                                                                                                                                                                                                   | Flag di output utilizzati per specificare il tipo di notifica da emettere; composto come segue: (tipi di modifiche \| DestS) a cui un client è interessato. | DWORD                |
| \_callback evento RTM \_ , \* \_ callback evento PRTM \_ ;                                                                                                                                                                                                                                                                              | Identifica il callback utilizzato per notificare ai client che si è verificata una modifica nello stato della route o nei client registrati.                                  | \_callback evento \_ RTM |



 

 

 




