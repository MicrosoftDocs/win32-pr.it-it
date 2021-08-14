---
description: In base al codice restituito da una chiamata precedente ad AcceptSecurityContext (Generale), il server può attendere una risposta dal client e può partecipare a scambi aggiuntivi con il client.
ms.assetid: 281e1f81-3524-4034-bee5-cef6b13cf402
title: Continuazione del server
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 06863a0e94fcfe65c7ab695d30be92044fe7341ffa0eb9091c5f1a81acdffc58
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118918290"
---
# <a name="server-continuation"></a>Continuazione del server

In base al codice restituito da una chiamata precedente ad [**AcceptSecurityContext (Generale),**](/windows/win32/api/sspi/nf-sspi-acceptsecuritycontext)il server può attendere una risposta dal client e può partecipare a scambi aggiuntivi con il client. Per continuare il protocollo di autenticazione, il server ripete le chiamate ad **AcceptSecurityContext (Generale).**

Lo stato restituito [**da AcceptSecurityContext (Generale)**](/windows/win32/api/sspi/nf-sspi-acceptsecuritycontext) viene controllato per verificare se il server deve attendere altri messaggi dal client. Nella maggior parte dei protocolli di autenticazione esiste un numero massimo di scambi anche per l'autenticazione reciproca. Attualmente, entrambi i protocolli NTLM [*e Kerberos*](../secgloss/k-gly.md) eseguono l'autenticazione reciproca con tre scambi.

 

 
