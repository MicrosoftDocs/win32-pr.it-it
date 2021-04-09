---
description: A B C D E F G H I J K L M N O P Q R S T U V W X Y Z
ROBOTS: NOINDEX, NOFOLLOW
ms.assetid: 50397050-3b5c-4683-972c-95d9f661b365
ms.tgt_platform: multiple
title: D (WMI)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d469b94ec6649c64722fb414880d2e79fc3c88b0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104050122"
---
# <a name="d-wmi"></a><span data-ttu-id="1aca7-103">D (WMI)</span><span class="sxs-lookup"><span data-stu-id="1aca7-103">D (WMI)</span></span>

<span data-ttu-id="1aca7-104">[A](gloss-a.md) B [C](gloss-c.md) d [E](gloss-e.md) [F](gloss-f.md) G [H](gloss-h.md) [i](gloss-i.md) J [K](gloss-k.md) [L](gloss-l.md) [M](gloss-m.md) [N](gloss-n.md) [O](gloss-o.md) [P](gloss-p.md) [Q](gloss-q.md) [R](gloss-r.md) [S](gloss-s.md) [T](gloss-t.md) U V [W](gloss-w.md) X Y Z</span><span class="sxs-lookup"><span data-stu-id="1aca7-104">[A](gloss-a.md) B [C](gloss-c.md) D [E](gloss-e.md) [F](gloss-f.md) G [H](gloss-h.md) [I](gloss-i.md) J [K](gloss-k.md) [L](gloss-l.md) [M](gloss-m.md) [N](gloss-n.md) [O](gloss-o.md) [P](gloss-p.md) [Q](gloss-q.md) [R](gloss-r.md) [S](gloss-s.md) [T](gloss-t.md) U V [W](gloss-w.md) X Y Z</span></span>

<dl> <dt>

<span data-ttu-id="1aca7-105"><span id="wmi.gloss_datetime"></span><span id="WMI.GLOSS_DATETIME"></span>**DateTime**</span><span class="sxs-lookup"><span data-stu-id="1aca7-105"><span id="wmi.gloss_datetime"></span><span id="WMI.GLOSS_DATETIME"></span>**datetime**</span></span>
</dt> <dd>

<span data-ttu-id="1aca7-106">Vedere [*CIM DateTime*](gloss-c.md).</span><span class="sxs-lookup"><span data-stu-id="1aca7-106">See [*CIM datetime*](gloss-c.md).</span></span>

</dd> <dt>

<span data-ttu-id="1aca7-107"><span id="wmi.gloss_decoupled_provider"></span><span id="WMI.GLOSS_DECOUPLED_PROVIDER"></span>**provider disaccoppiato**</span><span class="sxs-lookup"><span data-stu-id="1aca7-107"><span id="wmi.gloss_decoupled_provider"></span><span id="WMI.GLOSS_DECOUPLED_PROVIDER"></span>**decoupled provider**</span></span>
</dt> <dd>

<span data-ttu-id="1aca7-108">Provider gestito in un processo distinto da WMI.</span><span class="sxs-lookup"><span data-stu-id="1aca7-108">A provider hosted in a separate process from WMI.</span></span> <span data-ttu-id="1aca7-109">I provider disaccoppiati sono il metodo consigliato per instrumentare un'applicazione, poiché il provider può controllare la propria durata anziché essere avviato ogni volta che un utente accede al provider tramite WMI.</span><span class="sxs-lookup"><span data-stu-id="1aca7-109">Decoupled providers are the recommended way to instrument an application, because the provider can control its own lifetime instead of being started each time a user accesses the provider through WMI.</span></span>

</dd> <dt>

<span data-ttu-id="1aca7-110"><span id="wmi.gloss_direct_access"></span><span id="WMI.GLOSS_DIRECT_ACCESS"></span>**accesso diretto**</span><span class="sxs-lookup"><span data-stu-id="1aca7-110"><span id="wmi.gloss_direct_access"></span><span id="WMI.GLOSS_DIRECT_ACCESS"></span>**direct access**</span></span>
</dt> <dd>

<span data-ttu-id="1aca7-111">Un modo per accedere alle proprietà e ai metodi forniti da WMI in uno script come se si trattasse di proprietà e metodi di automazione di [**SWbemObject**](swbemobject.md).</span><span class="sxs-lookup"><span data-stu-id="1aca7-111">A way to access properties and methods supplied by WMI in a script as if they were automation properties and methods of [**SWbemObject**](swbemobject.md).</span></span>

<span data-ttu-id="1aca7-112">Accesso non diretto: `VolumeName = MyDisk.Properties_("VolumeName")`</span><span class="sxs-lookup"><span data-stu-id="1aca7-112">Nondirect access: `VolumeName = MyDisk.Properties_("VolumeName")`</span></span>

<span data-ttu-id="1aca7-113">Accesso diretto: `VolumeName = MyDisk.VolumeName`</span><span class="sxs-lookup"><span data-stu-id="1aca7-113">Direct access: `VolumeName = MyDisk.VolumeName`</span></span>

</dd> <dt>

<span data-ttu-id="1aca7-114"><span id="wmi.gloss_distributed_management_task_force"></span><span id="WMI.GLOSS_DISTRIBUTED_MANAGEMENT_TASK_FORCE"></span>**Distributed Management Task Force (DMTF)**</span><span class="sxs-lookup"><span data-stu-id="1aca7-114"><span id="wmi.gloss_distributed_management_task_force"></span><span id="WMI.GLOSS_DISTRIBUTED_MANAGEMENT_TASK_FORCE"></span>**Distributed Management Task Force (DMTF)**</span></span>
</dt> <dd>

<span data-ttu-id="1aca7-115">Un'organizzazione di standard internazionali che interagisce con i fornitori di tecnologie principali, tra cui Microsoft, per condurre lo sviluppo, l'adozione e l'unificazione degli standard di gestione e delle iniziative per ambienti desktop, aziendali e Internet.</span><span class="sxs-lookup"><span data-stu-id="1aca7-115">An international standards organization that works with key technology vendors, including Microsoft, to lead the development, adoption, and unification of management standards and initiatives for desktop, enterprise, and Internet environments.</span></span>

</dd> <dt>

<span data-ttu-id="1aca7-116"><span id="wmi.gloss_dmtf"></span><span id="WMI.GLOSS_DMTF"></span>**DMTF**</span><span class="sxs-lookup"><span data-stu-id="1aca7-116"><span id="wmi.gloss_dmtf"></span><span id="WMI.GLOSS_DMTF"></span>**DMTF**</span></span>
</dt> <dd>

<span data-ttu-id="1aca7-117">Vedere *Distributed Management Task Force (DMTF)*.</span><span class="sxs-lookup"><span data-stu-id="1aca7-117">See *Distributed Management Task Force (DMTF)*.</span></span>

</dd> <dt>

<span data-ttu-id="1aca7-118"><span id="wmi.gloss_dynamic_class"></span><span id="WMI.GLOSS_DYNAMIC_CLASS"></span>**classe dinamica**</span><span class="sxs-lookup"><span data-stu-id="1aca7-118"><span id="wmi.gloss_dynamic_class"></span><span id="WMI.GLOSS_DYNAMIC_CLASS"></span>**dynamic class**</span></span>
</dt> <dd>

<span data-ttu-id="1aca7-119">Classe CIM la cui definizione viene fornita da un [*provider*](gloss-p.md) in fase di esecuzione, in base alle esigenze.</span><span class="sxs-lookup"><span data-stu-id="1aca7-119">A CIM class whose definition is supplied by a [*provider*](gloss-p.md) at run time, as required.</span></span> <span data-ttu-id="1aca7-120">Le classi dinamiche rappresentano [*oggetti gestiti*](gloss-m.md) specifici del provider e non vengono archiviati nel [*repository CIM*](gloss-c.md).</span><span class="sxs-lookup"><span data-stu-id="1aca7-120">Dynamic classes represent provider-specific [*managed objects*](gloss-m.md) and are not stored in the [*CIM repository*](gloss-c.md).</span></span> <span data-ttu-id="1aca7-121">Le classi dinamiche supportano solo le *istanze dinamiche*.</span><span class="sxs-lookup"><span data-stu-id="1aca7-121">Dynamic classes support only *dynamic instances*.</span></span>

</dd> <dt>

<span data-ttu-id="1aca7-122"><span id="wmi.gloss_dynamic_instance"></span><span id="WMI.GLOSS_DYNAMIC_INSTANCE"></span>**istanza dinamica**</span><span class="sxs-lookup"><span data-stu-id="1aca7-122"><span id="wmi.gloss_dynamic_instance"></span><span id="WMI.GLOSS_DYNAMIC_INSTANCE"></span>**dynamic instance**</span></span>
</dt> <dd>

<span data-ttu-id="1aca7-123">Istanza di una classe CIM fornita da un [*provider*](gloss-p.md) quando richiesto.</span><span class="sxs-lookup"><span data-stu-id="1aca7-123">An instance of a CIM class that is supplied by a [*provider*](gloss-p.md) when required.</span></span> <span data-ttu-id="1aca7-124">Non è archiviato nel [*repository CIM*](gloss-c.md).</span><span class="sxs-lookup"><span data-stu-id="1aca7-124">It is not stored in the [*CIM repository*](gloss-c.md).</span></span> <span data-ttu-id="1aca7-125">Le istanze dinamiche possono essere fornite per classi statiche o dinamiche.</span><span class="sxs-lookup"><span data-stu-id="1aca7-125">Dynamic instances can be provided for either static or dynamic classes.</span></span> <span data-ttu-id="1aca7-126">Il supporto dinamico di istanze di una classe consente a un provider di fornire i valori delle [*Proprietà*](gloss-p.md) fino al minuto.</span><span class="sxs-lookup"><span data-stu-id="1aca7-126">Dynamically supporting instances of a class enables a provider to supply up-to-the-minute [*property*](gloss-p.md) values.</span></span>

</dd> </dl>

 

 



