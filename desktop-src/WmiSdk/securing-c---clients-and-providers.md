---
description: Sia i provider C++ che le applicazioni client devono eseguire molte delle stesse operazioni per mantenere la sicurezza WMI.
ms.assetid: 0199f469-2666-4794-b364-36c54aa360a8
ms.tgt_platform: multiple
title: Protezione di client e provider C++
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4151440f9e85f7cd9e6590842ffd3d103242410b38f52287dba83ba3bb3faec5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118316160"
---
# <a name="securing-c-clients-and-providers"></a>Protezione di client e provider C++

Sia i provider C++ che le applicazioni client devono eseguire molte delle stesse operazioni per mantenere la sicurezza WMI.

Le applicazioni client devono impostare correttamente i livelli [di rappresentazione](setting-the-default-process-security-level-using-c-.md) e [autenticazione](setting-authentication-in-wmi.md) DCOM durante la connessione a WMI. I callback dalle [chiamate asincrone comportano](setting-security-on-an-asynchronous-call.md) rischi per la sicurezza, pertanto le applicazioni client devono eseguire controlli di accesso per garantire che il callback sia da un'origine attendibile. [](performing-access-checks.md) I client devono proteggere i [consumer di eventi temporanei e permanenti.](securing-wmi-events.md)

Un provider può [eseguire controlli di accesso](performing-access-checks.md) per assicurarsi che le risorse create siano accessibili solo dai client appropriati.

Sia i provider che i client possono anche impostare la sicurezza su una [connessione proxy](setting-the-security-on-iwbemservices-and-other-proxies.md) specifica. Entrambi possono anche abilitare [i privilegi](executing-privileged-operations.md). Un provider di eventi deve garantire che il consumer del client abbia i privilegi necessari [per ricevere un evento richiesto.](providing-events-securely.md)

Un client o un provider potrebbe dover effettuare una connessione remota che richiede un servizio di autenticazione diverso, ad esempio NTLM anziché Kerberos.

 

 



