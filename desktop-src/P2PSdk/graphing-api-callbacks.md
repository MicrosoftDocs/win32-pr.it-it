---
description: "L'API Graphing usa i callback seguenti:"
ms.assetid: a8e083ab-b5e3-4186-99fb-cbb536e9d529
title: Grafi dei callback dell'API
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0604c03ce768372e4f6fa81abfe69184ef45f49f41a2907d652b77b97902b6f9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119776251"
---
# <a name="graphing-api-callbacks"></a>Grafi dei callback dell'API

L'API Graphing usa i callback seguenti:



| Callback                                                          | Descrizione                                                                                                                                                                                                                  |
|-------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [*DATI DI SICUREZZA GRATUITI DI PFNPEER \_ \_ \_*](/windows/desktop/api/P2P/nc-p2p-pfnpeer_free_security_data) | Specifica la funzione che l'infrastruttura peer graphing chiama per liberare i dati restituiti dai callback [*PFNPEER \_ SECURE \_ RECORD*](/windows/desktop/api/P2P/nc-p2p-pfnpeer_secure_record) e [*PFNPEER \_ VALIDATE \_ RECORD.*](/windows/desktop/api/P2P/nc-p2p-pfnpeer_validate_record) |
| [*RECORD SICURO PFNPEER \_ \_*](/windows/desktop/api/P2P/nc-p2p-pfnpeer_secure_record)            | Specifica la funzione chiamata dall'infrastruttura peer graphing per proteggere i record.                                                                                                                                        |
| [*RECORD DI CONVALIDA PFNPEER \_ \_*](/windows/desktop/api/P2P/nc-p2p-pfnpeer_validate_record)        | Specifica la funzione chiamata dall'infrastruttura peer graphing per convalidare i record.                                                                                                                                      |



 

 

 



