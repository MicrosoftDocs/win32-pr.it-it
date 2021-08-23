---
title: Servizi di sistema critici
description: I servizi di sistema critici non possono essere arrestati e riavviati da Gestione riavvio senza un riavvio del sistema. Gli aggiornamenti a qualsiasi file o risorsa in uso da uno di questi servizi richiedono un riavvio del sistema.
ms.assetid: 8db7c91c-2f96-4d0c-a5b8-59c41a7e4845
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cb8a50eca43a62d24e0ab6363844bef7457aaf05b34251f5d804dacabaead5e4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119010229"
---
# <a name="critical-system-services"></a>Servizi di sistema critici

I servizi di sistema critici non possono essere arrestati e riavviati da Gestione riavvio senza un riavvio del sistema. Gli aggiornamenti a qualsiasi file o risorsa in uso da uno di questi servizi richiedono un riavvio del sistema.

**Per determinare se un processo è un servizio di sistema critico.**

1.  Registrare il processo usando la [**funzione RmRegisterResources.**](/windows/desktop/api/RestartManager/nf-restartmanager-rmregisterresources)
2.  Chiamare la [**funzione RmGetList**](/windows/desktop/api/RestartManager/nf-restartmanager-rmgetlist) per ottenere la [**struttura RM PROCESS \_ \_ INFO.**](/windows/desktop/api/RestartManager/ns-restartmanager-rm_process_info)
3.  Il **membro ApplicationType** della struttura [**RM PROCESS \_ \_ INFO**](/windows/desktop/api/RestartManager/ns-restartmanager-rm_process_info) restituita contiene un [**valore di enumerazione RM APP \_ \_ TYPE.**](/windows/desktop/api/RestartManager/ne-restartmanager-rm_app_type) Questo valore è impostato su **RmCriticial per** un processo di sistema critico.

I servizi di sistema critici includono smss.exe, csrss.exe, wininit.exe, logonui.exe, lsass.exe, services.exe, winlogon.exe, System, svchost.exe con RPCSS e svchost.exe con Dcom/PnP.

 

 




