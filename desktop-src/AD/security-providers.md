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
# <a name="security-providers"></a><span data-ttu-id="80c8b-103">Provider di sicurezza</span><span class="sxs-lookup"><span data-stu-id="80c8b-103">Security Providers</span></span>

<span data-ttu-id="80c8b-104">Security Support Provider Interface (SSPI) fornisce il supporto per l'autenticazione reciproca ed è esposto direttamente tramite le API SSPI e i servizi a livello di SSPI, inclusa la RPC.</span><span class="sxs-lookup"><span data-stu-id="80c8b-104">The Security Support Provider Interface (SSPI) provides support for mutual authentication and is exposed directly through the SSPI APIs and services layered on SSPI, including RPC.</span></span>

<span data-ttu-id="80c8b-105">Non tutti i pacchetti di sicurezza disponibili per SSPI supportano l'autenticazione reciproca.</span><span class="sxs-lookup"><span data-stu-id="80c8b-105">Not all security packages available to SSPI support mutual authentication.</span></span> <span data-ttu-id="80c8b-106">Per ottenere l'autenticazione reciproca, l'applicazione deve richiedere l'autenticazione reciproca e un pacchetto di sicurezza che la supporti.</span><span class="sxs-lookup"><span data-stu-id="80c8b-106">To obtain mutual authentication, the application must request mutual authentication and a security package that supports it.</span></span> <span data-ttu-id="80c8b-107">Ad esempio, l'esempio di codice nell' [autenticazione reciproca in un servizio Windows Sockets con SCP](mutual-authentication-in-a-windows-sockets-service-with-an-scp.md) usa il pacchetto "Negotiate" in Secur32.dll, incluso in Windows 2000.</span><span class="sxs-lookup"><span data-stu-id="80c8b-107">For example, the code example in [Mutual Authentication in a Windows Sockets Service with an SCP](mutual-authentication-in-a-windows-sockets-service-with-an-scp.md) uses the "negotiate" package in Secur32.dll, which is included with Windows 2000.</span></span>

 

 




