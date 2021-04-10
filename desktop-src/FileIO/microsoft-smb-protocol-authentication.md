---
description: Il modello di sicurezza usato nel protocollo SMB Microsoft è identico a quello usato da altre varianti di SMB ed è costituito da due livelli di sicurezza&\# 8212; utente e condivisione.
ms.assetid: 985aa9fe-af3f-406d-920d-7fd7d0d58674
title: Autenticazione del protocollo SMB Microsoft
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 531e863b2a241bc861714980e6c5617e7d94e264
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103879114"
---
# <a name="microsoft-smb-protocol-authentication"></a><span data-ttu-id="972c9-103">Autenticazione del protocollo SMB Microsoft</span><span class="sxs-lookup"><span data-stu-id="972c9-103">Microsoft SMB Protocol Authentication</span></span>

<span data-ttu-id="972c9-104">Il modello di sicurezza usato nel protocollo SMB Microsoft è identico a quello usato da altre varianti di SMB ed è costituito da due livelli di sicurezza: utente e condivisione.</span><span class="sxs-lookup"><span data-stu-id="972c9-104">The security model used in Microsoft SMB Protocol is identical to the one used by other variants of SMB, and consists of two levels of security—user and share.</span></span> <span data-ttu-id="972c9-105">Una condivisione è un file, una directory o una stampante a cui è possibile accedere dai client del protocollo SMB Microsoft.</span><span class="sxs-lookup"><span data-stu-id="972c9-105">A share is a file, directory, or printer that can be accessed by Microsoft SMB Protocol clients.</span></span>

<span data-ttu-id="972c9-106">L'autenticazione a livello di utente indica che il client che tenta di accedere a una condivisione in un server deve fornire un nome utente e una password.</span><span class="sxs-lookup"><span data-stu-id="972c9-106">User-level authentication indicates that the client attempting to access a share on a server must provide a user name and password.</span></span> <span data-ttu-id="972c9-107">Una volta eseguita l'autenticazione, l'utente può accedere a tutte le condivisioni in un server non protette anche dalla sicurezza a livello di condivisione.</span><span class="sxs-lookup"><span data-stu-id="972c9-107">When authenticated, the user can then access all shares on a server not also protected by share-level security.</span></span> <span data-ttu-id="972c9-108">Questo livello di sicurezza consente agli amministratori di sistema di determinare in modo specifico quali utenti e gruppi possono accedere a una condivisione.</span><span class="sxs-lookup"><span data-stu-id="972c9-108">This security level allows system administrators to specifically determine which users and groups can access a share.</span></span>

<span data-ttu-id="972c9-109">L'autenticazione a livello di condivisione indica che l'accesso a una condivisione è controllato da una password assegnata solo a tale condivisione.</span><span class="sxs-lookup"><span data-stu-id="972c9-109">Share-level authentication indicates that access to a share is controlled by a password assigned to that share only.</span></span> <span data-ttu-id="972c9-110">Diversamente dalla sicurezza a livello di utente, questo livello di sicurezza non richiede un nome utente per l'autenticazione e non viene stabilita alcuna identità utente.</span><span class="sxs-lookup"><span data-stu-id="972c9-110">Unlike user-level security, this security level does not require a user name for authentication and no user identity is established.</span></span>

<span data-ttu-id="972c9-111">In entrambi i livelli di sicurezza, la password viene crittografata prima che venga inviata al server.</span><span class="sxs-lookup"><span data-stu-id="972c9-111">Under both of these security levels, the password is encrypted before it is sent to the server.</span></span> <span data-ttu-id="972c9-112">[NTLM](/windows/desktop/SecAuthN/microsoft-ntlm) e la crittografia precedente di LAN Manager (lm) sono supportati dal protocollo Microsoft SMB.</span><span class="sxs-lookup"><span data-stu-id="972c9-112">[NTLM](/windows/desktop/SecAuthN/microsoft-ntlm) and the older LAN Manager (LM) encryption are supported by Microsoft SMB Protocol.</span></span> <span data-ttu-id="972c9-113">Entrambi i metodi di crittografia utilizzano l'autenticazione di richiesta-risposta, in cui il server invia al client una stringa casuale e il client restituisce una stringa di risposta calcolata che dimostra che il client dispone di credenziali sufficienti per l'accesso.</span><span class="sxs-lookup"><span data-stu-id="972c9-113">Both encryption methods use challenge-response authentication, where the server sends the client a random string and the client returns a computed response string that proves the client has sufficient credentials for access.</span></span>

 

 
