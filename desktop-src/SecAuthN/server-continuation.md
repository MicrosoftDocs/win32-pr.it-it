---
description: In base al codice restituito da una chiamata precedente a AcceptSecurityContext (generale), il server può attendere una risposta dal client e può partecipare a scambi aggiuntivi con il client.
ms.assetid: 281e1f81-3524-4034-bee5-cef6b13cf402
title: Continuazione server
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 22fba8a60bea12daae0e6aaf93fed55fead5738c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106311599"
---
# <a name="server-continuation"></a>Continuazione server

In base al codice restituito da una chiamata precedente a [**AcceptSecurityContext (generale)**](/windows/win32/api/sspi/nf-sspi-acceptsecuritycontext), il server può attendere una risposta dal client e può partecipare a scambi aggiuntivi con il client. Per continuare il protocollo di autenticazione, il server ripete le chiamate a **AcceptSecurityContext (generale)**.

Lo stato restituito da [**AcceptSecurityContext (generale)**](/windows/win32/api/sspi/nf-sspi-acceptsecuritycontext) viene controllato per verificare se il server deve attendere messaggi aggiuntivi dal client. Nella maggior parte dei protocolli di autenticazione è disponibile un numero massimo di scambi anche per l'autenticazione reciproca. Attualmente, i protocolli NTLM e [*Kerberos*](../secgloss/k-gly.md) eseguono l'autenticazione reciproca con tre scambi.

 

 
