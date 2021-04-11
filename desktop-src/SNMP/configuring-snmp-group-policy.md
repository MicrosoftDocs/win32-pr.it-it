---
title: Configurazione Criteri di gruppo SNMP
description: Se si utilizza lo snap-in Microsoft Management Console (MMC) per Criteri di gruppo per amministrare le impostazioni dei criteri basate sul Registro di sistema applicabili a SNMP, è possibile che esistano una o più delle sottochiavi seguenti.
ms.assetid: de21d2f5-3337-47ba-afcf-347e289873d3
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 817797dbc0e67f6006e12751beca533cbbec3656
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104118223"
---
# <a name="configuring-snmp-group-policy"></a><span data-ttu-id="514da-103">Configurazione Criteri di gruppo SNMP</span><span class="sxs-lookup"><span data-stu-id="514da-103">Configuring SNMP Group Policy</span></span>

<span data-ttu-id="514da-104">Se si utilizza lo snap-in Microsoft Management Console (MMC) per Criteri di gruppo per amministrare le impostazioni dei criteri basate sul Registro di sistema applicabili a SNMP, è possibile che esistano una o più delle sottochiavi seguenti.</span><span class="sxs-lookup"><span data-stu-id="514da-104">If you use the Microsoft Management Console (MMC) snap-in for Group Policy to administer registry-based policy settings that apply to SNMP, one or more of the following subkeys may exist.</span></span>

<span data-ttu-id="514da-105">**HKEY \_ \_** \\  \\  \\  \\ **Parametri** SNMP dei criteri \\  software del computer locale ValidCommunities</span><span class="sxs-lookup"><span data-stu-id="514da-105">**HKEY\_LOCAL\_MACHINE**\\**SOFTWARE**\\**Policies**\\**SNMP**\\**Parameters**\\**ValidCommunities**</span></span>

<span data-ttu-id="514da-106">**HKEY \_ \_** \\  \\  \\  \\ **Parametri** SNMP dei criteri \\  software del computer locale PermittedManagers</span><span class="sxs-lookup"><span data-stu-id="514da-106">**HKEY\_LOCAL\_MACHINE**\\**SOFTWARE**\\**Policies**\\**SNMP**\\**Parameters**\\**PermittedManagers**</span></span>

<span data-ttu-id="514da-107">**HKEY \_ \_** \\  \\  \\  \\ **Parametri** SNMP dei criteri \\  software del computer locale TrapConfiguration</span><span class="sxs-lookup"><span data-stu-id="514da-107">**HKEY\_LOCAL\_MACHINE**\\**SOFTWARE**\\**Policies**\\**SNMP**\\**Parameters**\\**TrapConfiguration**</span></span>

<span data-ttu-id="514da-108">In genere, solo i membri del gruppo locale Administrators possono accedere alle sottochiavi del registro di sistema seguenti che archiviano i dati di configurazione per il servizio SNMP:</span><span class="sxs-lookup"><span data-stu-id="514da-108">Typically, only members of the Administrators local group can access the following registry subkeys that store configuration data for the SNMP service:</span></span>

<span data-ttu-id="514da-109">**HKEY \_ \_** \\  \\  \\  \\  \\ **Parametri** SNMP dei servizi \\  CurrentControlSet del sistema del computer locale ValidCommunities</span><span class="sxs-lookup"><span data-stu-id="514da-109">**HKEY\_LOCAL\_MACHINE**\\**System**\\**CurrentControlSet**\\**Services**\\**SNMP**\\**Parameters**\\**ValidCommunities**</span></span>

<span data-ttu-id="514da-110">**HKEY \_ \_** \\  \\  \\  \\  \\ **Parametri** SNMP dei servizi \\  CurrentControlSet del sistema del computer locale PermittedManagers</span><span class="sxs-lookup"><span data-stu-id="514da-110">**HKEY\_LOCAL\_MACHINE**\\**System**\\**CurrentControlSet**\\**Services**\\**SNMP**\\**Parameters**\\**PermittedManagers**</span></span>

<span data-ttu-id="514da-111">Per ulteriori informazioni sulle impostazioni dei criteri basate sul Registro di sistema, vedere [about criteri di gruppo](/previous-versions/windows/desktop/Policy/about-group-policy).</span><span class="sxs-lookup"><span data-stu-id="514da-111">For more information about registry-based policy settings, see [About Group Policy](/previous-versions/windows/desktop/Policy/about-group-policy).</span></span>

 

 