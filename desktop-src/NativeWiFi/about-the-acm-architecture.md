---
description: Informazioni sull'architettura di ACM
ms.assetid: 4a5c0085-0e7b-424d-9205-5ec39518a088
title: Informazioni sull'architettura di ACM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f037a1823f7045ccaf1dc573c6d213beeebe0a63
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104233703"
---
# <a name="about-the-acm-architecture"></a><span data-ttu-id="2fb09-103">Informazioni sull'architettura di ACM</span><span class="sxs-lookup"><span data-stu-id="2fb09-103">About the ACM Architecture</span></span>

<span data-ttu-id="2fb09-104">Il modulo di configurazione automatica (ACM) è il nuovo componente di configurazione wireless per Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="2fb09-104">The Auto Configuration Module (ACM) is the new wireless configuration component for Windows Vista.</span></span> <span data-ttu-id="2fb09-105">Windows XP con Service Pack 3 (SP3) e l'API LAN wireless per Windows XP con Service Pack 2 (SP2) usano invece il servizio Wireless Zero Configuration (WZC).</span><span class="sxs-lookup"><span data-stu-id="2fb09-105">Windows XP with Service Pack 3 (SP3) and Wireless LAN API for Windows XP with Service Pack 2 (SP2) use the Wireless Zero Configuration (WZC) service instead.</span></span>

<span data-ttu-id="2fb09-106">L'ACM analizza periodicamente le reti e usa un processo iterativo per selezionare e connettersi alla rete preferita nell'intervallo, se tale rete ha un'interfaccia abilitata per la connessione automatica.</span><span class="sxs-lookup"><span data-stu-id="2fb09-106">The ACM scans networks periodically and uses an iterative process to select and connect to the most preferred network in the range, if that network has an interface enabled for auto-connection.</span></span> <span data-ttu-id="2fb09-107">L'ACM Salva e recupera anche i profili di rete, che contengono le impostazioni di ACM, media Specific Module (MSM), Security e Independent Hardware Vendor (IHV).</span><span class="sxs-lookup"><span data-stu-id="2fb09-107">The ACM also saves and retrieves network profiles, which contain ACM, Media Specific Module (MSM), security, and independent hardware vendor (IHV) settings.</span></span> <span data-ttu-id="2fb09-108">Questi profili di rete sono per la configurazione automatica.</span><span class="sxs-lookup"><span data-stu-id="2fb09-108">These network profiles are for auto configuration.</span></span>

<span data-ttu-id="2fb09-109">La configurazione automatica supporta le impostazioni globali e per interfaccia e i profili di rete.</span><span class="sxs-lookup"><span data-stu-id="2fb09-109">Auto configuration supports both global and per-interface settings and network profiles.</span></span> <span data-ttu-id="2fb09-110">Le impostazioni globali e i profili di rete vengono configurati se il computer è stato aggiunto a un dominio con un oggetto Criteri di gruppo a livello di dominio o unità organizzativa (OU) nella gerarchia di Active Directory (AD).</span><span class="sxs-lookup"><span data-stu-id="2fb09-110">The global settings and network profiles are configured if the machine has joined a domain with a group policy object (GPO) either at the domain level or the organizational unit (OU) level in the Active Directory (AD) hierarchy.</span></span> <span data-ttu-id="2fb09-111">Le impostazioni e i profili di criteri di gruppo sono di sola lettura, applicati a ogni interfaccia 802,11 nel sistema e hanno sempre la precedenza sulle impostazioni per interfaccia e per utente e i profili di rete.</span><span class="sxs-lookup"><span data-stu-id="2fb09-111">These group policy settings and profiles are read-only, applied to each 802.11 interface in the system, and always take precedence over the per-interface and per-user settings and network profiles.</span></span> <span data-ttu-id="2fb09-112">I profili criteri di gruppo sono posizionati nella parte superiore dell'elenco Profilo di rete preferito in ogni interfaccia di rete 802,11.</span><span class="sxs-lookup"><span data-stu-id="2fb09-112">The group policy profiles are placed at the top of the preferred network profile list on each 802.11 network interface.</span></span>

<span data-ttu-id="2fb09-113">L'architettura di ACM è estendibile.</span><span class="sxs-lookup"><span data-stu-id="2fb09-113">The ACM architecture is extensible.</span></span> <span data-ttu-id="2fb09-114">IHV può implementare funzionalità wireless proprietarie senza modificare il Framework 802,11 nativo fornito.</span><span class="sxs-lookup"><span data-stu-id="2fb09-114">IHVs can implement proprietary wireless functionality without altering the provided native 802.11 framework.</span></span> <span data-ttu-id="2fb09-115">Le funzioni e le strutture di controllo IHV esposte abilitano questa estensibilità.</span><span class="sxs-lookup"><span data-stu-id="2fb09-115">The exposed IHV control functions and structures enable this extensibility.</span></span>

## <a name="related-topics"></a><span data-ttu-id="2fb09-116">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="2fb09-116">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="2fb09-117">Informazioni sul Wi-Fi nativo</span><span class="sxs-lookup"><span data-stu-id="2fb09-117">About Native Wifi</span></span>](about-native-wifi.md)
</dt> </dl>

 

 



