---
description: Se un file di configurazione automatica del proxy non è stato distribuito nella rete locale, WinHttpGetProxyForUrl non riesce a trovare un server proxy.
ms.assetid: a170e63a-8586-47df-af5e-4ee3621795b2
title: Individuazione senza un file di configurazione automatica
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 553f4f798a821ff219b587c494d5dccfbba8c4b22efd0d1692ca2069f53041de
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120097941"
---
# <a name="discovery-without-an-auto-config-file"></a>Individuazione senza un file di configurazione automatica

Se un file di configurazione automatica del proxy non è stato distribuito nella rete locale, [**WinHttpGetProxyForUrl**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpgetproxyforurl) non riesce a trovare un server proxy. Se **WinHttpGetProxyForUrl** ha esito negativo, esistono diverse possibili strategie di fall back per ottenere una configurazione proxy valida, a seconda dell'ambiente di runtime. Queste includono la richiesta dell'impostazione del proxy tramite un'interfaccia utente, la richiesta a un utente di archiviare la configurazione del proxy nel Registro di sistema usando l'utilità WinHTTP "ProxyCfg.exe" o l'uso di [**WinHttpGetIEProxyConfigForCurrentUser**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpgetieproxyconfigforcurrentuser) per verificare se un server proxy è elencato nelle impostazioni di Internet Explorer.

È possibile che non sia presente alcun file di configurazione automatica del proxy perché il client dispone di una connessione Internet diretta, ad esempio tramite un ISP, e non richiede un server proxy.

Potrebbe essere necessario un server proxy, d'altra parte, ma la rete locale potrebbe non supportare WPAD. In questo caso, la configurazione del proxy deve essere ottenuta dall'utente o trovata in un punto qualsiasi del computer client.

Un'applicazione basata su WinHTTP in esecuzione in un ambiente server di livello intermedio, ad esempio un'applicazione COM+ o ASP, deve basarsi su un amministratore del server che imposta una configurazione proxy predefinita nel Registro di sistema usando l'utilità "ProxyCfg.exe". Queste informazioni di configurazione predefinite possono quindi essere recuperate usando la funzione [**WinHttpGetDefaultProxyConfiguration**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpgetdefaultproxyconfiguration) o semplicemente specificando il flag **\_ WINHTTP ACCESS \_ TYPE \_ PRECONFIG** nella [**chiamata WinHttpOpen.**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpopen)

D'altra parte, un'applicazione WinHTTP in esecuzione in un computer desktop client può tentare di esaminare Internet Explorer proxy del client. [**WinHttpGetIEProxyConfigForCurrentUser**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpgetieproxyconfigforcurrentuser) inserisce una struttura [**WINHTTP \_ CURRENT USER \_ \_ \_ IE PROXY \_ CONFIG**](/windows/win32/api/winhttp/ns-winhttp-winhttp_current_user_ie_proxy_config) fornita dal chiamante con le impostazioni proxy Internet Explorer dell'utente corrente per la connessione attiva corrente (connessione remota, VPN o LAN). Questa configurazione può indicare che viene usato il rilevamento automatico o può specificare un URL per un file di configurazione automatica del proxy oppure può specificare un server proxy effettivo da usare oppure una combinazione dei tre. Se queste informazioni includono un URL PAC o un server proxy, l'applicazione WinHTTP può provare a usarle.

Un esempio che usa le funzioni [**WinHttpGetProxyForUrl**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpgetproxyforurl) e [**WinHttpGetIEProxyConfigForCurrentUser**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpgetieproxyconfigforcurrentuser) è disponibile negli esempi WinHTTP di Platform Software Development Kit (SDK).

 

 



