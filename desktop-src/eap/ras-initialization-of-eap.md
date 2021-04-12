---
title: Inizializzazione del punto di accesso di EAP
description: Al momento dell'inizializzazione, il punto di accesso (AP) interroga il registro di sistema per i protocolli di autenticazione installati.
ms.assetid: e230e01f-27df-4f61-8755-262ec11af660
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 185557c4b908780c09714aa9cc7fa4c80399812f
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2020
ms.locfileid: "104399033"
---
# <a name="access-point-initialization-of-eap"></a>Inizializzazione del punto di accesso di EAP

Al momento dell'inizializzazione, il punto di accesso (AP) interroga il registro di sistema per i protocolli di autenticazione installati. Il punto di accesso chiama quindi la funzione esportata [**RasEapGetInfo**](/previous-versions/windows/desktop/api/Raseapif/nf-raseapif-raseapgetinfo) per ogni protocollo di autenticazione. La funzione **RasEapGetInfo** riceve un singolo parametro di tipo [**PPP \_ EAP \_ info**](/windows/desktop/api/Raseapif/ns-raseapif-ppp_eap_info). Il punto di accesso usa il membro **dwEapTypeId** della struttura per specificare il protocollo di autenticazione. Si noti che una singola DLL può supportare più di un protocollo. Se **RasEapGetInfo** restituisce un valore diverso da **nessun \_ errore**, il punto di accesso presuppone che il protocollo di autenticazione non sia disponibile.

Al ritorno da [**RasEapGetInfo**](/previous-versions/windows/desktop/api/Raseapif/nf-raseapif-raseapgetinfo) , la struttura di [**\_ \_ informazioni EAP PPP**](/windows/desktop/api/Raseapif/ns-raseapif-ppp_eap_info) contiene puntatori alle funzioni [**RasEapInitialize**](/previous-versions/windows/desktop/legacy/aa363527(v=vs.85)), [**RasEapBegin**](/previous-versions/windows/desktop/legacy/aa363520(v=vs.85)), [**RasEapMakeMessage**](/previous-versions/windows/desktop/legacy/aa363532(v=vs.85))e [**RasEapEnd**](/previous-versions/windows/desktop/legacy/aa363521(v=vs.85)) nella DLL EAP. Il servizio AP Usa queste funzioni per interagire con il protocollo di autenticazione. Il punto di accesso chiama immediatamente **RasEapInitialize** per ogni protocollo di autenticazione per inizializzarlo. Quando il servizio viene arrestato, chiama di nuovo **RasEapInitialize** , questa volta con il parametro *FInitialize* impostato su **false** per indicare che il protocollo di autenticazione dovrebbe arrestarsi.

 

 