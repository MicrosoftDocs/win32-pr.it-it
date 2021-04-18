---
description: Il provider di servizi directory rispecchia le classi e le istanze da Active Directory nello spazio dei nomi LDAP (Lightweight Directory Access Protocol) WMI.
ms.assetid: 0215b614-cb10-4195-837d-bf81d523c560
ms.tgt_platform: multiple
title: Mapping di Active Directory a WMI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2e0162f722eb8a053270ac2a8e75eaed4f1cd405
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106314594"
---
# <a name="mapping-active-directory-to-wmi"></a><span data-ttu-id="a5ce1-103">Mapping di Active Directory a WMI</span><span class="sxs-lookup"><span data-stu-id="a5ce1-103">Mapping Active Directory to WMI</span></span>

<span data-ttu-id="a5ce1-104">Il provider di servizi directory rispecchia le classi e le istanze da Active Directory nello spazio dei nomi LDAP (Lightweight Directory Access Protocol) WMI.</span><span class="sxs-lookup"><span data-stu-id="a5ce1-104">The Directory Services Provider mirrors classes and instances from Active Directory into the WMI Lightweight Directory Access Protocol (LDAP) namespace.</span></span> <span data-ttu-id="a5ce1-105">A causa delle differenze fondamentali nei due ambienti, non è possibile rinominare semplicemente le classi e le istanze di Active Directory e sperare di accedere correttamente a tali classi e istanze in WMI.</span><span class="sxs-lookup"><span data-stu-id="a5ce1-105">Because of fundamental differences in the two environments, you cannot simply rename the Active Directory classes and instances and hope to properly access those classes and instances in WMI.</span></span> <span data-ttu-id="a5ce1-106">Al contrario, il provider di servizi directory segue le regole di denominazione per mantenere le relazioni esistenti tra le classi e le istanze di Active Directory.</span><span class="sxs-lookup"><span data-stu-id="a5ce1-106">Instead, the Directory Services provider follows naming rules to preserve the relationships that exist between the Active Directory classes and instances.</span></span>

<span data-ttu-id="a5ce1-107">Negli argomenti seguenti vengono fornite informazioni sul mapping di classi e istanze di Active Directory:</span><span class="sxs-lookup"><span data-stu-id="a5ce1-107">The following topics provide information about mapping Active Directory classes and instances:</span></span>

-   [<span data-ttu-id="a5ce1-108">Mapping di classi Active Directory</span><span class="sxs-lookup"><span data-stu-id="a5ce1-108">Mapping Active Directory Classes</span></span>](mapping-active-directory-classes.md)
-   [<span data-ttu-id="a5ce1-109">Mapping di istanze di Active Directory</span><span class="sxs-lookup"><span data-stu-id="a5ce1-109">Mapping Active Directory Instances</span></span>](mapping-active-directory-instances.md)

> [!Note]  
> <span data-ttu-id="a5ce1-110">Per ulteriori informazioni sul supporto e l'installazione di questo componente in un sistema operativo specifico, vedere la pagina relativa alla [disponibilità del sistema operativo dei componenti WMI](operating-system-availability-of-wmi-components.md).</span><span class="sxs-lookup"><span data-stu-id="a5ce1-110">For more information about support and installation of this component on a specific operating system, see [Operating System Availability of WMI Components](operating-system-availability-of-wmi-components.md).</span></span>

 

 

 



