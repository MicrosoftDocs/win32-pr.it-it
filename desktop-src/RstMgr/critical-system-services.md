---
title: Servizi di sistema critici
description: I servizi di sistema critici non possono essere arrestati e riavviati da Gestione riavvio senza riavvio del sistema. Gli aggiornamenti a qualsiasi file o risorsa in uso da parte di uno di questi servizi richiedono un riavvio del sistema.
ms.assetid: 8db7c91c-2f96-4d0c-a5b8-59c41a7e4845
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 14a8fcc921d065dda0670e27e240c93515bc8cb9
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104045407"
---
# <a name="critical-system-services"></a>Servizi di sistema critici

I servizi di sistema critici non possono essere arrestati e riavviati da Gestione riavvio senza riavvio del sistema. Gli aggiornamenti a qualsiasi file o risorsa in uso da parte di uno di questi servizi richiedono un riavvio del sistema.

**Per determinare se un processo è un servizio di sistema critico.**

1.  Registrare il processo utilizzando la funzione [**RmRegisterResources**](/windows/desktop/api/RestartManager/nf-restartmanager-rmregisterresources) .
2.  Chiamare la funzione [**RmGetList**](/windows/desktop/api/RestartManager/nf-restartmanager-rmgetlist) per ottenere la struttura delle [**\_ \_ informazioni del processo RM**](/windows/desktop/api/RestartManager/ns-restartmanager-rm_process_info) .
3.  Il membro **ApplicationType** della struttura di [**\_ \_ informazioni del processo RM**](/windows/desktop/api/RestartManager/ns-restartmanager-rm_process_info) restituito contiene un valore di enumerazione del [**\_ \_ tipo di app RM**](/windows/desktop/api/RestartManager/ne-restartmanager-rm_app_type) . Questo valore è impostato su **RmCriticial** per un processo di sistema critico.

I servizi di sistema critici includono smss.exe, csrss.exe, wininit.exe, logonui.exe, lsass.exe, services.exe, winlogon.exe, System, svchost.exe con RPCSS e svchost.exe con DCOM/PnP.

 

 




