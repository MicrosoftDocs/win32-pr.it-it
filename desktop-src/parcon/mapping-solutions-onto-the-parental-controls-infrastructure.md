---
description: Mapping di soluzioni nell'infrastruttura di Controllo genitori
ms.assetid: 09677019-2cf9-43fe-b16c-e802767bef3a
title: Mapping di soluzioni nell'infrastruttura di Controllo genitori
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5dcf16ec2d656828921ccd6992f2811dcf4590ab06731d1ac6474fd8d7625c26
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119951971"
---
# <a name="mapping-solutions-onto-the-parental-controls-infrastructure"></a>Mapping di soluzioni nell'infrastruttura di Controllo genitori

Sono immediatamente evidenti cinque categorie di offerte comuni di controllo dei genitori ISV e ISP/portale:

-   Applicazione client autonoma. Ad esempio, i client di posta elettronica e i lettori multimediali. Anche se i lettori multimediali hanno rischi per Internet e alcuni hanno servizi specifici, Windows Parental Controls promuove principalmente la registrazione e le restrizioni sulle attività di riproduzione solo per ridurre al minimo gli impatti della libreria e la registrazione del rumore per gli amministratori.
-   Soluzioni client/server. Gli esempi più importanti sono le soluzioni di messaggistica immediata.
-   Suite ISP. Si tratta di raccolte di soluzioni client/server e applicazioni client, spesso integrate in un'unica interfaccia utente client. Si noti che la maggior parte di queste offre anche la maggior parte o tutte le funzionalità usando l'accesso al browser, incrociando le soluzioni solo Web.
-   Soluzioni solo Web. Accesso tramite browser. Ad esempio, la funzionalità di posta elettronica e messaggistica immediata basata sul Web. L'accesso a queste categorie può essere bloccato da categorie di filtri Web popolate in modo appropriato.
-   Soluzioni simili a firewall. Fornisce filtri a livello di stack di rete e potenzialmente altre restrizioni del sistema operativo.

Consigli per l'implementazione di soluzioni conformi per ogni categoria sono specificate nella tabella seguente.



| Category                           | Registrazione                                                  | Impostazioni relative alle restrizioni                                    | Imposizione delle restrizioni                                 | Sostituzione del filtro contenuto Web                                                        | Uso del collegamento di estendibilità per la registrazione e l'accesso alle impostazioni               |
|------------------------------------|----------------------------------------------------------|----------------------------------------------------------|----------------------------------------------------------|---------------------------------------------------------------------------------------|-------------------------------------------------------------------------|
| Client "autonomo"<br/>    | Obbligatorio nel client<br/>                            | Obbligatorio nel client<br/>                            | Obbligatorio nel client<br/>                            | N/A<br/>                                                                        | Obbligatorio, sarà exe. Può semplicemente richiamare lo spostamento dell'interfaccia utente dell'app<br/>   |
| Soluzione client/server<br/>  | Obbligatorio nel client se non eseguito dal server<br/> | Obbligatorio nel client se non eseguito dal server<br/> | Obbligatorio nel client se non eseguito dal server<br/> | N/A<br/>                                                                        | Obbligatorio, sarà exe<br/>                                        |
| Famiglia di prodotti ISP<br/>               | Obbligatorio nel client se non eseguito dal server<br/> | Obbligatorio nel client se non eseguito dal server<br/> | Obbligatorio nel client se non eseguito dal server<br/> | Consigliare l'uso del filtro WPC, ma consentire la sostituzione se affidabile per più utenti<br/> | Obbligatorio, sarà exe<br/>                                        |
| Soluzione solo Web<br/>       | Consigliare l'esecuzione nel server<br/>                | Consigliare l'esecuzione nel server<br/>                | Consigliare l'esecuzione nel server<br/>                | N/A<br/>                                                                        | Consigliato. Esporre le impostazioni e la registrazione del server tramite exe<br/> |
| Soluzioni simili a firewall<br/> | Obbligatorio nel client<br/>                            | Obbligatorio nel client<br/>                            | Obbligatorio nel client<br/>                            | Consigliare l'uso del filtro WPC, ma consentire la sostituzione se affidabile per più utenti<br/> | Obbligatorio, sarà exe<br/>                                        |



 

 

 




