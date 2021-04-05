---
description: Descrive le impostazioni dei criteri di risparmio energia che costituiscono uno schema di risparmio energia.
ms.assetid: cd515cd6-67f4-45d0-b769-3abc7a56faa8
title: Impostazioni di criteri di risparmio energia
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2f490c758a890faf314be1ddffe9ac7a503bd473
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103756572"
---
# <a name="power-policy-settings"></a><span data-ttu-id="2995a-103">Impostazioni di criteri di risparmio energia</span><span class="sxs-lookup"><span data-stu-id="2995a-103">Power Policy Settings</span></span>

<span data-ttu-id="2995a-104">Combinazioni per il risparmio di energia e schemi sono costituite da preferenze e impostazioni dei criteri.</span><span class="sxs-lookup"><span data-stu-id="2995a-104">Power plans and schemes consist of preferences and policy settings.</span></span>

<span data-ttu-id="2995a-105">Una combinazione per il risparmio di energia è costituita da un gruppo di impostazioni di risparmio energia.</span><span class="sxs-lookup"><span data-stu-id="2995a-105">A power plan consists of a group of power setting preferences.</span></span> <span data-ttu-id="2995a-106">Queste preferenze sono costituite sia da un valore AC che da un controller di dominio per ogni impostazione di risparmio energia.</span><span class="sxs-lookup"><span data-stu-id="2995a-106">These preferences consist of both an AC and DC value for each of the power settings.</span></span> <span data-ttu-id="2995a-107">Ogni combinazione per il risparmio di energia viene identificata tramite un **GUID** univoco e un nome descrittivo.</span><span class="sxs-lookup"><span data-stu-id="2995a-107">Each power plan is identified through a unique **GUID** as well as a friendly name.</span></span> <span data-ttu-id="2995a-108">Windows Vista prevede tre combinazioni per il risparmio di energia predefinite: risparmio energia, bilanciato e prestazioni elevate.</span><span class="sxs-lookup"><span data-stu-id="2995a-108">Windows Vista has three default power plans: Power Saver, Balanced, and High Performance.</span></span> <span data-ttu-id="2995a-109">Questi piani possono essere personalizzati e possono essere creati piani aggiuntivi.</span><span class="sxs-lookup"><span data-stu-id="2995a-109">These plans can be customized, and additional plans can be created.</span></span> <span data-ttu-id="2995a-110">Tutte le combinazioni per il risparmio di energia hanno un attributo di personalità che indica il comportamento di risparmio energetico complessivo del piano.</span><span class="sxs-lookup"><span data-stu-id="2995a-110">All power plans have a personality attribute that indicates the overall power savings behavior of the plan.</span></span>

<span data-ttu-id="2995a-111">La tabella seguente illustra le tre personali del piano di risparmio energia.</span><span class="sxs-lookup"><span data-stu-id="2995a-111">The following table shows the three power plan personalities.</span></span> 

| <span data-ttu-id="2995a-112">Nome visualizzato</span><span class="sxs-lookup"><span data-stu-id="2995a-112">Display name</span></span>     | <span data-ttu-id="2995a-113">Descrizione</span><span class="sxs-lookup"><span data-stu-id="2995a-113">Description</span></span>                                                                   | <span data-ttu-id="2995a-114">**GUID**</span><span class="sxs-lookup"><span data-stu-id="2995a-114">**GUID**</span></span>                             |
|------------------|-------------------------------------------------------------------------------|--------------------------------------|
| <span data-ttu-id="2995a-115">Risparmio energia</span><span class="sxs-lookup"><span data-stu-id="2995a-115">Power Saver</span></span>      | <span data-ttu-id="2995a-116">Offre prestazioni ridotte che possono aumentare il risparmio di energia.</span><span class="sxs-lookup"><span data-stu-id="2995a-116">Delivers reduced performance which may increase power savings.</span></span>                | <span data-ttu-id="2995a-117">a1841308-3541-4fab-bc81-f71556f20b4a</span><span class="sxs-lookup"><span data-stu-id="2995a-117">a1841308-3541-4fab-bc81-f71556f20b4a</span></span> |
| <span data-ttu-id="2995a-118">Balanced</span><span class="sxs-lookup"><span data-stu-id="2995a-118">Balanced</span></span>         | <span data-ttu-id="2995a-119">Bilancia automaticamente le prestazioni e il consumo di energia in base alla domanda.</span><span class="sxs-lookup"><span data-stu-id="2995a-119">Automatically balances performance and power consumption according to demand.</span></span> | <span data-ttu-id="2995a-120">381b4222-f694-41f0-9685-ff5bb260df2e</span><span class="sxs-lookup"><span data-stu-id="2995a-120">381b4222-f694-41f0-9685-ff5bb260df2e</span></span> |
| <span data-ttu-id="2995a-121">Prestazioni elevate</span><span class="sxs-lookup"><span data-stu-id="2995a-121">High Performance</span></span> | <span data-ttu-id="2995a-122">Offre prestazioni massime a scapito di un consumo di energia superiore.</span><span class="sxs-lookup"><span data-stu-id="2995a-122">Delivers maximum performance at the expense of higher power consumption.</span></span>      | <span data-ttu-id="2995a-123">8c5e7fda-e8bf-4a96-9a85-a6e23a8c635c</span><span class="sxs-lookup"><span data-stu-id="2995a-123">8c5e7fda-e8bf-4a96-9a85-a6e23a8c635c</span></span> |



 

> [!Note]  
> <span data-ttu-id="2995a-124">I dispositivi che supportano la modalità [standby moderna](/windows-hardware/design/device-experiences/modern-standby) consentono solo la combinazione per il risparmio di energia **bilanciata** .</span><span class="sxs-lookup"><span data-stu-id="2995a-124">Devices that support [Modern Standby](/windows-hardware/design/device-experiences/modern-standby) mode only allow the **Balanced** power plan.</span></span> <span data-ttu-id="2995a-125">**Modern standby** è la soluzione più recente e semplificata per la gestione delle impostazioni di risparmio energia.</span><span class="sxs-lookup"><span data-stu-id="2995a-125">**Modern Standby** is the newer, more streamlined solution to power settings management.</span></span>

 

<span data-ttu-id="2995a-126">Ogni computer dispone di una singola combinazione per il risparmio di energia attiva.</span><span class="sxs-lookup"><span data-stu-id="2995a-126">Each computer has a single, active power plan.</span></span> <span data-ttu-id="2995a-127">Per impostazione predefinita, gli utenti senza privilegi sono in grado di accedere alle impostazioni di risparmio energia del sistema.</span><span class="sxs-lookup"><span data-stu-id="2995a-127">By default, nonprivileged users are able to access system power settings.</span></span> <span data-ttu-id="2995a-128">L'accesso a tutte le impostazioni di risparmio energia o a singole impostazioni può essere controllato tramite ACL nelle impostazioni di risparmio energia o tramite Criteri di gruppo.</span><span class="sxs-lookup"><span data-stu-id="2995a-128">Access to all or individual power settings can be controlled through ACLs on the power settings or through Group Policy.</span></span> <span data-ttu-id="2995a-129">Le applicazioni devono chiamare [**PowerSettingAccessCheck**](/windows/desktop/api/PowrProf/nf-powrprof-powersettingaccesscheck) per determinare se l'utente può accedere all'impostazione di risparmio energia.</span><span class="sxs-lookup"><span data-stu-id="2995a-129">Applications should call [**PowerSettingAccessCheck**](/windows/desktop/api/PowrProf/nf-powrprof-powersettingaccesscheck) to determine if the user has access to the power setting.</span></span>

<span data-ttu-id="2995a-130">Ogni impostazione di risparmio energia è identificata da un **GUID** univoco e include un nome descrittivo, una descrizione, valori consentiti e valori predefiniti per AC e DC.</span><span class="sxs-lookup"><span data-stu-id="2995a-130">Each power setting is identified by a unique **GUID** and includes a friendly name, description, allowable values, and default values for AC and DC.</span></span> <span data-ttu-id="2995a-131">È possibile creare impostazioni di risparmio energia personalizzate usando la funzione [**PowerCreateSetting**](/windows/desktop/api/PowrProf/nf-powrprof-powercreatesetting) .</span><span class="sxs-lookup"><span data-stu-id="2995a-131">Custom power settings can be created using the [**PowerCreateSetting**](/windows/desktop/api/PowrProf/nf-powrprof-powercreatesetting) function.</span></span>

## <a name="related-topics"></a><span data-ttu-id="2995a-132">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="2995a-132">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="2995a-133">Combinazioni per il risparmio di energia</span><span class="sxs-lookup"><span data-stu-id="2995a-133">Power Schemes</span></span>](power-schemes.md)
</dt> </dl>

 

 
