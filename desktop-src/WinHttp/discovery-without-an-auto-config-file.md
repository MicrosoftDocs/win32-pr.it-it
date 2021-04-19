---
description: Se un file di configurazione automatica del proxy non è stato distribuito nella rete locale, WinHttpGetProxyForUrl non è in grado di trovare un server proxy.
ms.assetid: a170e63a-8586-47df-af5e-4ee3621795b2
title: Individuazione senza un file di configurazione automatica
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b6a5ec281c2ef74e2a377cecbd30f16cbc49bd79
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106319818"
---
# <a name="discovery-without-an-auto-config-file"></a>Individuazione senza un file di configurazione automatica

Se un file di configurazione automatica del proxy non è stato distribuito nella rete locale, [**WinHttpGetProxyForUrl**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpgetproxyforurl) non è in grado di trovare un server proxy. Se **WinHttpGetProxyForUrl** ha esito negativo, esistono diverse possibili strategie di fallback per ottenere una configurazione del proxy valida, a seconda dell'ambiente di Runtime. Queste includono la richiesta di impostazione del proxy tramite un'interfaccia utente, che richiede a un utente di archiviare la configurazione del proxy nel registro di sistema utilizzando l'utilità WinHTTP "ProxyCfg.exe" o l'utilizzo di [**WinHttpGetIEProxyConfigForCurrentUser**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpgetieproxyconfigforcurrentuser) per verificare se un server proxy è elencato nelle impostazioni di Internet Explorer.

È possibile che non esistano file di configurazione automatica del proxy perché il client dispone di una connessione Internet diretta, ad esempio tramite un ISP, e non necessita di un server proxy.

Potrebbe essere necessario un server proxy, d'altra parte, ma la rete locale potrebbe non supportare WPAD. In questo caso, la configurazione del proxy deve essere ottenuta dall'utente o trovata in un punto qualsiasi nel computer client.

Un'applicazione basata su WinHTTP eseguita in un ambiente server di livello intermedio, ad esempio un'applicazione COM+ o ASP, deve basarsi su un amministratore del server che imposta una configurazione proxy predefinita nel registro di sistema utilizzando l'utilità "ProxyCfg.exe". Queste informazioni di configurazione predefinite possono quindi essere recuperate tramite la funzione [**WinHttpGetDefaultProxyConfiguration**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpgetdefaultproxyconfiguration) o semplicemente specificando il flag **di \_ \_ \_ preconfigurazione del tipo di accesso WinHTTP** nella chiamata [**WinHttpOpen**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpopen) .

D'altra parte, un'applicazione WinHTTP in esecuzione su un computer desktop client può tentare di esaminare le impostazioni proxy di Internet Explorer. [**WinHttpGetIEProxyConfigForCurrentUser**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpgetieproxyconfigforcurrentuser) riempie una struttura di configurazione del [**\_ \_ \_ \_ proxy \_**](/windows/win32/api/winhttp/ns-winhttp-winhttp_current_user_ie_proxy_config) di Internet Explorer fornita dal chiamante con le impostazioni proxy di Internet Explorer dell'utente corrente per la connessione attiva corrente (connessione remota, VPN o LAN). Questa configurazione può indicare che viene utilizzato il rilevamento automatico o che può specificare un URL per un file di configurazione automatica del proxy oppure può specificare un server proxy effettivo da utilizzare oppure una combinazione dei tre. Se queste informazioni includono un URL PAC o un server proxy, l'applicazione WinHTTP può provare a usarle.

Un esempio che usa le funzioni [**WinHttpGetProxyForUrl**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpgetproxyforurl) e [**WinHttpGetIEProxyConfigForCurrentUser**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpgetieproxyconfigforcurrentuser) è reperibile negli esempi di WinHTTP per Platform Software Development Kit (SDK).

 

 



