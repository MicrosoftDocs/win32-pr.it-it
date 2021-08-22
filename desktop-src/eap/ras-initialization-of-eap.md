---
title: Inizializzazione del punto di accesso di EAP
description: Al momento dell'inizializzazione, il punto di accesso (AP) esegue una query nel Registro di sistema per trovare i protocolli di autenticazione installati.
ms.assetid: e230e01f-27df-4f61-8755-262ec11af660
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b4ff650df29a446527224d8160b4080a252d525d26d32efedae254755ac9514a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118984431"
---
# <a name="access-point-initialization-of-eap"></a>Inizializzazione del punto di accesso di EAP

Al momento dell'inizializzazione, il punto di accesso (AP) esegue una query nel Registro di sistema per trovare i protocolli di autenticazione installati. Il punto di accesso chiama quindi la funzione esportata [**RasEapGetInfo**](/previous-versions/windows/desktop/api/Raseapif/nf-raseapif-raseapgetinfo) per ogni protocollo di autenticazione. La **funzione RasEapGetInfo** riceve un singolo parametro di tipo [**PPP \_ EAP \_ INFO.**](/windows/desktop/api/Raseapif/ns-raseapif-ppp_eap_info) Il punto di accesso usa **il membro dwEapTypeId** di questa struttura per specificare il protocollo di autenticazione. Si noti che una singola DLL può supportare più di un protocollo. Se **RasEapGetInfo** restituisce un valore diverso da **NO \_ ERROR,** il punto di accesso presuppone che il protocollo di autenticazione non sia disponibile.

Al ritorno da [**RasEapGetInfo,**](/previous-versions/windows/desktop/api/Raseapif/nf-raseapif-raseapgetinfo) la struttura [**\_ PPP EAP \_ INFO**](/windows/desktop/api/Raseapif/ns-raseapif-ppp_eap_info) contiene puntatori alle funzioni [**RasEapInitialize,**](/previous-versions/windows/desktop/legacy/aa363527(v=vs.85)) [**RasEapBegin,**](/previous-versions/windows/desktop/legacy/aa363520(v=vs.85)) [**RasEapMakeMessage**](/previous-versions/windows/desktop/legacy/aa363532(v=vs.85))e [**RasEapEnd**](/previous-versions/windows/desktop/legacy/aa363521(v=vs.85)) nella DLL EAP. Il servizio AP usa queste funzioni per interagire con il protocollo di autenticazione. Il punto di accesso chiama **immediatamente RasEapInitialize** per ogni protocollo di autenticazione per inizializzarlo. Quando il servizio viene arrestato, chiama **nuovamente RasEapInitialize,** questa volta con il parametro *fInitialize* impostato su **FALSE** per indicare che il protocollo di autenticazione deve arrestarsi.

 

 