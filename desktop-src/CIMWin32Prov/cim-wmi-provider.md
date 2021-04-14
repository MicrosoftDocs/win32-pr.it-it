---
description: Queste classi WMI sono dichiarate in CimWin32. mof.
ms.assetid: 53122499-1CC0-4B48-AEA1-B70B7BBC3A99
ms.tgt_platform: multiple
title: Provider WMI CIM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8a3249549e0915f51b6a9a6f2386c18ba695919a
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104523106"
---
# <a name="cim-wmi-provider"></a><span data-ttu-id="e5b08-103">Provider WMI CIM</span><span class="sxs-lookup"><span data-stu-id="e5b08-103">CIM WMI Provider</span></span>

<span data-ttu-id="e5b08-104">Queste classi WMI sono dichiarate in CimWin32. mof.</span><span class="sxs-lookup"><span data-stu-id="e5b08-104">These WMI classes are declared in CimWin32.mof.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="e5b08-105">Contenuto della sezione</span><span class="sxs-lookup"><span data-stu-id="e5b08-105">In this section</span></span>

<dl> <dt>

[<span data-ttu-id="e5b08-106">**\_Azione CIM**</span><span class="sxs-lookup"><span data-stu-id="e5b08-106">**CIM\_Action**</span></span>](cim-action.md)
</dt> <dd>

<span data-ttu-id="e5b08-107">Una classe di [**\_ azione CIM**](cim-action.md) è un'operazione che fa parte di un processo per creare un elemento software nello stato successivo o per eliminare l'elemento software nello stato corrente.</span><span class="sxs-lookup"><span data-stu-id="e5b08-107">A [**CIM\_Action**](cim-action.md) class is an operation that is part of a process to either create a software element in its next state or to eliminate the software element in the current state.</span></span>

</dd> <dt>

[<span data-ttu-id="e5b08-108">**\_ACTIONSEQUENCE CIM**</span><span class="sxs-lookup"><span data-stu-id="e5b08-108">**CIM\_ActionSequence**</span></span>](cim-actionsequence.md)
</dt> <dd>

<span data-ttu-id="e5b08-109">L'associazione [**CIM \_ ActionSequence**](cim-actionsequence.md) definisce una serie di operazioni che consentono di eseguire la transizione dell'elemento software (a cui fa riferimento l'associazione [**CIM \_ SoftwareElementActions**](cim-softwareelementactions.md) ) allo stato successivo oppure di rimuovere l'elemento software dallo stato corrente.</span><span class="sxs-lookup"><span data-stu-id="e5b08-109">The [**CIM\_ActionSequence**](cim-actionsequence.md) association defines a series of operations that transition the software element (referenced by the [**CIM\_SoftwareElementActions**](cim-softwareelementactions.md) association) to its next state, or removes the software element from its current state.</span></span>

</dd> <dt>

[<span data-ttu-id="e5b08-110">**\_ACTSASSPARE CIM**</span><span class="sxs-lookup"><span data-stu-id="e5b08-110">**CIM\_ActsAsSpare**</span></span>](cim-actsasspare.md)
</dt> <dd>

<span data-ttu-id="e5b08-111">L'associazione [**CIM \_ ActsAsSpare**](cim-actsasspare.md) indica gli elementi che possono essere sostituiti o sostituiti da altri elementi aggregati.</span><span class="sxs-lookup"><span data-stu-id="e5b08-111">The [**CIM\_ActsAsSpare**](cim-actsasspare.md) association indicates which elements can be spares or replace other aggregated elements.</span></span> <span data-ttu-id="e5b08-112">Una scorta può funzionare in modalità "hot-standby", come specificato in base a un elemento.</span><span class="sxs-lookup"><span data-stu-id="e5b08-112">A spare can operate in "hot-standby" mode as specified on an element-by-element basis.</span></span>

</dd> <dt>

[<span data-ttu-id="e5b08-113">**\_ADJACENTSLOTS CIM**</span><span class="sxs-lookup"><span data-stu-id="e5b08-113">**CIM\_AdjacentSlots**</span></span>](cim-adjacentslots.md)
</dt> <dd>

<span data-ttu-id="e5b08-114">L'associazione [**CIM \_ AdjacentSlots**](cim-adjacentslots.md) descrive il layout degli slot in una scheda di hosting o scheda di scheda.</span><span class="sxs-lookup"><span data-stu-id="e5b08-114">The [**CIM\_AdjacentSlots**](cim-adjacentslots.md) association describes the layout of slots on a hosting board or adapter card.</span></span> <span data-ttu-id="e5b08-115">Le informazioni, ad esempio la distanza tra gli slot e il fatto che siano "condivise" (se ne viene popolato uno, non è possibile usare l'altro slot), vengono trasmesse come proprietà di associazione.</span><span class="sxs-lookup"><span data-stu-id="e5b08-115">Information, such as the distance between the slots and whether they are "shared" (if one is populated, then the other slot cannot be used), is conveyed as association properties.</span></span>

</dd> <dt>

[<span data-ttu-id="e5b08-116">**\_AGGREGATEPEXTENT CIM**</span><span class="sxs-lookup"><span data-stu-id="e5b08-116">**CIM\_AggregatePExtent**</span></span>](cim-aggregatepextent.md)
</dt> <dd>

<span data-ttu-id="e5b08-117">La classe [**CIM \_ AggregatePExtent**](cim-aggregatepextent.md) fornisce informazioni di riepilogo sui blocchi logici indirizzabili, che si trovano nello stesso gruppo di ridondanza di archiviazione e si trovano nello stesso supporto fisico.</span><span class="sxs-lookup"><span data-stu-id="e5b08-117">The [**CIM\_AggregatePExtent**](cim-aggregatepextent.md) class provides summary information about addressable logical blocks, which are in the same storage redundancy group and located on the same physical media.</span></span>

</dd> <dt>

[<span data-ttu-id="e5b08-118">**\_AGGREGATEPSEXTENT CIM**</span><span class="sxs-lookup"><span data-stu-id="e5b08-118">**CIM\_AggregatePSExtent**</span></span>](cim-aggregatepsextent.md)
</dt> <dd>

<span data-ttu-id="e5b08-119">La classe [**CIM \_ AggregatePSExtent**](cim-aggregatepsextent.md) definisce il numero di blocchi logici indirizzabili in un singolo dispositivo di archiviazione, esclusi i blocchi logici mappati come dati di controllo.</span><span class="sxs-lookup"><span data-stu-id="e5b08-119">The [**CIM\_AggregatePSExtent**](cim-aggregatepsextent.md) class defines the number of addressable logical blocks on a single storage device, excluding logical blocks mapped as check data.</span></span> <span data-ttu-id="e5b08-120">Se vengono definiti set di volumi, i blocchi logici sono contenuti all'interno di un singolo set di volumi.</span><span class="sxs-lookup"><span data-stu-id="e5b08-120">If volume sets are defined, the logical blocks are contained within a single volume set.</span></span> <span data-ttu-id="e5b08-121">Si tratta di un raggruppamento alternativo per [**CIM \_ ProtectedSpaceExtent**](cim-protectedspaceextent.md), quando sono necessarie solo le informazioni di riepilogo o quando si usa la configurazione automatica.</span><span class="sxs-lookup"><span data-stu-id="e5b08-121">This is an alternative grouping for [**CIM\_ProtectedSpaceExtent**](cim-protectedspaceextent.md), when only summary information is needed or when automatic configuration is used.</span></span>

</dd> <dt>

[<span data-ttu-id="e5b08-122">**\_AGGREGATEREDUNDANCYCOMPONENT CIM**</span><span class="sxs-lookup"><span data-stu-id="e5b08-122">**CIM\_AggregateRedundancyComponent**</span></span>](cim-aggregateredundancycomponent.md)
</dt> <dd>

<span data-ttu-id="e5b08-123">La classe [**CIM \_ AggregateRedundancyComponent**](cim-aggregateredundancycomponent.md) descrive l'extent fisico aggregato in un gruppo di ridondanza di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="e5b08-123">The [**CIM\_AggregateRedundancyComponent**](cim-aggregateredundancycomponent.md) class describes the aggregate physical extent in a storage redundancy group.</span></span>

</dd> <dt>

[<span data-ttu-id="e5b08-124">**\_ALARMDEVICE CIM**</span><span class="sxs-lookup"><span data-stu-id="e5b08-124">**CIM\_AlarmDevice**</span></span>](cim-alarmdevice.md)
</dt> <dd>

<span data-ttu-id="e5b08-125">La classe [**CIM \_ AlarmDevice**](cim-alarmdevice.md) è un dispositivo di allarme che emette indicazioni udibili o visibili correlate alla situazione di un problema.</span><span class="sxs-lookup"><span data-stu-id="e5b08-125">The [**CIM\_AlarmDevice**](cim-alarmdevice.md) class is an alarm device that emits audible or visible indications related to a problem situation.</span></span>

</dd> <dt>

[<span data-ttu-id="e5b08-126">**\_ALLOCATEDRESOURCE CIM**</span><span class="sxs-lookup"><span data-stu-id="e5b08-126">**CIM\_AllocatedResource**</span></span>](cim-allocatedresource.md)
</dt> <dd>

<span data-ttu-id="e5b08-127">La classe [**CIM \_ AllocatedResource**](cim-allocatedresource.md) rappresenta un'associazione tra dispositivi logici e risorse di sistema e indica che la risorsa è assegnata al dispositivo.</span><span class="sxs-lookup"><span data-stu-id="e5b08-127">The [**CIM\_AllocatedResource**](cim-allocatedresource.md) class represents an association between logical devices and system resources and indicates that the resource is assigned to the device.</span></span>

</dd> <dt>

[<span data-ttu-id="e5b08-128">**\_APPLICATIONSYSTEM CIM**</span><span class="sxs-lookup"><span data-stu-id="e5b08-128">**CIM\_ApplicationSystem**</span></span>](cim-applicationsystem.md)
</dt> <dd>

<span data-ttu-id="e5b08-129">La classe [**CIM \_ ApplicationSystem**](cim-applicationsystem.md) rappresenta un'applicazione o un sistema software che supporta una particolare funzione di business che può essere gestita come unità indipendente.</span><span class="sxs-lookup"><span data-stu-id="e5b08-129">The [**CIM\_ApplicationSystem**](cim-applicationsystem.md) class represents an application or software system that supports a particular business function that can be managed as an independent unit.</span></span> <span data-ttu-id="e5b08-130">Un sistema di questo tipo può essere scomposto nei componenti funzionali usando la classe [**CIM \_ SoftwareFeature**](cim-softwarefeature.md) .</span><span class="sxs-lookup"><span data-stu-id="e5b08-130">Such a system can be decomposed into its functional components using the [**CIM\_SoftwareFeature**](cim-softwarefeature.md) class.</span></span> <span data-ttu-id="e5b08-131">Le funzionalità software per una particolare applicazione o sistema software si trovano usando l'associazione [**CIM \_ ApplicationSystemSoftwareFeature**](cim-applicationsystemsoftwarefeature.md) .</span><span class="sxs-lookup"><span data-stu-id="e5b08-131">The software features for a particular application or software system are located using the [**CIM\_ApplicationSystemSoftwareFeature**](cim-applicationsystemsoftwarefeature.md) association.</span></span>

</dd> <dt>

[<span data-ttu-id="e5b08-132">**\_APPLICATIONSYSTEMSOFTWAREFEATURE CIM**</span><span class="sxs-lookup"><span data-stu-id="e5b08-132">**CIM\_ApplicationSystemSoftwareFeature**</span></span>](cim-applicationsystemsoftwarefeature.md)
</dt> <dd>

<span data-ttu-id="e5b08-133">La classe [**CIM \_ ApplicationSystemSoftwareFeature**](cim-applicationsystemsoftwarefeature.md) rappresenta un'associazione che identifica le funzionalità software che costituiscono un particolare sistema applicativo.</span><span class="sxs-lookup"><span data-stu-id="e5b08-133">The [**CIM\_ApplicationSystemSoftwareFeature**](cim-applicationsystemsoftwarefeature.md) class represents an association that identifies the software features that make up a particular application system.</span></span> <span data-ttu-id="e5b08-134">Le funzionalità software possono essere incluse in prodotti diversi.</span><span class="sxs-lookup"><span data-stu-id="e5b08-134">The software features can be included in different products.</span></span>

</dd> <dt>

[<span data-ttu-id="e5b08-135">**\_ASSOCIATEDALARM CIM**</span><span class="sxs-lookup"><span data-stu-id="e5b08-135">**CIM\_AssociatedAlarm**</span></span>](cim-associatedalarm.md)
</dt> <dd>

<span data-ttu-id="e5b08-136">La dipendenza [**CIM \_ AssociatedAlarm**](cim-associatedalarm.md) associa un allarme a un dispositivo logico.</span><span class="sxs-lookup"><span data-stu-id="e5b08-136">The [**CIM\_AssociatedAlarm**](cim-associatedalarm.md) dependency associates an alarm with a logical device.</span></span>

</dd> <dt>

[<span data-ttu-id="e5b08-137">**\_ASSOCIATEDBATTERY CIM**</span><span class="sxs-lookup"><span data-stu-id="e5b08-137">**CIM\_AssociatedBattery**</span></span>](cim-associatedbattery.md)
</dt> <dd>

<span data-ttu-id="e5b08-138">La dipendenza [**CIM \_ AssociatedBattery**](cim-associatedbattery.md) associa una batteria a un dispositivo logico.</span><span class="sxs-lookup"><span data-stu-id="e5b08-138">The [**CIM\_AssociatedBattery**](cim-associatedbattery.md) dependency associates a battery with a logical device.</span></span> <span data-ttu-id="e5b08-139">Usare questa associazione per modellare singole batterie che costituiscono un gruppo di continuità (UPS, Power Supply).</span><span class="sxs-lookup"><span data-stu-id="e5b08-139">Use this association to model individual batteries that make up an uninterruptible power supply (UPS).</span></span>

</dd> <dt>

[<span data-ttu-id="e5b08-140">**\_ASSOCIATEDCOOLING CIM**</span><span class="sxs-lookup"><span data-stu-id="e5b08-140">**CIM\_AssociatedCooling**</span></span>](cim-associatedcooling.md)
</dt> <dd>

<span data-ttu-id="e5b08-141">L'associazione [**CIM \_ AssociatedCooling**](cim-associatedcooling.md) indica quando le ventole o altri dispositivi di raffreddamento sono specifici di un dispositivo (rispetto alla custodia o al raffreddamento del cabinet).</span><span class="sxs-lookup"><span data-stu-id="e5b08-141">The [**CIM\_AssociatedCooling**](cim-associatedcooling.md) association indicates when fans or other cooling devices are specific to a device (versus providing enclosure or cabinet cooling).</span></span>

</dd> <dt>

[<span data-ttu-id="e5b08-142">**\_ASSOCIATEDMEMORY CIM**</span><span class="sxs-lookup"><span data-stu-id="e5b08-142">**CIM\_AssociatedMemory**</span></span>](cim-associatedmemory.md)
</dt> <dd>

<span data-ttu-id="e5b08-143">La classe [**CIM \_ AssociateMemory**](cim-associatedmemory.md) associa la memoria installata o associata, ad esempio la memoria della cache con un dispositivo logico.</span><span class="sxs-lookup"><span data-stu-id="e5b08-143">The [**CIM\_AssociateMemory**](cim-associatedmemory.md) class associates installed or associated memory, such as cache memory with a logical device.</span></span>

</dd> <dt>

[<span data-ttu-id="e5b08-144">**\_ASSOCIATEDPROCESSORMEMORY CIM**</span><span class="sxs-lookup"><span data-stu-id="e5b08-144">**CIM\_AssociatedProcessorMemory**</span></span>](cim-associatedprocessormemory.md)
</dt> <dd>

<span data-ttu-id="e5b08-145">La classe [**CIM \_ AssociatedProcessorMemory**](cim-associatedprocessormemory.md) associa il processore e la memoria di sistema o la cache di un processore.</span><span class="sxs-lookup"><span data-stu-id="e5b08-145">The [**CIM\_AssociatedProcessorMemory**](cim-associatedprocessormemory.md) class associates the processor and system memory, or a processor's cache.</span></span>

</dd> <dt>

[<span data-ttu-id="e5b08-146">**\_ASSOCIATEDSENSOR CIM**</span><span class="sxs-lookup"><span data-stu-id="e5b08-146">**CIM\_AssociatedSensor**</span></span>](cim-associatedsensor.md)
</dt> <dd>

<span data-ttu-id="e5b08-147">La classe [**CIM \_ AssociatedSensor**](cim-associatedsensor.md) associa un sensore installato a un dispositivo logico.</span><span class="sxs-lookup"><span data-stu-id="e5b08-147">The [**CIM\_AssociatedSensor**](cim-associatedsensor.md) class associates an installed sensor with a logical device.</span></span> <span data-ttu-id="e5b08-148">Il sensore misura le proprietà di input e output critiche e può essere incluso nel dispositivo o installato nelle vicinanze.</span><span class="sxs-lookup"><span data-stu-id="e5b08-148">The sensor measures critical input and output properties, and can be included with the device or installed nearby.</span></span>

</dd> <dt>

[<span data-ttu-id="e5b08-149">**\_ASSOCIATEDSUPPLYCURRENTSENSOR CIM**</span><span class="sxs-lookup"><span data-stu-id="e5b08-149">**CIM\_AssociatedSupplyCurrentSensor**</span></span>](cim-associatedsupplycurrentsensor.md)
</dt> <dd>

<span data-ttu-id="e5b08-150">La classe [**CIM \_ AssociatedSupplyCurrentSensor**](cim-associatedsupplycurrentsensor.md) associa un alimentatore a un sensore corrente (amperaggio) che monitora la frequenza di input.</span><span class="sxs-lookup"><span data-stu-id="e5b08-150">The [**CIM\_AssociatedSupplyCurrentSensor**](cim-associatedsupplycurrentsensor.md) class associates a power supply with a current (amperage) sensor that monitors its input frequency.</span></span>

</dd> <dt>

[<span data-ttu-id="e5b08-151">**\_ASSOCIATEDSUPPLYVOLTAGESENSOR CIM**</span><span class="sxs-lookup"><span data-stu-id="e5b08-151">**CIM\_AssociatedSupplyVoltageSensor**</span></span>](cim-associatedsupplyvoltagesensor.md)
</dt> <dd>

<span data-ttu-id="e5b08-152">Associa un alimentatore a un sensore di tensione che monitora la tensione di input.</span><span class="sxs-lookup"><span data-stu-id="e5b08-152">Associates a power supply with a voltage sensor that monitors its input voltage.</span></span>

</dd> <dt>

[<span data-ttu-id="e5b08-153">**\_BASEDON CIM**</span><span class="sxs-lookup"><span data-stu-id="e5b08-153">**CIM\_BasedOn**</span></span>](cim-basedon.md)
</dt> <dd>

<span data-ttu-id="e5b08-154">La classe [**CIM \_ BasedOn**](cim-basedon.md) rappresenta un'associazione che descrive come possono essere assemblati gli extent di archiviazione da extent di livello inferiore.</span><span class="sxs-lookup"><span data-stu-id="e5b08-154">The [**CIM\_BasedOn**](cim-basedon.md) class represents an association that describes how storage extents can be assembled from lower-level extents.</span></span> <span data-ttu-id="e5b08-155">Ad esempio, gli extent fisici includono extent dello spazio protetto.</span><span class="sxs-lookup"><span data-stu-id="e5b08-155">For example, physical extents include protected space extents.</span></span> <span data-ttu-id="e5b08-156">I set di volumi vengono quindi assemblati da uno o più extent di spazio fisico o protetto.</span><span class="sxs-lookup"><span data-stu-id="e5b08-156">Thus, volume sets are assembled from one or more physical or protected space extents.</span></span> <span data-ttu-id="e5b08-157">La memoria cache può essere definita in modo indipendente e realizzata in un elemento fisico oppure può essere basata su extent di archiviazione volatili o non volatili.</span><span class="sxs-lookup"><span data-stu-id="e5b08-157">Cache memory can be defined independently and realized in a physical element, or it can be based on volatile or non-volatile storage extents.</span></span>

</dd> <dt>

[<span data-ttu-id="e5b08-158">**\_Batteria CIM**</span><span class="sxs-lookup"><span data-stu-id="e5b08-158">**CIM\_Battery**</span></span>](cim-battery.md)
</dt> <dd>

<span data-ttu-id="e5b08-159">La classe [**CIM \_ batteria**](cim-battery.md) rappresenta le funzionalità e la gestione del dispositivo logico della batteria.</span><span class="sxs-lookup"><span data-stu-id="e5b08-159">The [**CIM\_Battery**](cim-battery.md) class represents the capabilities and management of the battery logical device.</span></span> <span data-ttu-id="e5b08-160">Questa classe si applica alle batterie nei sistemi portatili e altre batterie interne ed esterne.</span><span class="sxs-lookup"><span data-stu-id="e5b08-160">This class applies to batteries in laptop systems and other internal and external batteries.</span></span>

</dd> <dt>

[<span data-ttu-id="e5b08-161">**\_BINARYSENSOR CIM**</span><span class="sxs-lookup"><span data-stu-id="e5b08-161">**CIM\_BinarySensor**</span></span>](cim-binarysensor.md)
</dt> <dd>

<span data-ttu-id="e5b08-162">La classe [**CIM \_ BinarySensor**](cim-binarysensor.md) fornisce un output booleano.</span><span class="sxs-lookup"><span data-stu-id="e5b08-162">The [**CIM\_BinarySensor**](cim-binarysensor.md) class provides a Boolean output.</span></span> <span data-ttu-id="e5b08-163">Sono state aggiunte le proprietà **CurrentState** e **PossibleStates** per i sensori, rendendo la sottoclasse **CIM \_ BinarySensor** non più necessaria, sebbene venga mantenuta per compatibilità con le versioni precedenti.</span><span class="sxs-lookup"><span data-stu-id="e5b08-163">The **CurrentState** and **PossibleStates** properties were added for sensoring, thus making the **CIM\_BinarySensor** subclass no longer necessary, although, it is retained for backward compatibility.</span></span> <span data-ttu-id="e5b08-164">È possibile creare un sensore binario creando un'istanza di un sensore con due stati possibili.</span><span class="sxs-lookup"><span data-stu-id="e5b08-164">A binary sensor can be created by instantiating a sensor with two possible states.</span></span>

</dd> <dt>

[<span data-ttu-id="e5b08-165">**CIM \_ bioselement**</span><span class="sxs-lookup"><span data-stu-id="e5b08-165">**CIM\_BIOSElement**</span></span>](cim-bioselement.md)
</dt> <dd>

<span data-ttu-id="e5b08-166">La classe [**CIM \_ bioselement**](cim-bioselement.md) rappresenta il software di basso livello che viene caricato in un archivio non volatile e utilizzato per avviare e configurare un sistema di computer.</span><span class="sxs-lookup"><span data-stu-id="e5b08-166">The [**CIM\_BIOSElement**](cim-bioselement.md) class represents the low-level software that is loaded into non-volatile storage and used to start and configure a computer system.</span></span>

</dd> <dt>

[<span data-ttu-id="e5b08-167">**\_BIOSFEATURE CIM**</span><span class="sxs-lookup"><span data-stu-id="e5b08-167">**CIM\_BIOSFeature**</span></span>](cim-biosfeature.md)
</dt> <dd>

<span data-ttu-id="e5b08-168">rappresenta le funzionalità del software di basso livello utilizzato per avviare e configurare un sistema di computer.</span><span class="sxs-lookup"><span data-stu-id="e5b08-168">represents the capabilities of the low-level software that is used to start and configure a computer system.</span></span>

</dd> <dt>

[<span data-ttu-id="e5b08-169">**\_BIOSFEATUREBIOSELEMENTS CIM**</span><span class="sxs-lookup"><span data-stu-id="e5b08-169">**CIM\_BIOSFeatureBIOSElements**</span></span>](cim-biosfeaturebioselements.md)
</dt> <dd>

<span data-ttu-id="e5b08-170">La classe [**CIM \_ BIOSFeatureBIOSElements**](cim-biosfeaturebioselements.md) associa una funzionalità BIOS e i relativi elementi BIOS aggregati.</span><span class="sxs-lookup"><span data-stu-id="e5b08-170">The [**CIM\_BIOSFeatureBIOSElements**](cim-biosfeaturebioselements.md) class associates a BIOS feature and its aggregated BIOS elements.</span></span>

</dd> <dt>

[<span data-ttu-id="e5b08-171">**\_BIOSLOADEDINNV CIM**</span><span class="sxs-lookup"><span data-stu-id="e5b08-171">**CIM\_BIOSLoadedInNV**</span></span>](cim-biosloadedinnv.md)
</dt> <dd>

<span data-ttu-id="e5b08-172">La classe [**CIM \_ BIOSLoadedInNV**](cim-biosloadedinnv.md) associa un elemento BIOS e l'archiviazione non volatile in cui viene caricata.</span><span class="sxs-lookup"><span data-stu-id="e5b08-172">The [**CIM\_BIOSLoadedInNV**](cim-biosloadedinnv.md) class associates a BIOS element and the non-volatile storage in which it is loaded.</span></span>

</dd> <dt>

[<span data-ttu-id="e5b08-173">**\_BOOTOSFROMFS CIM**</span><span class="sxs-lookup"><span data-stu-id="e5b08-173">**CIM\_BootOSFromFS**</span></span>](cim-bootosfromfs.md)
</dt> <dd>

<span data-ttu-id="e5b08-174">La classe [**CIM \_ BootOSFromFS**](cim-bootosfromfs.md) associa il sistema operativo e i file System da cui viene caricato il sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="e5b08-174">The [**CIM\_BootOSFromFS**](cim-bootosfromfs.md) class associates the operating system and the file systems from which the operating system is loaded.</span></span> <span data-ttu-id="e5b08-175">L'associazione è molti-a-molti; un sistema operativo distribuito può dipendere da diversi file System da caricare correttamente e completamente.</span><span class="sxs-lookup"><span data-stu-id="e5b08-175">The association is many-to-many; a distributed operating system can depend on several file systems to load correctly and completely.</span></span>

</dd> <dt>

[<span data-ttu-id="e5b08-176">**\_BOOTSAP CIM**</span><span class="sxs-lookup"><span data-stu-id="e5b08-176">**CIM\_BootSAP**</span></span>](cim-bootsap.md)
</dt> <dd>

<span data-ttu-id="e5b08-177">La classe [**CIM \_ BootSAP**](cim-bootsap.md) rappresenta i punti di accesso di un servizio di avvio.</span><span class="sxs-lookup"><span data-stu-id="e5b08-177">The [**CIM\_BootSAP**](cim-bootsap.md) class represents the access points of a boot service.</span></span>

</dd> <dt>

[<span data-ttu-id="e5b08-178">**\_BOOTSERVICE CIM**</span><span class="sxs-lookup"><span data-stu-id="e5b08-178">**CIM\_BootService**</span></span>](cim-bootservice.md)
</dt> <dd>

<span data-ttu-id="e5b08-179">La classe [**CIM \_ BOOTSERVICE**](cim-bootservice.md) rappresenta la funzionalità fornita da un dispositivo o un software, o da una rete, per caricare un sistema operativo in un computer di sistema.</span><span class="sxs-lookup"><span data-stu-id="e5b08-179">The [**CIM\_BootService**](cim-bootservice.md) class represents the functionality provided by a device or software, or by a network, to load an operating system on a unitary computer system.</span></span>

</dd> <dt>

[<span data-ttu-id="e5b08-180">**\_BOOTSERVICEACCESSBYSAP CIM**</span><span class="sxs-lookup"><span data-stu-id="e5b08-180">**CIM\_BootServiceAccessBySAP**</span></span>](cim-bootserviceaccessbysap.md)
</dt> <dd>

<span data-ttu-id="e5b08-181">La classe [**CIM \_ BootServiceAccessBySAP**](cim-bootserviceaccessbysap.md) associa un servizio di avvio e i relativi punti di accesso.</span><span class="sxs-lookup"><span data-stu-id="e5b08-181">The [**CIM\_BootServiceAccessBySAP**](cim-bootserviceaccessbysap.md) class associates a boot service and its access points.</span></span>

</dd> <dt>

[<span data-ttu-id="e5b08-182">**\_CACHEMEMORY CIM**</span><span class="sxs-lookup"><span data-stu-id="e5b08-182">**CIM\_CacheMemory**</span></span>](cim-cachememory.md)
</dt> <dd>

<span data-ttu-id="e5b08-183">La classe [**CIM \_ CacheMemory**](cim-cachememory.md) definisce le funzionalità e la gestione della memoria cache.</span><span class="sxs-lookup"><span data-stu-id="e5b08-183">The [**CIM\_CacheMemory**](cim-cachememory.md) class defines the capabilities and management of cache memory.</span></span>

</dd> <dt>

[<span data-ttu-id="e5b08-184">**\_Scheda CIM**</span><span class="sxs-lookup"><span data-stu-id="e5b08-184">**CIM\_Card**</span></span>](cim-card.md)
</dt> <dd>

<span data-ttu-id="e5b08-185">La [**classe \_ CIM**](cim-card.md) rappresenta un tipo di contenitore fisico che può essere inserito in un'altra scheda o lavagna host oppure è una lavagna di hosting/scheda madre in uno chassis.</span><span class="sxs-lookup"><span data-stu-id="e5b08-185">The [**CIM\_Card**](cim-card.md) class represents a type of physical container that can be plugged into another card or hosting board, or is itself a hosting board/motherboard in a chassis.</span></span> <span data-ttu-id="e5b08-186">Questa classe include tutti i pacchetti in grado di trasportare segnali e fornire un punto di montaggio per i componenti fisici, ad esempio chip o altri pacchetti fisici, ad esempio altre schede.</span><span class="sxs-lookup"><span data-stu-id="e5b08-186">This class includes any package that is capable of carrying signals and providing a mounting point for physical components, such as chips or other physical packages, such as other cards.</span></span>

</dd> <dt>

[<span data-ttu-id="e5b08-187">**\_CARDINSLOT CIM**</span><span class="sxs-lookup"><span data-stu-id="e5b08-187">**CIM\_CardInSlot**</span></span>](cim-cardinslot.md)
</dt> <dd>

<span data-ttu-id="e5b08-188">La classe [**CIM \_ CardInSlot**](cim-cardinslot.md) associa una scheda di adapter al contenitore in cui viene inserita.</span><span class="sxs-lookup"><span data-stu-id="e5b08-188">The [**CIM\_CardInSlot**](cim-cardinslot.md) class associates an adapter card with the container into which it is inserted.</span></span>

</dd> <dt>

[<span data-ttu-id="e5b08-189">**\_CARDONCARD CIM**</span><span class="sxs-lookup"><span data-stu-id="e5b08-189">**CIM\_CardOnCard**</span></span>](cim-cardoncard.md)
</dt> <dd>

<span data-ttu-id="e5b08-190">L'associazione [**CIM \_ CardOnCard**](cim-cardoncard.md) descrive le relazioni sulle schede che possono essere inserite in schede madri/battiscopa, daughtercards di un adapter o schede che supportano moduli speciali di tipo scheda.</span><span class="sxs-lookup"><span data-stu-id="e5b08-190">The [**CIM\_CardOnCard**](cim-cardoncard.md) association describes relationships about cards that can be plugged into motherboards/baseboards, daughtercards of an adapter, or cards that support special card-like modules.</span></span>

</dd> <dt>

[<span data-ttu-id="e5b08-191">**\_CDROMDRIVE CIM**</span><span class="sxs-lookup"><span data-stu-id="e5b08-191">**CIM\_CDROMDrive**</span></span>](cim-cdromdrive.md)
</dt> <dd>

<span data-ttu-id="e5b08-192">La classe [**CIM \_ CDROMDrive**](cim-cdromdrive.md) rappresenta un'unità CD-ROM nel computer.</span><span class="sxs-lookup"><span data-stu-id="e5b08-192">The [**CIM\_CDROMDrive**](cim-cdromdrive.md) class represents a CD-ROM drive on the computer.</span></span>

</dd> <dt>

[<span data-ttu-id="e5b08-193">**\_Chassis CIM**</span><span class="sxs-lookup"><span data-stu-id="e5b08-193">**CIM\_Chassis**</span></span>](cim-chassis.md)
</dt> <dd>

<span data-ttu-id="e5b08-194">La [**classe \_ chassis CIM**](cim-chassis.md) rappresenta gli elementi fisici che racchiudono altri elementi e fornisce funzionalità definibili, ad esempio un desktop, un nodo di elaborazione, un UPS, un'archiviazione su disco o su nastro o una combinazione di questi.</span><span class="sxs-lookup"><span data-stu-id="e5b08-194">The [**CIM\_Chassis**](cim-chassis.md) class represents the physical elements that enclose other elements and provide definable functionality, such as a desktop, processing node, UPS, disk or tape storage, or a combination of these.</span></span>

</dd> <dt>

[<span data-ttu-id="e5b08-195">**\_CHASSISINRACK CIM**</span><span class="sxs-lookup"><span data-stu-id="e5b08-195">**CIM\_ChassisInRack**</span></span>](cim-chassisinrack.md)
</dt> <dd>

<span data-ttu-id="e5b08-196">L'associazione [**CIM \_ ChassisInRack**](cim-chassisinrack.md) rappresenta la relazione "containing" tra un rack e uno chassis che contiene.</span><span class="sxs-lookup"><span data-stu-id="e5b08-196">The [**CIM\_ChassisInRack**](cim-chassisinrack.md) association represents the "containing" relationship between a rack and a chassis that it contains.</span></span>

</dd> <dt>

[<span data-ttu-id="e5b08-197">**\_Controllo CIM**</span><span class="sxs-lookup"><span data-stu-id="e5b08-197">**CIM\_Check**</span></span>](cim-check.md)
</dt> <dd>

<span data-ttu-id="e5b08-198">La classe [**CIM \_ Check**](cim-check.md) rappresenta una condizione o una caratteristica che dovrebbe essere true in un ambiente definito o con ambito da un'istanza di una classe [**CIM \_ ComputerSystem**](cim-computersystem.md) .</span><span class="sxs-lookup"><span data-stu-id="e5b08-198">The [**CIM\_Check**](cim-check.md) class represents a condition or characteristic that is expected to be true in an environment defined or scoped by an instance of a [**CIM\_ComputerSystem**](cim-computersystem.md) class.</span></span> <span data-ttu-id="e5b08-199">I controlli associati a un particolare elemento software sono organizzati in uno dei due gruppi usando la proprietà **Phase** dell'associazione [**CIM \_ SoftwareElementChecks**](cim-softwareelementchecks.md) .</span><span class="sxs-lookup"><span data-stu-id="e5b08-199">The checks associated with a particular software element are organized into one of two groups using the **Phase** property of the [**CIM\_SoftwareElementChecks**](cim-softwareelementchecks.md) association.</span></span>

</dd> <dt>

[<span data-ttu-id="e5b08-200">**\_Chip CIM**</span><span class="sxs-lookup"><span data-stu-id="e5b08-200">**CIM\_Chip**</span></span>](cim-chip.md)
</dt> <dd>

<span data-ttu-id="e5b08-201">La classe [**CIM \_ chip**](cim-chip.md) rappresenta il tipo di hardware del circuito integrato, tra cui ASICS, processori, chip di memoria e così via.</span><span class="sxs-lookup"><span data-stu-id="e5b08-201">The [**CIM\_Chip**](cim-chip.md) class represents the type of integrated circuit hardware, including ASICs, processors, memory chips, and so on.</span></span>

</dd> <dt>

[<span data-ttu-id="e5b08-202">**\_CLUSTERINGSAP CIM**</span><span class="sxs-lookup"><span data-stu-id="e5b08-202">**CIM\_ClusteringSAP**</span></span>](cim-clusteringsap.md)
</dt> <dd>

<span data-ttu-id="e5b08-203">La classe [**CIM \_ ClusteringSAP**](cim-clusteringsap.md) rappresenta i punti di accesso di un servizio di clustering.</span><span class="sxs-lookup"><span data-stu-id="e5b08-203">The [**CIM\_ClusteringSAP**](cim-clusteringsap.md) class represents the access points of a clustering service.</span></span>

</dd> <dt>

[<span data-ttu-id="e5b08-204">**\_CLUSTERINGSERVICE CIM**</span><span class="sxs-lookup"><span data-stu-id="e5b08-204">**CIM\_ClusteringService**</span></span>](cim-clusteringservice.md)
</dt> <dd>

<span data-ttu-id="e5b08-205">La classe [**CIM \_ ClusteringService**](cim-clusteringservice.md) rappresenta la funzionalità fornita da un cluster.</span><span class="sxs-lookup"><span data-stu-id="e5b08-205">The [**CIM\_ClusteringService**](cim-clusteringservice.md) class represents the functionality provided by a cluster.</span></span> <span data-ttu-id="e5b08-206">Ad esempio, la funzionalità di failover può essere modellata come servizio di un cluster di failover.</span><span class="sxs-lookup"><span data-stu-id="e5b08-206">For example, failover functionality can be modeled as a service of a failover cluster.</span></span>

</dd> <dt>

[<span data-ttu-id="e5b08-207">**\_CLUSTERSERVICEACCESSBYSAP CIM**</span><span class="sxs-lookup"><span data-stu-id="e5b08-207">**CIM\_ClusterServiceAccessBySAP**</span></span>](cim-clusterserviceaccessbysap.md)
</dt> <dd>

<span data-ttu-id="e5b08-208">La classe [**CIM \_ ClusterServiceAccessBySAP**](cim-clusterserviceaccessbysap.md) rappresenta la relazione tra un servizio di clustering e i relativi punti di accesso.</span><span class="sxs-lookup"><span data-stu-id="e5b08-208">The [**CIM\_ClusterServiceAccessBySAP**](cim-clusterserviceaccessbysap.md) class represents the relationship between a clustering service and its access points.</span></span>

</dd> <dt>

[<span data-ttu-id="e5b08-209">**\_COLLECTEDCOLLECTIONS CIM**</span><span class="sxs-lookup"><span data-stu-id="e5b08-209">**CIM\_CollectedCollections**</span></span>](cim-collectedcollections.md)
</dt> <dd>

<span data-ttu-id="e5b08-210">La classe [**CIM \_ CollectedCollections**](cim-collectedcollections.md) è un'associazione di aggregazione che rappresenta una raccolta di elementi di sistema gestiti (MSE) contenuti in una raccolta di mses.</span><span class="sxs-lookup"><span data-stu-id="e5b08-210">The [**CIM\_CollectedCollections**](cim-collectedcollections.md) class is an aggregation association that represents a collection of Managed System Elements (MSE) contained in a collection of MSEs.</span></span>

</dd> <dt>

[<span data-ttu-id="e5b08-211">**\_COLLECTEDMSES CIM**</span><span class="sxs-lookup"><span data-stu-id="e5b08-211">**CIM\_CollectedMSEs**</span></span>](cim-collectedmses.md)
</dt> <dd>

<span data-ttu-id="e5b08-212">La classe di associazione [**CIM \_ CollectedMSEs**](cim-collectedmses.md) rappresenta i membri dell'oggetto GROUPING, una classe [**CollectionOfMSEs**](cim-collectionofmses.md) .</span><span class="sxs-lookup"><span data-stu-id="e5b08-212">The [**CIM\_CollectedMSEs**](cim-collectedmses.md) association class represents the members of the grouping object, a [**CollectionOfMSEs**](cim-collectionofmses.md) class.</span></span>

</dd> <dt>

[<span data-ttu-id="e5b08-213">**\_COLLECTIONOFMSES CIM**</span><span class="sxs-lookup"><span data-stu-id="e5b08-213">**CIM\_CollectionOfMSEs**</span></span>](cim-collectionofmses.md)
</dt> <dd>

<span data-ttu-id="e5b08-214">L'oggetto [**CIM \_ CollectionOfMSEs**](cim-collectionofmses.md) consente il raggruppamento di oggetti [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md) allo scopo di associare le impostazioni e le configurazioni.</span><span class="sxs-lookup"><span data-stu-id="e5b08-214">The [**CIM\_CollectionOfMSEs**](cim-collectionofmses.md) object allows the grouping of [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md) objects for the purpose of associating settings and configurations.</span></span> <span data-ttu-id="e5b08-215">È astratto per richiedere ulteriori definizioni e perfezionamento semantico nelle sottoclassi.</span><span class="sxs-lookup"><span data-stu-id="e5b08-215">It is abstract to require further definition and semantic refinement in subclasses.</span></span>

</dd> <dt>

[<span data-ttu-id="e5b08-216">**\_COLLECTIONOFSENSORS CIM**</span><span class="sxs-lookup"><span data-stu-id="e5b08-216">**CIM\_CollectionOfSensors**</span></span>](cim-collectionofsensors.md)
</dt> <dd>

<span data-ttu-id="e5b08-217">L'associazione [**CIM \_ CollectionOfSensors**](cim-collectionofsensors.md) rappresenta i sensori binari che compongono il sensore multistato.</span><span class="sxs-lookup"><span data-stu-id="e5b08-217">The [**CIM\_CollectionOfSensors**](cim-collectionofsensors.md) association represents the binary sensors that make up the multistate sensor.</span></span>

</dd> <dt>

[<span data-ttu-id="e5b08-218">**\_COLLECTIONSETTING CIM**</span><span class="sxs-lookup"><span data-stu-id="e5b08-218">**CIM\_CollectionSetting**</span></span>](cim-collectionsetting.md)
</dt> <dd>

<span data-ttu-id="e5b08-219">La classe [**CIM \_ CollectionSetting**](cim-collectionsetting.md) rappresenta l'associazione tra un [**\_ CollectionOfMSEs CIM**](cim-collectionofmses.md) e la classe di impostazione definita.</span><span class="sxs-lookup"><span data-stu-id="e5b08-219">The [**CIM\_CollectionSetting**](cim-collectionsetting.md) class represents the association between a [**CIM\_CollectionOfMSEs**](cim-collectionofmses.md) and the setting class defined for them.</span></span>

</dd> <dt>

[<span data-ttu-id="e5b08-220">**\_COMPATIBLEPRODUCT CIM**</span><span class="sxs-lookup"><span data-stu-id="e5b08-220">**CIM\_CompatibleProduct**</span></span>](cim-compatibleproduct.md)
</dt> <dd>

<span data-ttu-id="e5b08-221">La classe [**CIM \_ CompatibleProduct**](cim-compatibleproduct.md) rappresenta un'associazione tra i prodotti che indica se due prodotti a cui viene fatto riferimento sono interoperativi, ad esempio se possono essere installati insieme o se uno può essere il contenitore fisico per l'altro e così via.</span><span class="sxs-lookup"><span data-stu-id="e5b08-221">The [**CIM\_CompatibleProduct**](cim-compatibleproduct.md) class represents an association between products that indicates whether two referenced products are interoperable, such as whether they can be installed together, or whether one can be the physical container for the other, and so on.</span></span>

</dd> <dt>

[<span data-ttu-id="e5b08-222">**\_Componente CIM**</span><span class="sxs-lookup"><span data-stu-id="e5b08-222">**CIM\_Component**</span></span>](cim-component.md)
</dt> <dd>

<span data-ttu-id="e5b08-223">L' [**associazione \_ componente CIM**](cim-component.md) rappresenta le parti di una relazione tra mses.</span><span class="sxs-lookup"><span data-stu-id="e5b08-223">The [**CIM\_Component**](cim-component.md) association represents the parts of a relationship between MSEs.</span></span>

</dd> <dt>

[<span data-ttu-id="e5b08-224">**\_ComputerSystem CIM**</span><span class="sxs-lookup"><span data-stu-id="e5b08-224">**CIM\_ComputerSystem**</span></span>](cim-computersystem.md)
</dt> <dd>

<span data-ttu-id="e5b08-225">Una classe [**CIM \_ ComputerSystem**](cim-computersystem.md) rappresenta una raccolta speciale di istanze [**CIM di \_ ManagedSystemElement**](cim-managedsystemelement.md) .</span><span class="sxs-lookup"><span data-stu-id="e5b08-225">A [**CIM\_ComputerSystem**](cim-computersystem.md) class represents a special collection of [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md) instances.</span></span> <span data-ttu-id="e5b08-226">Questa raccolta fornisce funzionalità del computer e funge da punto di aggregazione per associare uno o più degli elementi seguenti: file system, sistema operativo, processore e memoria (archiviazione volatile e non volatile).</span><span class="sxs-lookup"><span data-stu-id="e5b08-226">This collection provides computer capabilities and serves as an aggregation point to associate one or more of the following elements: file system, operating system, processor and memory (volatile and non-volatile storage).</span></span> <span data-ttu-id="e5b08-227">Questa classe è derivata dal [**\_ sistema CIM**](cim-system.md).</span><span class="sxs-lookup"><span data-stu-id="e5b08-227">This class is derived from [**CIM\_System**](cim-system.md).</span></span>

</dd> <dt>

[<span data-ttu-id="e5b08-228">**\_COMPUTERSYSTEMDMA CIM**</span><span class="sxs-lookup"><span data-stu-id="e5b08-228">**CIM\_ComputerSystemDMA**</span></span>](cim-computersystemdma.md)
</dt> <dd>

<span data-ttu-id="e5b08-229">La classe [**CIM \_ ComputerSystemDMA**](cim-computersystemdma.md) rappresenta un'associazione tra un sistema di computer e i canali di accesso diretto alla memoria (DMA) disponibili.</span><span class="sxs-lookup"><span data-stu-id="e5b08-229">The [**CIM\_ComputerSystemDMA**](cim-computersystemdma.md) class represents an association between a computer system and its available direct memory access (DMA) channels.</span></span>

</dd> <dt>

[<span data-ttu-id="e5b08-230">**\_COMPUTERSYSTEMIRQ CIM**</span><span class="sxs-lookup"><span data-stu-id="e5b08-230">**CIM\_ComputerSystemIRQ**</span></span>](cim-computersystemirq.md)
</dt> <dd>

<span data-ttu-id="e5b08-231">La classe [**CIM \_ ComputerSystemIRQ**](cim-computersystemirq.md) rappresenta un'associazione tra un sistema di computer e le relative righe di richiesta di interrupt (IRQ) disponibili.</span><span class="sxs-lookup"><span data-stu-id="e5b08-231">The [**CIM\_ComputerSystemIRQ**](cim-computersystemirq.md) class represents an association between a computer system and its available interrupt request lines (IRQs).</span></span>

</dd> <dt>

[<span data-ttu-id="e5b08-232">**\_COMPUTERSYSTEMMAPPEDIO CIM**</span><span class="sxs-lookup"><span data-stu-id="e5b08-232">**CIM\_ComputerSystemMappedIO**</span></span>](cim-computersystemmappedio.md)
</dt> <dd>

<span data-ttu-id="e5b08-233">La classe [**CIM \_ ComputerSystemMappedIO**](cim-computersystemmappedio.md) rappresenta un'associazione tra un sistema di computer e le relative porte I/O mappate alla memoria disponibili.</span><span class="sxs-lookup"><span data-stu-id="e5b08-233">The [**CIM\_ComputerSystemMappedIO**](cim-computersystemmappedio.md) class represents an association between a computer system and its available memory-mapped I/O ports.</span></span>

</dd> <dt>

[<span data-ttu-id="e5b08-234">**\_COMPUTERSYSTEMPACKAGE CIM**</span><span class="sxs-lookup"><span data-stu-id="e5b08-234">**CIM\_ComputerSystemPackage**</span></span>](cim-computersystempackage.md)
</dt> <dd>

<span data-ttu-id="e5b08-235">La classe [**CIM \_ ComputerSystemPackage**](cim-computersystempackage.md) rappresenta un'associazione che definisce in modo esplicito la relazione tra i sistemi di computer unitari e uno o più pacchetti fisici.</span><span class="sxs-lookup"><span data-stu-id="e5b08-235">The [**CIM\_ComputerSystemPackage**](cim-computersystempackage.md) class represents an association that explicitly defines the relationship between unitary computer systems and one or more physical packages.</span></span> <span data-ttu-id="e5b08-236">L'associazione è simile al modo in cui i dispositivi logici vengono realizzati da elementi fisici.</span><span class="sxs-lookup"><span data-stu-id="e5b08-236">The association is similar to the way that logical devices are realized by physical elements.</span></span>

</dd> <dt>

[<span data-ttu-id="e5b08-237">**\_COMPUTERSYSTEMRESOURCE CIM**</span><span class="sxs-lookup"><span data-stu-id="e5b08-237">**CIM\_ComputerSystemResource**</span></span>](cim-computersystemresource.md)
</dt> <dd>

<span data-ttu-id="e5b08-238">La classe [**CIM \_ ComputerSystemResource**](cim-computersystemresource.md) rappresenta un'associazione tra un sistema di computer e le risorse di sistema disponibili.</span><span class="sxs-lookup"><span data-stu-id="e5b08-238">The [**CIM\_ComputerSystemResource**](cim-computersystemresource.md) class represents an association between a computer system and its available system resources.</span></span>

</dd> <dt>

[<span data-ttu-id="e5b08-239">**\_Configurazione CIM**</span><span class="sxs-lookup"><span data-stu-id="e5b08-239">**CIM\_Configuration**</span></span>](cim-configuration.md)
</dt> <dd>

<span data-ttu-id="e5b08-240">L'oggetto di [**\_ configurazione CIM**](cim-configuration.md) consente il raggruppamento di set di parametri (definiti in oggetti [**\_ impostazione CIM**](cim-setting.md) ) e le dipendenze per uno o più elementi di sistema gestiti.</span><span class="sxs-lookup"><span data-stu-id="e5b08-240">The [**CIM\_Configuration**](cim-configuration.md) object allows the grouping of parameter sets (defined in [**CIM\_Setting**](cim-setting.md) objects) and dependencies for one or more managed system elements.</span></span>

</dd> <dt>

[<span data-ttu-id="e5b08-241">**\_CONNECTEDTO CIM**</span><span class="sxs-lookup"><span data-stu-id="e5b08-241">**CIM\_ConnectedTo**</span></span>](cim-connectedto.md)
</dt> <dd>

<span data-ttu-id="e5b08-242">La classe [**CIM \_ ConnectedTo**](cim-connectedto.md) rappresenta un'associazione che indica che due o più connettori fisici sono connessi.</span><span class="sxs-lookup"><span data-stu-id="e5b08-242">The [**CIM\_ConnectedTo**](cim-connectedto.md) class represents an association that indicates that two or more physical connectors are connected.</span></span>

</dd> <dt>

[<span data-ttu-id="e5b08-243">**\_CONNECTORONPACKAGE CIM**</span><span class="sxs-lookup"><span data-stu-id="e5b08-243">**CIM\_ConnectorOnPackage**</span></span>](cim-connectoronpackage.md)
</dt> <dd>

<span data-ttu-id="e5b08-244">La classe [**CIM \_ ConnectorOnPackage**](cim-connectoronpackage.md) rappresenta un'associazione che rende esplicita la relazione di contenimento tra i connettori e i pacchetti.</span><span class="sxs-lookup"><span data-stu-id="e5b08-244">The [**CIM\_ConnectorOnPackage**](cim-connectoronpackage.md) class represents an association that makes explicit the containment relationship between connectors and packages.</span></span> <span data-ttu-id="e5b08-245">I pacchetti fisici contengono connettori, oltre ad altri elementi fisici.</span><span class="sxs-lookup"><span data-stu-id="e5b08-245">Physical packages contain connectors as well as other physical elements.</span></span>

</dd> <dt>

[<span data-ttu-id="e5b08-246">**\_Contenitore CIM**</span><span class="sxs-lookup"><span data-stu-id="e5b08-246">**CIM\_Container**</span></span>](cim-container.md)
</dt> <dd>

<span data-ttu-id="e5b08-247">La [**classe \_ contenitore CIM**](cim-container.md) rappresenta un'associazione tra un elemento contenuto e un elemento fisico contenitore.</span><span class="sxs-lookup"><span data-stu-id="e5b08-247">The [**CIM\_Container**](cim-container.md) class represents an association between a contained and a containing physical element.</span></span> <span data-ttu-id="e5b08-248">Un oggetto contenitore deve essere un pacchetto fisico.</span><span class="sxs-lookup"><span data-stu-id="e5b08-248">A containing object must be a physical package.</span></span>

</dd> <dt>

[<span data-ttu-id="e5b08-249">**\_CONTROLLEDBY CIM**</span><span class="sxs-lookup"><span data-stu-id="e5b08-249">**CIM\_ControlledBy**</span></span>](cim-controlledby.md)
</dt> <dd>

<span data-ttu-id="e5b08-250">La relazione [**CIM \_ ControlledBy**](cim-controlledby.md) indica i dispositivi a cui viene eseguito il comando o a cui si accede tramite il dispositivo logico del controller.</span><span class="sxs-lookup"><span data-stu-id="e5b08-250">The [**CIM\_ControlledBy**](cim-controlledby.md) relationship indicates which devices are commanded by, or accessed through, the controller logical device.</span></span>

</dd> <dt>

[<span data-ttu-id="e5b08-251">**\_Controller CIM**</span><span class="sxs-lookup"><span data-stu-id="e5b08-251">**CIM\_Controller**</span></span>](cim-controller.md)
</dt> <dd>

<span data-ttu-id="e5b08-252">La classe del [**\_ controller CIM**](cim-controller.md) è una classe padre per il raggruppamento di dispositivi correlati al controllo.</span><span class="sxs-lookup"><span data-stu-id="e5b08-252">The [**CIM\_Controller**](cim-controller.md) class is a parent class for grouping miscellaneous control-related devices.</span></span> <span data-ttu-id="e5b08-253">Esempi di controller sono controller SCSI, controller USB e controller seriali.</span><span class="sxs-lookup"><span data-stu-id="e5b08-253">Examples of controllers are SCSI controllers, USB controllers, and serial controllers.</span></span>

</dd> <dt>

[<span data-ttu-id="e5b08-254">**\_COOLINGDEVICE CIM**</span><span class="sxs-lookup"><span data-stu-id="e5b08-254">**CIM\_CoolingDevice**</span></span>](cim-coolingdevice.md)
</dt> <dd>

<span data-ttu-id="e5b08-255">La classe [**CIM \_ CoolingDevice**](cim-coolingdevice.md) rappresenta le funzionalità e la gestione dei dispositivi di raffreddamento.</span><span class="sxs-lookup"><span data-stu-id="e5b08-255">The [**CIM\_CoolingDevice**](cim-coolingdevice.md) class represents the capabilities and management of cooling devices.</span></span>

</dd> <dt>

[<span data-ttu-id="e5b08-256">**\_COPYFILEACTION CIM**</span><span class="sxs-lookup"><span data-stu-id="e5b08-256">**CIM\_CopyFileAction**</span></span>](cim-copyfileaction.md)
</dt> <dd>

<span data-ttu-id="e5b08-257">La classe [**CIM \_ CopyFileAction**](cim-copyfileaction.md) rappresenta lo spostamento o la copia di file da un sistema di computer in una nuova posizione.</span><span class="sxs-lookup"><span data-stu-id="e5b08-257">The [**CIM\_CopyFileAction**](cim-copyfileaction.md) class represents moving or copying files from a computer system to a new location.</span></span>

</dd> <dt>

[<span data-ttu-id="e5b08-258">**\_CREATEDIRECTORYACTION CIM**</span><span class="sxs-lookup"><span data-stu-id="e5b08-258">**CIM\_CreateDirectoryAction**</span></span>](cim-createdirectoryaction.md)
</dt> <dd>

<span data-ttu-id="e5b08-259">La classe [**CIM \_ CreateDirectoryAction**](cim-createdirectoryaction.md) crea directory vuote per gli elementi software da installare localmente.</span><span class="sxs-lookup"><span data-stu-id="e5b08-259">The [**CIM\_CreateDirectoryAction**](cim-createdirectoryaction.md) class creates empty directories for software elements to be installed locally.</span></span>

</dd> <dt>

[<span data-ttu-id="e5b08-260">**\_CURRENTSENSOR CIM**</span><span class="sxs-lookup"><span data-stu-id="e5b08-260">**CIM\_CurrentSensor**</span></span>](cim-currentsensor.md)
</dt> <dd>

<span data-ttu-id="e5b08-261">La classe [**CIM \_ CurrentSensor**](cim-currentsensor.md) esiste per compatibilità con le versioni precedenti delle definizioni dello schema CIM.</span><span class="sxs-lookup"><span data-stu-id="e5b08-261">The [**CIM\_CurrentSensor**](cim-currentsensor.md) class exists for backward compatibility to earlier CIM schema definitions.</span></span>

</dd> <dt>

[<span data-ttu-id="e5b08-262">**File di \_ DataFile CIM**</span><span class="sxs-lookup"><span data-stu-id="e5b08-262">**CIM\_DataFile**</span></span>](cim-datafile.md)
</dt> <dd>

<span data-ttu-id="e5b08-263">La classe [**CIM \_ DataFile**](cim-datafile.md) rappresenta una raccolta denominata di dati o codice eseguibile.</span><span class="sxs-lookup"><span data-stu-id="e5b08-263">The [**CIM\_DataFile**](cim-datafile.md) class represents a named collection of data or executable code.</span></span> <span data-ttu-id="e5b08-264">Verranno restituite solo le istanze di file nei dischi fissi locali</span><span class="sxs-lookup"><span data-stu-id="e5b08-264">Only instances of files on local fixed disks will be returned</span></span>

</dd> <dt>

[<span data-ttu-id="e5b08-265">**\_Dipendenza CIM**</span><span class="sxs-lookup"><span data-stu-id="e5b08-265">**CIM\_Dependency**</span></span>](cim-dependency.md)
</dt> <dd>

<span data-ttu-id="e5b08-266">La classe di [**\_ dipendenza CIM**](cim-dependency.md) rappresenta un'associazione che stabilisce relazioni di dipendenza tra oggetti.</span><span class="sxs-lookup"><span data-stu-id="e5b08-266">The [**CIM\_Dependency**](cim-dependency.md) class represents an association that establishes dependency relationships between objects.</span></span>

</dd> <dt>

[<span data-ttu-id="e5b08-267">**\_DEPENDENCYCONTEXT CIM**</span><span class="sxs-lookup"><span data-stu-id="e5b08-267">**CIM\_DependencyContext**</span></span>](cim-dependencycontext.md)
</dt> <dd>

<span data-ttu-id="e5b08-268">La relazione [**CIM \_ DependencyContext**](cim-dependencycontext.md) associa una classe di [**\_ dipendenza CIM**](cim-dependency.md) a uno o più oggetti di [**\_ configurazione CIM**](cim-configuration.md) .</span><span class="sxs-lookup"><span data-stu-id="e5b08-268">The [**CIM\_DependencyContext**](cim-dependencycontext.md) relationship associates a [**CIM\_Dependency**](cim-dependency.md) class with one or more [**CIM\_Configuration**](cim-configuration.md) objects.</span></span> <span data-ttu-id="e5b08-269">Le dipendenze di un sistema di computer, ad esempio, possono variare in base alla rete a cui è collegato il sistema.</span><span class="sxs-lookup"><span data-stu-id="e5b08-269">For example, a computer system's dependencies can change based on the network to which the system is attached.</span></span>

</dd> <dt>

[<span data-ttu-id="e5b08-270">**\_DESKTOPMONITOR CIM**</span><span class="sxs-lookup"><span data-stu-id="e5b08-270">**CIM\_DesktopMonitor**</span></span>](cim-desktopmonitor.md)
</dt> <dd>

<span data-ttu-id="e5b08-271">La classe [**CIM \_ DesktopMonitor**](cim-desktopmonitor.md) rappresenta le funzionalità e la gestione del dispositivo logico monitor desktop (CRT).</span><span class="sxs-lookup"><span data-stu-id="e5b08-271">The [**CIM\_DesktopMonitor**](cim-desktopmonitor.md) class represents the capabilities and management of the desktop monitor (CRT) logical device.</span></span>

</dd> <dt>

[<span data-ttu-id="e5b08-272">**\_DEVICEACCESSEDBYFILE CIM**</span><span class="sxs-lookup"><span data-stu-id="e5b08-272">**CIM\_DeviceAccessedByFile**</span></span>](cim-deviceaccessedbyfile.md)
</dt> <dd>

<span data-ttu-id="e5b08-273">La classe di associazione [**CIM \_ DeviceAccessedByFile**](cim-deviceaccessedbyfile.md) specifica il dispositivo logico a cui si accede tramite la classe [**CIM \_ DeviceFile**](cim-devicefile.md) a cui si fa riferimento.</span><span class="sxs-lookup"><span data-stu-id="e5b08-273">The [**CIM\_DeviceAccessedByFile**](cim-deviceaccessedbyfile.md) association class specifies the logical device accessed by using the referenced [**CIM\_DeviceFile**](cim-devicefile.md) class.</span></span>

</dd> <dt>

[<span data-ttu-id="e5b08-274">**\_DEVICECONNECTION CIM**</span><span class="sxs-lookup"><span data-stu-id="e5b08-274">**CIM\_DeviceConnection**</span></span>](cim-deviceconnection.md)
</dt> <dd>

<span data-ttu-id="e5b08-275">La classe di associazione [**CIM \_ DeviceConnection**](cim-deviceconnection.md) rappresenta due o più dispositivi connessi.</span><span class="sxs-lookup"><span data-stu-id="e5b08-275">The [**CIM\_DeviceConnection**](cim-deviceconnection.md) association class represents two or more connected devices.</span></span>

</dd> <dt>

[<span data-ttu-id="e5b08-276">**\_DEVICEERRORCOUNTS CIM**</span><span class="sxs-lookup"><span data-stu-id="e5b08-276">**CIM\_DeviceErrorCounts**</span></span>](cim-deviceerrorcounts.md)
</dt> <dd>

<span data-ttu-id="e5b08-277">La classe [**CIM \_ DeviceErrorCounts**](cim-deviceerrorcounts.md) è una classe statistica che contiene contatori correlati agli errori per un dispositivo logico.</span><span class="sxs-lookup"><span data-stu-id="e5b08-277">The [**CIM\_DeviceErrorCounts**](cim-deviceerrorcounts.md) class is a statistical class that contains error-related counters for a logical device.</span></span> <span data-ttu-id="e5b08-278">I tipi di errore sono definiti da CCITT (REC X. 733) e ISO (IEC 10164-4).</span><span class="sxs-lookup"><span data-stu-id="e5b08-278">The types of errors are defined by CCITT (Rec X.733) and ISO (IEC 10164-4).</span></span>

</dd> <dt>

[<span data-ttu-id="e5b08-279">**\_DEVICEFILE CIM**</span><span class="sxs-lookup"><span data-stu-id="e5b08-279">**CIM\_DeviceFile**</span></span>](cim-devicefile.md)
</dt> <dd>

<span data-ttu-id="e5b08-280">La classe [**CIM \_ DeviceFile**](cim-devicefile.md) rappresenta un tipo di file logico, che rappresenta un dispositivo.</span><span class="sxs-lookup"><span data-stu-id="e5b08-280">The [**CIM\_DeviceFile**](cim-devicefile.md) class represents a type of logical file, which represents a device.</span></span> <span data-ttu-id="e5b08-281">Questa convenzione è utile per i sistemi operativi che gestiscono I dispositivi usando un modello di I/O del flusso di byte.</span><span class="sxs-lookup"><span data-stu-id="e5b08-281">This convention is useful for operating systems that manage devices using a byte stream I/O model.</span></span> <span data-ttu-id="e5b08-282">Il dispositivo logico associato a questo file viene specificato utilizzando la relazione [**CIM \_ DeviceAccessedByFile**](cim-deviceaccessedbyfile.md) .</span><span class="sxs-lookup"><span data-stu-id="e5b08-282">The logical device that is associated with this file is specified using the [**CIM\_DeviceAccessedByFile**](cim-deviceaccessedbyfile.md) relationship.</span></span>

</dd> <dt>

[<span data-ttu-id="e5b08-283">**\_DEVICESAPIMPLEMENTATION CIM**</span><span class="sxs-lookup"><span data-stu-id="e5b08-283">**CIM\_DeviceSAPImplementation**</span></span>](cim-devicesapimplementation.md)
</dt> <dd>

<span data-ttu-id="e5b08-284">La classe [**CIM \_ DeviceSAPImplementation**](cim-devicesapimplementation.md) rappresenta un'associazione tra un punto di accesso al servizio (SAP) e il modo in cui viene implementato.</span><span class="sxs-lookup"><span data-stu-id="e5b08-284">The [**CIM\_DeviceSAPImplementation**](cim-devicesapimplementation.md) class represents an association between a service access point (SAP) and how it is implemented.</span></span> <span data-ttu-id="e5b08-285">Quando molti dispositivi logici sono associati a un SAP, gli elementi operano insieme per fornire il punto di accesso.</span><span class="sxs-lookup"><span data-stu-id="e5b08-285">When many logical devices are associated with one SAP, the elements operate in conjunction to provide the access point.</span></span> <span data-ttu-id="e5b08-286">Se esistono implementazioni diverse di un SAP, ogni implementazione genera singole creazioni di istanze dell'oggetto SAP.</span><span class="sxs-lookup"><span data-stu-id="e5b08-286">If different implementations of a SAP exist, each implementation results in individual instantiations of the SAP object.</span></span>

</dd> <dt>

[<span data-ttu-id="e5b08-287">**\_DEVICESERVICEIMPLEMENTATION CIM**</span><span class="sxs-lookup"><span data-stu-id="e5b08-287">**CIM\_DeviceServiceImplementation**</span></span>](cim-deviceserviceimplementation.md)
</dt> <dd>

<span data-ttu-id="e5b08-288">La classe [**CIM \_ DeviceServiceImplementation**](cim-deviceserviceimplementation.md) rappresenta un'associazione tra un servizio e il modo in cui viene implementata.</span><span class="sxs-lookup"><span data-stu-id="e5b08-288">The [**CIM\_DeviceServiceImplementation**](cim-deviceserviceimplementation.md) class represents an association between a service and how it is implemented.</span></span> <span data-ttu-id="e5b08-289">Quando più dispositivi sono associati a un servizio, gli elementi operano insieme per fornire il servizio.</span><span class="sxs-lookup"><span data-stu-id="e5b08-289">When multiple devices are associated with one service, the elements operate in conjunction to provide the service.</span></span> <span data-ttu-id="e5b08-290">Se esistono implementazioni diverse di un servizio, ogni implementazione produce singole creazioni di istanze dell'oggetto servizio.</span><span class="sxs-lookup"><span data-stu-id="e5b08-290">If different implementations of a service exist, each implementation results in individual instantiations of the service object.</span></span>

</dd> <dt>

[<span data-ttu-id="e5b08-291">**\_DEVICESOFTWARE CIM**</span><span class="sxs-lookup"><span data-stu-id="e5b08-291">**CIM\_DeviceSoftware**</span></span>](cim-devicesoftware.md)
</dt> <dd>

<span data-ttu-id="e5b08-292">La relazione [**CIM \_ DeviceSoftware**](cim-devicesoftware.md) identifica il software associato a un dispositivo, ad esempio i driver, la configurazione o il software dell'applicazione o il firmware.</span><span class="sxs-lookup"><span data-stu-id="e5b08-292">The [**CIM\_DeviceSoftware**](cim-devicesoftware.md) relationship identifies software that is associated with a device, such as drivers, configuration or application software, or firmware.</span></span>

</dd> <dt>

[<span data-ttu-id="e5b08-293">**\_Directory CIM**</span><span class="sxs-lookup"><span data-stu-id="e5b08-293">**CIM\_Directory**</span></span>](cim-directory.md)
</dt> <dd>

<span data-ttu-id="e5b08-294">La classe [**CIM \_ directory**](cim-directory.md) rappresenta un tipo di file che raggruppa logicamente i file di dati che contiene e fornisce informazioni sul percorso per i file raggruppati.</span><span class="sxs-lookup"><span data-stu-id="e5b08-294">The [**CIM\_Directory**](cim-directory.md) class represents a file type that logically groups the data files that it contains and provides path information for the grouped files.</span></span>

</dd> <dt>

[<span data-ttu-id="e5b08-295">**\_DIRECTORYACTION CIM**</span><span class="sxs-lookup"><span data-stu-id="e5b08-295">**CIM\_DirectoryAction**</span></span>](cim-directoryaction.md)
</dt> <dd>

<span data-ttu-id="e5b08-296">La classe [**CIM \_ DirectoryAction**](cim-directoryaction.md) Abstract gestisce le directory.</span><span class="sxs-lookup"><span data-stu-id="e5b08-296">The [**CIM\_DirectoryAction**](cim-directoryaction.md) abstract class manages directories.</span></span> <span data-ttu-id="e5b08-297">La creazione della directory viene gestita dalla classe [**CIM \_ CreateDirectoryAction**](cim-createdirectoryaction.md) e la rimozione della directory viene gestita dalla classe [**CIM \_ RemoveDirectoryAction**](cim-removedirectoryaction.md) .</span><span class="sxs-lookup"><span data-stu-id="e5b08-297">Directory creation is handled by the [**CIM\_CreateDirectoryAction**](cim-createdirectoryaction.md) class and directory removal is handled by the [**CIM\_RemoveDirectoryAction**](cim-removedirectoryaction.md) class.</span></span>

</dd> <dt>

[<span data-ttu-id="e5b08-298">**\_DIRECTORYCONTAINSFILE CIM**</span><span class="sxs-lookup"><span data-stu-id="e5b08-298">**CIM\_DirectoryContainsFile**</span></span>](cim-directorycontainsfile.md)
</dt> <dd>

<span data-ttu-id="e5b08-299">La classe [**CIM \_ DirectoryContainsFile**](cim-directorycontainsfile.md) rappresenta un'associazione tra una directory e i file contenuti all'interno di tale directory.</span><span class="sxs-lookup"><span data-stu-id="e5b08-299">The [**CIM\_DirectoryContainsFile**](cim-directorycontainsfile.md) class represents an association between a directory and files contained within that directory.</span></span>

</dd> <dt>

[<span data-ttu-id="e5b08-300">**\_DIRECTORYSPECIFICATION CIM**</span><span class="sxs-lookup"><span data-stu-id="e5b08-300">**CIM\_DirectorySpecification**</span></span>](cim-directoryspecification.md)
</dt> <dd>

<span data-ttu-id="e5b08-301">La classe [**CIM \_ DirectorySpecification**](cim-directoryspecification.md) acquisisce la struttura di directory principale di un elemento software.</span><span class="sxs-lookup"><span data-stu-id="e5b08-301">The [**CIM\_DirectorySpecification**](cim-directoryspecification.md) class captures the major directory structure of a software element.</span></span> <span data-ttu-id="e5b08-302">Questa classe viene utilizzata per organizzare i file di un elemento software in unità gestibili che possono essere rilocate in un sistema di computer.</span><span class="sxs-lookup"><span data-stu-id="e5b08-302">This class is used to organize the files of a software element into manageable units that can be relocated on a computer system.</span></span>

</dd> <dt>

[<span data-ttu-id="e5b08-303">**\_DIRECTORYSPECIFICATIONFILE CIM**</span><span class="sxs-lookup"><span data-stu-id="e5b08-303">**CIM\_DirectorySpecificationFile**</span></span>](cim-directoryspecificationfile.md)
</dt> <dd>

<span data-ttu-id="e5b08-304">L'associazione [**CIM \_ DirectorySpecificationFile**](cim-directoryspecificationfile.md) rappresenta la directory che contiene il file specificato facendo riferimento alla classe [**CIM \_ DirectorySpecification**](cim-directoryspecification.md) .</span><span class="sxs-lookup"><span data-stu-id="e5b08-304">The [**CIM\_DirectorySpecificationFile**](cim-directoryspecificationfile.md) association represents the directory that contains the file specified by referencing the [**CIM\_DirectorySpecification**](cim-directoryspecification.md) class.</span></span>

</dd> <dt>

[<span data-ttu-id="e5b08-305">**\_DISCRETESENSOR CIM**</span><span class="sxs-lookup"><span data-stu-id="e5b08-305">**CIM\_DiscreteSensor**</span></span>](cim-discretesensor.md)
</dt> <dd>

<span data-ttu-id="e5b08-306">La classe [**CIM \_ DiscreteSensor**](cim-discretesensor.md) presenta un set di valori stringa validi che possono essere segnalati.</span><span class="sxs-lookup"><span data-stu-id="e5b08-306">The [**CIM\_DiscreteSensor**](cim-discretesensor.md) class has a set of legal string values that it can report.</span></span> <span data-ttu-id="e5b08-307">I valori vengono enumerati nella proprietà **PossibleValues** del sensore.</span><span class="sxs-lookup"><span data-stu-id="e5b08-307">The values are enumerated in the sensor's **PossibleValues** property.</span></span> <span data-ttu-id="e5b08-308">Un sensore discreto ha sempre una lettura corrente corrispondente a uno dei valori enumerati.</span><span class="sxs-lookup"><span data-stu-id="e5b08-308">A discrete sensor always has a current reading that corresponds to one of the enumerated values.</span></span>

</dd> <dt>

[<span data-ttu-id="e5b08-309">**\_DiskDrive CIM**</span><span class="sxs-lookup"><span data-stu-id="e5b08-309">**CIM\_DiskDrive**</span></span>](cim-diskdrive.md)
</dt> <dd>

<span data-ttu-id="e5b08-310">La classe [**CIM \_ DiskDrive**](cim-diskdrive.md) rappresenta un'unità disco fisica visualizzata dal sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="e5b08-310">The [**CIM\_DiskDrive**](cim-diskdrive.md) class represents a physical disk drive as seen by the operating system.</span></span> <span data-ttu-id="e5b08-311">Le funzionalità dell'unità disco corrispondono alle caratteristiche logiche e di gestione dell'unità e, in alcuni casi, potrebbero non riflettere le caratteristiche fisiche del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="e5b08-311">The disk drive features correspond to the logical and management characteristics of the drive, and in some cases, may not reflect the physical characteristics of the device.</span></span> <span data-ttu-id="e5b08-312">Un'interfaccia a un'unità fisica è un membro di questa classe.</span><span class="sxs-lookup"><span data-stu-id="e5b08-312">An interface to a physical drive is a member of this class.</span></span> <span data-ttu-id="e5b08-313">Tuttavia, un oggetto basato su un altro dispositivo logico non è un membro di questa classe.</span><span class="sxs-lookup"><span data-stu-id="e5b08-313">However, an object based on another logical device is not a member of this class.</span></span>

</dd> <dt>

[<span data-ttu-id="e5b08-314">**\_DISKETTEDRIVE CIM**</span><span class="sxs-lookup"><span data-stu-id="e5b08-314">**CIM\_DisketteDrive**</span></span>](cim-diskettedrive.md)
</dt> <dd>

<span data-ttu-id="e5b08-315">La classe [**CIM \_ DisketteDrive**](cim-diskettedrive.md) rappresenta le funzionalità e la gestione di un'unità floppy.</span><span class="sxs-lookup"><span data-stu-id="e5b08-315">The [**CIM\_DisketteDrive**](cim-diskettedrive.md) class represents the capabilities and management of a diskette drive.</span></span>

</dd> <dt>

[<span data-ttu-id="e5b08-316">**\_DISKPARTITION CIM**</span><span class="sxs-lookup"><span data-stu-id="e5b08-316">**CIM\_DiskPartition**</span></span>](cim-diskpartition.md)
</dt> <dd>

<span data-ttu-id="e5b08-317">La classe [**CIM \_ DiskPartition**](cim-diskpartition.md) rappresenta un intervallo contiguo di blocchi logici identificabili dal sistema operativo mediante i campi tipo e sottotipo della partizione.</span><span class="sxs-lookup"><span data-stu-id="e5b08-317">The [**CIM\_DiskPartition**](cim-diskpartition.md) class represents a contiguous range of logical blocks that is identifiable by the operating system by way of the partition's type and subtype fields.</span></span> <span data-ttu-id="e5b08-318">Le partizioni disco devono essere realizzate direttamente da supporti fisici (indicati dall'associazione [**CIM \_ RealizesDiskPartition**](cim-realizesdiskpartition.md) ) o basate su volumi di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="e5b08-318">Disk partitions should be directly realized by physical media (indicated by the [**CIM\_RealizesDiskPartition**](cim-realizesdiskpartition.md) association) or built on storage volumes.</span></span>

</dd> <dt>

[<span data-ttu-id="e5b08-319">**\_DISKSPACECHECK CIM**</span><span class="sxs-lookup"><span data-stu-id="e5b08-319">**CIM\_DiskSpaceCheck**</span></span>](cim-diskspacecheck.md)
</dt> <dd>

<span data-ttu-id="e5b08-320">La classe [**CIM \_ DiskSpaceCheck**](cim-diskspacecheck.md) controlla la quantità di spazio disponibile su disco del sistema e la specifica nella proprietà **AvailableDiskSpace** .</span><span class="sxs-lookup"><span data-stu-id="e5b08-320">The [**CIM\_DiskSpaceCheck**](cim-diskspacecheck.md) class checks the system's amount of available disk space and specifies it in the **AvailableDiskSpace** property.</span></span> <span data-ttu-id="e5b08-321">I dettagli vengono confrontati con il valore nella proprietà **AvailableSpace** dell'oggetto [**\_ file System CIM**](cim-filesystem.md) associato all'oggetto [**CIM \_ ComputerSystem**](cim-computersystem.md) , che descrive l'ambiente di sistema.</span><span class="sxs-lookup"><span data-stu-id="e5b08-321">Details are compared with the value in the **AvailableSpace** property of the [**CIM\_FileSystem**](cim-filesystem.md) object that is associated with the [**CIM\_ComputerSystem**](cim-computersystem.md) object, which describes the system environment.</span></span> <span data-ttu-id="e5b08-322">Se il valore della proprietà **AvailableSpace** è maggiore o uguale al valore specificato nella proprietà **AvailableDiskSpace** , la condizione viene soddisfatta.</span><span class="sxs-lookup"><span data-stu-id="e5b08-322">When the value of the **AvailableSpace** property is greater than or equal to the value specified in the **AvailableDiskSpace** property, the condition is satisfied.</span></span>

</dd> <dt>

[<span data-ttu-id="e5b08-323">**\_Visualizzazione CIM**</span><span class="sxs-lookup"><span data-stu-id="e5b08-323">**CIM\_Display**</span></span>](cim-display.md)
</dt> <dd>

<span data-ttu-id="e5b08-324">La classe di [**\_ visualizzazione CIM**](cim-display.md) è una classe padre per il raggruppamento di periferiche di visualizzazione varie.</span><span class="sxs-lookup"><span data-stu-id="e5b08-324">The [**CIM\_Display**](cim-display.md) class is a parent class for grouping miscellaneous display devices.</span></span>

</dd> <dt>

[<span data-ttu-id="e5b08-325">**\_DMA CIM**</span><span class="sxs-lookup"><span data-stu-id="e5b08-325">**CIM\_DMA**</span></span>](cim-dma.md)
</dt> <dd>

<span data-ttu-id="e5b08-326">La classe [**CIM \_ DMA**](cim-dma.md) rappresenta l'accesso diretto alla memoria (DMA) dell'architettura del computer.</span><span class="sxs-lookup"><span data-stu-id="e5b08-326">The [**CIM\_DMA**](cim-dma.md) class represents computer architecture direct memory access (DMA).</span></span>

</dd> <dt>

[<span data-ttu-id="e5b08-327">**CIM \_ ancorato**</span><span class="sxs-lookup"><span data-stu-id="e5b08-327">**CIM\_Docked**</span></span>](cim-docked.md)
</dt> <dd>

<span data-ttu-id="e5b08-328">L'associazione di [**CIM \_ ancorata**](cim-docked.md) rappresenta la relazione tra due chassis.</span><span class="sxs-lookup"><span data-stu-id="e5b08-328">The [**CIM\_Docked**](cim-docked.md) association represents the relationship between two chassis.</span></span> <span data-ttu-id="e5b08-329">Ad esempio, un portatile (un tipo di chassis) può essere ancorato in una stazione di ancoraggio (un altro tipo di chassis).</span><span class="sxs-lookup"><span data-stu-id="e5b08-329">For example, a laptop (a type of chassis) can be docked in a docking station (another type of chassis).</span></span> <span data-ttu-id="e5b08-330">Questa relazione tipica è descritta in modo esplicito.</span><span class="sxs-lookup"><span data-stu-id="e5b08-330">This typical relationship is explicitly described.</span></span>

</dd> <dt>

[<span data-ttu-id="e5b08-331">**\_ELEMENTCAPACITY CIM**</span><span class="sxs-lookup"><span data-stu-id="e5b08-331">**CIM\_ElementCapacity**</span></span>](cim-elementcapacity.md)
</dt> <dd>

<span data-ttu-id="e5b08-332">La classe [**CIM \_ ElementCapacity**](cim-elementcapacity.md) associa un oggetto [**CIM \_ PhysicalCapacity**](cim-physicalcapacity.md) a uno o più elementi fisici.</span><span class="sxs-lookup"><span data-stu-id="e5b08-332">The [**CIM\_ElementCapacity**](cim-elementcapacity.md) class associates a [**CIM\_PhysicalCapacity**](cim-physicalcapacity.md) object with one or more physical elements.</span></span> <span data-ttu-id="e5b08-333">Associa una descrizione dei requisiti hardware (o funzionalità) minimi e massimi agli elementi fisici descritti.</span><span class="sxs-lookup"><span data-stu-id="e5b08-333">It associates a description of the minimum and maximum hardware requirements (or capabilities) to the physical elements being described.</span></span>

</dd> <dt>

[<span data-ttu-id="e5b08-334">**\_ELEMENTCONFIGURATION CIM**</span><span class="sxs-lookup"><span data-stu-id="e5b08-334">**CIM\_ElementConfiguration**</span></span>](cim-elementconfiguration.md)
</dt> <dd>

<span data-ttu-id="e5b08-335">L'associazione [**CIM \_ ElementConfiguration**](cim-elementconfiguration.md) mette in correlazione un oggetto di [**\_ configurazione CIM**](cim-configuration.md) a uno o più elementi di sistema gestiti.</span><span class="sxs-lookup"><span data-stu-id="e5b08-335">The [**CIM\_ElementConfiguration**](cim-elementconfiguration.md) association relates a [**CIM\_Configuration**](cim-configuration.md) object to one or more managed system elements.</span></span> <span data-ttu-id="e5b08-336">L'oggetto di **\_ configurazione CIM** rappresenta un determinato comportamento o uno stato funzionale desiderato per il [**\_ ManagedSystemElement CIM**](cim-managedsystemelement.md)associato.</span><span class="sxs-lookup"><span data-stu-id="e5b08-336">The **CIM\_Configuration** object represents a certain behavior, or a desired functional state for the associated [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

[<span data-ttu-id="e5b08-337">**\_ELEMENTSETTING CIM**</span><span class="sxs-lookup"><span data-stu-id="e5b08-337">**CIM\_ElementSetting**</span></span>](cim-elementsetting.md)
</dt> <dd>

<span data-ttu-id="e5b08-338">La classe [**CIM \_ ElementSetting**](cim-elementsetting.md) rappresenta l'associazione tra gli elementi di sistema gestiti e la classe di impostazione definita.</span><span class="sxs-lookup"><span data-stu-id="e5b08-338">The [**CIM\_ElementSetting**](cim-elementsetting.md) class represents the association between managed system elements and the setting class defined for them.</span></span>

</dd> <dt>

[<span data-ttu-id="e5b08-339">**\_ELEMENTSLINKED CIM**</span><span class="sxs-lookup"><span data-stu-id="e5b08-339">**CIM\_ElementsLinked**</span></span>](cim-elementslinked.md)
</dt> <dd>

<span data-ttu-id="e5b08-340">L'associazione [**CIM \_ ElementsLinked**](cim-elementslinked.md) rappresenta elementi fisici collegati da un collegamento fisico.</span><span class="sxs-lookup"><span data-stu-id="e5b08-340">The [**CIM\_ElementsLinked**](cim-elementslinked.md) association represents physical elements that are cabled together by a physical link.</span></span>

</dd> <dt>

[<span data-ttu-id="e5b08-341">**\_ERRORCOUNTERSFORDEVICE CIM**</span><span class="sxs-lookup"><span data-stu-id="e5b08-341">**CIM\_ErrorCountersForDevice**</span></span>](cim-errorcountersfordevice.md)
</dt> <dd>

<span data-ttu-id="e5b08-342">La classe [**CIM \_ ErrorCountersForDevice**](cim-errorcountersfordevice.md) associa la classe [**CIM \_ DeviceErrorCounts**](cim-deviceerrorcounts.md) al dispositivo logico a cui si applica.</span><span class="sxs-lookup"><span data-stu-id="e5b08-342">The [**CIM\_ErrorCountersForDevice**](cim-errorcountersfordevice.md) class associates the [**CIM\_DeviceErrorCounts**](cim-deviceerrorcounts.md) class to the logical device to which it applies.</span></span>

</dd> <dt>

[<span data-ttu-id="e5b08-343">**\_EXECUTEPROGRAM CIM**</span><span class="sxs-lookup"><span data-stu-id="e5b08-343">**CIM\_ExecuteProgram**</span></span>](cim-executeprogram.md)
</dt> <dd>

<span data-ttu-id="e5b08-344">La classe [**CIM \_ ExecuteProgram**](cim-executeprogram.md) rappresenta i file che possono essere eseguiti nel sistema in cui è installato l'elemento software.</span><span class="sxs-lookup"><span data-stu-id="e5b08-344">The [**CIM\_ExecuteProgram**](cim-executeprogram.md) class represents files that can be executed on the system where the software element is installed.</span></span>

</dd> <dt>

[<span data-ttu-id="e5b08-345">**\_Esportazione CIM**</span><span class="sxs-lookup"><span data-stu-id="e5b08-345">**CIM\_Export**</span></span>](cim-export.md)
</dt> <dd>

<span data-ttu-id="e5b08-346">La classe di [**\_ esportazione CIM**](cim-export.md) rappresenta un'associazione tra un file system locale e le relative directory, che indicano che le directory specificate sono disponibili per il montaggio.</span><span class="sxs-lookup"><span data-stu-id="e5b08-346">The [**CIM\_Export**](cim-export.md) class represents an association between a local file system and its directories, which indicate that the specified directories are available for mount.</span></span> <span data-ttu-id="e5b08-347">Quando si esporta un intero file system, la directory deve fare riferimento alla directory più in alto della file system.</span><span class="sxs-lookup"><span data-stu-id="e5b08-347">When exporting an entire file system, the directory should reference the topmost directory of the file system.</span></span>

</dd> <dt>

[<span data-ttu-id="e5b08-348">**\_EXTRACAPACITYGROUP CIM**</span><span class="sxs-lookup"><span data-stu-id="e5b08-348">**CIM\_ExtraCapacityGroup**</span></span>](cim-extracapacitygroup.md)
</dt> <dd>

<span data-ttu-id="e5b08-349">La classe [**CIM \_ ExtraCapacityGroup**](cim-extracapacitygroup.md) è derivata da un gruppo di ridondanza che indica che gli elementi aggregati hanno una capacità o una capacità superiore a quella necessaria.</span><span class="sxs-lookup"><span data-stu-id="e5b08-349">The [**CIM\_ExtraCapacityGroup**](cim-extracapacitygroup.md) class is derived from a redundancy group that indicates the aggregated elements have more capacity or capability than is needed.</span></span> <span data-ttu-id="e5b08-350">Un esempio di questo tipo di ridondanza è l'installazione di N + 1 alimentatori o ventilatori in un sistema.</span><span class="sxs-lookup"><span data-stu-id="e5b08-350">An example of this type of redundancy is the installation of N+1 power supplies or fans in a system.</span></span>

</dd> <dt>

[<span data-ttu-id="e5b08-351">**\_Ventola CIM**</span><span class="sxs-lookup"><span data-stu-id="e5b08-351">**CIM\_Fan**</span></span>](cim-fan.md)
</dt> <dd>

<span data-ttu-id="e5b08-352">La classe [**CIM \_ fan**](cim-fan.md) rappresenta le funzionalità e la gestione di un dispositivo di raffreddamento ventola.</span><span class="sxs-lookup"><span data-stu-id="e5b08-352">The [**CIM\_Fan**](cim-fan.md) class represents the capabilities and management of a fan cooling device.</span></span>

</dd> <dt>

[<span data-ttu-id="e5b08-353">**Azione filecim \_**</span><span class="sxs-lookup"><span data-stu-id="e5b08-353">**CIM\_FileAction**</span></span>](cim-fileaction.md)
</dt> <dd>

<span data-ttu-id="e5b08-354">La classe [**CIM \_ fileaction**](cim-fileaction.md) consente all'autore di individuare i file già esistenti nel computer di un utente, quindi spostare o copiare tali file in una nuova posizione.</span><span class="sxs-lookup"><span data-stu-id="e5b08-354">The [**CIM\_FileAction**](cim-fileaction.md) class allows the author to locate files that already exist on a user's computer, and then move or copy those files to a new location.</span></span>

</dd> <dt>

[<span data-ttu-id="e5b08-355">**Specifica del filecim \_**</span><span class="sxs-lookup"><span data-stu-id="e5b08-355">**CIM\_FileSpecification**</span></span>](cim-filespecification.md)
</dt> <dd>

<span data-ttu-id="e5b08-356">La classe [**CIM \_ filespecification**](cim-filespecification.md) rappresenta un file che si trova in una posizione di sistema.</span><span class="sxs-lookup"><span data-stu-id="e5b08-356">The [**CIM\_FileSpecification**](cim-filespecification.md) class represents a file that is either on or off of the system.</span></span> <span data-ttu-id="e5b08-357">Il file si trova nella directory identificata dall'associazione [**CIM \_ DirectorySpecificationFile**](cim-directoryspecificationfile.md) .</span><span class="sxs-lookup"><span data-stu-id="e5b08-357">The file is located in the directory identified by the [**CIM\_DirectorySpecificationFile**](cim-directoryspecificationfile.md) association.</span></span> <span data-ttu-id="e5b08-358">Il metodo [**Invoke**](invoke-method-in-class-cim-filespecification.md) usa le informazioni per verificare l'esistenza del file.</span><span class="sxs-lookup"><span data-stu-id="e5b08-358">The [**Invoke**](invoke-method-in-class-cim-filespecification.md) method uses the information to check for the file's existence.</span></span> <span data-ttu-id="e5b08-359">Si noti che le proprietà con un valore **null** non vengono controllate.</span><span class="sxs-lookup"><span data-stu-id="e5b08-359">Note that properties with a **Null** value are not checked.</span></span>

</dd> <dt>

[<span data-ttu-id="e5b08-360">**Filestorage CIM \_**</span><span class="sxs-lookup"><span data-stu-id="e5b08-360">**CIM\_FileStorage**</span></span>](cim-filestorage.md)
</dt> <dd>

<span data-ttu-id="e5b08-361">L'associazione [**CIM \_ filestorage**](cim-filestorage.md) collega i file System e i file logici risolti tramite l'file System.</span><span class="sxs-lookup"><span data-stu-id="e5b08-361">The [**CIM\_FileStorage**](cim-filestorage.md) association links the file system and the logical files addressed through the file system.</span></span>

</dd> <dt>

[<span data-ttu-id="e5b08-362">**\_File System CIM**</span><span class="sxs-lookup"><span data-stu-id="e5b08-362">**CIM\_FileSystem**</span></span>](cim-filesystem.md)
</dt> <dd>

<span data-ttu-id="e5b08-363">La classe [**CIM \_ filesystem**](cim-filesystem.md) rappresenta un file o un set di dati locale in un sistema di computer o montato in modalità remota da un file server.</span><span class="sxs-lookup"><span data-stu-id="e5b08-363">The [**CIM\_FileSystem**](cim-filesystem.md) class represents a file or data set local to a computer system or remotely mounted from a file server.</span></span>

</dd> <dt>

[<span data-ttu-id="e5b08-364">**\_Piatto CIM**</span><span class="sxs-lookup"><span data-stu-id="e5b08-364">**CIM\_FlatPanel**</span></span>](cim-flatpanel.md)
</dt> <dd>

<span data-ttu-id="e5b08-365">La classe [**CIM \_ piatto**](cim-flatpanel.md) rappresenta le funzionalità e la gestione del dispositivo logico del pannello flat.</span><span class="sxs-lookup"><span data-stu-id="e5b08-365">The [**CIM\_FlatPanel**](cim-flatpanel.md) class represents the capabilities and management of the flat panel logical device.</span></span>

</dd> <dt>

[<span data-ttu-id="e5b08-366">**\_FROMDIRECTORYACTION CIM**</span><span class="sxs-lookup"><span data-stu-id="e5b08-366">**CIM\_FromDirectoryAction**</span></span>](cim-fromdirectoryaction.md)
</dt> <dd>

<span data-ttu-id="e5b08-367">L'associazione [**CIM \_ FromDirectoryAction**](cim-fromdirectoryaction.md) identifica la directory di origine per l'azione del file.</span><span class="sxs-lookup"><span data-stu-id="e5b08-367">The [**CIM\_FromDirectoryAction**](cim-fromdirectoryaction.md) association identifies the source directory for the file action.</span></span> <span data-ttu-id="e5b08-368">Quando si utilizza questa associazione, si presuppone che la directory di origine sia stata creata da un'azione precedente.</span><span class="sxs-lookup"><span data-stu-id="e5b08-368">When this association is used, the assumption is that the source directory was created by a previous action.</span></span> <span data-ttu-id="e5b08-369">Questa associazione non può esistere con un'associazione [**CIM \_ FromDirectorySpecification**](cim-fromdirectoryspecification.md) ; un'azione file può coinvolgere solo una singola directory di origine.</span><span class="sxs-lookup"><span data-stu-id="e5b08-369">This association cannot exist with a [**CIM\_FromDirectorySpecification**](cim-fromdirectoryspecification.md) association; a file action can only involve a single source directory.</span></span>

</dd> <dt>

[<span data-ttu-id="e5b08-370">**\_FROMDIRECTORYSPECIFICATION CIM**</span><span class="sxs-lookup"><span data-stu-id="e5b08-370">**CIM\_FromDirectorySpecification**</span></span>](cim-fromdirectoryspecification.md)
</dt> <dd>

<span data-ttu-id="e5b08-371">L'associazione [**CIM \_ FromDirectorySpecification**](cim-fromdirectoryspecification.md) identifica la directory di origine per l'azione del file.</span><span class="sxs-lookup"><span data-stu-id="e5b08-371">The [**CIM\_FromDirectorySpecification**](cim-fromdirectoryspecification.md) association identifies the source directory for the file action.</span></span> <span data-ttu-id="e5b08-372">Quando si utilizza questa associazione, il presupposto è che la directory di origine esista già.</span><span class="sxs-lookup"><span data-stu-id="e5b08-372">When this association is used, the assumption is that the source directory already exists.</span></span> <span data-ttu-id="e5b08-373">Questa associazione non può esistere con un'associazione [**CIM \_ FromDirectoryAction**](cim-fromdirectoryaction.md) ; un'azione file può coinvolgere solo una singola directory di origine.</span><span class="sxs-lookup"><span data-stu-id="e5b08-373">This association cannot exist with a [**CIM\_FromDirectoryAction**](cim-fromdirectoryaction.md) association; a file action can only involve a single source directory.</span></span>

</dd> <dt>

[<span data-ttu-id="e5b08-374">**\_FRU CIM**</span><span class="sxs-lookup"><span data-stu-id="e5b08-374">**CIM\_FRU**</span></span>](cim-fru.md)
</dt> <dd>

<span data-ttu-id="e5b08-375">La classe [**CIM \_ FRU**](cim-fru.md) rappresenta una raccolta definita dal fornitore di prodotti ed elementi fisici associati a un'unità sostituibile sul campo (FRU) per supportare, gestire o aggiornare un prodotto nella posizione del cliente.</span><span class="sxs-lookup"><span data-stu-id="e5b08-375">The [**CIM\_FRU**](cim-fru.md) class represents a vendor-defined collection of products and physical elements that are associated with a field replaceable unit (FRU) to support, maintain, or upgrade a product at the customer's location.</span></span>

</dd> <dt>

[<span data-ttu-id="e5b08-376">**\_FRUINCLUDESPRODUCT CIM**</span><span class="sxs-lookup"><span data-stu-id="e5b08-376">**CIM\_FRUIncludesProduct**</span></span>](cim-fruincludesproduct.md)
</dt> <dd>

<span data-ttu-id="e5b08-377">La classe [**CIM \_ FRUIncludesProduct**](cim-fruincludesproduct.md) indica che un'unità sostituibile sul campo (FRU) può essere costituita da altri prodotti.</span><span class="sxs-lookup"><span data-stu-id="e5b08-377">The [**CIM\_FRUIncludesProduct**](cim-fruincludesproduct.md) class indicates that a field replaceable unit (FRU) may be composed of other products.</span></span>

</dd> <dt>

[<span data-ttu-id="e5b08-378">**\_FRUPHYSICALELEMENTS CIM**</span><span class="sxs-lookup"><span data-stu-id="e5b08-378">**CIM\_FRUPhysicalElements**</span></span>](cim-fruphysicalelements.md)
</dt> <dd>

<span data-ttu-id="e5b08-379">La classe [**CIM \_ FRUPhysicalElements**](cim-fruphysicalelements.md) rappresenta gli elementi fisici che costituiscono un'unità sostituibile sul campo (FRU).</span><span class="sxs-lookup"><span data-stu-id="e5b08-379">The [**CIM\_FRUPhysicalElements**](cim-fruphysicalelements.md) class represents the physical elements that make up a field replaceable unit (FRU).</span></span>

</dd> <dt>

[<span data-ttu-id="e5b08-380">**\_HEATPIPE CIM**</span><span class="sxs-lookup"><span data-stu-id="e5b08-380">**CIM\_HeatPipe**</span></span>](cim-heatpipe.md)
</dt> <dd>

<span data-ttu-id="e5b08-381">La classe [**CIM \_ HeatPipe**](cim-heatpipe.md) rappresenta le funzionalità e la gestione di un dispositivo di raffreddamento con pipe di calore.</span><span class="sxs-lookup"><span data-stu-id="e5b08-381">The [**CIM\_HeatPipe**](cim-heatpipe.md) class represents the capabilities and management of a heat pipe cooling device.</span></span>

</dd> <dt>

[<span data-ttu-id="e5b08-382">**\_HOSTEDACCESSPOINT CIM**</span><span class="sxs-lookup"><span data-stu-id="e5b08-382">**CIM\_HostedAccessPoint**</span></span>](cim-hostedaccesspoint.md)
</dt> <dd>

<span data-ttu-id="e5b08-383">La classe [**CIM \_ HostedAccessPoint**](cim-hostedaccesspoint.md) rappresenta un'associazione tra un punto di accesso al servizio (SAP) e il sistema in cui viene fornito.</span><span class="sxs-lookup"><span data-stu-id="e5b08-383">The [**CIM\_HostedAccessPoint**](cim-hostedaccesspoint.md) class represents an association between a service access point (SAP) and the system on which it is provided.</span></span> <span data-ttu-id="e5b08-384">Ogni sistema può ospitare molti SAP.</span><span class="sxs-lookup"><span data-stu-id="e5b08-384">Each system may host many SAPs.</span></span>

</dd> <dt>

[<span data-ttu-id="e5b08-385">**\_HOSTEDBOOTSAP CIM**</span><span class="sxs-lookup"><span data-stu-id="e5b08-385">**CIM\_HostedBootSAP**</span></span>](cim-hostedbootsap.md)
</dt> <dd>

<span data-ttu-id="e5b08-386">La classe [**CIM \_ HostedBootSAP**](cim-hostedbootsap.md) definisce il computer del sistema di hosting per una classe [**CIM \_ BootSAP**](cim-bootsap.md) .</span><span class="sxs-lookup"><span data-stu-id="e5b08-386">The [**CIM\_HostedBootSAP**](cim-hostedbootsap.md) class defines the hosting unitary computer system for a [**CIM\_BootSAP**](cim-bootsap.md) class.</span></span> <span data-ttu-id="e5b08-387">Poiché questa relazione è sottoclassata da [**CIM \_ HostedAccessPoint**](cim-hostedaccesspoint.md), eredita lo schema di ambito/denominazione definito per [**CIM \_ serviceAccessPoint**](cim-serviceaccesspoint.md), in cui un punto di accesso rinvia al relativo sistema di hosting.</span><span class="sxs-lookup"><span data-stu-id="e5b08-387">Since this relationship is subclassed from [**CIM\_HostedAccessPoint**](cim-hostedaccesspoint.md), it inherits the scoping/naming scheme defined for [**CIM\_ServiceAccessPoint**](cim-serviceaccesspoint.md), where an access point defers to its hosting system.</span></span> <span data-ttu-id="e5b08-388">In questo caso, **CIM \_ BootSAP** deve rinviare alla relativa classe [**CIM \_ UnitaryComputerSystem**](cim-unitarycomputersystem.md) di hosting.</span><span class="sxs-lookup"><span data-stu-id="e5b08-388">In this case, **CIM\_BootSAP** must defer to its hosting [**CIM\_UnitaryComputerSystem**](cim-unitarycomputersystem.md) class.</span></span>

</dd> <dt>

[<span data-ttu-id="e5b08-389">**\_HOSTEDBOOTSERVICE CIM**</span><span class="sxs-lookup"><span data-stu-id="e5b08-389">**CIM\_HostedBootService**</span></span>](cim-hostedbootservice.md)
</dt> <dd>

<span data-ttu-id="e5b08-390">La classe [**CIM \_ HostedBootService**](cim-hostedbootservice.md) associa un sistema di hosting e un servizio di avvio.</span><span class="sxs-lookup"><span data-stu-id="e5b08-390">The [**CIM\_HostedBootService**](cim-hostedbootservice.md) class associates a hosting system and a boot service.</span></span> <span data-ttu-id="e5b08-391">Poiché questa relazione è sottoclassata da [**CIM \_ servizio ospitato**](cim-hostedservice.md), eredita lo schema di ambito/denominazione definito per il servizio, dove un servizio rinvia al relativo sistema di hosting.</span><span class="sxs-lookup"><span data-stu-id="e5b08-391">Since this relationship is subclassed from [**CIM\_HostedService**](cim-hostedservice.md), it inherits the scoping/naming scheme defined for service, where a service defers to its hosting system.</span></span>

</dd> <dt>

[<span data-ttu-id="e5b08-392">**\_HOSTEDFILESYSTEM CIM**</span><span class="sxs-lookup"><span data-stu-id="e5b08-392">**CIM\_HostedFileSystem**</span></span>](cim-hostedfilesystem.md)
</dt> <dd>

<span data-ttu-id="e5b08-393">L'associazione [**CIM \_ HostedFileSystem**](cim-hostedfilesystem.md) rappresenta un collegamento tra il computer e i file System ospitati nel computer.</span><span class="sxs-lookup"><span data-stu-id="e5b08-393">The [**CIM\_HostedFileSystem**](cim-hostedfilesystem.md) association represents a link between the computer system and the file system hosted on the computer system.</span></span>

</dd> <dt>

[<span data-ttu-id="e5b08-394">**\_HOSTEDJOBDESTINATION CIM**</span><span class="sxs-lookup"><span data-stu-id="e5b08-394">**CIM\_HostedJobDestination**</span></span>](cim-hostedjobdestination.md)
</dt> <dd>

<span data-ttu-id="e5b08-395">La classe [**CIM \_ HostedJobDestination**](cim-hostedjobdestination.md) rappresenta un'associazione tra una destinazione del processo e il sistema in cui risiede.</span><span class="sxs-lookup"><span data-stu-id="e5b08-395">The [**CIM\_HostedJobDestination**](cim-hostedjobdestination.md) class represents an association between a job destination and the system on which it resides.</span></span> <span data-ttu-id="e5b08-396">Un sistema può ospitare numerose code di processi.</span><span class="sxs-lookup"><span data-stu-id="e5b08-396">A system may host many job queues.</span></span> <span data-ttu-id="e5b08-397">Le destinazioni dei processi rinviano al sistema host.</span><span class="sxs-lookup"><span data-stu-id="e5b08-397">Job destinations defer to the hosting system.</span></span>

</dd> <dt>

[<span data-ttu-id="e5b08-398">**\_Servizio ospitato CIM**</span><span class="sxs-lookup"><span data-stu-id="e5b08-398">**CIM\_HostedService**</span></span>](cim-hostedservice.md)
</dt> <dd>

<span data-ttu-id="e5b08-399">La classe [**CIM \_ servizio ospitato**](cim-hostedservice.md) rappresenta un'associazione tra un servizio e il sistema in cui risiede la funzionalità.</span><span class="sxs-lookup"><span data-stu-id="e5b08-399">The [**CIM\_HostedService**](cim-hostedservice.md) class represents an association between a service and the system on which the functionality resides.</span></span> <span data-ttu-id="e5b08-400">Un sistema può ospitare molti servizi, che rinviano al sistema host.</span><span class="sxs-lookup"><span data-stu-id="e5b08-400">A system may host many services, which defer to the hosting system.</span></span> <span data-ttu-id="e5b08-401">Il modello non rappresenta servizi ospitati in più sistemi.</span><span class="sxs-lookup"><span data-stu-id="e5b08-401">The model does not represent services hosted across multiple systems.</span></span>

</dd> <dt>

[<span data-ttu-id="e5b08-402">**\_INFRAREDCONTROLLER CIM**</span><span class="sxs-lookup"><span data-stu-id="e5b08-402">**CIM\_InfraredController**</span></span>](cim-infraredcontroller.md)
</dt> <dd>

<span data-ttu-id="e5b08-403">La classe [**CIM \_ InfraredController**](cim-infraredcontroller.md) rappresenta le funzionalità e la gestione di un controller a infrarossi.</span><span class="sxs-lookup"><span data-stu-id="e5b08-403">The [**CIM\_InfraredController**](cim-infraredcontroller.md) class represents the capabilities and management of an infrared controller.</span></span>

</dd> <dt>

[<span data-ttu-id="e5b08-404">**CIM \_ installato**</span><span class="sxs-lookup"><span data-stu-id="e5b08-404">**CIM\_InstalledOS**</span></span>](cim-installedos.md)
</dt> <dd>

<span data-ttu-id="e5b08-405">La classe di associazione [**CIM \_ installatoos**](cim-installedos.md) rappresenta un collegamento tra il computer e il sistema operativo installato.</span><span class="sxs-lookup"><span data-stu-id="e5b08-405">The [**CIM\_InstalledOS**](cim-installedos.md) association class represents a link between the computer system and the installed operating system.</span></span> <span data-ttu-id="e5b08-406">Un sistema operativo viene installato quando si trova in un ambito di archiviazione del computer (ad esempio, copiato in un'unità disco o scaricato in memoria).</span><span class="sxs-lookup"><span data-stu-id="e5b08-406">An operating system is installed when it is in a computer system's storage extent (for example, copied to a disk drive or downloaded to memory).</span></span>

</dd> <dt>

[<span data-ttu-id="e5b08-407">**\_INSTALLEDSOFTWAREELEMENT CIM**</span><span class="sxs-lookup"><span data-stu-id="e5b08-407">**CIM\_InstalledSoftwareElement**</span></span>](cim-installedsoftwareelement.md)
</dt> <dd>

<span data-ttu-id="e5b08-408">La classe [**CIM \_ InstalledSoftwareElement**](cim-installedsoftwareelement.md) associa un sistema di computer a un elemento software installato.</span><span class="sxs-lookup"><span data-stu-id="e5b08-408">The [**CIM\_InstalledSoftwareElement**](cim-installedsoftwareelement.md) class associates a computer system with an installed software element.</span></span>

</dd> <dt>

[<span data-ttu-id="e5b08-409">**\_IRQ CIM**</span><span class="sxs-lookup"><span data-stu-id="e5b08-409">**CIM\_IRQ**</span></span>](cim-irq.md)
</dt> <dd>

<span data-ttu-id="e5b08-410">La classe [**CIM \_ IRQ**](cim-irq.md) rappresenta un IRQ (Intel Architecture interrupt request line).</span><span class="sxs-lookup"><span data-stu-id="e5b08-410">The [**CIM\_IRQ**](cim-irq.md) class represents an Intel architecture interrupt request line (IRQ).</span></span>

</dd> <dt>

[<span data-ttu-id="e5b08-411">**\_Processo CIM**</span><span class="sxs-lookup"><span data-stu-id="e5b08-411">**CIM\_Job**</span></span>](cim-job.md)
</dt> <dd>

<span data-ttu-id="e5b08-412">La classe del [**\_ processo CIM**](cim-job.md) rappresenta un'unità di lavoro per un sistema, ad esempio un processo di stampa.</span><span class="sxs-lookup"><span data-stu-id="e5b08-412">The [**CIM\_Job**](cim-job.md) class represents a unit of work for a system, such as a print job.</span></span> <span data-ttu-id="e5b08-413">Un processo è diverso da un processo perché è possibile pianificare un processo.</span><span class="sxs-lookup"><span data-stu-id="e5b08-413">A job is distinct from a process because a job can be scheduled.</span></span>

</dd> <dt>

[<span data-ttu-id="e5b08-414">**\_JOBDESTINATION CIM**</span><span class="sxs-lookup"><span data-stu-id="e5b08-414">**CIM\_JobDestination**</span></span>](cim-jobdestination.md)
</dt> <dd>

<span data-ttu-id="e5b08-415">La classe [**CIM \_ JobDestination**](cim-jobdestination.md) rappresenta il punto in cui un processo viene inviato per l'elaborazione.</span><span class="sxs-lookup"><span data-stu-id="e5b08-415">The [**CIM\_JobDestination**](cim-jobdestination.md) class represents where a job is submitted for processing.</span></span> <span data-ttu-id="e5b08-416">Può fare riferimento a una coda che contiene zero o più processi, ad esempio una coda di stampa contenente processi di stampa.</span><span class="sxs-lookup"><span data-stu-id="e5b08-416">It can refer to a queue that contains zero or more jobs, such as a print queue containing print jobs.</span></span> <span data-ttu-id="e5b08-417">Le destinazioni dei processi sono ospitate in sistemi, in modo analogo al modo in cui i servizi sono ospitati nei sistemi.</span><span class="sxs-lookup"><span data-stu-id="e5b08-417">Job destinations are hosted on systems, similar to the way in which services are hosted on systems.</span></span>

</dd> <dt>

[<span data-ttu-id="e5b08-418">**\_JOBDESTINATIONJOBS CIM**</span><span class="sxs-lookup"><span data-stu-id="e5b08-418">**CIM\_JobDestinationJobs**</span></span>](cim-jobdestinationjobs.md)
</dt> <dd>

<span data-ttu-id="e5b08-419">L'associazione [**CIM \_ JobDestinationJobs**](cim-jobdestinationjobs.md) descrive la posizione di invio di un processo per l'elaborazione, ovvero la destinazione del processo.</span><span class="sxs-lookup"><span data-stu-id="e5b08-419">The [**CIM\_JobDestinationJobs**](cim-jobdestinationjobs.md) association describes where a job is submitted for processing (that is, to which job destination).</span></span>

</dd> <dt>

[<span data-ttu-id="e5b08-420">**\_Tastiera CIM**</span><span class="sxs-lookup"><span data-stu-id="e5b08-420">**CIM\_Keyboard**</span></span>](cim-keyboard.md)
</dt> <dd>

<span data-ttu-id="e5b08-421">La classe [**CIM \_ Keyboard**](cim-keyboard.md) rappresenta le funzionalità e la gestione del dispositivo logico da tastiera.</span><span class="sxs-lookup"><span data-stu-id="e5b08-421">The [**CIM\_Keyboard**](cim-keyboard.md) class represents the capabilities and management of the keyboard logical device.</span></span>

</dd> <dt>

[<span data-ttu-id="e5b08-422">**\_LINKHASCONNECTOR CIM**</span><span class="sxs-lookup"><span data-stu-id="e5b08-422">**CIM\_LinkHasConnector**</span></span>](cim-linkhasconnector.md)
</dt> <dd>

<span data-ttu-id="e5b08-423">La classe [**CIM \_ LinkHasConnector**](cim-linkhasconnector.md) associa i cavi e i collegamenti usati come connettori fisici, che connettono gli elementi fisici.</span><span class="sxs-lookup"><span data-stu-id="e5b08-423">The [**CIM\_LinkHasConnector**](cim-linkhasconnector.md) class associates cables and links used as physical connectors, which connect the physical elements.</span></span> <span data-ttu-id="e5b08-424">Questa associazione definisce in modo esplicito la relazione dei connettori per [**CIM \_ PhysicalLink**](cim-physicallink.md).</span><span class="sxs-lookup"><span data-stu-id="e5b08-424">This association explicitly defines the relationship of connectors for [**CIM\_PhysicalLink**](cim-physicallink.md).</span></span>

</dd> <dt>

[<span data-ttu-id="e5b08-425">**\_LOCALFILESYSTEM CIM**</span><span class="sxs-lookup"><span data-stu-id="e5b08-425">**CIM\_LocalFileSystem**</span></span>](cim-localfilesystem.md)
</dt> <dd>

<span data-ttu-id="e5b08-426">La classe [**CIM \_ LocalFileSystem**](cim-localfilesystem.md) rappresenta l'archivio file controllato da un sistema di computer tramite mezzi locali, ad esempio l'accesso diretto ai driver di dispositivo.</span><span class="sxs-lookup"><span data-stu-id="e5b08-426">The [**CIM\_LocalFileSystem**](cim-localfilesystem.md) class represents the file store controlled by a computer system through local means (for example, direct device-driver access).</span></span> <span data-ttu-id="e5b08-427">L'archivio file può essere gestito direttamente dal computer, senza la necessità che un altro computer funga da file server.</span><span class="sxs-lookup"><span data-stu-id="e5b08-427">The file store can be managed directly by the computer system, without the need for another computer to act as a file server.</span></span> <span data-ttu-id="e5b08-428">Per un file system cluster, tuttavia, il file system è locale e, di conseguenza, rinvia al cluster.</span><span class="sxs-lookup"><span data-stu-id="e5b08-428">For a clustered file system, however, the file system is local and, therefore, defers to the cluster.</span></span>

</dd> <dt>

[<span data-ttu-id="e5b08-429">**\_Percorso CIM**</span><span class="sxs-lookup"><span data-stu-id="e5b08-429">**CIM\_Location**</span></span>](cim-location.md)
</dt> <dd>

<span data-ttu-id="e5b08-430">La classe del [**\_ percorso CIM**](cim-location.md) rappresenta la posizione e l'indirizzo di un elemento fisico.</span><span class="sxs-lookup"><span data-stu-id="e5b08-430">The [**CIM\_Location**](cim-location.md) class represents the position and address of a physical element.</span></span>

</dd> <dt>

[<span data-ttu-id="e5b08-431">**\_LOGICALDEVICE CIM**</span><span class="sxs-lookup"><span data-stu-id="e5b08-431">**CIM\_LogicalDevice**</span></span>](cim-logicaldevice.md)
</dt> <dd>

<span data-ttu-id="e5b08-432">La classe [**CIM \_ LogicalDevice**](cim-logicaldevice.md) rappresenta un'entità hardware che può essere o meno realizzata nell'hardware fisico.</span><span class="sxs-lookup"><span data-stu-id="e5b08-432">The [**CIM\_LogicalDevice**](cim-logicaldevice.md) class represents a hardware entity that may or may not be realized in physical hardware.</span></span>

</dd> <dt>

[<span data-ttu-id="e5b08-433">**\_Disco logico CIM**</span><span class="sxs-lookup"><span data-stu-id="e5b08-433">**CIM\_LogicalDisk**</span></span>](cim-logicaldisk.md)
</dt> <dd>

<span data-ttu-id="e5b08-434">La classe [**CIM \_ disco logico**](cim-logicaldisk.md) rappresenta un intervallo contiguo di blocchi logici identificabili da un file System tramite il campo **DeviceID** (Key) del disco.</span><span class="sxs-lookup"><span data-stu-id="e5b08-434">The [**CIM\_LogicalDisk**](cim-logicaldisk.md) class represents a contiguous range of logical blocks that is identifiable by a file system through the disk's **DeviceID** (key) field.</span></span> <span data-ttu-id="e5b08-435">Ad esempio, in un ambiente Windows, il campo **DeviceID** contiene una lettera di unità; in un ambiente UNIX, contiene il percorso di accesso; e in un ambiente NetWare contiene il nome del volume.</span><span class="sxs-lookup"><span data-stu-id="e5b08-435">For example, in a Windows environment, the **DeviceID** field contains a drive letter; in a UNIX environment, it contains the access path; and in a NetWare environment, it contains the volume name.</span></span>

</dd> <dt>

[<span data-ttu-id="e5b08-436">**\_LOGICALDISKBASEDONPARTITION CIM**</span><span class="sxs-lookup"><span data-stu-id="e5b08-436">**CIM\_LogicalDiskBasedOnPartition**</span></span>](cim-logicaldiskbasedonpartition.md)
</dt> <dd>

<span data-ttu-id="e5b08-437">La classe [**CIM \_ LogicalDiskBasedOnPartition**](cim-logicaldiskbasedonpartition.md) associa un disco logico con la partizione del disco in cui risiede.</span><span class="sxs-lookup"><span data-stu-id="e5b08-437">The [**CIM\_LogicalDiskBasedOnPartition**](cim-logicaldiskbasedonpartition.md) class associates a logical disk with the disk partition on which it resides.</span></span>

</dd> <dt>

[<span data-ttu-id="e5b08-438">**\_LOGICALDISKBASEDONVOLUMESET CIM**</span><span class="sxs-lookup"><span data-stu-id="e5b08-438">**CIM\_LogicalDiskBasedOnVolumeSet**</span></span>](cim-logicaldiskbasedonvolumeset.md)
</dt> <dd>

<span data-ttu-id="e5b08-439">L'associazione [**CIM \_ LogicalDiskBasedOnVolumeSet**](cim-logicaldiskbasedonvolumeset.md) mette in relazione i dischi logici con il volume in cui sono stati trovati.</span><span class="sxs-lookup"><span data-stu-id="e5b08-439">The [**CIM\_LogicalDiskBasedOnVolumeSet**](cim-logicaldiskbasedonvolumeset.md) association relates logical disks with the volume on which they are found.</span></span> <span data-ttu-id="e5b08-440">I dischi logici possono essere basati su un singolo volume, ad esempio esposto da un responsabile del volume software, o una partizione disco.</span><span class="sxs-lookup"><span data-stu-id="e5b08-440">Logical disks can be based on a single volume (for example, exposed by a software volume manager) or a disk partition.</span></span>

</dd> <dt>

[<span data-ttu-id="e5b08-441">**\_LogicalElement CIM**</span><span class="sxs-lookup"><span data-stu-id="e5b08-441">**CIM\_LogicalElement**</span></span>](cim-logicalelement.md)
</dt> <dd>

<span data-ttu-id="e5b08-442">La classe [**CIM \_ LogicalElement**](cim-logicalelement.md) è la classe di base per tutti i componenti di sistema che rappresentano componenti di sistema astratti, ad esempio profili, processi o funzionalità del sistema, sotto forma di dispositivi logici.</span><span class="sxs-lookup"><span data-stu-id="e5b08-442">The [**CIM\_LogicalElement**](cim-logicalelement.md) class is the base class for all system components that represent abstract system components, such as profiles, processes, or system capabilities, in the form of logical devices.</span></span>

</dd> <dt>

[<span data-ttu-id="e5b08-443">**\_LOGICALFILE CIM**</span><span class="sxs-lookup"><span data-stu-id="e5b08-443">**CIM\_LogicalFile**</span></span>](cim-logicalfile.md)
</dt> <dd>

<span data-ttu-id="e5b08-444">La classe [**CIM \_ LogicalFile**](cim-logicalfile.md) rappresenta una raccolta denominata di dati, che può essere un codice eseguibile, che si trova in un file System in un extent di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="e5b08-444">The [**CIM\_LogicalFile**](cim-logicalfile.md) class represents a named collection of data, which can be executable code, that is located in a file system on a storage extent.</span></span>

</dd> <dt>

[<span data-ttu-id="e5b08-445">**\_LOGICALIDENTITY CIM**</span><span class="sxs-lookup"><span data-stu-id="e5b08-445">**CIM\_LogicalIdentity**</span></span>](cim-logicalidentity.md)
</dt> <dd>

<span data-ttu-id="e5b08-446">La classe [**CIM \_ LogicalIdentity**](cim-logicalidentity.md) è un'associazione astratta e generica che indica che due elementi logici rappresentano aspetti diversi della stessa entità sottostante.</span><span class="sxs-lookup"><span data-stu-id="e5b08-446">The [**CIM\_LogicalIdentity**](cim-logicalidentity.md) class is an abstract and generic association that indicates that two logical elements represent different aspects of the same underlying entity.</span></span>

</dd> <dt>

[<span data-ttu-id="e5b08-447">**\_MAGNETOOPTICALDRIVE CIM**</span><span class="sxs-lookup"><span data-stu-id="e5b08-447">**CIM\_MagnetoOpticalDrive**</span></span>](cim-magnetoopticaldrive.md)
</dt> <dd>

<span data-ttu-id="e5b08-448">La classe [**CIM \_ MagnetoOpticalDrive**](cim-magnetoopticaldrive.md) rappresenta le funzionalità e la gestione di un'unità magneto-ottico, un sottotipo del dispositivo di accesso multimediale.</span><span class="sxs-lookup"><span data-stu-id="e5b08-448">The [**CIM\_MagnetoOpticalDrive**](cim-magnetoopticaldrive.md) class represents the capabilities and management of a magneto-optical drive, a subtype of the media access device.</span></span>

</dd> <dt>

[<span data-ttu-id="e5b08-449">**\_MANAGEDSYSTEMELEMENT CIM**</span><span class="sxs-lookup"><span data-stu-id="e5b08-449">**CIM\_ManagedSystemElement**</span></span>](cim-managedsystemelement.md)
</dt> <dd>

<span data-ttu-id="e5b08-450">La classe [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md) è la classe di base per la gerarchia degli elementi di sistema.</span><span class="sxs-lookup"><span data-stu-id="e5b08-450">The [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md) class is the base class for the system element hierarchy.</span></span> <span data-ttu-id="e5b08-451">Qualsiasi componente di sistema distinguibile è un candidato per l'inclusione in questa classe.</span><span class="sxs-lookup"><span data-stu-id="e5b08-451">Any distinguishable system component is a candidate for inclusion in this class.</span></span>

</dd> <dt>

[<span data-ttu-id="e5b08-452">**\_MANAGEMENTCONTROLLER CIM**</span><span class="sxs-lookup"><span data-stu-id="e5b08-452">**CIM\_ManagementController**</span></span>](cim-managementcontroller.md)
</dt> <dd>

<span data-ttu-id="e5b08-453">La classe [**CIM \_ ManagementController**](cim-managementcontroller.md) è correlata alle funzionalità e alla gestione di un controller di gestione.</span><span class="sxs-lookup"><span data-stu-id="e5b08-453">The [**CIM\_ManagementController**](cim-managementcontroller.md) class relates to the capabilities and management of a management controller.</span></span>

</dd> <dt>

[<span data-ttu-id="e5b08-454">**\_MEDIAACCESSDEVICE CIM**</span><span class="sxs-lookup"><span data-stu-id="e5b08-454">**CIM\_MediaAccessDevice**</span></span>](cim-mediaaccessdevice.md)
</dt> <dd>

<span data-ttu-id="e5b08-455">La classe [**CIM \_ MediaAccessDevice**](cim-mediaaccessdevice.md) rappresenta la possibilità di accedere a uno o più supporti e quindi di usare il supporto per archiviare e recuperare i dati.</span><span class="sxs-lookup"><span data-stu-id="e5b08-455">The [**CIM\_MediaAccessDevice**](cim-mediaaccessdevice.md) class represents the ability to access one or more media, and then use the media to store and retrieve data.</span></span>

</dd> <dt>

[<span data-ttu-id="e5b08-456">**\_MEDIAPRESENT CIM**</span><span class="sxs-lookup"><span data-stu-id="e5b08-456">**CIM\_MediaPresent**</span></span>](cim-mediapresent.md)
</dt> <dd>

<span data-ttu-id="e5b08-457">L'associazione [**CIM \_ MediaPresent**](cim-mediapresent.md) descrive una relazione in cui è necessario accedere a un extent di archiviazione tramite un dispositivo di accesso multimediale.</span><span class="sxs-lookup"><span data-stu-id="e5b08-457">The [**CIM\_MediaPresent**](cim-mediapresent.md) association describes a relationship where a storage extent must be accessed through a media access device.</span></span>

</dd> <dt>

[<span data-ttu-id="e5b08-458">**\_Memoria CIM**</span><span class="sxs-lookup"><span data-stu-id="e5b08-458">**CIM\_Memory**</span></span>](cim-memory.md)
</dt> <dd>

<span data-ttu-id="e5b08-459">La classe [**CIM \_ Memory**](cim-memory.md) rappresenta le funzionalità e la gestione dei dispositivi logici correlati alla memoria.</span><span class="sxs-lookup"><span data-stu-id="e5b08-459">The [**CIM\_Memory**](cim-memory.md) class represents the capabilities and management of memory-related logical devices.</span></span>

</dd> <dt>

[<span data-ttu-id="e5b08-460">**\_MEMORYCAPACITY CIM**</span><span class="sxs-lookup"><span data-stu-id="e5b08-460">**CIM\_MemoryCapacity**</span></span>](cim-memorycapacity.md)
</dt> <dd>

<span data-ttu-id="e5b08-461">La classe [**CIM \_ MemoryCapacity**](cim-memorycapacity.md) rappresenta la memoria che può essere installata su un elemento fisico e le configurazioni minime e massime.</span><span class="sxs-lookup"><span data-stu-id="e5b08-461">The [**CIM\_MemoryCapacity**](cim-memorycapacity.md) class represents memory that can be installed on a physical element and its minimum and maximum configurations.</span></span> <span data-ttu-id="e5b08-462">Le informazioni sulla memoria attualmente installata e i requisiti minimi e massimi di un elemento si trovano nelle istanze della classe [**CIM \_ PhysicalMemory**](cim-physicalmemory.md) .</span><span class="sxs-lookup"><span data-stu-id="e5b08-462">Information on memory that is currently installed and an element's minimum and maximum requirements is located in instances of the [**CIM\_PhysicalMemory**](cim-physicalmemory.md) class.</span></span>

</dd> <dt>

[<span data-ttu-id="e5b08-463">**\_MEMORYCHECK CIM**</span><span class="sxs-lookup"><span data-stu-id="e5b08-463">**CIM\_MemoryCheck**</span></span>](cim-memorycheck.md)
</dt> <dd>

<span data-ttu-id="e5b08-464">La classe [**CIM \_ MemoryCheck**](cim-memorycheck.md) specifica una condizione per la quantità minima di memoria che deve essere disponibile in un sistema.</span><span class="sxs-lookup"><span data-stu-id="e5b08-464">The [**CIM\_MemoryCheck**](cim-memorycheck.md) class specifies a condition for the minimum amount of memory that must be available on a system.</span></span>

</dd> <dt>

[<span data-ttu-id="e5b08-465">**\_MEMORYMAPPEDIO CIM**</span><span class="sxs-lookup"><span data-stu-id="e5b08-465">**CIM\_MemoryMappedIO**</span></span>](cim-memorymappedio.md)
</dt> <dd>

<span data-ttu-id="e5b08-466">La classe [**CIM \_ MemoryMappedIO**](cim-memorymappedio.md) rappresenta l'I/O mappato alla memoria dell'architettura del computer.</span><span class="sxs-lookup"><span data-stu-id="e5b08-466">The [**CIM\_MemoryMappedIO**](cim-memorymappedio.md) class represents computer architecture memory-mapped I/O.</span></span> <span data-ttu-id="e5b08-467">Questa classe indirizza le risorse di memoria e di I/O della porta.</span><span class="sxs-lookup"><span data-stu-id="e5b08-467">This class addresses memory and port I/O resources.</span></span>

</dd> <dt>

[<span data-ttu-id="e5b08-468">**\_MEMORYONCARD CIM**</span><span class="sxs-lookup"><span data-stu-id="e5b08-468">**CIM\_MemoryOnCard**</span></span>](cim-memoryoncard.md)
</dt> <dd>

<span data-ttu-id="e5b08-469">La classe [**CIM \_ MemoryOnCard**](cim-memoryoncard.md) associa la memoria fisica che si trova sulle lavagne di hosting, schede scheda e così via.</span><span class="sxs-lookup"><span data-stu-id="e5b08-469">The [**CIM\_MemoryOnCard**](cim-memoryoncard.md) class associates physical memory located on hosting boards, adapter cards, and so on.</span></span> <span data-ttu-id="e5b08-470">Questa associazione definisce in modo esplicito la relazione di memoria con le schede.</span><span class="sxs-lookup"><span data-stu-id="e5b08-470">This association explicitly defines the relationship of memory to cards.</span></span>

</dd> <dt>

[<span data-ttu-id="e5b08-471">**\_MEMORYWITHMEDIA CIM**</span><span class="sxs-lookup"><span data-stu-id="e5b08-471">**CIM\_MemoryWithMedia**</span></span>](cim-memorywithmedia.md)
</dt> <dd>

<span data-ttu-id="e5b08-472">La classe [**CIM \_ MemoryWithMedia**](cim-memorywithmedia.md) associa la memoria fisica a un supporto fisico e alla relativa cartuccia.</span><span class="sxs-lookup"><span data-stu-id="e5b08-472">The [**CIM\_MemoryWithMedia**](cim-memorywithmedia.md) class associates physical memory with a physical media and its cartridge.</span></span> <span data-ttu-id="e5b08-473">La memoria fornisce l'identificazione dei supporti e archivia i dati specifici dell'utente.</span><span class="sxs-lookup"><span data-stu-id="e5b08-473">The memory provides media identification and stores user-specific data.</span></span>

</dd> <dt>

[<span data-ttu-id="e5b08-474">**\_MODIFYSETTINGACTION CIM**</span><span class="sxs-lookup"><span data-stu-id="e5b08-474">**CIM\_ModifySettingAction**</span></span>](cim-modifysettingaction.md)
</dt> <dd>

<span data-ttu-id="e5b08-475">La classe [**CIM \_ ModifySettingAction**](cim-modifysettingaction.md) rappresenta le informazioni per la modifica di un file di impostazioni specifico, per una voce specifica, con un valore specifico.</span><span class="sxs-lookup"><span data-stu-id="e5b08-475">The [**CIM\_ModifySettingAction**](cim-modifysettingaction.md) class represents the information for modifying a specific setting file, for a specific entry, with a specific value.</span></span>

</dd> <dt>

[<span data-ttu-id="e5b08-476">**\_MONITORRESOLUTION CIM**</span><span class="sxs-lookup"><span data-stu-id="e5b08-476">**CIM\_MonitorResolution**</span></span>](cim-monitorresolution.md)
</dt> <dd>

<span data-ttu-id="e5b08-477">La classe [**CIM \_ MonitorResolution**](cim-monitorresolution.md) rappresenta la relazione tra risoluzioni orizzontali e verticali e la frequenza di aggiornamento e la modalità di analisi per un monitor desktop.</span><span class="sxs-lookup"><span data-stu-id="e5b08-477">The [**CIM\_MonitorResolution**](cim-monitorresolution.md) class represents the relationship between horizontal and vertical resolutions and the refresh rate and scan mode for a desktop monitor.</span></span> <span data-ttu-id="e5b08-478">I valori vengono specificati nell'oggetto controller video.</span><span class="sxs-lookup"><span data-stu-id="e5b08-478">Values are specified in the video controller object.</span></span>

</dd> <dt>

[<span data-ttu-id="e5b08-479">**\_MONITORSETTING CIM**</span><span class="sxs-lookup"><span data-stu-id="e5b08-479">**CIM\_MonitorSetting**</span></span>](cim-monitorsetting.md)
</dt> <dd>

<span data-ttu-id="e5b08-480">La classe [**CIM \_ MonitorSetting**](cim-monitorsetting.md) associa la risoluzione del monitoraggio al monitor desktop a cui si applica.</span><span class="sxs-lookup"><span data-stu-id="e5b08-480">The [**CIM\_MonitorSetting**](cim-monitorsetting.md) class associates the monitor resolution with the desktop monitor to which it applies.</span></span>

</dd> <dt>

[<span data-ttu-id="e5b08-481">**\_Montaggio CIM**</span><span class="sxs-lookup"><span data-stu-id="e5b08-481">**CIM\_Mount**</span></span>](cim-mount.md)
</dt> <dd>

<span data-ttu-id="e5b08-482">La classe di [**\_ montaggio CIM**](cim-mount.md) rappresenta un'associazione tra un file System e una directory a cui è collegata.</span><span class="sxs-lookup"><span data-stu-id="e5b08-482">The [**CIM\_Mount**](cim-mount.md) class represents an association between a file system and a directory to which it is attached.</span></span>

</dd> <dt>

[<span data-ttu-id="e5b08-483">**\_MULTISTATESENSOR CIM**</span><span class="sxs-lookup"><span data-stu-id="e5b08-483">**CIM\_MultiStateSensor**</span></span>](cim-multistatesensor.md)
</dt> <dd>

<span data-ttu-id="e5b08-484">La classe [**CIM \_ MultiStateSensor**](cim-multistatesensor.md) rappresenta un set di sensori binari a più membri in cui ogni sensore binario segnala un risultato booleano.</span><span class="sxs-lookup"><span data-stu-id="e5b08-484">The [**CIM\_MultiStateSensor**](cim-multistatesensor.md) class represents a multi-member set of binary sensors where each binary sensor reports a Boolean result.</span></span>

</dd> <dt>

[<span data-ttu-id="e5b08-485">**\_NETWORKADAPTER CIM**</span><span class="sxs-lookup"><span data-stu-id="e5b08-485">**CIM\_NetworkAdapter**</span></span>](cim-networkadapter.md)
</dt> <dd>

<span data-ttu-id="e5b08-486">La classe [**CIM \_ NetworkAdapter**](cim-networkadapter.md) è una classe astratta che definisce i concetti relativi all'hardware di rete generale, ad esempio l'indirizzo permanente o la velocità dell'operazione.</span><span class="sxs-lookup"><span data-stu-id="e5b08-486">The [**CIM\_NetworkAdapter**](cim-networkadapter.md) class is an abstract class that defines general networking hardware concepts (for example, permanent address or speed of operation).</span></span> <span data-ttu-id="e5b08-487">Le informazioni vengono trasmesse mediante l'associazione [**CIM \_ DeviceSAPImplementation**](cim-devicesapimplementation.md) .</span><span class="sxs-lookup"><span data-stu-id="e5b08-487">The information is conveyed using the [**CIM\_DeviceSAPImplementation**](cim-devicesapimplementation.md) association.</span></span>

</dd> <dt>

[<span data-ttu-id="e5b08-488">**\_NFS CIM**</span><span class="sxs-lookup"><span data-stu-id="e5b08-488">**CIM\_NFS**</span></span>](cim-nfs.md)
</dt> <dd>

<span data-ttu-id="e5b08-489">La classe [**CIM \_ NFS**](cim-nfs.md) rappresenta una file system remota montata usando il protocollo di rete file System (NFS), da un sistema di computer.</span><span class="sxs-lookup"><span data-stu-id="e5b08-489">The [**CIM\_NFS**](cim-nfs.md) class represents a remote file system that is mounted, using the network file system (NFS) protocol, from a computer system.</span></span>

</dd> <dt>

[<span data-ttu-id="e5b08-490">**\_NONVOLATILESTORAGE CIM**</span><span class="sxs-lookup"><span data-stu-id="e5b08-490">**CIM\_NonVolatileStorage**</span></span>](cim-nonvolatilestorage.md)
</dt> <dd>

<span data-ttu-id="e5b08-491">La classe [**CIM \_ NonVolatileStorage**](cim-nonvolatilestorage.md) rappresenta le funzionalità e la gestione di risorse di archiviazione non volatili.</span><span class="sxs-lookup"><span data-stu-id="e5b08-491">The [**CIM\_NonVolatileStorage**](cim-nonvolatilestorage.md) class represents the capabilities and management of non-volatile storage.</span></span> <span data-ttu-id="e5b08-492">La memoria non volatile include in modo nativo archiviazione flash e ROM.</span><span class="sxs-lookup"><span data-stu-id="e5b08-492">Nonvolatile memory natively includes flash and ROM storage.</span></span>

</dd> <dt>

[<span data-ttu-id="e5b08-493">**\_NUMERICSENSOR CIM**</span><span class="sxs-lookup"><span data-stu-id="e5b08-493">**CIM\_NumericSensor**</span></span>](cim-numericsensor.md)
</dt> <dd>

<span data-ttu-id="e5b08-494">La classe [**CIM \_ NumericSensor**](cim-numericsensor.md) rappresenta un sensore numerico che restituisce letture numeriche e, facoltativamente, supporta le impostazioni di soglia.</span><span class="sxs-lookup"><span data-stu-id="e5b08-494">The [**CIM\_NumericSensor**](cim-numericsensor.md) class represents a numeric sensor that returns numeric readings and optionally supports thresholds settings.</span></span>

</dd> <dt>

[<span data-ttu-id="e5b08-495">**\_OPERATINGSYSTEM CIM**</span><span class="sxs-lookup"><span data-stu-id="e5b08-495">**CIM\_OperatingSystem**</span></span>](cim-operatingsystem.md)
</dt> <dd>

<span data-ttu-id="e5b08-496">La classe [**CIM \_ OperatingSystem**](cim-operatingsystem.md) rappresenta un sistema operativo del computer, costituito da software e firmware che rendono utilizzabile l'hardware di un sistema di computer.</span><span class="sxs-lookup"><span data-stu-id="e5b08-496">The [**CIM\_OperatingSystem**](cim-operatingsystem.md) class represents a computer operating system, which is made up of software and firmware that make a computer system's hardware usable.</span></span>

</dd> <dt>

[<span data-ttu-id="e5b08-497">**\_OPERATINGSYSTEMSOFTWAREFEATURE CIM**</span><span class="sxs-lookup"><span data-stu-id="e5b08-497">**CIM\_OperatingSystemSoftwareFeature**</span></span>](cim-operatingsystemsoftwarefeature.md)
</dt> <dd>

<span data-ttu-id="e5b08-498">La classe [**CIM \_ OperatingSystemSoftwareFeature**](cim-operatingsystemsoftwarefeature.md) rappresenta le funzionalità software che costituiscono il sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="e5b08-498">The [**CIM\_OperatingSystemSoftwareFeature**](cim-operatingsystemsoftwarefeature.md) class represents the software features that make up the operating system.</span></span>

</dd> <dt>

[<span data-ttu-id="e5b08-499">**\_OSPROCESS CIM**</span><span class="sxs-lookup"><span data-stu-id="e5b08-499">**CIM\_OSProcess**</span></span>](cim-osprocess.md)
</dt> <dd>

<span data-ttu-id="e5b08-500">La classe [**CIM \_ OSProcess**](cim-osprocess.md) associa il sistema operativo e uno o più processi in esecuzione nel contesto del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="e5b08-500">The [**CIM\_OSProcess**](cim-osprocess.md) class associates the operating system and one or more processes running in the context of the operating system.</span></span>

</dd> <dt>

[<span data-ttu-id="e5b08-501">**\_OSVERSIONCHECK CIM**</span><span class="sxs-lookup"><span data-stu-id="e5b08-501">**CIM\_OSVersionCheck**</span></span>](cim-osversioncheck.md)
</dt> <dd>

<span data-ttu-id="e5b08-502">La classe [**CIM \_ OSVersionCheck**](cim-osversioncheck.md) specifica le versioni del sistema operativo in grado di supportare un elemento software.</span><span class="sxs-lookup"><span data-stu-id="e5b08-502">The [**CIM\_OSVersionCheck**](cim-osversioncheck.md) class specifies the versions of the operating system that can support a software element.</span></span>

</dd> <dt>

[<span data-ttu-id="e5b08-503">**\_PACKAGEALARM CIM**</span><span class="sxs-lookup"><span data-stu-id="e5b08-503">**CIM\_PackageAlarm**</span></span>](cim-packagealarm.md)
</dt> <dd>

<span data-ttu-id="e5b08-504">L'associazione [**CIM \_ PackageAlarm**](/windows/desktop/SecCrypto/extendedproperties-newenum) rappresenta la relazione in cui viene installato un dispositivo di allarme come parte di un pacchetto.</span><span class="sxs-lookup"><span data-stu-id="e5b08-504">The [**CIM\_PackageAlarm**](/windows/desktop/SecCrypto/extendedproperties-newenum) association represents the relationship in which an alarm device is installed as part of a package.</span></span> <span data-ttu-id="e5b08-505">L'installazione indica i problemi con l'ambiente del pacchetto, ovvero il relativo stato di sicurezza o l'integrità generale.</span><span class="sxs-lookup"><span data-stu-id="e5b08-505">The installation indicates issues with the package's environment—its security state or its overall health.</span></span>

</dd> <dt>

[<span data-ttu-id="e5b08-506">**\_PACKAGECOOLING CIM**</span><span class="sxs-lookup"><span data-stu-id="e5b08-506">**CIM\_PackageCooling**</span></span>](cim-packagecooling.md)
</dt> <dd>

<span data-ttu-id="e5b08-507">L'associazione [**CIM \_ PackageCooling**](cim-packagecooling.md) rappresenta la relazione in cui un dispositivo di raffreddamento viene installato in un pacchetto, ad esempio uno chassis o un rack, per facilitare il raffreddamento del pacchetto.</span><span class="sxs-lookup"><span data-stu-id="e5b08-507">The [**CIM\_PackageCooling**](cim-packagecooling.md) association represents the relationship in which a cooling device is installed in a package, such as a chassis or rack, to assist with the package's cooling.</span></span>

</dd> <dt>

[<span data-ttu-id="e5b08-508">**\_PACKAGEDCOMPONENT CIM**</span><span class="sxs-lookup"><span data-stu-id="e5b08-508">**CIM\_PackagedComponent**</span></span>](cim-packagedcomponent.md)
</dt> <dd>

<span data-ttu-id="e5b08-509">L'associazione [**CIM \_ PackagedComponent**](cim-packagedcomponent.md) rappresenta una relazione esplicita in cui un componente è in genere contenuto in un pacchetto fisico, ad esempio uno chassis o una scheda.</span><span class="sxs-lookup"><span data-stu-id="e5b08-509">The [**CIM\_PackagedComponent**](cim-packagedcomponent.md) association represents an explicit relationship in which a component is typically contained by a physical package, such as a chassis or card.</span></span>

</dd> <dt>

[<span data-ttu-id="e5b08-510">**\_PACKAGEINCHASSIS CIM**</span><span class="sxs-lookup"><span data-stu-id="e5b08-510">**CIM\_PackageInChassis**</span></span>](cim-packageinchassis.md)
</dt> <dd>

<span data-ttu-id="e5b08-511">L'associazione [**CIM \_ PackageInChassis**](cim-packageinchassis.md) rappresenta la relazione in cui uno chassis può contenere altri pacchetti, ad esempio altri chassis e schede.</span><span class="sxs-lookup"><span data-stu-id="e5b08-511">The [**CIM\_PackageInChassis**](cim-packageinchassis.md) association represents the relationship in which a chassis can contain other packages, such as other chassis and cards.</span></span>

</dd> <dt>

[<span data-ttu-id="e5b08-512">**\_PACKAGEINSLOT CIM**</span><span class="sxs-lookup"><span data-stu-id="e5b08-512">**CIM\_PackageInSlot**</span></span>](cim-packageinslot.md)
</dt> <dd>

<span data-ttu-id="e5b08-513">L'associazione [**CIM \_ PackageInSlot**](cim-packageinslot.md) rappresenta la relazione tra le schede dispositivo e lo chassis in cui sono montate.</span><span class="sxs-lookup"><span data-stu-id="e5b08-513">The [**CIM\_PackageInSlot**](cim-packageinslot.md) association represents the relationship between device cards and the chassis in which they are mounted.</span></span>

</dd> <dt>

[<span data-ttu-id="e5b08-514">**\_PACKAGETEMPSENSOR CIM**</span><span class="sxs-lookup"><span data-stu-id="e5b08-514">**CIM\_PackageTempSensor**</span></span>](cim-packagetempsensor.md)
</dt> <dd>

<span data-ttu-id="e5b08-515">L'associazione [**CIM \_ PackageTempSensor**](cim-packagetempsensor.md) rappresenta la relazione in cui un sensore di temperatura viene spesso installato in un pacchetto, ad esempio uno chassis o un rack, per monitorare l'ambiente del pacchetto.</span><span class="sxs-lookup"><span data-stu-id="e5b08-515">The [**CIM\_PackageTempSensor**](cim-packagetempsensor.md) association represents the relationship in which a temperature sensor is often installed in a package, such as a chassis or a rack, to monitor the package's environment.</span></span>

</dd> <dt>

[<span data-ttu-id="e5b08-516">**\_PARALLELCONTROLLER CIM**</span><span class="sxs-lookup"><span data-stu-id="e5b08-516">**CIM\_ParallelController**</span></span>](cim-parallelcontroller.md)
</dt> <dd>

<span data-ttu-id="e5b08-517">L'associazione [**CIM \_ ParallelController**](cim-parallelcontroller.md) è correlata alle funzionalità e alla gestione del dispositivo logico della porta parallela.</span><span class="sxs-lookup"><span data-stu-id="e5b08-517">The [**CIM\_ParallelController**](cim-parallelcontroller.md) association relates to the capabilities and management of the parallel port logical device.</span></span>

</dd> <dt>

[<span data-ttu-id="e5b08-518">**\_PARTICIPATESINSET CIM**</span><span class="sxs-lookup"><span data-stu-id="e5b08-518">**CIM\_ParticipatesInSet**</span></span>](cim-participatesinset.md)
</dt> <dd>

<span data-ttu-id="e5b08-519">La classe [**CIM \_ ParticipatesInSet**](cim-participatesinset.md) identifica gli elementi fisici che devono essere sostituiti insieme.</span><span class="sxs-lookup"><span data-stu-id="e5b08-519">The [**CIM\_ParticipatesInSet**](cim-participatesinset.md) class identifies physical elements that should be replaced together.</span></span>

</dd> <dt>

[<span data-ttu-id="e5b08-520">**\_PCICONTROLLER CIM**</span><span class="sxs-lookup"><span data-stu-id="e5b08-520">**CIM\_PCIController**</span></span>](cim-pcicontroller.md)
</dt> <dd>

<span data-ttu-id="e5b08-521">La classe [**CIM \_ PCIController**](cim-pcicontroller.md) rappresenta le proprietà e la gestione di un controller PCI.</span><span class="sxs-lookup"><span data-stu-id="e5b08-521">The [**CIM\_PCIController**](cim-pcicontroller.md) class represents the properties and management of a PCI controller.</span></span> <span data-ttu-id="e5b08-522">Le proprietà di questa classe e delle relative sottoclassi sono definite nelle diverse specifiche PCI pubblicate da PCI SIG.</span><span class="sxs-lookup"><span data-stu-id="e5b08-522">The properties in this class and its subclasses are defined in the various PCI specifications published by the PCI SIG.</span></span>

</dd> <dt>

[<span data-ttu-id="e5b08-523">**\_PCMCIACONTROLLER CIM**</span><span class="sxs-lookup"><span data-stu-id="e5b08-523">**CIM\_PCMCIAController**</span></span>](cim-pcmciacontroller.md)
</dt> <dd>

<span data-ttu-id="e5b08-524">La classe [**CIM \_ PCMCIAController**](cim-pcmciacontroller.md) rappresenta le funzionalità e la gestione di un controller PCMCIA (Personal Computer Memory Card International Association).</span><span class="sxs-lookup"><span data-stu-id="e5b08-524">The [**CIM\_PCMCIAController**](cim-pcmciacontroller.md) class represents the capabilities and management of a Personal Computer Memory Card International Association (PCMCIA) controller.</span></span>

</dd> <dt>

[<span data-ttu-id="e5b08-525">**\_PCVIDEOCONTROLLER CIM**</span><span class="sxs-lookup"><span data-stu-id="e5b08-525">**CIM\_PCVideoController**</span></span>](cim-pcvideocontroller.md)
</dt> <dd>

<span data-ttu-id="e5b08-526">Il [**\_ PCVideoController CIM**](cim-pcvideocontroller.md) rappresenta le funzionalità e la gestione di un personal computer controller video, un sottotipo di un controller video.</span><span class="sxs-lookup"><span data-stu-id="e5b08-526">The [**CIM\_PCVideoController**](cim-pcvideocontroller.md) represents the capabilities and management of a personal computer video controller, a subtype of a video controller.</span></span>

</dd> <dt>

[<span data-ttu-id="e5b08-527">**\_PEXTENTREDUNDANCYCOMPONENT CIM**</span><span class="sxs-lookup"><span data-stu-id="e5b08-527">**CIM\_PExtentRedundancyComponent**</span></span>](cim-pextentredundancycomponent.md)
</dt> <dd>

<span data-ttu-id="e5b08-528">La classe [**CIM \_ PExtentRedundancyComponent**](cim-pextentredundancycomponent.md) rappresenta gli extent fisici che fanno parte di un gruppo di ridondanza di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="e5b08-528">The [**CIM\_PExtentRedundancyComponent**](cim-pextentredundancycomponent.md) class represents the physical extents that participate in a storage redundancy group.</span></span>

</dd> <dt>

[<span data-ttu-id="e5b08-529">**\_PHYSICALCAPACITY CIM**</span><span class="sxs-lookup"><span data-stu-id="e5b08-529">**CIM\_PhysicalCapacity**</span></span>](cim-physicalcapacity.md)
</dt> <dd>

<span data-ttu-id="e5b08-530">La classe [**CIM \_ PhysicalCapacity**](cim-physicalcapacity.md) è una classe astratta che rappresenta i requisiti minimi e massimi di un elemento fisico e la capacità di supportare diversi tipi di hardware.</span><span class="sxs-lookup"><span data-stu-id="e5b08-530">The [**CIM\_PhysicalCapacity**](cim-physicalcapacity.md) class is an abstract class that represents a physical element's minimum and maximum requirements and its ability to support different types of hardware.</span></span> <span data-ttu-id="e5b08-531">Ad esempio, è possibile modellare i requisiti di memoria minimi e massimi come sottoclasse di **CIM \_ PhysicalCapacity**.</span><span class="sxs-lookup"><span data-stu-id="e5b08-531">For example, minimum and maximum memory requirements can be modeled as a subclass of **CIM\_PhysicalCapacity**.</span></span>

</dd> <dt>

[<span data-ttu-id="e5b08-532">**\_PHYSICALCOMPONENT CIM**</span><span class="sxs-lookup"><span data-stu-id="e5b08-532">**CIM\_PhysicalComponent**</span></span>](cim-physicalcomponent.md)
</dt> <dd>

<span data-ttu-id="e5b08-533">La classe [**CIM \_ PhysicalComponent**](cim-physicalcomponent.md) rappresenta un componente di base o di basso livello all'interno di un pacchetto.</span><span class="sxs-lookup"><span data-stu-id="e5b08-533">The [**CIM\_PhysicalComponent**](cim-physicalcomponent.md) class represents a low-level or basic component within a package.</span></span> <span data-ttu-id="e5b08-534">Un elemento fisico che non è un collegamento, un connettore o un pacchetto è un discendente (o membro) di questa classe.</span><span class="sxs-lookup"><span data-stu-id="e5b08-534">A physical element that is not a link, connector, or package is a descendant (or member) of this class.</span></span>

</dd> <dt>

[<span data-ttu-id="e5b08-535">**\_PHYSICALCONNECTOR CIM**</span><span class="sxs-lookup"><span data-stu-id="e5b08-535">**CIM\_PhysicalConnector**</span></span>](cim-physicalconnector.md)
</dt> <dd>

<span data-ttu-id="e5b08-536">La classe [**CIM \_ PhysicalConnector**](cim-physicalconnector.md) rappresenta qualsiasi elemento fisico usato per connettersi ad altri elementi.</span><span class="sxs-lookup"><span data-stu-id="e5b08-536">The [**CIM\_PhysicalConnector**](cim-physicalconnector.md) class represents any physical element that is used to connect to other elements.</span></span> <span data-ttu-id="e5b08-537">Qualsiasi oggetto in grado di connettersi e trasmettere segnali o potere tra due o più elementi fisici è un discendente (o membro) di questa classe.</span><span class="sxs-lookup"><span data-stu-id="e5b08-537">Any object that can connect and transmit signals or power between two or more physical elements is a descendant (or member) of this class.</span></span>

</dd> <dt>

[<span data-ttu-id="e5b08-538">**\_PhysicalElement CIM**</span><span class="sxs-lookup"><span data-stu-id="e5b08-538">**CIM\_PhysicalElement**</span></span>](cim-physicalelement.md)
</dt> <dd>

<span data-ttu-id="e5b08-539">Le sottoclassi [**CIM \_ PhysicalElement**](cim-physicalelement.md) definiscono qualsiasi componente di un sistema con un'identità fisica distinta.</span><span class="sxs-lookup"><span data-stu-id="e5b08-539">The [**CIM\_PhysicalElement**](cim-physicalelement.md) subclasses define any component of a system that has a distinct physical identity.</span></span> <span data-ttu-id="e5b08-540">Le istanze di questa classe possono essere definite in termini di etichette che possono essere fisicamente collegate all'oggetto.</span><span class="sxs-lookup"><span data-stu-id="e5b08-540">Instances of this class can be defined in terms of labels that can be physically attached to the object.</span></span>

</dd> <dt>

[<span data-ttu-id="e5b08-541">**\_PHYSICALELEMENTLOCATION CIM**</span><span class="sxs-lookup"><span data-stu-id="e5b08-541">**CIM\_PhysicalElementLocation**</span></span>](cim-physicalelementlocation.md)
</dt> <dd>

<span data-ttu-id="e5b08-542">La classe [**CIM \_ PhysicalElementLocation**](cim-physicalelementlocation.md) associa un elemento fisico a un [**oggetto \_ percorso CIM**](cim-location.md) a scopo di inventario o sostituzione.</span><span class="sxs-lookup"><span data-stu-id="e5b08-542">The [**CIM\_PhysicalElementLocation**](cim-physicalelementlocation.md) class associates a physical element with a [**CIM\_Location**](cim-location.md) object for inventory or replacement purposes.</span></span>

</dd> <dt>

[<span data-ttu-id="e5b08-543">**\_PHYSICALEXTENT CIM**</span><span class="sxs-lookup"><span data-stu-id="e5b08-543">**CIM\_PhysicalExtent**</span></span>](cim-physicalextent.md)
</dt> <dd>

<span data-ttu-id="e5b08-544">La classe [**CIM \_ PhysicalExtent**](cim-physicalextent.md) rappresenta un'implementazione RAID di SCC.</span><span class="sxs-lookup"><span data-stu-id="e5b08-544">The [**CIM\_PhysicalExtent**](cim-physicalextent.md) class represents an SCC RAID implementation.</span></span> <span data-ttu-id="e5b08-545">Definisce gli indirizzi di blocco indirizzabili consecutivi in un singolo dispositivo di archiviazione che vengono considerati come un singolo extent di archiviazione nella stessa classe [**CIM \_ StorageRedundancyGroup**](cim-storageredundancygroup.md) .</span><span class="sxs-lookup"><span data-stu-id="e5b08-545">It defines the consecutive addressable block addresses on a single storage device that are treated as a single storage extent in the same [**CIM\_StorageRedundancyGroup**](cim-storageredundancygroup.md) class.</span></span> <span data-ttu-id="e5b08-546">In alternativa, quando si usa la configurazione automatica, è possibile creare un'istanza o estendere la classe [**CIM \_ AggregatePExtent**](cim-aggregatepextent.md) .</span><span class="sxs-lookup"><span data-stu-id="e5b08-546">An alternative, when automatic configuration is used, is to instantiate or extend the [**CIM\_AggregatePExtent**](cim-aggregatepextent.md) class.</span></span>

</dd> <dt>

[<span data-ttu-id="e5b08-547">**\_PHYSICALFRAME CIM**</span><span class="sxs-lookup"><span data-stu-id="e5b08-547">**CIM\_PhysicalFrame**</span></span>](cim-physicalframe.md)
</dt> <dd>

<span data-ttu-id="e5b08-548">La classe [**CIM \_ PhysicalFrame**](cim-physicalframe.md) è una classe padre di rack, chassis e altre enclosure di frame così come sono definiti nelle classi di estensione.</span><span class="sxs-lookup"><span data-stu-id="e5b08-548">The [**CIM\_PhysicalFrame**](cim-physicalframe.md) class is a parent class of rack, chassis, and other frame enclosures as they are defined in extension classes.</span></span> <span data-ttu-id="e5b08-549">In questa classe padre sono incluse proprietà quali **VisibleAlarm** e **AudibleAlarm** e i dati relativi alle violazioni della sicurezza.</span><span class="sxs-lookup"><span data-stu-id="e5b08-549">Properties such as **VisibleAlarm** and **AudibleAlarm**, and data related to security breaches are included in this parent class.</span></span>

</dd> <dt>

[<span data-ttu-id="e5b08-550">**\_PHYSICALLINK CIM**</span><span class="sxs-lookup"><span data-stu-id="e5b08-550">**CIM\_PhysicalLink**</span></span>](cim-physicallink.md)
</dt> <dd>

<span data-ttu-id="e5b08-551">La classe [**CIM \_ PhysicalLink**](cim-physicallink.md) rappresenta il cablaggio di elementi fisici.</span><span class="sxs-lookup"><span data-stu-id="e5b08-551">The [**CIM\_PhysicalLink**](cim-physicallink.md) class represents the cabling of physical elements.</span></span>

</dd> <dt>

[<span data-ttu-id="e5b08-552">**\_PHYSICALMEDIA CIM**</span><span class="sxs-lookup"><span data-stu-id="e5b08-552">**CIM\_PhysicalMedia**</span></span>](cim-physicalmedia.md)
</dt> <dd>

<span data-ttu-id="e5b08-553">La classe [**CIM \_ PhysicalMedia**](cim-physicalmedia.md) rappresenta i tipi di documentazione e supporti di archiviazione, ad esempio nastri, CD ROM e così via.</span><span class="sxs-lookup"><span data-stu-id="e5b08-553">The [**CIM\_PhysicalMedia**](cim-physicalmedia.md) class represents types of documentation and storage medium, such as tapes, CD ROMs, and so on.</span></span>

</dd> <dt>

[<span data-ttu-id="e5b08-554">**\_PHYSICALMEMORY CIM**</span><span class="sxs-lookup"><span data-stu-id="e5b08-554">**CIM\_PhysicalMemory**</span></span>](cim-physicalmemory.md)
</dt> <dd>

<span data-ttu-id="e5b08-555">La classe [**CIM \_ PhysicalMemory**](cim-physicalmemory.md) rappresenta dispositivi di memoria di basso livello, ad esempio SIMM, DIMM, chip di memoria RAW e così via.</span><span class="sxs-lookup"><span data-stu-id="e5b08-555">The [**CIM\_PhysicalMemory**](cim-physicalmemory.md) class represents low-level memory devices, such as SIMMS, DIMMs, raw memory chips, and so on.</span></span>

</dd> <dt>

[<span data-ttu-id="e5b08-556">**\_PHYSICALPACKAGE CIM**</span><span class="sxs-lookup"><span data-stu-id="e5b08-556">**CIM\_PhysicalPackage**</span></span>](cim-physicalpackage.md)
</dt> <dd>

<span data-ttu-id="e5b08-557">La classe [**CIM \_ PhysicalPackage**](cim-physicalpackage.md) rappresenta elementi fisici che contengono o ospitano altri componenti.</span><span class="sxs-lookup"><span data-stu-id="e5b08-557">The [**CIM\_PhysicalPackage**](cim-physicalpackage.md) class represents physical elements that contain or host other components.</span></span> <span data-ttu-id="e5b08-558">Gli esempi sono un'enclosure rack o una scheda scheda.</span><span class="sxs-lookup"><span data-stu-id="e5b08-558">Examples are a rack enclosure or an adapter card.</span></span>

</dd> <dt>

[<span data-ttu-id="e5b08-559">**\_POINTINGDEVICE CIM**</span><span class="sxs-lookup"><span data-stu-id="e5b08-559">**CIM\_PointingDevice**</span></span>](cim-pointingdevice.md)
</dt> <dd>

<span data-ttu-id="e5b08-560">La classe [**CIM \_ PointingDevice**](cim-pointingdevice.md) rappresenta un dispositivo che punta alle aree sullo schermo.</span><span class="sxs-lookup"><span data-stu-id="e5b08-560">The [**CIM\_PointingDevice**](cim-pointingdevice.md) class represents a device that points to regions on the display.</span></span> <span data-ttu-id="e5b08-561">Qualsiasi dispositivo che manipola un puntatore o punta a aree in una visualizzazione visiva è un membro di questa classe.</span><span class="sxs-lookup"><span data-stu-id="e5b08-561">Any device that manipulates a pointer, or points to regions on a visual display, is a member of this class.</span></span> <span data-ttu-id="e5b08-562">Ad esempio mouse, stilo, touch pad o tablet.</span><span class="sxs-lookup"><span data-stu-id="e5b08-562">For example, a mouse, stylus, touch pad, or tablet.</span></span>

</dd> <dt>

[<span data-ttu-id="e5b08-563">**\_POTSMODEM CIM**</span><span class="sxs-lookup"><span data-stu-id="e5b08-563">**CIM\_POTSModem**</span></span>](cim-potsmodem.md)
</dt> <dd>

<span data-ttu-id="e5b08-564">La classe [**CIM \_ POTSModem**](cim-potsmodem.md) rappresenta un dispositivo che converte i dati binari in modulazioni Wave per la trasmissione basata su audio connettendosi alla rete Plain Old Phone System (POTS).</span><span class="sxs-lookup"><span data-stu-id="e5b08-564">The [**CIM\_POTSModem**](cim-potsmodem.md) class represents a device that translates binary data into wave modulations for sound-based transmission by connecting to the Plain Old Telephone System (POTS) network.</span></span>

</dd> <dt>

[<span data-ttu-id="e5b08-565">**\_Alimentatore CIM**</span><span class="sxs-lookup"><span data-stu-id="e5b08-565">**CIM\_PowerSupply**</span></span>](cim-powersupply.md)
</dt> <dd>

<span data-ttu-id="e5b08-566">La classe [**CIM \_ alimentatore**](cim-powersupply.md) rappresenta le funzionalità e la gestione del dispositivo logico dell'alimentatore.</span><span class="sxs-lookup"><span data-stu-id="e5b08-566">The [**CIM\_PowerSupply**](cim-powersupply.md) class represents the capabilities and management of the power supply logical device.</span></span>

</dd> <dt>

[<span data-ttu-id="e5b08-567">**\_Stampante CIM**</span><span class="sxs-lookup"><span data-stu-id="e5b08-567">**CIM\_Printer**</span></span>](cim-printer.md)
</dt> <dd>

<span data-ttu-id="e5b08-568">La classe [**CIM \_ Printer**](cim-printer.md) rappresenta le funzionalità e la gestione del dispositivo logico Printer.</span><span class="sxs-lookup"><span data-stu-id="e5b08-568">The [**CIM\_Printer**](cim-printer.md) class represents the capabilities and management of the printer logical device.</span></span>

</dd> <dt>

[<span data-ttu-id="e5b08-569">**\_Processo CIM**</span><span class="sxs-lookup"><span data-stu-id="e5b08-569">**CIM\_Process**</span></span>](cim-process.md)
</dt> <dd>

<span data-ttu-id="e5b08-570">La classe di [**\_ processo CIM**](cim-process.md) rappresenta una singola istanza di un programma in esecuzione.</span><span class="sxs-lookup"><span data-stu-id="e5b08-570">The [**CIM\_Process**](cim-process.md) class represents a single instance of a running program.</span></span> <span data-ttu-id="e5b08-571">Un utente visualizza in genere un processo come un'applicazione o un'attività.</span><span class="sxs-lookup"><span data-stu-id="e5b08-571">A user typically sees a process as an application or task.</span></span>

</dd> <dt>

[<span data-ttu-id="e5b08-572">**\_PROCESSEXECUTABLE CIM**</span><span class="sxs-lookup"><span data-stu-id="e5b08-572">**CIM\_ProcessExecutable**</span></span>](cim-processexecutable.md)
</dt> <dd>

<span data-ttu-id="e5b08-573">La classe [**CIM \_ ProcessExecutable**](cim-processexecutable.md) rappresenta un collegamento tra un processo e un file di dati e indica che il file partecipa all'esecuzione del processo.</span><span class="sxs-lookup"><span data-stu-id="e5b08-573">The [**CIM\_ProcessExecutable**](cim-processexecutable.md) class represents a link between a process and data file, and indicates that the file participates in the execution of the process.</span></span>

</dd> <dt>

[<span data-ttu-id="e5b08-574">**\_Processore CIM**</span><span class="sxs-lookup"><span data-stu-id="e5b08-574">**CIM\_Processor**</span></span>](cim-processor.md)
</dt> <dd>

<span data-ttu-id="e5b08-575">La classe del [**\_ processore CIM**](cim-processor.md) rappresenta le funzionalità e la gestione del dispositivo logico del processore.</span><span class="sxs-lookup"><span data-stu-id="e5b08-575">The [**CIM\_Processor**](cim-processor.md) class represents the capabilities and management of the processor logical device.</span></span>

</dd> <dt>

[<span data-ttu-id="e5b08-576">**\_PROCESSTHREAD CIM**</span><span class="sxs-lookup"><span data-stu-id="e5b08-576">**CIM\_ProcessThread**</span></span>](cim-processthread.md)
</dt> <dd>

<span data-ttu-id="e5b08-577">La classe [**CIM \_ ProcessThread**](cim-processthread.md) rappresenta un collegamento tra un processo e i thread in esecuzione nel contesto del processo.</span><span class="sxs-lookup"><span data-stu-id="e5b08-577">The [**CIM\_ProcessThread**](cim-processthread.md) class represents a link between a process and the threads running in the context of the process.</span></span>

</dd> <dt>

[<span data-ttu-id="e5b08-578">**\_Prodotto CIM**</span><span class="sxs-lookup"><span data-stu-id="e5b08-578">**CIM\_Product**</span></span>](cim-product.md)
</dt> <dd>

<span data-ttu-id="e5b08-579">La classe di [**\_ prodotto CIM**](cim-product.md) è una classe concreta che rappresenta una raccolta di elementi fisici, funzionalità software e altri prodotti, acquisiti come unità.</span><span class="sxs-lookup"><span data-stu-id="e5b08-579">The [**CIM\_Product**](cim-product.md) class is a concrete class that represents a collection of physical elements, software features and, other products, acquired as a unit.</span></span> <span data-ttu-id="e5b08-580">L'acquisizione implica un accordo tra il fornitore e il consumer, che può avere implicazioni sulla licenza, il supporto e la garanzia di prodotti.</span><span class="sxs-lookup"><span data-stu-id="e5b08-580">Acquisition implies an agreement between the supplier and consumer, which can have implications on product licensing, support, and warranty.</span></span>

</dd> <dt>

[<span data-ttu-id="e5b08-581">**\_PRODUCTFRU CIM**</span><span class="sxs-lookup"><span data-stu-id="e5b08-581">**CIM\_ProductFRU**</span></span>](cim-productfru.md)
</dt> <dd>

<span data-ttu-id="e5b08-582">La classe [**CIM \_ ProductFRU**](cim-productfru.md) rappresenta un'associazione tra il prodotto e un'unità sostituibile sul campo (FRU), che fornisce informazioni sui componenti del prodotto che sono stati o sono stati sostituiti.</span><span class="sxs-lookup"><span data-stu-id="e5b08-582">The [**CIM\_ProductFRU**](cim-productfru.md) class represents an association between the product and a field replaceable unit (FRU), which provides information about product components that have been, or are being replaced.</span></span>

</dd> <dt>

[<span data-ttu-id="e5b08-583">**\_PRODUCTPARENTCHILD CIM**</span><span class="sxs-lookup"><span data-stu-id="e5b08-583">**CIM\_ProductParentChild**</span></span>](cim-productparentchild.md)
</dt> <dd>

<span data-ttu-id="e5b08-584">L'associazione [**CIM \_ ProductParentChild**](cim-productparentchild.md) definisce una gerarchia padre-figlio tra i prodotti.</span><span class="sxs-lookup"><span data-stu-id="e5b08-584">The [**CIM\_ProductParentChild**](cim-productparentchild.md) association defines a parent-child hierarchy among products.</span></span> <span data-ttu-id="e5b08-585">Ad esempio, un prodotto può essere fornito con altri prodotti.</span><span class="sxs-lookup"><span data-stu-id="e5b08-585">For example, a product can come bundled with other products.</span></span>

</dd> <dt>

[<span data-ttu-id="e5b08-586">**\_PRODUCTPHYSICALELEMENTS CIM**</span><span class="sxs-lookup"><span data-stu-id="e5b08-586">**CIM\_ProductPhysicalElements**</span></span>](cim-productphysicalelements.md)
</dt> <dd>

<span data-ttu-id="e5b08-587">La classe [**CIM \_ ProductPhysicalElements**](cim-productphysicalelements.md) rappresenta gli elementi fisici che costituiscono un prodotto.</span><span class="sxs-lookup"><span data-stu-id="e5b08-587">The [**CIM\_ProductPhysicalElements**](cim-productphysicalelements.md) class represents the physical elements that make up a product.</span></span>

</dd> <dt>

[<span data-ttu-id="e5b08-588">**\_PRODUCTPRODUCTDEPENDENCY CIM**</span><span class="sxs-lookup"><span data-stu-id="e5b08-588">**CIM\_ProductProductDependency**</span></span>](cim-productproductdependency.md)
</dt> <dd>

<span data-ttu-id="e5b08-589">La classe [**CIM \_ ProductProductDependency**](cim-productproductdependency.md) rappresenta un'associazione tra due prodotti, che indica che è necessario installare o assente per il funzionamento dell'altro.</span><span class="sxs-lookup"><span data-stu-id="e5b08-589">The [**CIM\_ProductProductDependency**](cim-productproductdependency.md) class represents an association between two products, which indicates that one must be installed or absent for the other to function.</span></span> <span data-ttu-id="e5b08-590">Questa operazione è concettualmente equivalente all'associazione [**CIM \_ ServiceServiceDependency**](cim-serviceservicedependency.md) .</span><span class="sxs-lookup"><span data-stu-id="e5b08-590">This is conceptually equivalent to the [**CIM\_ServiceServiceDependency**](cim-serviceservicedependency.md) association.</span></span>

</dd> <dt>

[<span data-ttu-id="e5b08-591">**\_PRODUCTSOFTWAREFEATURES CIM**</span><span class="sxs-lookup"><span data-stu-id="e5b08-591">**CIM\_ProductSoftwareFeatures**</span></span>](cim-productsoftwarefeatures.md)
</dt> <dd>

<span data-ttu-id="e5b08-592">L'associazione [**CIM \_ ProductSoftwareFeatures**](cim-productsoftwarefeatures.md) identifica le funzionalità software per un determinato prodotto.</span><span class="sxs-lookup"><span data-stu-id="e5b08-592">The [**CIM\_ProductSoftwareFeatures**](cim-productsoftwarefeatures.md) association identifies the software features for a particular product.</span></span>

</dd> <dt>

[<span data-ttu-id="e5b08-593">**\_PRODUCTSUPPORT CIM**</span><span class="sxs-lookup"><span data-stu-id="e5b08-593">**CIM\_ProductSupport**</span></span>](cim-productsupport.md)
</dt> <dd>

<span data-ttu-id="e5b08-594">La classe [**CIM \_ ProductSupport**](cim-productsupport.md) rappresenta un'associazione tra il prodotto e il supporto dell'accesso che comunica come si ottiene il supporto per il prodotto.</span><span class="sxs-lookup"><span data-stu-id="e5b08-594">The [**CIM\_ProductSupport**](cim-productsupport.md) class represents an association between product and support access that conveys how support is obtained for the product.</span></span> <span data-ttu-id="e5b08-595">Sono disponibili vari tipi di supporto per un prodotto; lo stesso oggetto di supporto può fornire assistenza per più prodotti.</span><span class="sxs-lookup"><span data-stu-id="e5b08-595">Various types of support are available for a product; the same support object can provide assistance for multiple products.</span></span>

</dd> <dt>

[<span data-ttu-id="e5b08-596">**\_PROTECTEDSPACEEXTENT CIM**</span><span class="sxs-lookup"><span data-stu-id="e5b08-596">**CIM\_ProtectedSpaceExtent**</span></span>](cim-protectedspaceextent.md)
</dt> <dd>

<span data-ttu-id="e5b08-597">La classe [**CIM \_ ProtectedSpaceExtent**](cim-protectedspaceextent.md) rappresenta indirizzi di blocco logico indirizzabili, che vengono trattati come un singolo extent di archiviazione, ma si trovano in un singolo extent fisico.</span><span class="sxs-lookup"><span data-stu-id="e5b08-597">The [**CIM\_ProtectedSpaceExtent**](cim-protectedspaceextent.md) class represents addressable logical-block addresses, which are treated as a single storage extent, but are located on a single physical extent.</span></span>

</dd> <dt>

[<span data-ttu-id="e5b08-598">**\_PSEXTENTBASEDONPEXTENT CIM**</span><span class="sxs-lookup"><span data-stu-id="e5b08-598">**CIM\_PSExtentBasedOnPExtent**</span></span>](cim-psextentbasedonpextent.md)
</dt> <dd>

<span data-ttu-id="e5b08-599">La classe [**CIM \_ PSExtentBasedOnPExtent**](cim-psextentbasedonpextent.md) associa gli extent dello spazio protetto basati su un extent fisico.</span><span class="sxs-lookup"><span data-stu-id="e5b08-599">The [**CIM\_PSExtentBasedOnPExtent**](cim-psextentbasedonpextent.md) class associates protected space extents that are based on a physical extent.</span></span>

</dd> <dt>

[<span data-ttu-id="e5b08-600">**\_Rack CIM**</span><span class="sxs-lookup"><span data-stu-id="e5b08-600">**CIM\_Rack**</span></span>](cim-rack.md)
</dt> <dd>

<span data-ttu-id="e5b08-601">La classe [**CIM \_ rack**](cim-rack.md) rappresenta un rack (un frame fisico o un'enclosure) in cui vengono archiviati gli chassis.</span><span class="sxs-lookup"><span data-stu-id="e5b08-601">The [**CIM\_Rack**](cim-rack.md) class represents a rack (a physical frame or enclosure) in which chassis are stored.</span></span> <span data-ttu-id="e5b08-602">In genere, un rack rappresenta l'enclosure; tutti i componenti funzionanti sono inclusi nello chassis.</span><span class="sxs-lookup"><span data-stu-id="e5b08-602">Typically, a rack represents the enclosure; all functioning components are packaged in the chassis.</span></span>

</dd> <dt>

[<span data-ttu-id="e5b08-603">**CIM \_ realizza**</span><span class="sxs-lookup"><span data-stu-id="e5b08-603">**CIM\_Realizes**</span></span>](cim-realizes.md)
</dt> <dd>

<span data-ttu-id="e5b08-604">La classe [**CIM \_ realizza**](cim-realizes.md) la classe che rappresenta l'associazione che definisce il mapping tra un dispositivo logico e il componente fisico che implementa il dispositivo.</span><span class="sxs-lookup"><span data-stu-id="e5b08-604">The [**CIM\_Realizes**](cim-realizes.md) class represents the association that defines the mapping between a logical device and the physical component that implements the device.</span></span>

</dd> <dt>

[<span data-ttu-id="e5b08-605">**\_REALIZESAGGREGATEPEXTENT CIM**</span><span class="sxs-lookup"><span data-stu-id="e5b08-605">**CIM\_RealizesAggregatePExtent**</span></span>](cim-realizesaggregatepextent.md)
</dt> <dd>

<span data-ttu-id="e5b08-606">L'associazione [**CIM \_ RealizesAggregatePExtent**](cim-realizesaggregatepextent.md) rappresenta la relazione in cui la classe [**CIM \_ AggregatePExtent**](cim-aggregatepextent.md) è realizzata su un supporto fisico.</span><span class="sxs-lookup"><span data-stu-id="e5b08-606">The [**CIM\_RealizesAggregatePExtent**](cim-realizesaggregatepextent.md) association represents the relationship in which the [**CIM\_AggregatePExtent**](cim-aggregatepextent.md) class is realized on a physical media.</span></span>

</dd> <dt>

[<span data-ttu-id="e5b08-607">**\_REALIZESDISKPARTITION CIM**</span><span class="sxs-lookup"><span data-stu-id="e5b08-607">**CIM\_RealizesDiskPartition**</span></span>](cim-realizesdiskpartition.md)
</dt> <dd>

<span data-ttu-id="e5b08-608">La classe [**CIM \_ RealizesDiskPartition**](cim-realizesdiskpartition.md) rappresenta una partizione disco su un supporto fisico che modella la creazione di partizioni in un'unità IDE o SCSI non elaborata.</span><span class="sxs-lookup"><span data-stu-id="e5b08-608">The [**CIM\_RealizesDiskPartition**](cim-realizesdiskpartition.md) class represents a disk partition on a physical media that models the creation of partitions on a raw SCSI or IDE drive.</span></span>

</dd> <dt>

[<span data-ttu-id="e5b08-609">**\_REALIZESPEXTENT CIM**</span><span class="sxs-lookup"><span data-stu-id="e5b08-609">**CIM\_RealizesPExtent**</span></span>](cim-realizespextent.md)
</dt> <dd>

<span data-ttu-id="e5b08-610">L'associazione [**CIM \_ RealizesPExtent**](cim-realizespextent.md) rappresenta la relazione in cui gli extent fisici vengono realizzati su un supporto fisico.</span><span class="sxs-lookup"><span data-stu-id="e5b08-610">The [**CIM\_RealizesPExtent**](cim-realizespextent.md) association represents the relationship in which physical extents are realized on a physical media.</span></span> <span data-ttu-id="e5b08-611">Inoltre, viene specificato l'indirizzo iniziale dell'extent fisico sul supporto fisico.</span><span class="sxs-lookup"><span data-stu-id="e5b08-611">In addition, the starting address of the physical extent on the physical media is specified.</span></span>

</dd> <dt>

[<span data-ttu-id="e5b08-612">**\_REBOOTACTION CIM**</span><span class="sxs-lookup"><span data-stu-id="e5b08-612">**CIM\_RebootAction**</span></span>](cim-rebootaction.md)
</dt> <dd>

<span data-ttu-id="e5b08-613">La classe [**CIM \_ rebootaction**](cim-rebootaction.md) causa un riavvio del sistema in cui è installato l'elemento software.</span><span class="sxs-lookup"><span data-stu-id="e5b08-613">The [**CIM\_RebootAction**](cim-rebootaction.md) class causes a system reboot where the software element is installed.</span></span>

</dd> <dt>

[<span data-ttu-id="e5b08-614">**\_REDUNDANCYCOMPONENT CIM**</span><span class="sxs-lookup"><span data-stu-id="e5b08-614">**CIM\_RedundancyComponent**</span></span>](cim-redundancycomponent.md)
</dt> <dd>

<span data-ttu-id="e5b08-615">La classe [**CIM \_ RedundancyComponent**](cim-redundancycomponent.md) associa un gruppo di ridondanza composto da elementi di sistema gestiti e indica che, insieme, gli elementi forniscono la ridondanza.</span><span class="sxs-lookup"><span data-stu-id="e5b08-615">The [**CIM\_RedundancyComponent**](cim-redundancycomponent.md) class associates a redundancy group composed of managed system elements and indicates that, together, the elements provide redundancy.</span></span> <span data-ttu-id="e5b08-616">Tutti gli elementi aggregati in un gruppo di ridondanza devono essere istanze della stessa classe di oggetti.</span><span class="sxs-lookup"><span data-stu-id="e5b08-616">All elements aggregated in a redundancy group should be instantiations of the same object class.</span></span>

</dd> <dt>

[<span data-ttu-id="e5b08-617">**\_REDUNDANCYGROUP CIM**</span><span class="sxs-lookup"><span data-stu-id="e5b08-617">**CIM\_RedundancyGroup**</span></span>](cim-redundancygroup.md)
</dt> <dd>

<span data-ttu-id="e5b08-618">La classe [**CIM \_ RedundancyGroup**](cim-redundancygroup.md) rappresenta una raccolta di elementi di sistema gestiti, che indica che i componenti aggregati, insieme, forniscono la ridondanza.</span><span class="sxs-lookup"><span data-stu-id="e5b08-618">The [**CIM\_RedundancyGroup**](cim-redundancygroup.md) class represents a collection of managed system elements, which indicates that the aggregated components, together, provide redundancy.</span></span> <span data-ttu-id="e5b08-619">Tutti gli elementi aggregati in un gruppo di ridondanza devono essere istanze della stessa classe di oggetti.</span><span class="sxs-lookup"><span data-stu-id="e5b08-619">All elements aggregated in a redundancy group should be instantiations of the same object class.</span></span>

</dd> <dt>

[<span data-ttu-id="e5b08-620">**\_Refrigerazione CIM**</span><span class="sxs-lookup"><span data-stu-id="e5b08-620">**CIM\_Refrigeration**</span></span>](cim-refrigeration.md)
</dt> <dd>

<span data-ttu-id="e5b08-621">La classe di [**\_ refrigerazione CIM**](cim-refrigeration.md) rappresenta le funzionalità e la gestione di un dispositivo di raffreddamento a freddo.</span><span class="sxs-lookup"><span data-stu-id="e5b08-621">The [**CIM\_Refrigeration**](cim-refrigeration.md) class represents the capabilities and management of a refrigeration cooling device.</span></span>

</dd> <dt>

[<span data-ttu-id="e5b08-622">**\_RELATEDSTATISTICS CIM**</span><span class="sxs-lookup"><span data-stu-id="e5b08-622">**CIM\_RelatedStatistics**</span></span>](cim-relatedstatistics.md)
</dt> <dd>

<span data-ttu-id="e5b08-623">L'associazione [**CIM \_ RelatedStatistics**](cim-relatedstatistics.md) rappresenta gerarchie e dipendenze di classi [**CIM \_ StatisticalInformation**](cim-statisticalinformation.md) correlate.</span><span class="sxs-lookup"><span data-stu-id="e5b08-623">The [**CIM\_RelatedStatistics**](cim-relatedstatistics.md) association represents hierarchies and dependencies of related [**CIM\_StatisticalInformation**](cim-statisticalinformation.md) classes.</span></span>

</dd> <dt>

[<span data-ttu-id="e5b08-624">**\_REMOTEFILESYSTEM CIM**</span><span class="sxs-lookup"><span data-stu-id="e5b08-624">**CIM\_RemoteFileSystem**</span></span>](cim-remotefilesystem.md)
</dt> <dd>

<span data-ttu-id="e5b08-625">La classe [**CIM \_ RemoteFileSystem**](cim-remotefilesystem.md) rappresenta una file system remota a cui si accede tramite un servizio correlato alla rete.</span><span class="sxs-lookup"><span data-stu-id="e5b08-625">The [**CIM\_RemoteFileSystem**](cim-remotefilesystem.md) class represents a remote file system that is accessed by way of a network-related service.</span></span> <span data-ttu-id="e5b08-626">In questo caso, l'archivio file è ospitato da un computer che funge da file server.</span><span class="sxs-lookup"><span data-stu-id="e5b08-626">In this case, the file store is hosted by a computer, which acts as a file server.</span></span>

</dd> <dt>

[<span data-ttu-id="e5b08-627">**\_REMOVEDIRECTORYACTION CIM**</span><span class="sxs-lookup"><span data-stu-id="e5b08-627">**CIM\_RemoveDirectoryAction**</span></span>](cim-removedirectoryaction.md)
</dt> <dd>

<span data-ttu-id="e5b08-628">La classe [**CIM \_ RemoveDirectoryAction**](cim-removedirectoryaction.md) rimuove le directory per gli elementi software.</span><span class="sxs-lookup"><span data-stu-id="e5b08-628">The [**CIM\_RemoveDirectoryAction**](cim-removedirectoryaction.md) class removes directories for software elements.</span></span>

</dd> <dt>

[<span data-ttu-id="e5b08-629">**\_REMOVEFILEACTION CIM**</span><span class="sxs-lookup"><span data-stu-id="e5b08-629">**CIM\_RemoveFileAction**</span></span>](cim-removefileaction.md)
</dt> <dd>

<span data-ttu-id="e5b08-630">La classe [**CIM \_ RemoveFileAction**](cim-removefileaction.md) Disinstalla i file.</span><span class="sxs-lookup"><span data-stu-id="e5b08-630">The [**CIM\_RemoveFileAction**](cim-removefileaction.md) class uninstalls files.</span></span>

</dd> <dt>

[<span data-ttu-id="e5b08-631">**\_REPLACEMENTSET CIM**</span><span class="sxs-lookup"><span data-stu-id="e5b08-631">**CIM\_ReplacementSet**</span></span>](cim-replacementset.md)
</dt> <dd>

<span data-ttu-id="e5b08-632">La classe [**CIM \_ ReplacementSet**](cim-replacementset.md) aggrega gli elementi fisici che devono essere sostituiti insieme.</span><span class="sxs-lookup"><span data-stu-id="e5b08-632">The [**CIM\_ReplacementSet**](cim-replacementset.md) class aggregates physical elements that must be replaced together.</span></span> <span data-ttu-id="e5b08-633">Ad esempio, quando si sostituisce una scheda di memoria, è possibile rimuovere e sostituire anche i chip di memoria del componente.</span><span class="sxs-lookup"><span data-stu-id="e5b08-633">For example, when replacing a memory card, the component memory chips can also be removed and replaced.</span></span> <span data-ttu-id="e5b08-634">In alternativa, è possibile usare questa associazione per sostituire o aggiornare un set di chip di memoria.</span><span class="sxs-lookup"><span data-stu-id="e5b08-634">Or, this association can be used to replace or upgrade a set of memory chips.</span></span>

</dd> <dt>

[<span data-ttu-id="e5b08-635">**\_RESIDESONEXTENT CIM**</span><span class="sxs-lookup"><span data-stu-id="e5b08-635">**CIM\_ResidesOnExtent**</span></span>](cim-residesonextent.md)
</dt> <dd>

<span data-ttu-id="e5b08-636">La classe [**CIM \_ ResidesOnExtent**](cim-residesonextent.md) rappresenta un'associazione tra un file System e l'extent di archiviazione in cui si trova.</span><span class="sxs-lookup"><span data-stu-id="e5b08-636">The [**CIM\_ResidesOnExtent**](cim-residesonextent.md) class represents an association between a file system and the storage extent where it is located.</span></span> <span data-ttu-id="e5b08-637">In genere, un file system risiede su un disco logico.</span><span class="sxs-lookup"><span data-stu-id="e5b08-637">Typically, a file system resides on a logical disk.</span></span>

</dd> <dt>

[<span data-ttu-id="e5b08-638">**CIM \_ in esecuzione**</span><span class="sxs-lookup"><span data-stu-id="e5b08-638">**CIM\_RunningOS**</span></span>](cim-runningos.md)
</dt> <dd>

<span data-ttu-id="e5b08-639">La classe [**CIM \_ RunningOS**](cim-runningos.md) rappresenta il sistema operativo attualmente in esecuzione.</span><span class="sxs-lookup"><span data-stu-id="e5b08-639">The [**CIM\_RunningOS**](cim-runningos.md) class represents the currently executing operating system.</span></span> <span data-ttu-id="e5b08-640">Al massimo, un sistema operativo può essere eseguito in qualsiasi momento in un computer. il computer potrebbe non essere attualmente avviato o il sistema operativo potrebbe essere sconosciuto.</span><span class="sxs-lookup"><span data-stu-id="e5b08-640">At most, one operating system can execute at any time on a computer system; the computer system may not be currently booted, or its operating system may be unknown.</span></span>

</dd> <dt>

[<span data-ttu-id="e5b08-641">**\_SAPSAPDEPENDENCY CIM**</span><span class="sxs-lookup"><span data-stu-id="e5b08-641">**CIM\_SAPSAPDependency**</span></span>](cim-sapsapdependency.md)
</dt> <dd>

<span data-ttu-id="e5b08-642">La classe [**CIM \_ SAPSAPDependency**](cim-sapsapdependency.md) è un'associazione tra due punti di accesso al servizio (SAP), che indica che il secondo SAP è necessario affinché il primo SAP si connetta con il servizio.</span><span class="sxs-lookup"><span data-stu-id="e5b08-642">The [**CIM\_SAPSAPDependency**](cim-sapsapdependency.md) class is an association between two service access points (SAPs), which indicates that the second SAP is required for the first SAP to connect with its service.</span></span>

</dd> <dt>

[<span data-ttu-id="e5b08-643">**\_Scanner CIM**</span><span class="sxs-lookup"><span data-stu-id="e5b08-643">**CIM\_Scanner**</span></span>](cim-scanner.md)
</dt> <dd>

<span data-ttu-id="e5b08-644">Lo [**\_ scanner CIM**](cim-scanner.md) rappresenta le funzionalità e la gestione del dispositivo logico dello scanner.</span><span class="sxs-lookup"><span data-stu-id="e5b08-644">The [**CIM\_Scanner**](cim-scanner.md) represents the capabilities and management of the scanner logical device.</span></span>

</dd> <dt>

[<span data-ttu-id="e5b08-645">**\_Controller SCSI CIM**</span><span class="sxs-lookup"><span data-stu-id="e5b08-645">**CIM\_SCSIController**</span></span>](cim-scsicontroller.md)
</dt> <dd>

<span data-ttu-id="e5b08-646">La classe [**CIM \_ controller SCSI**](cim-scsicontroller.md) rappresenta le funzionalità e la gestione del dispositivo logico del controller SCSI.</span><span class="sxs-lookup"><span data-stu-id="e5b08-646">The [**CIM\_SCSIController**](cim-scsicontroller.md) class represents the capabilities and management of the SCSI controller logical device.</span></span>

</dd> <dt>

[<span data-ttu-id="e5b08-647">**\_SCSIINTERFACE CIM**</span><span class="sxs-lookup"><span data-stu-id="e5b08-647">**CIM\_SCSIInterface**</span></span>](cim-scsiinterface.md)
</dt> <dd>

<span data-ttu-id="e5b08-648">rappresenta una relazione [**CIM \_ ControlledBy**](cim-controlledby.md) che indica i dispositivi a cui si accede tramite un controller SCSI e le caratteristiche di accesso.</span><span class="sxs-lookup"><span data-stu-id="e5b08-648">represents a [**CIM\_ControlledBy**](cim-controlledby.md) relationship that indicates which devices are accessed through a SCSI controller and the access characteristics.</span></span>

</dd> <dt>

[<span data-ttu-id="e5b08-649">**\_Sensore CIM**</span><span class="sxs-lookup"><span data-stu-id="e5b08-649">**CIM\_Sensor**</span></span>](cim-sensor.md)
</dt> <dd>

<span data-ttu-id="e5b08-650">La classe del [**\_ sensore CIM**](cim-sensor.md) rappresenta un dispositivo hardware in grado di misurare le caratteristiche di una proprietà fisica, ad esempio le caratteristiche di temperatura o di tensione di un sistema di computer.</span><span class="sxs-lookup"><span data-stu-id="e5b08-650">The [**CIM\_Sensor**](cim-sensor.md) class represents a hardware device that is capable of measuring the characteristics of a physical property (for example, the temperature or voltage characteristics of a unitary computer system).</span></span>

</dd> <dt>

[<span data-ttu-id="e5b08-651">**\_Controller seriale CIM**</span><span class="sxs-lookup"><span data-stu-id="e5b08-651">**CIM\_SerialController**</span></span>](cim-serialcontroller.md)
</dt> <dd>

<span data-ttu-id="e5b08-652">La classe [**CIM \_ controller seriale**](cim-serialcontroller.md) rappresenta le funzionalità e la gestione del dispositivo logico della porta seriale.</span><span class="sxs-lookup"><span data-stu-id="e5b08-652">The [**CIM\_SerialController**](cim-serialcontroller.md) class represents the capabilities and management of the serial port logical device.</span></span>

</dd> <dt>

[<span data-ttu-id="e5b08-653">**\_SERIALINTERFACE CIM**</span><span class="sxs-lookup"><span data-stu-id="e5b08-653">**CIM\_SerialInterface**</span></span>](cim-serialinterface.md)
</dt> <dd>

<span data-ttu-id="e5b08-654">La classe [**CIM \_ SerialInterface**](cim-serialinterface.md) rappresenta una relazione [**CIM \_ ControlledBy**](cim-controlledby.md) che indica i dispositivi a cui si accede tramite il controller seriale e le caratteristiche dell'accesso.</span><span class="sxs-lookup"><span data-stu-id="e5b08-654">The [**CIM\_SerialInterface**](cim-serialinterface.md) class represents a [**CIM\_ControlledBy**](cim-controlledby.md) relationship that indicates which devices are accessed through the serial controller and the characteristics of the access.</span></span>

</dd> <dt>

[<span data-ttu-id="e5b08-655">**\_Servizio CIM**</span><span class="sxs-lookup"><span data-stu-id="e5b08-655">**CIM\_Service**</span></span>](cim-service.md)
</dt> <dd>

<span data-ttu-id="e5b08-656">La classe del [**\_ servizio CIM**](cim-service.md) rappresenta un elemento logico che contiene informazioni per rappresentare e gestire la funzionalità fornita da una funzionalità del dispositivo o del software.</span><span class="sxs-lookup"><span data-stu-id="e5b08-656">The [**CIM\_Service**](cim-service.md) class represents a logical element that contains information to represent and manage the functionality provided by a device or software feature.</span></span> <span data-ttu-id="e5b08-657">Un servizio è un oggetto generico per la configurazione e la gestione dell'implementazione di funzionalità. non si tratta della funzionalità stessa.</span><span class="sxs-lookup"><span data-stu-id="e5b08-657">A service is a general-purpose object to configure and manage the implementation of functionality; it is not the functionality itself.</span></span>

</dd> <dt>

[<span data-ttu-id="e5b08-658">**\_SERVICEACCESSBYSAP CIM**</span><span class="sxs-lookup"><span data-stu-id="e5b08-658">**CIM\_ServiceAccessBySAP**</span></span>](cim-serviceaccessbysap.md)
</dt> <dd>

<span data-ttu-id="e5b08-659">La classe di associazione [**CIM \_ ServiceAccessBySAP**](cim-serviceaccessbysap.md) rappresenta i punti di accesso per un servizio.</span><span class="sxs-lookup"><span data-stu-id="e5b08-659">The [**CIM\_ServiceAccessBySAP**](cim-serviceaccessbysap.md) association class represents the access points for a service.</span></span> <span data-ttu-id="e5b08-660">Ad esempio, è possibile accedere a una stampante mediante i punti di accesso (SAP) di NetWare, Macintosh o Windows, che sono potenzialmente ospitati in sistemi diversi.</span><span class="sxs-lookup"><span data-stu-id="e5b08-660">For example, a printer can be accessed by NetWare, Macintosh, or Windows service access points (SAPs), which are potentially hosted on different systems.</span></span>

</dd> <dt>

[<span data-ttu-id="e5b08-661">**\_SERVICEACCESSPOINT CIM**</span><span class="sxs-lookup"><span data-stu-id="e5b08-661">**CIM\_ServiceAccessPoint**</span></span>](cim-serviceaccesspoint.md)
</dt> <dd>

<span data-ttu-id="e5b08-662">La classe [**CIM \_ serviceAccessPoint**](cim-serviceaccesspoint.md) rappresenta la possibilità di usare o richiamare un servizio.</span><span class="sxs-lookup"><span data-stu-id="e5b08-662">The [**CIM\_ServiceAccessPoint**](cim-serviceaccesspoint.md) class represents the ability to use or invoke a service.</span></span> <span data-ttu-id="e5b08-663">I punti di accesso rappresentano i servizi disponibili per l'utilizzo da altre entità.</span><span class="sxs-lookup"><span data-stu-id="e5b08-663">Access points represent services that are available for use by other entities.</span></span>

</dd> <dt>

[<span data-ttu-id="e5b08-664">**\_SERVICESAPDEPENDENCY CIM**</span><span class="sxs-lookup"><span data-stu-id="e5b08-664">**CIM\_ServiceSAPDependency**</span></span>](cim-servicesapdependency.md)
</dt> <dd>

<span data-ttu-id="e5b08-665">La classe [**CIM \_ ServiceSAPDependency**](cim-servicesapdependency.md) rappresenta un'associazione tra un servizio e un punto di accesso al servizio (SAP), che indica che il servizio SAP a cui viene fatto riferimento viene usato dal servizio per fornire le funzionalità.</span><span class="sxs-lookup"><span data-stu-id="e5b08-665">The [**CIM\_ServiceSAPDependency**](cim-servicesapdependency.md) class represents an association between a service and a service access point (SAP), which indicates that the referenced SAP is used by the service to provide its functionality.</span></span>

</dd> <dt>

[<span data-ttu-id="e5b08-666">**\_SERVICESERVICEDEPENDENCY CIM**</span><span class="sxs-lookup"><span data-stu-id="e5b08-666">**CIM\_ServiceServiceDependency**</span></span>](cim-serviceservicedependency.md)
</dt> <dd>

<span data-ttu-id="e5b08-667">La classe [**CIM \_ ServiceServiceDependency**](cim-serviceservicedependency.md) rappresenta un'associazione tra due servizi.</span><span class="sxs-lookup"><span data-stu-id="e5b08-667">The [**CIM\_ServiceServiceDependency**](cim-serviceservicedependency.md) class represents an association between two services.</span></span>

</dd> <dt>

[<span data-ttu-id="e5b08-668">**\_Impostazione CIM**</span><span class="sxs-lookup"><span data-stu-id="e5b08-668">**CIM\_Setting**</span></span>](cim-setting.md)
</dt> <dd>

<span data-ttu-id="e5b08-669">La classe di [**\_ Impostazioni CIM**](cim-setting.md) rappresenta i parametri operativi e correlati alla configurazione per uno o più elementi di sistema gestiti.</span><span class="sxs-lookup"><span data-stu-id="e5b08-669">The [**CIM\_Setting**](cim-setting.md) class represents configuration-related and operational parameters for one or more managed system elements.</span></span>

</dd> <dt>

[<span data-ttu-id="e5b08-670">**\_SETTINGCHECK CIM**</span><span class="sxs-lookup"><span data-stu-id="e5b08-670">**CIM\_SettingCheck**</span></span>](cim-settingcheck.md)
</dt> <dd>

<span data-ttu-id="e5b08-671">La classe [**CIM \_ SettingCheck**](cim-settingcheck.md) specifica le informazioni necessarie per controllare un determinato file di impostazioni per una voce specifica che contiene un valore uguale al valore specificato.</span><span class="sxs-lookup"><span data-stu-id="e5b08-671">The [**CIM\_SettingCheck**](cim-settingcheck.md) class specifies information needed to check a particular setting file for a specific entry that contains a value equal to the value specified.</span></span> <span data-ttu-id="e5b08-672">Si presuppone che non venga fatta distinzione tra maiuscole e minuscole.</span><span class="sxs-lookup"><span data-stu-id="e5b08-672">All comparisons are assumed to be case insensitive.</span></span>

</dd> <dt>

[<span data-ttu-id="e5b08-673">**\_SETTINGCONTEXT CIM**</span><span class="sxs-lookup"><span data-stu-id="e5b08-673">**CIM\_SettingContext**</span></span>](cim-settingcontext.md)
</dt> <dd>

<span data-ttu-id="e5b08-674">La classe [**CIM \_ SettingContext**](cim-settingcontext.md) associa gli oggetti di configurazione a oggetti setting.</span><span class="sxs-lookup"><span data-stu-id="e5b08-674">The [**CIM\_SettingContext**](cim-settingcontext.md) class associates configuration objects with setting objects.</span></span>

</dd> <dt>

[<span data-ttu-id="e5b08-675">**\_Slot CIM**</span><span class="sxs-lookup"><span data-stu-id="e5b08-675">**CIM\_Slot**</span></span>](cim-slot.md)
</dt> <dd>

<span data-ttu-id="e5b08-676">La classe di [**\_ slot CIM**](cim-slot.md) rappresenta i connettori in cui vengono inseriti i pacchetti.</span><span class="sxs-lookup"><span data-stu-id="e5b08-676">The [**CIM\_Slot**](cim-slot.md) class represents connectors into which packages are inserted.</span></span>

</dd> <dt>

[<span data-ttu-id="e5b08-677">**\_SLOTINSLOT CIM**</span><span class="sxs-lookup"><span data-stu-id="e5b08-677">**CIM\_SlotInSlot**</span></span>](cim-slotinslot.md)
</dt> <dd>

<span data-ttu-id="e5b08-678">La relazione [**CIM \_ SlotInSlot**](cim-slotinslot.md) rappresenta la capacità di un adattatore speciale di estendere la struttura degli slot esistente per consentire l'inserimento di schede altrimenti incompatibili in un frame o in una lavagna di hosting.</span><span class="sxs-lookup"><span data-stu-id="e5b08-678">The [**CIM\_SlotInSlot**](cim-slotinslot.md) relationship represents the ability of a special adapter to extend the existing slot structure to enable otherwise incompatible cards to be plugged into a frame or hosting board.</span></span>

</dd> <dt>

[<span data-ttu-id="e5b08-679">**\_Software CIM**</span><span class="sxs-lookup"><span data-stu-id="e5b08-679">**CIM\_SoftwareElement**</span></span>](cim-softwareelement.md)
</dt> <dd>

<span data-ttu-id="e5b08-680">La classe [**CIM \_ SoftwareElement**](cim-softwareelement.md) scompone un oggetto [**\_ SoftwareFeature CIM**](cim-softwarefeature.md) in un set di parti gestibili o distribuibile singolarmente per una determinata piattaforma.</span><span class="sxs-lookup"><span data-stu-id="e5b08-680">The [**CIM\_SoftwareElement**](cim-softwareelement.md) class decomposes a [**CIM\_SoftwareFeature**](cim-softwarefeature.md) object into a set of individually manageable or deployable parts for a particular platform.</span></span> <span data-ttu-id="e5b08-681">La piattaforma di un elemento software viene identificata in modo univoco dall'architettura hardware e dal sistema operativo sottostanti.</span><span class="sxs-lookup"><span data-stu-id="e5b08-681">A software element's platform is uniquely identified by its underlying hardware architecture and operating system.</span></span>

</dd> <dt>

[<span data-ttu-id="e5b08-682">**\_SOFTWAREELEMENTACTIONS CIM**</span><span class="sxs-lookup"><span data-stu-id="e5b08-682">**CIM\_SoftwareElementActions**</span></span>](cim-softwareelementactions.md)
</dt> <dd>

<span data-ttu-id="e5b08-683">L'associazione [**CIM \_ SoftwareElementActions**](cim-softwareelementactions.md) identifica le azioni per un elemento software.</span><span class="sxs-lookup"><span data-stu-id="e5b08-683">The [**CIM\_SoftwareElementActions**](cim-softwareelementactions.md) association identifies the actions for a software element.</span></span>

</dd> <dt>

[<span data-ttu-id="e5b08-684">**\_SOFTWAREELEMENTCHECKS CIM**</span><span class="sxs-lookup"><span data-stu-id="e5b08-684">**CIM\_SoftwareElementChecks**</span></span>](cim-softwareelementchecks.md)
</dt> <dd>

<span data-ttu-id="e5b08-685">La classe di associazione [**CIM \_ SoftwareElementChecks**](cim-softwareelementchecks.md) mette in correlazione un elemento software con informazioni sulla condizione o sulla posizione che possono essere richieste da una funzionalità.</span><span class="sxs-lookup"><span data-stu-id="e5b08-685">The [**CIM\_SoftwareElementChecks**](cim-softwareelementchecks.md) association class relates a software element with condition or location information that a feature may require.</span></span>

</dd> <dt>

[<span data-ttu-id="e5b08-686">**\_SOFTWAREELEMENTVERSIONCHECK CIM**</span><span class="sxs-lookup"><span data-stu-id="e5b08-686">**CIM\_SoftwareElementVersionCheck**</span></span>](cim-softwareelementversioncheck.md)
</dt> <dd>

<span data-ttu-id="e5b08-687">La classe [**CIM \_ SoftwareElementVersionCheck**](cim-softwareelementversioncheck.md) rappresenta un tipo di elemento software che deve esistere nell'ambiente.</span><span class="sxs-lookup"><span data-stu-id="e5b08-687">The [**CIM\_SoftwareElementVersionCheck**](cim-softwareelementversioncheck.md) class represents a type of software element that must exist in the environment.</span></span>

</dd> <dt>

[<span data-ttu-id="e5b08-688">**\_SoftwareFeature CIM**</span><span class="sxs-lookup"><span data-stu-id="e5b08-688">**CIM\_SoftwareFeature**</span></span>](cim-softwarefeature.md)
</dt> <dd>

<span data-ttu-id="e5b08-689">La classe [**CIM \_ SoftwareFeature**](cim-softwarefeature.md) rappresenta una funzione o una funzionalità specifica di un prodotto o di un sistema applicativo.</span><span class="sxs-lookup"><span data-stu-id="e5b08-689">The [**CIM\_SoftwareFeature**](cim-softwarefeature.md) class represents a particular function or capability of a product or application system.</span></span>

</dd> <dt>

[<span data-ttu-id="e5b08-690">**\_SOFTWAREFEATURESAPIMPLEMENTATION CIM**</span><span class="sxs-lookup"><span data-stu-id="e5b08-690">**CIM\_SoftwareFeatureSAPImplementation**</span></span>](cim-softwarefeaturesapimplementation.md)
</dt> <dd>

<span data-ttu-id="e5b08-691">La classe [**CIM \_ SoftwareFeatureSAPImplementation**](cim-softwarefeaturesapimplementation.md) rappresenta un'associazione tra un punto di accesso al servizio (SAP) e il modo in cui viene implementato nel software.</span><span class="sxs-lookup"><span data-stu-id="e5b08-691">The [**CIM\_SoftwareFeatureSAPImplementation**](cim-softwarefeaturesapimplementation.md) class represents an association between a service access point (SAP) and how it is implemented in software.</span></span>

</dd> <dt>

[<span data-ttu-id="e5b08-692">**\_SOFTWAREFEATURESERVICEIMPLEMENTATION CIM**</span><span class="sxs-lookup"><span data-stu-id="e5b08-692">**CIM\_SoftwareFeatureServiceImplementation**</span></span>](cim-softwarefeatureserviceimplementation.md)
</dt> <dd>

<span data-ttu-id="e5b08-693">La classe [**CIM \_ SoftwareFeatureServiceImplementation**](cim-softwarefeatureserviceimplementation.md) rappresenta un'associazione tra un servizio e il modo in cui viene implementata nel software.</span><span class="sxs-lookup"><span data-stu-id="e5b08-693">The [**CIM\_SoftwareFeatureServiceImplementation**](cim-softwarefeatureserviceimplementation.md) class represents an association between a service and how it is implemented in software.</span></span>

</dd> <dt>

[<span data-ttu-id="e5b08-694">**\_SOFTWAREFEATURESOFTWAREELEMENTS CIM**</span><span class="sxs-lookup"><span data-stu-id="e5b08-694">**CIM\_SoftwareFeatureSoftwareElements**</span></span>](cim-softwarefeaturesoftwareelements.md)
</dt> <dd>

<span data-ttu-id="e5b08-695">L'associazione [**CIM \_ SoftwareFeatureSoftwareElements**](cim-softwarefeaturesoftwareelements.md) identifica gli elementi software che costituiscono una funzionalità software specifica.</span><span class="sxs-lookup"><span data-stu-id="e5b08-695">The [**CIM\_SoftwareFeatureSoftwareElements**](cim-softwarefeaturesoftwareelements.md) association identifies the software elements that make up a specific software feature.</span></span>

</dd> <dt>

[<span data-ttu-id="e5b08-696">**\_SPAREGROUP CIM**</span><span class="sxs-lookup"><span data-stu-id="e5b08-696">**CIM\_SpareGroup**</span></span>](cim-sparegroup.md)
</dt> <dd>

<span data-ttu-id="e5b08-697">La classe [**CIM \_ SpareGroup**](cim-sparegroup.md) è derivata dalla classe [**CIM \_ RedundancyGroup**](cim-redundancygroup.md) e indica che uno o più elementi aggregati possono essere risparmiati.</span><span class="sxs-lookup"><span data-stu-id="e5b08-697">The [**CIM\_SpareGroup**](cim-sparegroup.md) class is derived from the [**CIM\_RedundancyGroup**](cim-redundancygroup.md) class and indicates that one or more of the aggregated elements can be spared.</span></span>

</dd> <dt>

[<span data-ttu-id="e5b08-698">**\_STATISTICALINFORMATION CIM**</span><span class="sxs-lookup"><span data-stu-id="e5b08-698">**CIM\_StatisticalInformation**</span></span>](cim-statisticalinformation.md)
</dt> <dd>

<span data-ttu-id="e5b08-699">La classe [**CIM \_ StatisticalInformation**](cim-statisticalinformation.md) è una classe radice per la raccolta arbitraria di dati statistici o metriche applicabili a uno o più elementi di sistema gestiti.</span><span class="sxs-lookup"><span data-stu-id="e5b08-699">The [**CIM\_StatisticalInformation**](cim-statisticalinformation.md) class is a root class for the arbitrary collection of statistical data or metrics applicable to one or more managed system elements.</span></span>

</dd> <dt>

[<span data-ttu-id="e5b08-700">**\_Statistiche CIM**</span><span class="sxs-lookup"><span data-stu-id="e5b08-700">**CIM\_Statistics**</span></span>](cim-statistics.md)
</dt> <dd>

<span data-ttu-id="e5b08-701">La classe [**CIM \_ Statistics**](cim-statistics.md) rappresenta un'associazione che mette in correlazione gli elementi di sistema gestiti ai gruppi statistici che vi si applicano.</span><span class="sxs-lookup"><span data-stu-id="e5b08-701">The [**CIM\_Statistics**](cim-statistics.md) class represents an association that relates managed system elements to the statistical groups that apply to them.</span></span>

</dd> <dt>

[<span data-ttu-id="e5b08-702">**\_STORAGEDEFECT CIM**</span><span class="sxs-lookup"><span data-stu-id="e5b08-702">**CIM\_StorageDefect**</span></span>](cim-storagedefect.md)
</dt> <dd>

<span data-ttu-id="e5b08-703">L'aggregazione [**CIM \_ StorageDefect**](cim-storagedefect.md) raccoglie gli errori di archiviazione per un extent di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="e5b08-703">The [**CIM\_StorageDefect**](cim-storagedefect.md) aggregation collects the storage errors for a storage extent.</span></span>

</dd> <dt>

[<span data-ttu-id="e5b08-704">**\_STORAGEERROR CIM**</span><span class="sxs-lookup"><span data-stu-id="e5b08-704">**CIM\_StorageError**</span></span>](cim-storageerror.md)
</dt> <dd>

<span data-ttu-id="e5b08-705">La classe [**CIM \_ StorageError**](cim-storageerror.md) rappresenta i blocchi di supporti o di spazio di memoria di cui è stato eseguito il mapping fuori uso a causa di errori.</span><span class="sxs-lookup"><span data-stu-id="e5b08-705">The [**CIM\_StorageError**](cim-storageerror.md) class represents blocks of media or memory space that are mapped out-of-use due to errors.</span></span> <span data-ttu-id="e5b08-706">La chiave della classe è la proprietà **IndirizzoIniziale** dei byte in errore.</span><span class="sxs-lookup"><span data-stu-id="e5b08-706">The key of the class is the **StartingAddress** property of the bytes in error.</span></span>

</dd> <dt>

[<span data-ttu-id="e5b08-707">**\_STORAGEEXTENT CIM**</span><span class="sxs-lookup"><span data-stu-id="e5b08-707">**CIM\_StorageExtent**</span></span>](cim-storageextent.md)
</dt> <dd>

<span data-ttu-id="e5b08-708">La classe [**CIM \_ StorageExtent**](cim-storageextent.md) rappresenta le funzionalità e la gestione dei diversi supporti esistenti per archiviare i dati e consentire il recupero dei dati.</span><span class="sxs-lookup"><span data-stu-id="e5b08-708">The [**CIM\_StorageExtent**](cim-storageextent.md) class represents the capabilities and management of the various media that exist to store data and allow data retrieval.</span></span> <span data-ttu-id="e5b08-709">Questa classe padre può rappresentare i vari componenti di RAID (hardware o software) o un'estensione logica non elaborata in un supporto fisico.</span><span class="sxs-lookup"><span data-stu-id="e5b08-709">This parent class can represent the various components of RAID (hardware or software) or a raw logical extent on top of physical media.</span></span>

</dd> <dt>

[<span data-ttu-id="e5b08-710">**\_STORAGEREDUNDANCYGROUP CIM**</span><span class="sxs-lookup"><span data-stu-id="e5b08-710">**CIM\_StorageRedundancyGroup**</span></span>](cim-storageredundancygroup.md)
</dt> <dd>

<span data-ttu-id="e5b08-711">La classe [**CIM \_ StorageRedundancyGroup**](cim-storageredundancygroup.md) rappresenta informazioni di ridondanza relative all'archiviazione di massa.</span><span class="sxs-lookup"><span data-stu-id="e5b08-711">The [**CIM\_StorageRedundancyGroup**](cim-storageredundancygroup.md) class represents mass storage-related redundancy information.</span></span>

</dd> <dt>

[<span data-ttu-id="e5b08-712">**\_SUPPORTACCESS CIM**</span><span class="sxs-lookup"><span data-stu-id="e5b08-712">**CIM\_SupportAccess**</span></span>](cim-supportaccess.md)
</dt> <dd>

<span data-ttu-id="e5b08-713">La classe [**CIM \_ SupportAccess**](cim-supportaccess.md) definisce come ottenere assistenza per un prodotto.</span><span class="sxs-lookup"><span data-stu-id="e5b08-713">The [**CIM\_SupportAccess**](cim-supportaccess.md) class defines how to obtain assistance for a product.</span></span>

</dd> <dt>

[<span data-ttu-id="e5b08-714">**\_SWAPSPACECHECK CIM**</span><span class="sxs-lookup"><span data-stu-id="e5b08-714">**CIM\_SwapSpaceCheck**</span></span>](cim-swapspacecheck.md)
</dt> <dd>

<span data-ttu-id="e5b08-715">La classe [**CIM \_ SwapSpaceCheck**](cim-swapspacecheck.md) specifica la quantità di spazio di swapping che deve essere disponibile nel sistema.</span><span class="sxs-lookup"><span data-stu-id="e5b08-715">The [**CIM\_SwapSpaceCheck**](cim-swapspacecheck.md) class specifies the amount of swap space that must be available on the system.</span></span>

</dd> <dt>

[<span data-ttu-id="e5b08-716">**\_Sistema CIM**</span><span class="sxs-lookup"><span data-stu-id="e5b08-716">**CIM\_System**</span></span>](cim-system.md)
</dt> <dd>

<span data-ttu-id="e5b08-717">La classe di [**\_ sistema CIM**](cim-system.md) aggrega un set enumerabile di elementi di sistema gestiti.</span><span class="sxs-lookup"><span data-stu-id="e5b08-717">The [**CIM\_System**](cim-system.md) class aggregates an enumerable set of managed system elements.</span></span> <span data-ttu-id="e5b08-718">L'aggregazione funziona come un intero funzionale.</span><span class="sxs-lookup"><span data-stu-id="e5b08-718">The aggregation operates as a functional whole.</span></span> <span data-ttu-id="e5b08-719">All'interno di una sottoclasse particolare del sistema è presente un elenco ben definito di classi di elementi di sistema gestite le cui istanze devono essere aggregate.</span><span class="sxs-lookup"><span data-stu-id="e5b08-719">Within any particular subclass of the system, there is a well-defined list of managed system element classes whose instances must be aggregated.</span></span>

</dd> <dt>

[<span data-ttu-id="e5b08-720">**\_SYSTEMCOMPONENT CIM**</span><span class="sxs-lookup"><span data-stu-id="e5b08-720">**CIM\_SystemComponent**</span></span>](cim-systemcomponent.md)
</dt> <dd>

<span data-ttu-id="e5b08-721">classe di associazione Common Information Model (CIM) che stabilisce le relazioni tra un sistema e gli elementi del sistema gestito di cui è composto.</span><span class="sxs-lookup"><span data-stu-id="e5b08-721">a Common Information Model (CIM) association class that establishes relationships between a system and the managed system elements of which it is composed.</span></span>

</dd> <dt>

[<span data-ttu-id="e5b08-722">**\_SYSTEMDEVICE CIM**</span><span class="sxs-lookup"><span data-stu-id="e5b08-722">**CIM\_SystemDevice**</span></span>](cim-systemdevice.md)
</dt> <dd>

<span data-ttu-id="e5b08-723">L'associazione [**CIM \_ SystemDevice**](cim-systemdevice.md) rappresenta una relazione esplicita in cui i dispositivi logici possono essere aggregati da un sistema.</span><span class="sxs-lookup"><span data-stu-id="e5b08-723">The [**CIM\_SystemDevice**](cim-systemdevice.md) association represents an explicit relationship in which logical devices can be aggregated by a system.</span></span>

</dd> <dt>

[<span data-ttu-id="e5b08-724">**\_SYSTEMRESOURCE CIM**</span><span class="sxs-lookup"><span data-stu-id="e5b08-724">**CIM\_SystemResource**</span></span>](cim-systemresource.md)
</dt> <dd>

<span data-ttu-id="e5b08-725">La classe [**CIM \_ SystemResource**](cim-systemresource.md) rappresenta un'entità gestita dal BIOS o un sistema operativo che è disponibile per l'uso da parte di software e dispositivi logici.</span><span class="sxs-lookup"><span data-stu-id="e5b08-725">The [**CIM\_SystemResource**](cim-systemresource.md) class represents an entity managed by BIOS, or an operating system that is available for use by software and logical devices.</span></span>

</dd> <dt>

[<span data-ttu-id="e5b08-726">**\_Contagiri CIM**</span><span class="sxs-lookup"><span data-stu-id="e5b08-726">**CIM\_Tachometer**</span></span>](cim-tachometer.md)
</dt> <dd>

<span data-ttu-id="e5b08-727">La classe [**CIM \_ contagiri**](cim-tachometer.md) esiste per la compatibilità con le versioni precedenti delle definizioni dello schema CIM.</span><span class="sxs-lookup"><span data-stu-id="e5b08-727">The [**CIM\_Tachometer**](cim-tachometer.md) class exists for backward compatibility with earlier CIM schema definitions.</span></span>

</dd> <dt>

[<span data-ttu-id="e5b08-728">**\_TAPEDRIVE CIM**</span><span class="sxs-lookup"><span data-stu-id="e5b08-728">**CIM\_TapeDrive**</span></span>](cim-tapedrive.md)
</dt> <dd>

<span data-ttu-id="e5b08-729">La classe [**CIM \_ TapeDrive**](cim-tapedrive.md) rappresenta un'unità nastro nel sistema.</span><span class="sxs-lookup"><span data-stu-id="e5b08-729">The [**CIM\_TapeDrive**](cim-tapedrive.md) class represents a tape drive on the system.</span></span> <span data-ttu-id="e5b08-730">Le unità nastro si distinguono principalmente in quanto è possibile accedervi solo in modo sequenziale.</span><span class="sxs-lookup"><span data-stu-id="e5b08-730">Tape drives are primarily distinguished in that they can only be accessed sequentially.</span></span>

</dd> <dt>

[<span data-ttu-id="e5b08-731">**\_Sensore CIM**</span><span class="sxs-lookup"><span data-stu-id="e5b08-731">**CIM\_TemperatureSensor**</span></span>](cim-temperaturesensor.md)
</dt> <dd>

<span data-ttu-id="e5b08-732">La classe [**CIM \_ sensore**](cim-temperaturesensor.md) esiste per la compatibilità con le versioni precedenti delle definizioni dello schema CIM.</span><span class="sxs-lookup"><span data-stu-id="e5b08-732">The [**CIM\_TemperatureSensor**](cim-temperaturesensor.md) class exists for backward compatibility with earlier CIM schema definitions.</span></span>

</dd> <dt>

[<span data-ttu-id="e5b08-733">**\_Thread CIM**</span><span class="sxs-lookup"><span data-stu-id="e5b08-733">**CIM\_Thread**</span></span>](cim-thread.md)
</dt> <dd>

<span data-ttu-id="e5b08-734">La classe di [**\_ thread CIM**](cim-thread.md) rappresenta la possibilità di eseguire unità di un processo o di un'attività, in parallelo.</span><span class="sxs-lookup"><span data-stu-id="e5b08-734">The [**CIM\_Thread**](cim-thread.md) class represents the ability to execute units of a process or task, in parallel.</span></span> <span data-ttu-id="e5b08-735">Un processo può avere molti thread, ognuno dei quali è debole per il processo.</span><span class="sxs-lookup"><span data-stu-id="e5b08-735">A process can have many threads, each of which is weak to the process.</span></span>

</dd> <dt>

[<span data-ttu-id="e5b08-736">**\_TODIRECTORYACTION CIM**</span><span class="sxs-lookup"><span data-stu-id="e5b08-736">**CIM\_ToDirectoryAction**</span></span>](cim-todirectoryaction.md)
</dt> <dd>

<span data-ttu-id="e5b08-737">L'associazione [**CIM \_ ToDirectoryAction**](cim-todirectoryaction.md) identifica la directory di destinazione per l'azione del file.</span><span class="sxs-lookup"><span data-stu-id="e5b08-737">The [**CIM\_ToDirectoryAction**](cim-todirectoryaction.md) association identifies the target directory for the file action.</span></span>

</dd> <dt>

[<span data-ttu-id="e5b08-738">**\_TODIRECTORYSPECIFICATION CIM**</span><span class="sxs-lookup"><span data-stu-id="e5b08-738">**CIM\_ToDirectorySpecification**</span></span>](cim-todirectoryspecification.md)
</dt> <dd>

<span data-ttu-id="e5b08-739">L'associazione [**CIM \_ ToDirectorySpecification**](cim-todirectoryspecification.md) identifica la directory di destinazione per l'azione del file.</span><span class="sxs-lookup"><span data-stu-id="e5b08-739">The [**CIM\_ToDirectorySpecification**](cim-todirectoryspecification.md) association identifies the target directory for the file action.</span></span>

</dd> <dt>

[<span data-ttu-id="e5b08-740">**\_UNINTERRUPTIBLEPOWERSUPPLY CIM**</span><span class="sxs-lookup"><span data-stu-id="e5b08-740">**CIM\_UninterruptiblePowerSupply**</span></span>](cim-uninterruptiblepowersupply.md)
</dt> <dd>

<span data-ttu-id="e5b08-741">La classe [**CIM \_ UninterruptiblePowerSupply**](cim-uninterruptiblepowersupply.md) rappresenta le funzionalità e la gestione di un gruppo di continuità (UPS, Power Supply).</span><span class="sxs-lookup"><span data-stu-id="e5b08-741">The [**CIM\_UninterruptiblePowerSupply**](cim-uninterruptiblepowersupply.md) class represents the capabilities and management of an uninterruptible power supply (UPS).</span></span>

</dd> <dt>

[<span data-ttu-id="e5b08-742">**\_UNITARYCOMPUTERSYSTEM CIM**</span><span class="sxs-lookup"><span data-stu-id="e5b08-742">**CIM\_UnitaryComputerSystem**</span></span>](cim-unitarycomputersystem.md)
</dt> <dd>

<span data-ttu-id="e5b08-743">La classe [**CIM \_ UnitaryComputerSystem**](cim-unitarycomputersystem.md) rappresenta un computer desktop, mobile, di rete, un server o un altro tipo di computer a nodo singolo.</span><span class="sxs-lookup"><span data-stu-id="e5b08-743">The [**CIM\_UnitaryComputerSystem**](cim-unitarycomputersystem.md) class represents a desktop, mobile, network computer, server, or other type of single-node computer system.</span></span>

</dd> <dt>

[<span data-ttu-id="e5b08-744">**\_USBCONTROLLER CIM**</span><span class="sxs-lookup"><span data-stu-id="e5b08-744">**CIM\_USBController**</span></span>](cim-usbcontroller.md)
</dt> <dd>

<span data-ttu-id="e5b08-745">La classe [**CIM \_ USBController**](cim-usbcontroller.md) rappresenta le funzionalità e la gestione di un controller USB.</span><span class="sxs-lookup"><span data-stu-id="e5b08-745">The [**CIM\_USBController**](cim-usbcontroller.md) class represents the capabilities and management of a USB controller.</span></span>

</dd> <dt>

[<span data-ttu-id="e5b08-746">**\_USBCONTROLLERHASHUB CIM**</span><span class="sxs-lookup"><span data-stu-id="e5b08-746">**CIM\_USBControllerHasHub**</span></span>](cim-usbcontrollerhashub.md)
</dt> <dd>

<span data-ttu-id="e5b08-747">La classe [**CIM \_ USBControllerHasHub**](cim-usbcontrollerhashub.md) definisce gli hub a valle del controller USB.</span><span class="sxs-lookup"><span data-stu-id="e5b08-747">The [**CIM\_USBControllerHasHub**](cim-usbcontrollerhashub.md) class defines the hubs that are downstream of the USB controller.</span></span>

</dd> <dt>

[<span data-ttu-id="e5b08-748">**\_USBDEVICE CIM**</span><span class="sxs-lookup"><span data-stu-id="e5b08-748">**CIM\_USBDevice**</span></span>](cim-usbdevice.md)
</dt> <dd>

<span data-ttu-id="e5b08-749">La classe [**CIM \_ usbdevice**](cim-usbdevice.md) rappresenta le caratteristiche di gestione di un dispositivo USB.</span><span class="sxs-lookup"><span data-stu-id="e5b08-749">The [**CIM\_USBDevice**](cim-usbdevice.md) class represents the management characteristics of a USB device.</span></span>

</dd> <dt>

[<span data-ttu-id="e5b08-750">**\_Usbhub CIM**</span><span class="sxs-lookup"><span data-stu-id="e5b08-750">**CIM\_USBHub**</span></span>](cim-usbhub.md)
</dt> <dd>

<span data-ttu-id="e5b08-751">La classe [**CIM \_ USBHub**](cim-usbhub.md) rappresenta le funzionalità e la gestione di un hub USB.</span><span class="sxs-lookup"><span data-stu-id="e5b08-751">The [**CIM\_USBHub**](cim-usbhub.md) class represents the capabilities and management of a USB hub.</span></span>

</dd> <dt>

[<span data-ttu-id="e5b08-752">**\_USERDEVICE CIM**</span><span class="sxs-lookup"><span data-stu-id="e5b08-752">**CIM\_UserDevice**</span></span>](cim-userdevice.md)
</dt> <dd>

<span data-ttu-id="e5b08-753">La classe [**CIM \_ UserDevice**](cim-userdevice.md) è una classe padre da cui discendono altre classi, ad esempio [**CIM \_ Keyboard**](cim-keyboard.md) o [**CIM \_ DesktopMonitor**](cim-desktopmonitor.md).</span><span class="sxs-lookup"><span data-stu-id="e5b08-753">The [**CIM\_UserDevice**](cim-userdevice.md) class is a parent class from which other classes, such as [**CIM\_Keyboard**](cim-keyboard.md) or [**CIM\_DesktopMonitor**](cim-desktopmonitor.md), descend.</span></span> <span data-ttu-id="e5b08-754">I dispositivi utente sono dispositivi logici che consentono all'utente di un sistema informatico di immettere, visualizzare o ascoltare i dati.</span><span class="sxs-lookup"><span data-stu-id="e5b08-754">User devices are logical devices that allow a computer system's user to input, view, or hear data.</span></span>

</dd> <dt>

[<span data-ttu-id="e5b08-755">**\_VERSIONCOMPATIBILITYCHECK CIM**</span><span class="sxs-lookup"><span data-stu-id="e5b08-755">**CIM\_VersionCompatibilityCheck**</span></span>](cim-versioncompatibilitycheck.md)
</dt> <dd>

<span data-ttu-id="e5b08-756">La classe [**CIM \_ VersionCompatibilityCheck**](cim-versioncompatibilitycheck.md) specifica se è consentito creare lo stato successivo di un elemento software.</span><span class="sxs-lookup"><span data-stu-id="e5b08-756">The [**CIM\_VersionCompatibilityCheck**](cim-versioncompatibilitycheck.md) class specifies whether it is permissible to create the next state of a software element.</span></span>

</dd> <dt>

[<span data-ttu-id="e5b08-757">**\_VIDEOBIOSELEMENT CIM**</span><span class="sxs-lookup"><span data-stu-id="e5b08-757">**CIM\_VideoBIOSElement**</span></span>](cim-videobioselement.md)
</dt> <dd>

<span data-ttu-id="e5b08-758">La classe [**CIM \_ VideoBIOSElement**](cim-videobioselement.md) rappresenta il software di basso livello che viene caricato in un archivio non volatile e utilizzato per configurare e accedere al controller video e alla visualizzazione di un sistema di computer.</span><span class="sxs-lookup"><span data-stu-id="e5b08-758">The [**CIM\_VideoBIOSElement**](cim-videobioselement.md) class represents the low-level software that is loaded into non-volatile storage and used to configure and access a computer system's video controller and display.</span></span>

</dd> <dt>

[<span data-ttu-id="e5b08-759">**\_VIDEOBIOSFEATURE CIM**</span><span class="sxs-lookup"><span data-stu-id="e5b08-759">**CIM\_VideoBIOSFeature**</span></span>](cim-videobiosfeature.md)
</dt> <dd>

<span data-ttu-id="e5b08-760">La classe [**CIM \_ VideoBIOSFeature**](cim-videobiosfeature.md) rappresenta le funzionalità del software di basso livello utilizzato per configurare e accedere al controller video e alla visualizzazione di un sistema di computer.</span><span class="sxs-lookup"><span data-stu-id="e5b08-760">The [**CIM\_VideoBIOSFeature**](cim-videobiosfeature.md) class represents the capabilities of the low-level software used to configure and access a computer system's video controller and display.</span></span>

</dd> <dt>

[<span data-ttu-id="e5b08-761">**\_VIDEOBIOSFEATUREVIDEOBIOSELEMENTS CIM**</span><span class="sxs-lookup"><span data-stu-id="e5b08-761">**CIM\_VideoBIOSFeatureVideoBIOSElements**</span></span>](cim-videobiosfeaturevideobioselements.md)
</dt> <dd>

<span data-ttu-id="e5b08-762">La classe [**CIM \_ VideoBIOSFeatureVideoBIOSElements**](cim-videobiosfeaturevideobioselements.md) associa una funzionalità BIOS video e i relativi elementi BIOS video aggregati.</span><span class="sxs-lookup"><span data-stu-id="e5b08-762">The [**CIM\_VideoBIOSFeatureVideoBIOSElements**](cim-videobiosfeaturevideobioselements.md) class associates a video BIOS feature and its aggregated video BIOS elements.</span></span>

</dd> <dt>

[<span data-ttu-id="e5b08-763">**\_VIDEOCONTROLLER CIM**</span><span class="sxs-lookup"><span data-stu-id="e5b08-763">**CIM\_VideoController**</span></span>](cim-videocontroller.md)
</dt> <dd>

<span data-ttu-id="e5b08-764">La classe [**CIM \_ VideoController**](cim-videocontroller.md) rappresenta le funzionalità e la gestione del controller video.</span><span class="sxs-lookup"><span data-stu-id="e5b08-764">The [**CIM\_VideoController**](cim-videocontroller.md) class represents the capabilities and management of the video controller.</span></span>

</dd> <dt>

[<span data-ttu-id="e5b08-765">**\_VIDEOCONTROLLERRESOLUTION CIM**</span><span class="sxs-lookup"><span data-stu-id="e5b08-765">**CIM\_VideoControllerResolution**</span></span>](cim-videocontrollerresolution.md)
</dt> <dd>

<span data-ttu-id="e5b08-766">La classe [**CIM \_ VideoControllerResolution**](cim-videocontrollerresolution.md) rappresenta le varie modalità video che un controller video può supportare.</span><span class="sxs-lookup"><span data-stu-id="e5b08-766">The [**CIM\_VideoControllerResolution**](cim-videocontrollerresolution.md) class represents the various video modes that a video controller can support.</span></span>

</dd> <dt>

[<span data-ttu-id="e5b08-767">**\_VIDEOSETTING CIM**</span><span class="sxs-lookup"><span data-stu-id="e5b08-767">**CIM\_VideoSetting**</span></span>](cim-videosetting.md)
</dt> <dd>

<span data-ttu-id="e5b08-768">La classe [**CIM \_ VideoSetting**](cim-videosetting.md) associa l'oggetto impostazione [**\_ VideoControllerResolution CIM**](cim-videocontrollerresolution.md) al controller a cui si applica.</span><span class="sxs-lookup"><span data-stu-id="e5b08-768">The [**CIM\_VideoSetting**](cim-videosetting.md) class associates the [**CIM\_VideoControllerResolution**](cim-videocontrollerresolution.md) setting object with the controller to which it applies.</span></span>

</dd> <dt>

[<span data-ttu-id="e5b08-769">**\_VOLATILESTORAGE CIM**</span><span class="sxs-lookup"><span data-stu-id="e5b08-769">**CIM\_VolatileStorage**</span></span>](cim-volatilestorage.md)
</dt> <dd>

<span data-ttu-id="e5b08-770">La classe [**CIM \_ VolatileStorage**](cim-volatilestorage.md) rappresenta le funzionalità e la gestione dell'archiviazione volatile.</span><span class="sxs-lookup"><span data-stu-id="e5b08-770">The [**CIM\_VolatileStorage**](cim-volatilestorage.md) class represents the capabilities and management of volatile storage.</span></span>

</dd> <dt>

[<span data-ttu-id="e5b08-771">**\_Sensore CIM**</span><span class="sxs-lookup"><span data-stu-id="e5b08-771">**CIM\_VoltageSensor**</span></span>](cim-voltagesensor.md)
</dt> <dd>

<span data-ttu-id="e5b08-772">La classe [**CIM \_ sensore**](cim-voltagesensor.md) esiste per compatibilità con le versioni precedenti delle definizioni dello schema CIM.</span><span class="sxs-lookup"><span data-stu-id="e5b08-772">The [**CIM\_VoltageSensor**](cim-voltagesensor.md) class exists for backward compatibility to earlier CIM schema definitions.</span></span> <span data-ttu-id="e5b08-773">Con aggiunte alle classi CIM [**\_ Sensor**](cim-sensor.md) e [**cim \_ NumericSensor**](cim-numericsensor.md) nella versione 2,2, non è più necessario.</span><span class="sxs-lookup"><span data-stu-id="e5b08-773">With additions to the [**CIM\_Sensor**](cim-sensor.md) and [**CIM\_NumericSensor**](cim-numericsensor.md) classes in version 2.2, it is no longer necessary.</span></span>

</dd> <dt>

[<span data-ttu-id="e5b08-774">**\_Volume del volume CIM**</span><span class="sxs-lookup"><span data-stu-id="e5b08-774">**CIM\_VolumeSet**</span></span>](cim-volumeset.md)
</dt> <dd>

<span data-ttu-id="e5b08-775">La classe [**CIM \_ volumet**](cim-volumeset.md) rappresenta un intervallo contiguo di blocchi logici presentati all'ambiente operativo per la lettura e la scrittura di dati utente.</span><span class="sxs-lookup"><span data-stu-id="e5b08-775">The [**CIM\_VolumeSet**](cim-volumeset.md) class represents a contiguous range of logical blocks presented to the operating environment for reading and writing user data.</span></span>

</dd> <dt>

[<span data-ttu-id="e5b08-776">**\_Wormdrive CIM**</span><span class="sxs-lookup"><span data-stu-id="e5b08-776">**CIM\_WORMDrive**</span></span>](cim-wormdrive.md)
</dt> <dd>

<span data-ttu-id="e5b08-777">La classe [**CIM \_ WORMDrive**](cim-wormdrive.md) rappresenta le funzionalità e la gestione di un'unità worm, un sottotipo del dispositivo di accesso multimediale.</span><span class="sxs-lookup"><span data-stu-id="e5b08-777">The [**CIM\_WORMDrive**](cim-wormdrive.md) class represents the capabilities and management of a WORM drive, a subtype of the media access device.</span></span>

</dd> </dl>

 

 
