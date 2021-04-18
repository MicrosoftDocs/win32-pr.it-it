---
description: I criteri del ticket Kerberos vengono definiti a livello di dominio e implementati dal Centro distribuzione chiavi del dominio (KDC).
ms.assetid: 4774218b-7cbd-4e8d-a064-44ebdc37e534
title: Criteri Kerberos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4559353e65a25a380c0c2aa4bb7e5d56f7681af1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106313294"
---
# <a name="kerberos-policy"></a><span data-ttu-id="50d1e-103">Criteri Kerberos</span><span class="sxs-lookup"><span data-stu-id="50d1e-103">Kerberos Policy</span></span>

<span data-ttu-id="50d1e-104">I criteri del ticket Kerberos vengono definiti a livello di dominio e implementati dal [*centro distribuzione chiavi*](../secgloss/k-gly.md) del dominio (KDC).</span><span class="sxs-lookup"><span data-stu-id="50d1e-104">Kerberos ticket policy is defined at the domain level and implemented by the domain's [*Key Distribution Center*](../secgloss/k-gly.md) (KDC).</span></span> <span data-ttu-id="50d1e-105">Il criterio Kerberos viene archiviato nel Active Directory come un subset degli attributi dei criteri di sicurezza del dominio.</span><span class="sxs-lookup"><span data-stu-id="50d1e-105">Kerberos policy is stored in the Active Directory as a subset of the attributes of domain security policy.</span></span> <span data-ttu-id="50d1e-106">Per impostazione predefinita, le opzioni dei criteri possono essere impostate solo dai membri del gruppo Domain Administrators.</span><span class="sxs-lookup"><span data-stu-id="50d1e-106">By default, policy options can be set only by members of the Domain Administrators group.</span></span> <span data-ttu-id="50d1e-107">I criteri di dominio includono opzioni che:</span><span class="sxs-lookup"><span data-stu-id="50d1e-107">Domain policy includes options that:</span></span>

-   <span data-ttu-id="50d1e-108">Supporto per ticket aggiornati</span><span class="sxs-lookup"><span data-stu-id="50d1e-108">Support postdated tickets</span></span>
-   <span data-ttu-id="50d1e-109">Supporto della delega vincolata (solo Windows Server 2003)</span><span class="sxs-lookup"><span data-stu-id="50d1e-109">Support constrained delegation (Windows Server 2003 only)</span></span>
-   <span data-ttu-id="50d1e-110">Ticket di supporto che possono essere trasmessi</span><span class="sxs-lookup"><span data-stu-id="50d1e-110">Support tickets that can be forwarded</span></span>
-   <span data-ttu-id="50d1e-111">Supporto di ticket rinnovabili</span><span class="sxs-lookup"><span data-stu-id="50d1e-111">Support renewable tickets</span></span>
-   <span data-ttu-id="50d1e-112">Imposta validità massima ticket</span><span class="sxs-lookup"><span data-stu-id="50d1e-112">Set maximum ticket age</span></span>
-   <span data-ttu-id="50d1e-113">Imposta validità massima del rinnovo</span><span class="sxs-lookup"><span data-stu-id="50d1e-113">Set maximum renewal age</span></span>
-   <span data-ttu-id="50d1e-114">Imposta validità massima ticket proxy</span><span class="sxs-lookup"><span data-stu-id="50d1e-114">Set maximum proxy ticket age</span></span>
-   <span data-ttu-id="50d1e-115">Disconnettere forzatamente gli utenti quando i ticket scadono</span><span class="sxs-lookup"><span data-stu-id="50d1e-115">Forcibly log off users when tickets expire</span></span>

<span data-ttu-id="50d1e-116">Con la [*delega vincolata*](../secgloss/c-gly.md)è possibile impostare un computer in modo da consentire l'invio delle credenziali solo a un elenco specifico di servizi.</span><span class="sxs-lookup"><span data-stu-id="50d1e-116">With [*constrained delegation*](../secgloss/c-gly.md), a computer can be set to allow forwarding of credentials only to a specific list of services.</span></span> <span data-ttu-id="50d1e-117">Tali servizi devono trovarsi nello stesso dominio del computer che invia le credenziali.</span><span class="sxs-lookup"><span data-stu-id="50d1e-117">Those services must reside in the same domain as the computer forwarding the credentials.</span></span> <span data-ttu-id="50d1e-118">In *delega vincolata*, i ticket non vengono più inviati dal client al server.</span><span class="sxs-lookup"><span data-stu-id="50d1e-118">Under *constrained delegation*, tickets are no longer sent from the client to the server.</span></span> <span data-ttu-id="50d1e-119">Il computer server crea ticket di servizio da inviare in base alle informazioni necessarie per autenticare il client.</span><span class="sxs-lookup"><span data-stu-id="50d1e-119">The server computer creates service tickets to forward as necessary from information used to authenticate the client.</span></span>

<span data-ttu-id="50d1e-120">Sebbene i criteri Kerberos per un dominio consentano l'autenticazione delegata consentendo l'invio dei ticket, l'aspetto del criterio non deve essere applicato a tutti gli utenti o a tutti i computer.</span><span class="sxs-lookup"><span data-stu-id="50d1e-120">Although Kerberos policy for a domain may permit delegated authentication by allowing tickets to be forwarded, that aspect of policy need not apply to all users or all computers.</span></span> <span data-ttu-id="50d1e-121">Un attributo di un singolo account utente può essere impostato in modo da disabilitare l'invio delle [*credenziali*](../secgloss/c-gly.md) dell'utente da qualsiasi server.</span><span class="sxs-lookup"><span data-stu-id="50d1e-121">An attribute of an individual user account can be set to disable forwarding of that user's [*credentials*](../secgloss/c-gly.md) by any server.</span></span> <span data-ttu-id="50d1e-122">È possibile impostare un attributo dell'account di un singolo computer per disabilitare l'invio di credenziali da qualsiasi utente.</span><span class="sxs-lookup"><span data-stu-id="50d1e-122">An attribute of an individual computer's account can be set to disable forwarding of credentials from any user.</span></span> <span data-ttu-id="50d1e-123">In entrambi i casi, è possibile disabilitare la delega creando un criterio di gruppo da applicare a tutti gli utenti o a tutti i computer in un'unità organizzativa del Active Directory.</span><span class="sxs-lookup"><span data-stu-id="50d1e-123">In both cases, delegation can be disabled by creating a group policy to apply to all users or all computers in an organizational unit of the Active Directory.</span></span>

<span data-ttu-id="50d1e-124">**Windows XP/2000:** La delega vincolata non è supportata.</span><span class="sxs-lookup"><span data-stu-id="50d1e-124">**Windows XP/2000:** Constrained delegation is not supported.</span></span>

 

 
