---
title: Provider di sicurezza
description: Security Support Provider Interface (SSPI) fornisce il supporto per l'autenticazione reciproca ed è esposto direttamente tramite le API SSPI e i servizi a livello di SSPI, inclusa la RPC.
ms.assetid: 3aa64aa1-c707-489f-a0a3-08bf6ac151ec
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bcf033550c2a2da66b7eab05f23289ba988690e7
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104044094"
---
# <a name="security-providers"></a>Provider di sicurezza

Security Support Provider Interface (SSPI) fornisce il supporto per l'autenticazione reciproca ed è esposto direttamente tramite le API SSPI e i servizi a livello di SSPI, inclusa la RPC.

Non tutti i pacchetti di sicurezza disponibili per SSPI supportano l'autenticazione reciproca. Per ottenere l'autenticazione reciproca, l'applicazione deve richiedere l'autenticazione reciproca e un pacchetto di sicurezza che la supporti. Ad esempio, l'esempio di codice nell' [autenticazione reciproca in un servizio Windows Sockets con SCP](mutual-authentication-in-a-windows-sockets-service-with-an-scp.md) usa il pacchetto "Negotiate" in Secur32.dll, incluso in Windows 2000.

 

 




