---
description: Descrive un set di classi con le proprietà e i metodi richiesti, necessari per gestire un'entità reale o per supportare uno scenario di utilizzo, in modo interoperativo.
ms.assetid: 75644856-3B47-43B8-835C-783A6BEE7251
title: Classe Msvm_RegisteredProfile
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_RegisteredProfile
- Msvm_RegisteredProfile.InstanceID
- Msvm_RegisteredProfile.Caption
- Msvm_RegisteredProfile.Description
- Msvm_RegisteredProfile.ElementName
- Msvm_RegisteredProfile.RegisteredOrganization
- Msvm_RegisteredProfile.OtherRegisteredOrganization
- Msvm_RegisteredProfile.RegisteredName
- Msvm_RegisteredProfile.RegisteredVersion
- Msvm_RegisteredProfile.AdvertiseTypes
- Msvm_RegisteredProfile.AdvertiseTypeDescriptions
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: a7014687355524fbe10ff01869cac6c3fd35a894
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104050083"
---
# <a name="msvm_registeredprofile-class"></a><span data-ttu-id="e71b0-103">\_Classe MSVM RegisteredProfile</span><span class="sxs-lookup"><span data-stu-id="e71b0-103">Msvm\_RegisteredProfile class</span></span>

<span data-ttu-id="e71b0-104">Descrive un set di classi con le proprietà e i metodi richiesti, necessari per gestire un'entità reale o per supportare uno scenario di utilizzo, in modo interoperativo.</span><span class="sxs-lookup"><span data-stu-id="e71b0-104">Describes a set of classes with required properties and methods, necessary to manage a real-world entity or to support a usage scenario, in an interoperable fashion.</span></span>

<span data-ttu-id="e71b0-105">La sintassi seguente è semplificata Managed Object Format codice (MOF) e include tutte le proprietà ereditate.</span><span class="sxs-lookup"><span data-stu-id="e71b0-105">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="e71b0-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="e71b0-106">Syntax</span></span>

``` syntax
class Msvm_RegisteredProfile : CIM_RegisteredProfile
{
  string InstanceID;
  string Caption;
  string Description;
  string ElementName;
  uint16 RegisteredOrganization;
  string OtherRegisteredOrganization;
  string RegisteredName;
  string RegisteredVersion;
  uint16 AdvertiseTypes[];
  string AdvertiseTypeDescriptions[];
};
```

## <a name="members"></a><span data-ttu-id="e71b0-107">Members</span><span class="sxs-lookup"><span data-stu-id="e71b0-107">Members</span></span>

<span data-ttu-id="e71b0-108">La **classe \_ RegisteredProfile di MSVM** dispone di questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="e71b0-108">The **Msvm\_RegisteredProfile** class has these types of members:</span></span>

-   [<span data-ttu-id="e71b0-109">Proprietà</span><span class="sxs-lookup"><span data-stu-id="e71b0-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="e71b0-110">Proprietà</span><span class="sxs-lookup"><span data-stu-id="e71b0-110">Properties</span></span>

<span data-ttu-id="e71b0-111">La **classe \_ RegisteredProfile di MSVM** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="e71b0-111">The **Msvm\_RegisteredProfile** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="e71b0-112">**AdvertiseTypeDescriptions**</span><span class="sxs-lookup"><span data-stu-id="e71b0-112">**AdvertiseTypeDescriptions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e71b0-113">Tipo di dati: matrice di **stringhe**</span><span class="sxs-lookup"><span data-stu-id="e71b0-113">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="e71b0-114">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="e71b0-114">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e71b0-115">Matrice di stringhe che fornisce informazioni aggiuntive correlate alla proprietà **AdvertiseType** .</span><span class="sxs-lookup"><span data-stu-id="e71b0-115">An array of strings that provides additional information related to the **AdvertiseType** property.</span></span> <span data-ttu-id="e71b0-116">Una descrizione deve essere specificata quando **AdvertiseType** è 1 (other).</span><span class="sxs-lookup"><span data-stu-id="e71b0-116">A description must be provided when the **AdvertiseType** is 1 (Other).</span></span> <span data-ttu-id="e71b0-117">Una voce in questa matrice corrisponde allo stesso indice nella matrice **AdvertiseTypes** .</span><span class="sxs-lookup"><span data-stu-id="e71b0-117">An entry in this array corresponds to the same index in the **AdvertiseTypes** array.</span></span> <span data-ttu-id="e71b0-118">Questa proprietà viene ereditata da [**CIM \_ RegisteredProfile**](/previous-versions//ee309375(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="e71b0-118">This property is inherited from [**CIM\_RegisteredProfile**](/previous-versions//ee309375(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="e71b0-119">**AdvertiseTypes**</span><span class="sxs-lookup"><span data-stu-id="e71b0-119">**AdvertiseTypes**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e71b0-120">Tipo di dati: matrice **UInt16**</span><span class="sxs-lookup"><span data-stu-id="e71b0-120">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="e71b0-121">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="e71b0-121">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e71b0-122">Specifica l'annuncio per le informazioni sul profilo.</span><span class="sxs-lookup"><span data-stu-id="e71b0-122">Specifies the advertisement for the profile information.</span></span> <span data-ttu-id="e71b0-123">Viene usato dai servizi pubblicitari dell'infrastruttura WBEM per determinare gli elementi da pubblicizzare, attraverso i meccanismi.</span><span class="sxs-lookup"><span data-stu-id="e71b0-123">It is used by the advertising services of the WBEM infrastructure to determine what should be advertised, through what mechanisms.</span></span> <span data-ttu-id="e71b0-124">La proprietà è una matrice in modo che sia possibile annunciare il profilo utilizzando diversi meccanismi.</span><span class="sxs-lookup"><span data-stu-id="e71b0-124">The property is an array so that the profile can be advertised using several mechanisms.</span></span> <span data-ttu-id="e71b0-125">Se questa proprietà è **null**, equivale a specificare il valore 2 (non annunciato).</span><span class="sxs-lookup"><span data-stu-id="e71b0-125">If this property is **Null**, this is equivalent to specifying the value 2 (Not Advertised).</span></span> <span data-ttu-id="e71b0-126">Questa proprietà viene ereditata da [**CIM \_ RegisteredProfile**](/previous-versions//ee309375(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="e71b0-126">This property is inherited from [**CIM\_RegisteredProfile**](/previous-versions//ee309375(v=vs.85)).</span></span>

<dl> <dt>

<span data-ttu-id="e71b0-127"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Altro** (1)</span><span class="sxs-lookup"><span data-stu-id="e71b0-127"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>
</dt> <dt>

<span data-ttu-id="e71b0-128"><span id="Not_Advertised"></span><span id="not_advertised"></span><span id="NOT_ADVERTISED"></span>**Non pubblicizzato** (2)</span><span class="sxs-lookup"><span data-stu-id="e71b0-128"><span id="Not_Advertised"></span><span id="not_advertised"></span><span id="NOT_ADVERTISED"></span>**Not Advertised** (2)</span></span>
</dt> <dt>

<span data-ttu-id="e71b0-129"><span id="SLP_"></span><span id="slp_"></span>**SLP** (3)</span><span class="sxs-lookup"><span data-stu-id="e71b0-129"><span id="SLP_"></span><span id="slp_"></span>**SLP** (3 )</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="e71b0-130">**Didascalia**</span><span class="sxs-lookup"><span data-stu-id="e71b0-130">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e71b0-131">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="e71b0-131">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e71b0-132">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="e71b0-132">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e71b0-133">Breve descrizione dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="e71b0-133">A short description of the object.</span></span> <span data-ttu-id="e71b0-134">Questa proprietà viene ereditata da [**CIM \_ managementelement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="e71b0-134">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="e71b0-135">**Descrizione**</span><span class="sxs-lookup"><span data-stu-id="e71b0-135">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e71b0-136">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="e71b0-136">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e71b0-137">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="e71b0-137">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e71b0-138">Descrizione dell'oggetto .</span><span class="sxs-lookup"><span data-stu-id="e71b0-138">A description of the object.</span></span> <span data-ttu-id="e71b0-139">Questa proprietà viene ereditata da [**CIM \_ managementelement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="e71b0-139">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="e71b0-140">**ElementName**</span><span class="sxs-lookup"><span data-stu-id="e71b0-140">**ElementName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e71b0-141">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="e71b0-141">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e71b0-142">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="e71b0-142">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e71b0-143">Nome visualizzato per l'oggetto.</span><span class="sxs-lookup"><span data-stu-id="e71b0-143">A display name for the object.</span></span> <span data-ttu-id="e71b0-144">Questa proprietà viene ereditata da [**CIM \_ managementelement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="e71b0-144">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="e71b0-145">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="e71b0-145">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e71b0-146">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="e71b0-146">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e71b0-147">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="e71b0-147">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e71b0-148">Qualificatori: **chiave**, **sostituzione**</span><span class="sxs-lookup"><span data-stu-id="e71b0-148">Qualifiers: **Key**, **Override**</span></span>
</dt> </dl>

<span data-ttu-id="e71b0-149">Stringa che identifica in modo univoco un'istanza di questa classe.</span><span class="sxs-lookup"><span data-stu-id="e71b0-149">A string that uniquely identifies an instance of this class.</span></span> <span data-ttu-id="e71b0-150">Questa proprietà viene ereditata da [**CIM \_ managementelement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="e71b0-150">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="e71b0-151">**OtherRegisteredOrganization**</span><span class="sxs-lookup"><span data-stu-id="e71b0-151">**OtherRegisteredOrganization**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e71b0-152">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="e71b0-152">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e71b0-153">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="e71b0-153">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e71b0-154">Qualificatori: **maxlen** (256)</span><span class="sxs-lookup"><span data-stu-id="e71b0-154">Qualifiers: **MaxLen** ( 256 )</span></span>
</dt> </dl>

<span data-ttu-id="e71b0-155">Stringa che fornisce una descrizione dell'organizzazione quando **RegisteredOrganization** contiene 1 (other).</span><span class="sxs-lookup"><span data-stu-id="e71b0-155">A string that provides a description of the organization when **RegisteredOrganization** contains 1 (Other).</span></span> <span data-ttu-id="e71b0-156">Questa proprietà viene ereditata da [**CIM \_ RegisteredProfile**](/previous-versions//ee309375(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="e71b0-156">This property is inherited from [**CIM\_RegisteredProfile**](/previous-versions//ee309375(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="e71b0-157">**Registratore**</span><span class="sxs-lookup"><span data-stu-id="e71b0-157">**RegisteredName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e71b0-158">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="e71b0-158">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e71b0-159">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="e71b0-159">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e71b0-160">Qualificatori: **maxlen** (256)</span><span class="sxs-lookup"><span data-stu-id="e71b0-160">Qualifiers: **MaxLen** ( 256 )</span></span>
</dt> </dl>

<span data-ttu-id="e71b0-161">Nome del profilo registrato.</span><span class="sxs-lookup"><span data-stu-id="e71b0-161">The name of this registered profile.</span></span> <span data-ttu-id="e71b0-162">Poiché possono esistere più versioni per lo stesso **registratore**, la combinazione di **registeredname**, **RegisteredOrganization** e **RegisteredVersion** deve identificare in modo univoco il profilo registrato nell'ambito dell'organizzazione.</span><span class="sxs-lookup"><span data-stu-id="e71b0-162">Since multiple versions can exist for the same **RegisteredName**, the combination of **RegisteredName**, **RegisteredOrganization**, and **RegisteredVersion** must uniquely identify the registered profile within the scope of the organization.</span></span> <span data-ttu-id="e71b0-163">Questa proprietà viene ereditata da [**CIM \_ RegisteredProfile**](/previous-versions//ee309375(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="e71b0-163">This property is inherited from [**CIM\_RegisteredProfile**](/previous-versions//ee309375(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="e71b0-164">**RegisteredOrganization**</span><span class="sxs-lookup"><span data-stu-id="e71b0-164">**RegisteredOrganization**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e71b0-165">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="e71b0-165">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="e71b0-166">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="e71b0-166">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e71b0-167">Organizzazione che definisce questo profilo.</span><span class="sxs-lookup"><span data-stu-id="e71b0-167">The organization that defines this profile.</span></span> <span data-ttu-id="e71b0-168">Questa proprietà viene ereditata da [**CIM \_ RegisteredProfile**](/previous-versions//ee309375(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="e71b0-168">This property is inherited from [**CIM\_RegisteredProfile**](/previous-versions//ee309375(v=vs.85)).</span></span>

<dl> <dt>

<span data-ttu-id="e71b0-169"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Altro** (1)</span><span class="sxs-lookup"><span data-stu-id="e71b0-169"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>
</dt> <dt>

<span data-ttu-id="e71b0-170"><span id="DMTF"></span><span id="dmtf"></span>**DMTF** (2)</span><span class="sxs-lookup"><span data-stu-id="e71b0-170"><span id="DMTF"></span><span id="dmtf"></span>**DMTF** (2)</span></span>
</dt> <dt>

<span data-ttu-id="e71b0-171"><span id="CompTIA"></span><span id="comptia"></span><span id="COMPTIA"></span>**CompTIA** (3)</span><span class="sxs-lookup"><span data-stu-id="e71b0-171"><span id="CompTIA"></span><span id="comptia"></span><span id="COMPTIA"></span>**CompTIA** (3)</span></span>
</dt> <dt>

<span data-ttu-id="e71b0-172"><span id="Consortium_for_Service_Innovation"></span><span id="consortium_for_service_innovation"></span><span id="CONSORTIUM_FOR_SERVICE_INNOVATION"></span>**Consorzio per l'innovazione dei servizi** (4)</span><span class="sxs-lookup"><span data-stu-id="e71b0-172"><span id="Consortium_for_Service_Innovation"></span><span id="consortium_for_service_innovation"></span><span id="CONSORTIUM_FOR_SERVICE_INNOVATION"></span>**Consortium for Service Innovation** (4)</span></span>
</dt> <dt>

<span data-ttu-id="e71b0-173"><span id="FAST"></span><span id="fast"></span>**Veloce** (5)</span><span class="sxs-lookup"><span data-stu-id="e71b0-173"><span id="FAST"></span><span id="fast"></span>**FAST** (5)</span></span>
</dt> <dt>

<span data-ttu-id="e71b0-174"><span id="GGF"></span><span id="ggf"></span>**Ggf** (6)</span><span class="sxs-lookup"><span data-stu-id="e71b0-174"><span id="GGF"></span><span id="ggf"></span>**GGF** (6)</span></span>
</dt> <dt>

<span data-ttu-id="e71b0-175"><span id="INTAP"></span><span id="intap"></span>**Intap** (7)</span><span class="sxs-lookup"><span data-stu-id="e71b0-175"><span id="INTAP"></span><span id="intap"></span>**INTAP** (7)</span></span>
</dt> <dt>

<span data-ttu-id="e71b0-176"><span id="itSMF"></span><span id="itsmf"></span><span id="ITSMF"></span>**itSMF** (8)</span><span class="sxs-lookup"><span data-stu-id="e71b0-176"><span id="itSMF"></span><span id="itsmf"></span><span id="ITSMF"></span>**itSMF** (8)</span></span>
</dt> <dt>

<span data-ttu-id="e71b0-177"><span id="NAC"></span><span id="nac"></span>**NAC** (9)</span><span class="sxs-lookup"><span data-stu-id="e71b0-177"><span id="NAC"></span><span id="nac"></span>**NAC** (9)</span></span>
</dt> <dt>

<span data-ttu-id="e71b0-178"><span id="__10___________Northwest_Energy_Efficiency_Alliance"></span><span id="__10___________northwest_energy_efficiency_alliance"></span><span id="__10___________NORTHWEST_ENERGY_EFFICIENCY_ALLIANCE"></span>**//10 alleanza di efficienza energetica Northwest** (10)</span><span class="sxs-lookup"><span data-stu-id="e71b0-178"><span id="__10___________Northwest_Energy_Efficiency_Alliance"></span><span id="__10___________northwest_energy_efficiency_alliance"></span><span id="__10___________NORTHWEST_ENERGY_EFFICIENCY_ALLIANCE"></span>**//10 Northwest Energy Efficiency Alliance** (10)</span></span>
</dt> <dt>

<span data-ttu-id="e71b0-179"><span id="SNIA"></span><span id="snia"></span>**SNIA** (11)</span><span class="sxs-lookup"><span data-stu-id="e71b0-179"><span id="SNIA"></span><span id="snia"></span>**SNIA** (11)</span></span>
</dt> <dt>

<span data-ttu-id="e71b0-180"><span id="TM_Forum"></span><span id="tm_forum"></span><span id="TM_FORUM"></span>**Forum TM** (12)</span><span class="sxs-lookup"><span data-stu-id="e71b0-180"><span id="TM_Forum"></span><span id="tm_forum"></span><span id="TM_FORUM"></span>**TM Forum** (12)</span></span>
</dt> <dt>

<span data-ttu-id="e71b0-181"><span id="The_Open_Group"></span><span id="the_open_group"></span><span id="THE_OPEN_GROUP"></span>**Gruppo aperto** (13)</span><span class="sxs-lookup"><span data-stu-id="e71b0-181"><span id="The_Open_Group"></span><span id="the_open_group"></span><span id="THE_OPEN_GROUP"></span>**The Open Group** (13)</span></span>
</dt> <dt>

<span data-ttu-id="e71b0-182"><span id="ANSI"></span><span id="ansi"></span>**ANSI** (14)</span><span class="sxs-lookup"><span data-stu-id="e71b0-182"><span id="ANSI"></span><span id="ansi"></span>**ANSI** (14)</span></span>
</dt> <dt>

<span data-ttu-id="e71b0-183"><span id="IEEE"></span><span id="ieee"></span>**IEEE** (15)</span><span class="sxs-lookup"><span data-stu-id="e71b0-183"><span id="IEEE"></span><span id="ieee"></span>**IEEE** (15)</span></span>
</dt> <dt>

<span data-ttu-id="e71b0-184"><span id="IETF"></span><span id="ietf"></span>**IETF** (16)</span><span class="sxs-lookup"><span data-stu-id="e71b0-184"><span id="IETF"></span><span id="ietf"></span>**IETF** (16)</span></span>
</dt> <dt>

<span data-ttu-id="e71b0-185"><span id="INCITS"></span><span id="incits"></span>**Inci** (17)</span><span class="sxs-lookup"><span data-stu-id="e71b0-185"><span id="INCITS"></span><span id="incits"></span>**INCITS** (17)</span></span>
</dt> <dt>

<span data-ttu-id="e71b0-186"><span id="ISO"></span><span id="iso"></span>**ISO** (18)</span><span class="sxs-lookup"><span data-stu-id="e71b0-186"><span id="ISO"></span><span id="iso"></span>**ISO** (18)</span></span>
</dt> <dt>

<span data-ttu-id="e71b0-187"><span id="W3C"></span><span id="w3c"></span>**W3C** (19)</span><span class="sxs-lookup"><span data-stu-id="e71b0-187"><span id="W3C"></span><span id="w3c"></span>**W3C** (19)</span></span>
</dt> <dt>

<span data-ttu-id="e71b0-188"><span id="__20___________OGF"></span><span id="__20___________ogf"></span>**OGF 20** (20)</span><span class="sxs-lookup"><span data-stu-id="e71b0-188"><span id="__20___________OGF"></span><span id="__20___________ogf"></span>**//20 OGF** (20)</span></span>
</dt> <dt>

<span data-ttu-id="e71b0-189"><span id="The_Green_Grid"></span><span id="the_green_grid"></span><span id="THE_GREEN_GRID"></span>**Griglia verde** (21)</span><span class="sxs-lookup"><span data-stu-id="e71b0-189"><span id="The_Green_Grid"></span><span id="the_green_grid"></span><span id="THE_GREEN_GRID"></span>**The Green Grid** (21)</span></span>
</dt> <dt>

<span data-ttu-id="e71b0-190"><span id="DMTF_Reserved_"></span><span id="dmtf_reserved_"></span><span id="DMTF_RESERVED_"></span>**DMTF riservato** (..</span><span class="sxs-lookup"><span data-stu-id="e71b0-190"><span id="DMTF_Reserved_"></span><span id="dmtf_reserved_"></span><span id="DMTF_RESERVED_"></span>**DMTF Reserved** (..</span></span> <span data-ttu-id="e71b0-191">)</span><span class="sxs-lookup"><span data-stu-id="e71b0-191">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="e71b0-192">**RegisteredVersion**</span><span class="sxs-lookup"><span data-stu-id="e71b0-192">**RegisteredVersion**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e71b0-193">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="e71b0-193">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e71b0-194">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="e71b0-194">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e71b0-195">Versione di questo profilo.</span><span class="sxs-lookup"><span data-stu-id="e71b0-195">The version of this profile.</span></span> <span data-ttu-id="e71b0-196">Il formato della stringa deve essere: "*M*. *N*. *U*"dove:</span><span class="sxs-lookup"><span data-stu-id="e71b0-196">The string must be in the form: "*M*.*N*.*U*" Where:</span></span>

-   <span data-ttu-id="e71b0-197">*M* è la versione principale (in formato numerico) che descrive la creazione o l'ultima modifica del profilo.</span><span class="sxs-lookup"><span data-stu-id="e71b0-197">*M* is the major version (in numeric form) describing the profile's creation or last modification.</span></span>
-   <span data-ttu-id="e71b0-198">*N* è la versione secondaria (in formato numerico) che descrive la creazione o l'ultima modifica del profilo.</span><span class="sxs-lookup"><span data-stu-id="e71b0-198">*N* is the minor version (in numeric form) describing the profile's creation or last modification.</span></span>
-   <span data-ttu-id="e71b0-199">*U* è l'aggiornamento (in formato numerico) che descrive la creazione o l'ultima modifica del profilo.</span><span class="sxs-lookup"><span data-stu-id="e71b0-199">*U* is the update (in numeric form) describing the profile's creation or last modification.</span></span>

<span data-ttu-id="e71b0-200">Questa proprietà viene ereditata da [**CIM \_ RegisteredProfile**](/previous-versions//ee309375(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="e71b0-200">This property is inherited from [**CIM\_RegisteredProfile**](/previous-versions//ee309375(v=vs.85)).</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="e71b0-201">Requisiti</span><span class="sxs-lookup"><span data-stu-id="e71b0-201">Requirements</span></span>



| <span data-ttu-id="e71b0-202">Requisito</span><span class="sxs-lookup"><span data-stu-id="e71b0-202">Requirement</span></span> | <span data-ttu-id="e71b0-203">Valore</span><span class="sxs-lookup"><span data-stu-id="e71b0-203">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e71b0-204">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="e71b0-204">Minimum supported client</span></span><br/> | <span data-ttu-id="e71b0-205">Windows 8.1 \[ solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="e71b0-205">Windows 8.1 \[desktop apps only\]</span></span><br/>                                                            |
| <span data-ttu-id="e71b0-206">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="e71b0-206">Minimum supported server</span></span><br/> | <span data-ttu-id="e71b0-207">Solo app desktop Windows Server 2012 R2 \[\]</span><span class="sxs-lookup"><span data-stu-id="e71b0-207">Windows Server 2012 R2 \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="e71b0-208">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="e71b0-208">Namespace</span></span><br/>                | <span data-ttu-id="e71b0-209">\\Interoperabilità radice</span><span class="sxs-lookup"><span data-stu-id="e71b0-209">Root\\interop</span></span><br/>                                                                                |
| <span data-ttu-id="e71b0-210">MOF</span><span class="sxs-lookup"><span data-stu-id="e71b0-210">MOF</span></span><br/>                      | <dl> <span data-ttu-id="e71b0-211"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="e71b0-211"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="e71b0-212">DLL</span><span class="sxs-lookup"><span data-stu-id="e71b0-212">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e71b0-213"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="e71b0-213"><dt>Vmms.exe</dt></span></span> </dl>                     |



 

