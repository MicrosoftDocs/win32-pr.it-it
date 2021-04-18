---
title: Confronto tra le funzioni di Windows 2000 e RRAS ridistribuibile
description: L'API RAS viene distribuita come funzionalità di Windows 2000 e sistemi operativi successivi ed è disponibile come ridistribuibile per Windows NT 4,0 con Service Pack 3 (SP3) e versioni precedenti.
ms.assetid: fd6c76b9-52e2-405e-b62e-055cfbdb5ad6
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 745ad0c50654c8269c3e62b03629a7ae12a17476
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "106298943"
---
# <a name="function-comparison-windows-2000-vs-rras-redistributable"></a>Confronto tra le funzioni: Windows 2000 e RRAS ridistribuibile

L'API RAS viene distribuita come funzionalità di Windows 2000 e sistemi operativi successivi ed è disponibile come ridistribuibile per Windows NT 4,0 con Service Pack 3 (SP3) e versioni precedenti. RAS fornisce le stesse funzionalità in entrambi i formati, ma la convenzione di denominazione utilizzata è diversa per gli elementi di riferimento in ogni versione dell'API RAS.

Le funzioni RAS per Windows NT 4,0 con SP3 e versioni precedenti iniziano in genere con il prefisso "RasAdmin". Le funzioni analoghe per il servizio Routing e accesso remoto (RRAS) iniziano con il prefisso "MprAdmin". Ad esempio, RAS fornisce una funzione denominata [**RasAdminPortGetInfo**](rasadminportgetinfo.md). La funzione analoga in RRAS è denominata [**MprAdminPortGetInfo**](/windows/desktop/api/Mprapi/nf-mprapi-mpradminportgetinfo). Come esempio simile, RAS fornisce la funzione di callback [**RasAdminGetIpAddressForUser**](rasadmingetipaddressforuser.md). RRAS fornisce una funzione di callback simile denominata [**MprAdminGetIpAddressForUser**](/windows/desktop/api/Mprapi/nf-mprapi-mpradmingetipaddressforuser). Le eccezioni a questa regola sono [**RasAdminPortClearStatistics**](rasadminportclearstatistics.md), che in RRAS è [**MprAdminPortClearStats**](/windows/desktop/api/Mprapi/nf-mprapi-mpradminportclearstats)e [**RasAdminFreeBuffer**](rasadminfreebuffer.md), che in RRAS è [**MprAdminBufferFree**](/windows/desktop/api/Mprapi/nf-mprapi-mpradminbufferfree).

Nella tabella seguente sono elencate le funzioni RAS di Windows NT 4,0 SP3 e le funzioni RRAS corrispondenti.



| RAS di Windows NT 4,0                                                                   | RRAS                                                                                 |
|--------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------|
| [**RasAdminAcceptNewConnection**](rasadminacceptnewconnection.md)                   | [**MprAdminAcceptNewConnection**](/windows/desktop/api/Mprapi/nf-mprapi-mpradminacceptnewconnection)                   |
| [**RasAdminConnectionHangupNotification**](rasadminconnectionhangupnotification.md) | [**MprAdminConnectionHangupNotification**](/windows/desktop/api/Mprapi/nf-mprapi-mpradminconnectionhangupnotification) |
| [**RasAdminFreeBuffer**](rasadminfreebuffer.md)                                     | [**MprAdminBufferFree**](/windows/desktop/api/Mprapi/nf-mprapi-mpradminbufferfree)                                     |
| [**RasAdminGetErrorString**](rasadmingeterrorstring.md)                             | [**MprAdminGetErrorString**](/windows/desktop/api/Mprapi/nf-mprapi-mpradmingeterrorstring)                             |
| [**RasAdminGetIpAddressForUser**](rasadmingetipaddressforuser.md)                   | [**MprAdminGetIpAddressForUser**](/windows/desktop/api/Mprapi/nf-mprapi-mpradmingetipaddressforuser)                   |
| [**RasAdminPortClearStatistics**](rasadminportclearstatistics.md)                   | [**MprAdminPortClearStats**](/windows/desktop/api/Mprapi/nf-mprapi-mpradminportclearstats)                             |
| [**RasAdminPortDisconnect**](rasadminportdisconnect.md)                             | [**MprAdminPortDisconnect**](/windows/desktop/api/Mprapi/nf-mprapi-mpradminportdisconnect)                             |
| [**RasAdminPortEnum**](rasadminportenum.md)                                         | [**MprAdminPortEnum**](/windows/desktop/api/Mprapi/nf-mprapi-mpradminportenum)                                         |
| [**RasAdminPortGetInfo**](rasadminportgetinfo.md)                                   | [**MprAdminPortGetInfo**](/windows/desktop/api/Mprapi/nf-mprapi-mpradminportgetinfo)                                   |
| [**RasAdminReleaseIpAddress**](rasadminreleaseipaddress.md)                         | [**MprAdminReleaseIpAddress**](/windows/desktop/api/Mprapi/nf-mprapi-mpradminreleaseipaddress)                         |
| [**RasAdminUserGetInfo**](rasadminusergetinfo.md)                                   | [**MprAdminUserGetInfo**](/windows/desktop/api/Mprapi/nf-mprapi-mpradminusergetinfo)                                   |
| [**RasAdminUserSetInfo**](rasadminusersetinfo.md)                                   | [**MprAdminUserSetInfo**](/windows/desktop/api/Mprapi/nf-mprapi-mpradminusersetinfo)                                   |



 

Sebbene le funzioni RRAS siano simili a quelle di Windows NT 4,0 con SP3 e le controparti RAS precedenti nella funzionalità, le funzioni RRAS utilizzano spesso un set di parametri diverso. Per informazioni complete sull'elenco di parametri di questa funzione, vedere la pagina di riferimento relativa a una determinata funzione.

RRAS Redistributable per Windows NT 4,0 con SP3 e versioni precedenti aggiunge le funzioni seguenti, che non hanno controparti RAS:

[**MprAdminAcceptNewLink**](/windows/desktop/api/Mprapi/nf-mprapi-mpradminacceptnewlink)

[**MprAdminConnectionClearStats**](/windows/desktop/api/Mprapi/nf-mprapi-mpradminconnectionclearstats)

[**MprAdminConnectionEnum**](/windows/desktop/api/Mprapi/nf-mprapi-mpradminconnectionenum)

[**MprAdminConnectionGetInfo**](/windows/desktop/api/Mprapi/nf-mprapi-mpradminconnectiongetinfo)

[**MprAdminGetPDCServer**](/windows/desktop/api/Mprapi/nf-mprapi-mpradmingetpdcserver)

[**MprAdminIsServiceRunning**](/windows/desktop/api/Mprapi/nf-mprapi-mpradminisservicerunning)

[**MprAdminLinkHangupNotification**](/windows/desktop/api/Mprapi/nf-mprapi-mpradminlinkhangupnotification)

[**MprAdminPortReset**](/windows/desktop/api/Mprapi/nf-mprapi-mpradminportreset)

[**MprAdminServerConnect**](/windows/desktop/api/Mprapi/nf-mprapi-mpradminserverconnect)

[**MprAdminServerDisconnect**](/windows/desktop/api/Mprapi/nf-mprapi-mpradminserverdisconnect)

Oltre alle funzioni precedenti, Windows 2000 e i sistemi operativi successivi aggiungono le funzioni seguenti:

[**MprAdminSendUserMessage**](/windows/desktop/api/Mprapi/nf-mprapi-mpradminsendusermessage)

[**MprAdminAcceptNewConnection2**](/windows/desktop/api/Mprapi/nf-mprapi-mpradminacceptnewconnection2)

[**MprAdminConnectionHangupNotification2**](/windows/desktop/api/Mprapi/nf-mprapi-mpradminconnectionhangupnotification2)

 

 




