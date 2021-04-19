---
description: Mapping di soluzioni nell'infrastruttura dei controlli padre
ms.assetid: 09677019-2cf9-43fe-b16c-e802767bef3a
title: Mapping di soluzioni nell'infrastruttura dei controlli padre
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ea410663af2e3b2363b7026a6997da5c19a1077a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106311836"
---
# <a name="mapping-solutions-onto-the-parental-controls-infrastructure"></a>Mapping di soluzioni nell'infrastruttura dei controlli padre

Cinque categorie di ISV comuni e di provider di servizi e di controllo parentale del portale sono facilmente evidenti:

-   Applicazione client autonoma. Esempi sono i client di posta elettronica e i lettori multimediali. Sebbene i lettori multimediali abbiano rischi per Internet e altri abbiano servizi specifici, i controlli padre di Windows favoriscono principalmente la registrazione e le restrizioni sulle attività di riproduzione solo per ridurre al minimo gli effetti della libreria e la registrazione di rumori per gli amministratori.
-   Soluzioni client/server. Gli esempi più importanti sono le soluzioni di messaggistica immediata.
-   Suite ISP. Si tratta di raccolte di soluzioni client/server e applicazioni client, spesso integrate in una singola interfaccia utente client. Si noti che la maggior parte di questi fornisce anche la maggior parte o tutte le funzionalità usando l'accesso al browser, attraversando le soluzioni solo Web.
-   Soluzioni Web. Accesso tramite browser. Esempi sono la funzionalità di posta elettronica e messaggistica immediata basata sul Web. È possibile che l'accesso a questi blocchi venga bloccato dalle categorie di filtri Web compilate in modo appropriato.
-   Soluzioni simili al firewall. Fornisce il filtro a livello di stack di rete e potenzialmente altre restrizioni del sistema operativo.

Nella tabella seguente sono indicati i suggerimenti per l'implementazione di soluzioni conformi per ogni categoria.



| Category                           | Registrazione                                                  | Impostazioni delle restrizioni                                    | Imposizione delle restrizioni                                 | Sostituzione filtro contenuto Web                                                        | Uso del collegamento di estendibilità per la registrazione e l'accesso alle impostazioni               |
|------------------------------------|----------------------------------------------------------|----------------------------------------------------------|----------------------------------------------------------|---------------------------------------------------------------------------------------|-------------------------------------------------------------------------|
| Client "autonomo"<br/>    | Obbligatorio sul client<br/>                            | Obbligatorio sul client<br/>                            | Obbligatorio sul client<br/>                            | N/D<br/>                                                                        | Obbligatoria, sarà exe. Può semplicemente richiamare la navigazione dell'interfaccia utente dell'app<br/>   |
| Soluzione client/server<br/>  | Obbligatorio sul client se non eseguito dal server<br/> | Obbligatorio sul client se non eseguito dal server<br/> | Obbligatorio sul client se non eseguito dal server<br/> | N/D<br/>                                                                        | Obbligatorio, sarà exe<br/>                                        |
| Suite ISP<br/>               | Obbligatorio sul client se non eseguito dal server<br/> | Obbligatorio sul client se non eseguito dal server<br/> | Obbligatorio sul client se non eseguito dal server<br/> | È consigliabile usare il filtro WPC, ma è possibile sostituirlo se è affidabile per più utenti<br/> | Obbligatorio, sarà exe<br/>                                        |
| Soluzione solo Web<br/>       | Consigliare l'esecuzione nel server<br/>                | Consigliare l'esecuzione nel server<br/>                | Consigliare l'esecuzione nel server<br/>                | N/D<br/>                                                                        | Consigliato. Esporre le impostazioni e la registrazione del server tramite exe<br/> |
| Soluzioni simili al firewall<br/> | Obbligatorio sul client<br/>                            | Obbligatorio sul client<br/>                            | Obbligatorio sul client<br/>                            | È consigliabile usare il filtro WPC, ma è possibile sostituirlo se è affidabile per più utenti<br/> | Obbligatorio, sarà exe<br/>                                        |



 

 

 




