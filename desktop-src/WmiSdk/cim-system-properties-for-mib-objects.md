---
description: WMI definisce un set di proprietà di sistema associate a tutte le classi e istanze delle classi, oltre alle proprietà specifiche della classe.
ms.assetid: ea8ca4e4-9969-48fc-9b9f-5a5c8442006d
ms.tgt_platform: multiple
title: Proprietà di sistema CIM per oggetti MIB
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2f0425afecc399c3cd1399e8bf565908b1c7c5d2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106313193"
---
# <a name="cim-system-properties-for-mib-objects"></a><span data-ttu-id="492e1-103">Proprietà di sistema CIM per oggetti MIB</span><span class="sxs-lookup"><span data-stu-id="492e1-103">CIM System Properties for MIB Objects</span></span>

<span data-ttu-id="492e1-104">WMI definisce un set di proprietà di sistema associate a tutte le classi e istanze delle classi, oltre alle proprietà specifiche della classe.</span><span class="sxs-lookup"><span data-stu-id="492e1-104">WMI defines a set of system properties that are associated with all classes and instances of classes in addition to class-specific properties.</span></span>

> [!Note]  
> <span data-ttu-id="492e1-105">Per ulteriori informazioni sull'installazione del provider, vedere [configurazione dell'ambiente WMI SNMP](setting-up-the-wmi-snmp-environment.md).</span><span class="sxs-lookup"><span data-stu-id="492e1-105">For more information about installing the provider, see [Setting up the WMI SNMP Environment](setting-up-the-wmi-snmp-environment.md).</span></span>

 

<span data-ttu-id="492e1-106">Il provider SNMP utilizza le proprietà di sistema CIM seguenti quando si esegue il mapping delle definizioni di oggetti MIB alle definizioni di classi CIM.</span><span class="sxs-lookup"><span data-stu-id="492e1-106">The SNMP Provider uses the following CIM system properties when mapping MIB object definitions to CIM class definitions.</span></span> <span data-ttu-id="492e1-107">Per il provider SNMP per la risoluzione completa di un oggetto gruppo, è necessario che siano presenti proprietà obbligatorie.</span><span class="sxs-lookup"><span data-stu-id="492e1-107">Mandatory properties must be present for the SNMP Provider to fully resolve a group object.</span></span> <span data-ttu-id="492e1-108">La mancata definizione di una proprietà obbligatoria restituisce un errore.</span><span class="sxs-lookup"><span data-stu-id="492e1-108">Failure to define a mandatory property returns an error.</span></span>



<table>
<thead>
<tr class="header">
<th><span data-ttu-id="492e1-109">Proprietà</span><span class="sxs-lookup"><span data-stu-id="492e1-109">Property</span></span></th>
<th><span data-ttu-id="492e1-110">Descrizione</span><span class="sxs-lookup"><span data-stu-id="492e1-110">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="492e1-111"><strong>__CLASS</strong></span><span class="sxs-lookup"><span data-stu-id="492e1-111"><strong>__CLASS</strong></span></span></td>
<td><span data-ttu-id="492e1-112"><strong>stringa</strong> di Obbligatorio</span><span class="sxs-lookup"><span data-stu-id="492e1-112"><strong>string</strong>Mandatory</span></span><br/> <span data-ttu-id="492e1-113">Per le istanze, la classe a cui appartiene l'oggetto.</span><span class="sxs-lookup"><span data-stu-id="492e1-113">For instances, the class to which the object belongs.</span></span> <span data-ttu-id="492e1-114">Per le classi, questo è il nome della classe.</span><span class="sxs-lookup"><span data-stu-id="492e1-114">For classes, this is the class name.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="492e1-115"><strong>__DYNASTY</strong></span><span class="sxs-lookup"><span data-stu-id="492e1-115"><strong>__DYNASTY</strong></span></span></td>
<td><span data-ttu-id="492e1-116"><strong>stringa</strong> di Opzionale</span><span class="sxs-lookup"><span data-stu-id="492e1-116"><strong>string</strong>Optional</span></span><br/> <span data-ttu-id="492e1-117">Nome della classe che rappresenta la classe di base finale per l'oggetto corrente (non la classe padre immediata).</span><span class="sxs-lookup"><span data-stu-id="492e1-117">Name of the class that is the ultimate base class for the current object (not its immediate parent class).</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="492e1-118"><strong>__GENUS</strong></span><span class="sxs-lookup"><span data-stu-id="492e1-118"><strong>__GENUS</strong></span></span></td>
<td><span data-ttu-id="492e1-119"><strong>UInt32</strong> Obbligatorio</span><span class="sxs-lookup"><span data-stu-id="492e1-119"><strong>uint32</strong>Mandatory</span></span><br/> <span data-ttu-id="492e1-120">Tipo di oggetto.</span><span class="sxs-lookup"><span data-stu-id="492e1-120">Type of object.</span></span> <span data-ttu-id="492e1-121">I valori possibili sono:</span><span class="sxs-lookup"><span data-stu-id="492e1-121">Values are:</span></span><br/> <dl> <span data-ttu-id="492e1-122">1 = classe</span><span class="sxs-lookup"><span data-stu-id="492e1-122">1 = class</span></span><br />
<span data-ttu-id="492e1-123">2 = istanza</span><span class="sxs-lookup"><span data-stu-id="492e1-123">2 = instance</span></span><br />
</dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="492e1-124"><strong>__NAMESPACE</strong></span><span class="sxs-lookup"><span data-stu-id="492e1-124"><strong>__NAMESPACE</strong></span></span></td>
<td><span data-ttu-id="492e1-125"><strong>stringa</strong> di Obbligatorio</span><span class="sxs-lookup"><span data-stu-id="492e1-125"><strong>string</strong>Mandatory</span></span><br/> <span data-ttu-id="492e1-126">Spazio dei nomi in cui si trova l'oggetto.</span><span class="sxs-lookup"><span data-stu-id="492e1-126">Namespace where the object is located.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="492e1-127"><strong>__PATH</strong></span><span class="sxs-lookup"><span data-stu-id="492e1-127"><strong>__PATH</strong></span></span></td>
<td><span data-ttu-id="492e1-128"><strong>stringa</strong> di Obbligatorio</span><span class="sxs-lookup"><span data-stu-id="492e1-128"><strong>string</strong>Mandatory</span></span><br/> <span data-ttu-id="492e1-129">Percorso assoluto dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="492e1-129">Absolute path to the object.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="492e1-130"><strong>__PROPERTYCOUNT</strong></span><span class="sxs-lookup"><span data-stu-id="492e1-130"><strong>__PROPERTYCOUNT</strong></span></span></td>
<td><span data-ttu-id="492e1-131"><strong>UInt32</strong> Obbligatorio</span><span class="sxs-lookup"><span data-stu-id="492e1-131"><strong>uint32</strong>Mandatory</span></span><br/> <span data-ttu-id="492e1-132">Numero di proprietà non di sistema definite per l'oggetto.</span><span class="sxs-lookup"><span data-stu-id="492e1-132">Number of non-system properties defined for the object.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="492e1-133"><strong>__RELPATH</strong></span><span class="sxs-lookup"><span data-stu-id="492e1-133"><strong>__RELPATH</strong></span></span></td>
<td><span data-ttu-id="492e1-134"><strong>stringa</strong> di Obbligatorio</span><span class="sxs-lookup"><span data-stu-id="492e1-134"><strong>string</strong>Mandatory</span></span><br/> <span data-ttu-id="492e1-135">Percorso relativo dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="492e1-135">Relative path to the object.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="492e1-136"><strong>__SERVER</strong></span><span class="sxs-lookup"><span data-stu-id="492e1-136"><strong>__SERVER</strong></span></span></td>
<td><span data-ttu-id="492e1-137"><strong>stringa</strong> di Obbligatorio</span><span class="sxs-lookup"><span data-stu-id="492e1-137"><strong>string</strong>Mandatory</span></span><br/> <span data-ttu-id="492e1-138">Server che fornisce l'oggetto.</span><span class="sxs-lookup"><span data-stu-id="492e1-138">Server supplying the object.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="492e1-139"><strong>__SUPERCLASS</strong></span><span class="sxs-lookup"><span data-stu-id="492e1-139"><strong>__SUPERCLASS</strong></span></span></td>
<td><span data-ttu-id="492e1-140"><strong>stringa</strong> di Opzionale</span><span class="sxs-lookup"><span data-stu-id="492e1-140"><strong>string</strong>Optional</span></span><br/> <span data-ttu-id="492e1-141">Classe padre immediata dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="492e1-141">Immediate parent class of the object.</span></span><br/></td>
</tr>
</tbody>
</table>



 

 

 




