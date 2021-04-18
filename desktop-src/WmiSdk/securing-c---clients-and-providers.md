---
description: Sia i provider C++ che le applicazioni client devono eseguire molte delle stesse operazioni per gestire la sicurezza di WMI.
ms.assetid: 0199f469-2666-4794-b364-36c54aa360a8
ms.tgt_platform: multiple
title: Protezione di client e provider C++
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ac93ee88f710bf17a2b6199b3a9b2e89279b4651
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106309892"
---
# <a name="securing-c-clients-and-providers"></a>Protezione di client e provider C++

Sia i provider C++ che le applicazioni client devono eseguire molte delle stesse operazioni per gestire la sicurezza di WMI.

Per la connessione a WMI, le applicazioni client devono impostare correttamente la [rappresentazione](setting-the-default-process-security-level-using-c-.md) DCOM e i livelli di [autenticazione](setting-authentication-in-wmi.md) . I callback da [chiamate asincrone](setting-security-on-an-asynchronous-call.md) presentano rischi per la sicurezza, quindi le applicazioni client devono [eseguire verifiche di accesso](performing-access-checks.md) per garantire che il callback provenga da un'origine attendibile. I client devono proteggere [i consumer di eventi temporanei e permanenti](securing-wmi-events.md).

Un provider può [eseguire verifiche di accesso](performing-access-checks.md) per assicurarsi che le risorse create siano accessibili solo ai client appropriati.

Sia i provider che i client possono inoltre impostare la sicurezza in una connessione [proxy specifica](setting-the-security-on-iwbemservices-and-other-proxies.md) . Entrambi possono anche abilitare i [privilegi](executing-privileged-operations.md). Un provider di eventi deve garantire che il consumer client disponga dei privilegi necessari per la [ricezione di un evento richiesto](providing-events-securely.md).

Un client o un provider potrebbe dover effettuare una connessione remota che richiede un servizio di autenticazione diverso, ad esempio NTLM invece di Kerberos.

 

 



