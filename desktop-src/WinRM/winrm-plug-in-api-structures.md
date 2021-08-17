---
title: Strutture dell'API plug-in WinRM
description: Strutture dell'API plug-in WinRM
ms.assetid: 745619bc-c7b3-48fa-8212-cb1b5b9ed4db
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a4a57cbc31ae19bd858a191cec827760d055a87fc7ca19b134f61b17f8fd065e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117742770"
---
# <a name="winrm-plug-in-api-structures"></a>Strutture dell'API plug-in WinRM

La tabella seguente offre una panoramica delle strutture nell'API (Application Programming Interface) del plug-in Windows Remote Management (WinRM).



| Struttura                                                        | Descrizione                                                                              |
|------------------------------------------------------------------|------------------------------------------------------------------------------------------|
| [**WSMAN \_ AUTHZ \_ QUOTA**](/windows/desktop/api/Wsman/ns-wsman-wsman_authz_quota)                 | Definisce le informazioni sulle quote in base all'utente.                                           |
| [**DETTAGLI DEL CERTIFICATO WSMAN \_ \_**](/windows/desktop/api/Wsman/ns-wsman-wsman_certificate_details) | Rappresenta i campi all'interno del certificato client.                                     |
| [**COMANDO \_ \_ WSMAN ARG \_ SET**](/windows/desktop/api/Wsman/ns-wsman-wsman_command_arg_set)        | Rappresenta il set di argomenti passati alla riga di comando.                  |
| [**FILTRO \_ WSMAN**](/windows/desktop/api/Wsman/ns-wsman-wsman_filter)                            | Definisce il filtro utilizzato per un'operazione.                                             |
| [**FRAMMENTO \_ WSMAN**](/windows/desktop/api/Wsman/ns-wsman-wsman_fragment)                        | Definisce le informazioni sul frammento per un'operazione.                                       |
| [**INFORMAZIONI SULL'OPERAZIONE WSMAN \_ \_**](/windows/desktop/api/Wsman/ns-wsman-wsman_operation_info)           | Rappresenta un punto finale della risorsa specifico per il quale il plug-in deve eseguire la richiesta. |
| [**RICHIESTA DEL PLUG-IN WSMAN \_ \_**](/windows/desktop/api/Wsman/ns-wsman-wsman_plugin_request)           | Contiene informazioni sulla richiesta e viene passato a ogni operazione del plug-in.       |
| [**DETTAGLI DEL MITTENTE WSMAN \_ \_**](/windows/desktop/api/Wsman/ns-wsman-wsman_sender_details)           | Specifica i dettagli del client per ogni richiesta in ingresso.                                      |



 

 

 




