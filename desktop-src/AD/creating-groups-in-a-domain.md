---
title: Creazione di gruppi in un dominio
description: Un oggetto gruppo viene creato in Active Directory Domain Services nel contenitore del dominio in cui sarà contenuto il nuovo gruppo.
ms.assetid: 40792878-4219-4242-8cf7-b092b28f2ff4
ms.tgt_platform: multiple
keywords:
- gruppi AD, creazione di gruppi in un dominio
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 100700b08fb82b750ee68dfed6bcb26060929e87
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/17/2020
ms.locfileid: "104046534"
---
# <a name="creating-groups-in-a-domain"></a><span data-ttu-id="ce060-104">Creazione di gruppi in un dominio</span><span class="sxs-lookup"><span data-stu-id="ce060-104">Creating Groups in a Domain</span></span>

<span data-ttu-id="ce060-105">Un oggetto gruppo viene creato in Active Directory Domain Services nel contenitore del dominio in cui sarà contenuto il nuovo gruppo.</span><span class="sxs-lookup"><span data-stu-id="ce060-105">A group object is created in Active Directory Domain Services in the domain container where the new group will be contained.</span></span> <span data-ttu-id="ce060-106">I gruppi possono essere creati alla radice del dominio, all'interno di un'unità organizzativa o all'interno di un contenitore.</span><span class="sxs-lookup"><span data-stu-id="ce060-106">Groups can be created at the root of the domain, within an organizational unit, or within a container.</span></span> <span data-ttu-id="ce060-107">Per creare un oggetto gruppo, usare il metodo [**IADsContainer:: create**](/windows/desktop/api/iads/nf-iads-iadscontainer-create) o [**IDirectoryObject:: CreateDSObject**](/windows/desktop/api/iads/nf-iads-idirectoryobject-createdsobject) .</span><span class="sxs-lookup"><span data-stu-id="ce060-107">To create a group object, use the [**IADsContainer::Create**](/windows/desktop/api/iads/nf-iads-iadscontainer-create) or the [**IDirectoryObject::CreateDSObject**](/windows/desktop/api/iads/nf-iads-idirectoryobject-createdsobject) method.</span></span>

<span data-ttu-id="ce060-108">Gli attributi seguenti sono necessari per rendere l'oggetto gruppo un gruppo valido che verrà riconosciuto dal server Active Directory e dal sistema di sicurezza di Windows:</span><span class="sxs-lookup"><span data-stu-id="ce060-108">The following attributes are required to make the group object a legal group that the Active Directory server and the Windows security system will recognize:</span></span>

<dl> <dt>

<span data-ttu-id="ce060-109"><span id="cn"></span><span id="CN"></span>**CN**</span><span class="sxs-lookup"><span data-stu-id="ce060-109"><span id="cn"></span><span id="CN"></span>**cn**</span></span>
</dt> <dd>

<span data-ttu-id="ce060-110">Specifica il nome dell'oggetto gruppo nella directory.</span><span class="sxs-lookup"><span data-stu-id="ce060-110">Specifies the name of the group object in the directory.</span></span> <span data-ttu-id="ce060-111">Si tratta del nome distinto relativo dell'oggetto all'interno del contenitore in cui viene creato il gruppo.</span><span class="sxs-lookup"><span data-stu-id="ce060-111">This will be the object's relative distinguished name within the container where the group is created.</span></span>

</dd> <dt>

<span data-ttu-id="ce060-112"><span id="groupType"></span><span id="grouptype"></span><span id="GROUPTYPE"></span>**groupType**</span><span class="sxs-lookup"><span data-stu-id="ce060-112"><span id="groupType"></span><span id="grouptype"></span><span id="GROUPTYPE"></span>**groupType**</span></span>
</dt> <dd>

<span data-ttu-id="ce060-113">Contiene un numero intero che specifica il tipo e l'ambito del gruppo.</span><span class="sxs-lookup"><span data-stu-id="ce060-113">Contains an integer that specifies the group type and scope.</span></span> <span data-ttu-id="ce060-114">Il [**\_ tipo di gruppo Ads \_ \_ enum**](/windows/win32/api/iads/ne-iads-ads_group_type_enum) Enumeration definisce i valori possibili per l'attributo **GroupType** .</span><span class="sxs-lookup"><span data-stu-id="ce060-114">The [**ADS\_GROUP\_TYPE\_ENUM**](/windows/win32/api/iads/ne-iads-ads_group_type_enum) enumeration defines the possible values for the **groupType** attribute.</span></span>

<span data-ttu-id="ce060-115">Nell'elenco seguente vengono definiti i tipi e i valori di gruppo comuni per questo attributo.</span><span class="sxs-lookup"><span data-stu-id="ce060-115">The following list defines common group types and values for this attribute.</span></span>

<dl> <dt>

<span data-ttu-id="ce060-116"><span id="Domain_Local_Distribution"></span><span id="domain_local_distribution"></span><span id="DOMAIN_LOCAL_DISTRIBUTION"></span>Distribuzione locale di dominio</span><span class="sxs-lookup"><span data-stu-id="ce060-116"><span id="Domain_Local_Distribution"></span><span id="domain_local_distribution"></span><span id="DOMAIN_LOCAL_DISTRIBUTION"></span>Domain Local Distribution</span></span>
</dt> <dd>

<span data-ttu-id="ce060-117">**tipo di gruppo ADS gruppo \_ \_ \_ locale di dominio \_ \_**</span><span class="sxs-lookup"><span data-stu-id="ce060-117">**ADS\_GROUP\_TYPE\_DOMAIN\_LOCAL\_GROUP**</span></span>

</dd> <dt>

<span data-ttu-id="ce060-118"><span id="Domain_Local_Security"></span><span id="domain_local_security"></span><span id="DOMAIN_LOCAL_SECURITY"></span>Sicurezza locale di dominio</span><span class="sxs-lookup"><span data-stu-id="ce060-118"><span id="Domain_Local_Security"></span><span id="domain_local_security"></span><span id="DOMAIN_LOCAL_SECURITY"></span>Domain Local Security</span></span>
</dt> <dd>

<span data-ttu-id="ce060-119">**Annunci \_ tipo di gruppo \_ \_ dominio \_ locale \_** gruppo di \| **annunci \_ \_ \_ sicurezza \_ tipo** di gruppo abilitato</span><span class="sxs-lookup"><span data-stu-id="ce060-119">**ADS\_GROUP\_TYPE\_DOMAIN\_LOCAL\_GROUP** \| **ADS\_GROUP\_TYPE\_SECURITY\_ENABLED**</span></span>

</dd> <dt>

<span data-ttu-id="ce060-120"><span id="Global_Distribution"></span><span id="global_distribution"></span><span id="GLOBAL_DISTRIBUTION"></span>Distribuzione globale</span><span class="sxs-lookup"><span data-stu-id="ce060-120"><span id="Global_Distribution"></span><span id="global_distribution"></span><span id="GLOBAL_DISTRIBUTION"></span>Global Distribution</span></span>
</dt> <dd>

<span data-ttu-id="ce060-121">**tipo di gruppo ADS gruppo \_ \_ \_ globale \_**</span><span class="sxs-lookup"><span data-stu-id="ce060-121">**ADS\_GROUP\_TYPE\_GLOBAL\_GROUP**</span></span>

</dd> <dt>

<span data-ttu-id="ce060-122"><span id="Global_Security"></span><span id="global_security"></span><span id="GLOBAL_SECURITY"></span>Sicurezza globale</span><span class="sxs-lookup"><span data-stu-id="ce060-122"><span id="Global_Security"></span><span id="global_security"></span><span id="GLOBAL_SECURITY"></span>Global Security</span></span>
</dt> <dd>

<span data-ttu-id="ce060-123">**Annunci \_ tipo di gruppo gruppo di annunci \_ \_ \_ gruppo globale** \| **\_ \_ \_ sicurezza \_ abilitata**</span><span class="sxs-lookup"><span data-stu-id="ce060-123">**ADS\_GROUP\_TYPE\_GLOBAL\_GROUP** \| **ADS\_GROUP\_TYPE\_SECURITY\_ENABLED**</span></span>

</dd> <dt>

<span data-ttu-id="ce060-124"><span id="Universal_Distribution"></span><span id="universal_distribution"></span><span id="UNIVERSAL_DISTRIBUTION"></span>Distribuzione universale</span><span class="sxs-lookup"><span data-stu-id="ce060-124"><span id="Universal_Distribution"></span><span id="universal_distribution"></span><span id="UNIVERSAL_DISTRIBUTION"></span>Universal Distribution</span></span>
</dt> <dd>

<span data-ttu-id="ce060-125">**\_gruppo Ads \_ tipo gruppo \_ universale \_**</span><span class="sxs-lookup"><span data-stu-id="ce060-125">**ADS\_GROUP\_TYPE\_UNIVERSAL\_GROUP**</span></span>

</dd> <dt>

<span data-ttu-id="ce060-126"><span id="Universal_Security"></span><span id="universal_security"></span><span id="UNIVERSAL_SECURITY"></span>Sicurezza universale</span><span class="sxs-lookup"><span data-stu-id="ce060-126"><span id="Universal_Security"></span><span id="universal_security"></span><span id="UNIVERSAL_SECURITY"></span>Universal Security</span></span>
</dt> <dd>

<span data-ttu-id="ce060-127">**Annunci \_ \_tipo di \_ \_ gruppo** gruppi di annunci gruppo universale \| **\_ \_ \_ sicurezza \_ abilitata**</span><span class="sxs-lookup"><span data-stu-id="ce060-127">**ADS\_GROUP\_TYPE\_UNIVERSAL\_GROUP** \| **ADS\_GROUP\_TYPE\_SECURITY\_ENABLED**</span></span>

</dd> <dt>


</dt> <dd>

</dd> </dl>

<span data-ttu-id="ce060-128">Se il gruppo è destinato a impostare il controllo di accesso per gli oggetti directory, il gruppo deve essere un gruppo di sicurezza globale o universale.</span><span class="sxs-lookup"><span data-stu-id="ce060-128">If the group is intended for setting access control on directory objects, the group should be a Global Security or Universal Security group.</span></span>

<span data-ttu-id="ce060-129">Tenere presente che i gruppi di sicurezza universali possono essere creati solo in domini Windows 2000 in esecuzione in modalità nativa.</span><span class="sxs-lookup"><span data-stu-id="ce060-129">Be aware that Universal Security groups can only be created on Windows 2000 domains running in native mode.</span></span> <span data-ttu-id="ce060-130">Per ulteriori informazioni sul rilevamento della modalità mista e nativa, vedere [rilevamento della modalità operativa di un dominio](detecting-the-operation-mode-of-a-domain.md).</span><span class="sxs-lookup"><span data-stu-id="ce060-130">For more information about detecting mixed and native mode, see [Detecting the Operation Mode of a Domain](detecting-the-operation-mode-of-a-domain.md).</span></span>

</dd> <dt>

<span data-ttu-id="ce060-131"><span id="sAMAccountName"></span><span id="samaccountname"></span><span id="SAMACCOUNTNAME"></span>**sAMAccountName**</span><span class="sxs-lookup"><span data-stu-id="ce060-131"><span id="sAMAccountName"></span><span id="samaccountname"></span><span id="SAMACCOUNTNAME"></span>**sAMAccountName**</span></span>
</dt> <dd>

<span data-ttu-id="ce060-132">Contiene una stringa che rappresenta il nome utilizzato per supportare client e server di una versione precedente.</span><span class="sxs-lookup"><span data-stu-id="ce060-132">Contains a string that is the name used to support clients and servers from a previous version.</span></span> <span data-ttu-id="ce060-133">Il valore di **sAMAccountName** deve essere composto da meno di 20 caratteri per supportare i client di una versione precedente di Windows.</span><span class="sxs-lookup"><span data-stu-id="ce060-133">The **sAMAccountName** should be less than 20 characters to support clients of a previous version of Windows.</span></span>

<span data-ttu-id="ce060-134">**SAMAccountName** deve essere univoco tra tutti gli oggetti entità di sicurezza all'interno del dominio.</span><span class="sxs-lookup"><span data-stu-id="ce060-134">The **sAMAccountName** must be unique among all security principal objects within the domain.</span></span> <span data-ttu-id="ce060-135">È necessario eseguire una query sul dominio per verificare che **sAMAccountName** sia univoco all'interno del dominio.</span><span class="sxs-lookup"><span data-stu-id="ce060-135">A query should be performed against the domain to verify that the **sAMAccountName** is unique within the domain.</span></span>

</dd> </dl>

<span data-ttu-id="ce060-136">I membri del gruppo possono essere aggiunti in fase di creazione usando il metodo [**IDirectoryObject:: CreateDSObject**](/windows/desktop/api/iads/nf-iads-idirectoryobject-createdsobject) .</span><span class="sxs-lookup"><span data-stu-id="ce060-136">The members of the group can be added at creation time using the [**IDirectoryObject::CreateDSObject**](/windows/desktop/api/iads/nf-iads-idirectoryobject-createdsobject) method.</span></span> <span data-ttu-id="ce060-137">Facoltativamente, i membri possono essere aggiunti al gruppo dopo la creazione usando il metodo [**IADsGroup:: Add**](/windows/desktop/api/iads/nf-iads-iadsgroup-add) .</span><span class="sxs-lookup"><span data-stu-id="ce060-137">Optionally, members can be added to the group after creation using the [**IADsGroup::Add**](/windows/desktop/api/iads/nf-iads-iadsgroup-add) method.</span></span> <span data-ttu-id="ce060-138">Per ulteriori informazioni sull'aggiunta di membri a un gruppo, vedere [aggiunta di membri a gruppi in un dominio](adding-members-to-groups-in-a-domain.md).</span><span class="sxs-lookup"><span data-stu-id="ce060-138">For more information about adding members to a group, see [Adding Members to Groups in a Domain](adding-members-to-groups-in-a-domain.md).</span></span>

 

 