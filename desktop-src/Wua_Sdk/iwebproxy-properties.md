---
description: L'interfaccia IWebProxy definisce le proprietà seguenti.
ms.assetid: 449b19ec-dc95-40f7-87af-84fb7dacb328
title: Proprietà di IWebProxy
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 96628e7c799232b741e1834964a3a8ef6f6264c2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104401598"
---
# <a name="iwebproxy-properties"></a>Proprietà di IWebProxy

L'interfaccia [**IWebProxy**](/windows/desktop/api/Wuapi/nn-wuapi-iwebproxy) definisce le proprietà seguenti.



| Proprietà                                                   | Descrizione                                                                                                               |
|------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------|
| [**Indirizzo**](/windows/desktop/api/Wuapi/nf-wuapi-iwebproxy-get_address)                       | Ottiene e imposta l'indirizzo e il numero di porta decimale del server proxy.                                                |
| [**Rilevamento automatico**](/windows/desktop/api/Wuapi/nf-wuapi-iwebproxy-get_autodetect)                 | Ottiene e imposta un valore booleano che indica se [**IWebProxy**](/windows/desktop/api/Wuapi/nn-wuapi-iwebproxy) rileva automaticamente le impostazioni proxy. |
| [**BypassList**](/windows/desktop/api/Wuapi/nf-wuapi-iwebproxy-get_bypasslist)                 | Ottiene e imposta una raccolta di indirizzi che non utilizzano il server proxy.                                                 |
| [**BypassProxyOnLocal**](/windows/desktop/api/Wuapi/nf-wuapi-iwebproxy-get_bypassproxyonlocal) | Ottiene e imposta un valore booleano che indica se gli indirizzi locali ignorano il server proxy.                             |
| [**ReadOnly**](/windows/desktop/api/Wuapi/nf-wuapi-iwebproxy-get_readonly)                     | Ottiene un valore booleano che indica se l'oggetto [**WebProxy**](/windows/desktop/api/Wuapi/nn-wuapi-iwebproxy) è di sola lettura.                        |
| [**Nome utente**](/windows/desktop/api/Wuapi/nf-wuapi-iwebproxy-get_username)                     | Ottiene e imposta il nome utente da inviare al server proxy per l'autenticazione.                                             |



 

 

 



