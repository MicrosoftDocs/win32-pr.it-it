---
description: "L'API Graphing usa i callback seguenti:"
ms.assetid: a8e083ab-b5e3-4186-99fb-cbb536e9d529
title: Callback dell'API Graphing
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c11f4f559307e457822cd0e7ce18ef4b44119697
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104050022"
---
# <a name="graphing-api-callbacks"></a>Callback dell'API Graphing

L'API Graphing usa i callback seguenti:



| Callback                                                          | Descrizione                                                                                                                                                                                                                  |
|-------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [*PFNPEER \_ \_ i dati di sicurezza gratuiti \_*](/windows/desktop/api/P2P/nc-p2p-pfnpeer_free_security_data) | Specifica la funzione chiamata dall'infrastruttura peer Graphing per liberare i dati restituiti da [*PFNPEER \_ Secure \_ record*](/windows/desktop/api/P2P/nc-p2p-pfnpeer_secure_record) e [*PFNPEER \_ Validate \_ record*](/windows/desktop/api/P2P/nc-p2p-pfnpeer_validate_record) Callbacks. |
| [*\_record sicuro \_ PFNPEER*](/windows/desktop/api/P2P/nc-p2p-pfnpeer_secure_record)            | Specifica la funzione chiamata dall'infrastruttura del Peer Graphing per proteggere i record.                                                                                                                                        |
| [*\_record di convalida PFNPEER \_*](/windows/desktop/api/P2P/nc-p2p-pfnpeer_validate_record)        | Specifica la funzione chiamata dall'infrastruttura del Peer Graphing per convalidare i record.                                                                                                                                      |



 

 

 



