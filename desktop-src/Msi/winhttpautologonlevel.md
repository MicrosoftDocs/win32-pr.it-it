---
description: Il criterio di accesso automatico (accesso automatico) determina quando è accettabile che WinHTTP includa le credenziali predefinite in una richiesta al server.
ms.assetid: 4ED8B6BC-E52D-4DE9-A9AE-1FDF61A978A9
title: WinHttpAutoLogonLevel
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7760faa94e24b7fe5b33717c504b03e4de42c0aa
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103882697"
---
# <a name="winhttpautologonlevel"></a><span data-ttu-id="5cb20-103">WinHttpAutoLogonLevel</span><span class="sxs-lookup"><span data-stu-id="5cb20-103">WinHttpAutoLogonLevel</span></span>

<span data-ttu-id="5cb20-104">Il criterio di accesso automatico (accesso automatico) determina quando è accettabile che *WinHTTP* includa le credenziali predefinite in una richiesta al server.</span><span class="sxs-lookup"><span data-stu-id="5cb20-104">The automatic logon (auto-logon) policy determines when it is acceptable for *WinHTTP* to include the default credentials in a request to the server.</span></span>

<span data-ttu-id="5cb20-105">È possibile impostare questo valore su **L** per il livello di sicurezza automatico WinHTTP ( **\_ \_ \_ \_ bassa**), impostare su **M** per il livello di sicurezza di WinHTTP AutoLogon **\_ \_ \_ \_ media** e impostare su **H** per il **livello di sicurezza con \_ logo automatico WinHTTP \_ \_ \_ alto**.</span><span class="sxs-lookup"><span data-stu-id="5cb20-105">You can set this value to **L** for **WINHTTP\_AUTOLOGON\_SECURITY\_LEVEL\_LOW**, set to **M** for **WINHTTP\_AUTOLOGON\_SECURITY\_LEVEL\_MEDIUM**, and set to **H** for **WINHTTP\_AUTOLOGON\_SECURITY\_LEVEL\_HIGH**.</span></span> <span data-ttu-id="5cb20-106">Il livello predefinito è **la \_ \_ \_ \_ media del livello di sicurezza WinHTTP AutoLogon**.</span><span class="sxs-lookup"><span data-stu-id="5cb20-106">The default level is **WINHTTP\_AUTOLOGON\_SECURITY\_LEVEL\_MEDIUM**.</span></span> <span data-ttu-id="5cb20-107">Per ulteriori informazioni sui criteri di accesso automatici, vedere la sezione relativa all' [autenticazione in WinHTTP](../winhttp/authentication-in-winhttp.md).</span><span class="sxs-lookup"><span data-stu-id="5cb20-107">For more information about automatic logon policy, see the section for [Authentication in WinHTTP](../winhttp/authentication-in-winhttp.md).</span></span>

<span data-ttu-id="5cb20-108">**Windows 8 e Windows Server 2012:** Questo criterio richiede l'esecuzione di Windows Installer in Windows 8 o Windows Server 2012 e non è disponibile in tutte le versioni precedenti di Windows.</span><span class="sxs-lookup"><span data-stu-id="5cb20-108">**Windows 8 and Windows Server 2012:** This policy requires Windows Installer running on the Windows 8 or Windows Server 2012 and is unavailable on all earlier versions of Windows.</span></span>

## <a name="registry-key"></a><span data-ttu-id="5cb20-109">Chiave del Registro di sistema</span><span class="sxs-lookup"><span data-stu-id="5cb20-109">Registry Key</span></span>

<span data-ttu-id="5cb20-110">**HKEY \_ Criteri software del \_ computer locale** \\  \\  \\ **Microsoft** \\ **Windows** \\ **Installer**</span><span class="sxs-lookup"><span data-stu-id="5cb20-110">**HKEY\_LOCAL\_MACHINE**\\**Software**\\**Policies**\\**Microsoft**\\**Windows**\\**Installer**</span></span>

## <a name="data-type"></a><span data-ttu-id="5cb20-111">Tipo di dati</span><span class="sxs-lookup"><span data-stu-id="5cb20-111">Data Type</span></span>

<span data-ttu-id="5cb20-112">**REG \_ SZ**</span><span class="sxs-lookup"><span data-stu-id="5cb20-112">**REG\_SZ**</span></span>

 

 
