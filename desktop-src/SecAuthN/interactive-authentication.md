---
description: L'autenticazione è interattiva quando viene richiesto all'utente di fornire informazioni di accesso. L'autorità di sicurezza locale (LSA) esegue un'autenticazione interattiva quando un utente esegue l'accesso tramite l'interfaccia utente GINA.
ms.assetid: 86a318fa-4d7c-4191-a309-d25b492dd915
title: Autenticazione interattiva
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: afeb09044f4b34f28c02cd0f03b3358a8158af65
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104348061"
---
# <a name="interactive-authentication"></a><span data-ttu-id="80a8d-104">Autenticazione interattiva</span><span class="sxs-lookup"><span data-stu-id="80a8d-104">Interactive Authentication</span></span>

<span data-ttu-id="80a8d-105">L'autenticazione è interattiva quando viene richiesto all'utente di fornire informazioni di accesso.</span><span class="sxs-lookup"><span data-stu-id="80a8d-105">Authentication is interactive when a user is prompted to supply logon information.</span></span> <span data-ttu-id="80a8d-106">L' [*autorità di sicurezza locale*](../secgloss/l-gly.md) (LSA) esegue un'autenticazione interattiva quando un utente esegue l'accesso tramite l'interfaccia utente [*Gina*](../secgloss/g-gly.md) .</span><span class="sxs-lookup"><span data-stu-id="80a8d-106">The [*Local Security Authority*](../secgloss/l-gly.md) (LSA) performs an interactive authentication when a user logs on through the [*GINA*](../secgloss/g-gly.md) user interface.</span></span> <span data-ttu-id="80a8d-107">Nella figura seguente sono illustrate le parti di una tipica autenticazione interattiva.</span><span class="sxs-lookup"><span data-stu-id="80a8d-107">The following illustration shows the parts of a typical interactive authentication.</span></span>

![autenticazione interattiva](images/lsaint3.png)

<span data-ttu-id="80a8d-109">Un utente segnala al sistema di avviare la sequenza di accesso digitando la firma di accesso condiviso (SAS, [*Secure Attention Sequence*](../secgloss/s-gly.md) ) CTRL + ALT + CANC.</span><span class="sxs-lookup"><span data-stu-id="80a8d-109">A user signals the system to begin the logon sequence by typing the CTRL+ALT+DEL [*secure attention sequence*](../secgloss/s-gly.md) (SAS).</span></span> <span data-ttu-id="80a8d-110">[*Winlogon*](../secgloss/w-gly.md) riceve la firma di accesso condiviso e chiama Gina per visualizzare un'interfaccia utente e ottenere i dati di accesso dell'utente, ad esempio un nome utente e una password.</span><span class="sxs-lookup"><span data-stu-id="80a8d-110">[*Winlogon*](../secgloss/w-gly.md) receives the SAS and calls the GINA to display a user interface and obtain the user's logon data, such as a user name and password.</span></span>

<span data-ttu-id="80a8d-111">Dopo aver ottenuto i dati di accesso, GINA chiama la funzione [**LsaLogonUser**](/windows/desktop/api/Ntsecapi/nf-ntsecapi-lsalogonuser) per autenticare l'utente, specificando il pacchetto di autenticazione da usare per valutare i dati di accesso.</span><span class="sxs-lookup"><span data-stu-id="80a8d-111">After obtaining the logon data, the GINA calls the [**LsaLogonUser**](/windows/desktop/api/Ntsecapi/nf-ntsecapi-lsalogonuser) function to authenticate the user, specifying which authentication package must be used to evaluate the logon data.</span></span>

<span data-ttu-id="80a8d-112">LSA chiama il pacchetto di autenticazione specificato e vi passa i dati di accesso.</span><span class="sxs-lookup"><span data-stu-id="80a8d-112">The LSA calls the specified authentication package and passes the logon data to it.</span></span> <span data-ttu-id="80a8d-113">Il pacchetto di autenticazione esamina i dati e determina se l'autenticazione ha avuto esito positivo.</span><span class="sxs-lookup"><span data-stu-id="80a8d-113">The authentication package examines the data and determines whether the authentication is successful.</span></span> <span data-ttu-id="80a8d-114">Il risultato dell'autenticazione viene restituito a GINA da LSA e da LSA.</span><span class="sxs-lookup"><span data-stu-id="80a8d-114">The authentication result is returned to the LSA and from the LSA, to the GINA.</span></span>

<span data-ttu-id="80a8d-115">GINA Visualizza l'esito positivo o negativo dell'autenticazione per l'utente e restituisce il risultato dell'autenticazione a Winlogon.</span><span class="sxs-lookup"><span data-stu-id="80a8d-115">The GINA displays the success or failure of the authentication to the user and returns the result of the authentication to Winlogon.</span></span> <span data-ttu-id="80a8d-116">Se l'autenticazione ha esito positivo, viene avviata la sessione di accesso dell'utente e viene salvato un set di [*credenziali*](../secgloss/c-gly.md) di accesso per riferimento futuro.</span><span class="sxs-lookup"><span data-stu-id="80a8d-116">If the authentication succeeds, the user's logon session begins and a set of logon [*credentials*](../secgloss/c-gly.md) are saved for future reference.</span></span>

> [!Note]  
> <span data-ttu-id="80a8d-117">In generale, uno sviluppatore che scrive un oggetto GINA personalizzato per accettare dati di accesso specializzati, ad esempio una [*Smart Card*](../secgloss/s-gly.md) o dati di analisi retinica, deve anche scrivere un pacchetto di autenticazione responsabile dell'elaborazione dei dati e della relativa autenticità.</span><span class="sxs-lookup"><span data-stu-id="80a8d-117">In general, a developer who writes a custom GINA to accept specialized logon data, such as a [*smart card*](../secgloss/s-gly.md) or retinal-scan data, must also write an authentication package responsible for processing that data and determining its authenticity.</span></span>

 

<span data-ttu-id="80a8d-118">Per ulteriori informazioni su Winlogon e GINA, vedere [Winlogon e Gina](winlogon-and-gina.md).</span><span class="sxs-lookup"><span data-stu-id="80a8d-118">For more information about Winlogon and GINAs, see [Winlogon and GINA](winlogon-and-gina.md).</span></span> <span data-ttu-id="80a8d-119">Per ulteriori informazioni sui pacchetti di autenticazione, vedere [creazione di pacchetti di sicurezza personalizzati](creating-custom-security-packages.md).</span><span class="sxs-lookup"><span data-stu-id="80a8d-119">For more information about authentication packages, see [Creating Custom Security Packages](creating-custom-security-packages.md).</span></span>

 

 
