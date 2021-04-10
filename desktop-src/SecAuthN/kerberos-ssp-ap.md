---
description: Il pacchetto di autenticazione Kerberos viene utilizzato per l'accesso a una rete. gli accessi locali vengono gestiti da MSV1 \_ 0.
ms.assetid: 43970c99-53f1-43c1-9d9f-65573572f731
title: SSP/AP Kerberos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9d14565c8c6526d9cab34d7b9ddec9a0a04ff8de
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104050139"
---
# <a name="kerberos-sspap"></a><span data-ttu-id="23951-103">SSP/AP Kerberos</span><span class="sxs-lookup"><span data-stu-id="23951-103">Kerberos SSP/AP</span></span>

<span data-ttu-id="23951-104">Il pacchetto di autenticazione [*Kerberos*](../secgloss/k-gly.md) viene utilizzato per l'accesso a una rete. gli accessi locali vengono gestiti da MSV1 \_ 0.</span><span class="sxs-lookup"><span data-stu-id="23951-104">The [*Kerberos*](../secgloss/k-gly.md) authentication package is used when logging on to a network; local logons are handled by MSV1\_0.</span></span>

<span data-ttu-id="23951-105">Quando un utente esegue l'accesso utilizzando un account di rete, per impostazione predefinita Kerberos tenta di connettersi al [*centro distribuzione chiavi*](../secgloss/k-gly.md) Kerberos (KDC) sul controller di dominio e di ottenere un ticket di concessione ticket (TGT) utilizzando i dati di accesso forniti dall'utente.</span><span class="sxs-lookup"><span data-stu-id="23951-105">When a user logs on using a network account, by default, Kerberos attempts to connect to the Kerberos [*Key Distribution Center*](../secgloss/k-gly.md) (KDC) on the domain controller and obtain a ticket granting ticket (TGT) by using the logon data supplied by the user.</span></span>

<span data-ttu-id="23951-106">Se un KDC Kerberos non è disponibile, Windows usa MSV1 \_ 0 e l'autenticazione pass-through come descritto [nel \_ pacchetto di autenticazione MSV1 0](msv1-0-authentication-package.md).</span><span class="sxs-lookup"><span data-stu-id="23951-106">If a Kerberos KDC is not available, Windows uses MSV1\_0 and pass-through authentication as described in [MSV1\_0 Authentication Package](msv1-0-authentication-package.md).</span></span>

<span data-ttu-id="23951-107">Il pacchetto di autenticazione Kerberos supporta la versione 5, Revisione 6 del protocollo Kerberos.</span><span class="sxs-lookup"><span data-stu-id="23951-107">The Kerberos authentication package supports version 5, revision 6 of the Kerberos protocol.</span></span> <span data-ttu-id="23951-108">Questo protocollo si basa su Internet [RFC 4120](https://www.ietf.org/rfc/rfc4120.txt).</span><span class="sxs-lookup"><span data-stu-id="23951-108">This protocol is based on Internet [RFC 4120](https://www.ietf.org/rfc/rfc4120.txt).</span></span> <span data-ttu-id="23951-109">Per ulteriori informazioni, vedere il sito Web IETF:</span><span class="sxs-lookup"><span data-stu-id="23951-109">For more information, see the IETF website:</span></span>

[https://www.ietf.org](https://www.ietf.org/)

<span data-ttu-id="23951-110">Per ulteriori informazioni su Kerberos, vedere [Microsoft Kerberos](microsoft-kerberos.md).</span><span class="sxs-lookup"><span data-stu-id="23951-110">For more information about Kerberos, see [Microsoft Kerberos](microsoft-kerberos.md).</span></span>

## <a name="kerberos-credential-formats"></a><span data-ttu-id="23951-111">Formati di credenziali Kerberos</span><span class="sxs-lookup"><span data-stu-id="23951-111">Kerberos Credential Formats</span></span>

<span data-ttu-id="23951-112">Le [*credenziali*](../secgloss/c-gly.md) utente assegnate dal pacchetto di autenticazione Kerberos dopo un tentativo di accesso riuscito sono un ticket e una chiave di crittografia temporanea, spesso detta [*chiave di sessione*](../secgloss/s-gly.md).</span><span class="sxs-lookup"><span data-stu-id="23951-112">The user [*credentials*](../secgloss/c-gly.md) assigned by the Kerberos authentication package after a successful logon attempt are a ticket and a temporary encryption key, often called a [*session key*](../secgloss/s-gly.md).</span></span> <span data-ttu-id="23951-113">Il ticket contiene una copia crittografata delle credenziali del client e della chiave della sessione.</span><span class="sxs-lookup"><span data-stu-id="23951-113">The ticket contains both an encrypted copy of the client's credentials and the session key.</span></span>

 

 
