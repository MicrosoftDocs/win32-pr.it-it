---
description: La \_ classe di montaggio CIM rappresenta un'associazione tra un file System e una directory a cui è collegata.
ms.assetid: abf1833b-9b39-45c0-8400-2be2bf3a1c3c
ms.tgt_platform: multiple
title: Classe CIM_Mount
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_Mount
- CIM_Mount.Dependent
- CIM_Mount.Antecedent
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 5b86587466517a10302b3109a521e902a66892c4
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104127079"
---
# <a name="cim_mount-class"></a><span data-ttu-id="4a7d2-103">\_Classe di montaggio CIM</span><span class="sxs-lookup"><span data-stu-id="4a7d2-103">CIM\_Mount class</span></span>

<span data-ttu-id="4a7d2-104">La classe di **\_ montaggio CIM** rappresenta un'associazione tra un file System e una directory a cui è collegata.</span><span class="sxs-lookup"><span data-stu-id="4a7d2-104">The **CIM\_Mount** class represents an association between a file system and a directory to which it is attached.</span></span>

<span data-ttu-id="4a7d2-105">Per la semantica di questa relazione è necessario che la directory montata sia contenuta in una file system (tramite l'associazione di archiviazione file) diversa da quella file system a cui viene fatto riferimento come dipendente.</span><span class="sxs-lookup"><span data-stu-id="4a7d2-105">The semantics of this relationship require that the mounted directory be contained by a file system (via the file storage association) that is different from the file system referenced as the dependent.</span></span> <span data-ttu-id="4a7d2-106">La file system che contiene la directory può essere locale o remota.</span><span class="sxs-lookup"><span data-stu-id="4a7d2-106">The directory's containing file system can be local or remote.</span></span> <span data-ttu-id="4a7d2-107">Ad esempio, un file system locale in un sistema di computer Solaris può montare una directory dall'file system a cui si accede tramite l'unità CDROM del computer (ovvero un altro file system locale).</span><span class="sxs-lookup"><span data-stu-id="4a7d2-107">For example, a local file system on a Solaris computer system can mount a directory from the file system accessed via the computer's CDROM drive (that is, another local file system).</span></span> <span data-ttu-id="4a7d2-108">D'altra parte, in un caso "remoto", la directory viene esportata per la prima volta dalla relativa file system, ospitata in un altro computer che funge, ad esempio, come file server.</span><span class="sxs-lookup"><span data-stu-id="4a7d2-108">On the other hand, in a "remote" case, the directory is first exported by its file system, which is hosted on another computer system acting, for example, as a file server.</span></span> <span data-ttu-id="4a7d2-109">Per distinguere i due montaggi, è sempre necessario definire un'associazione di [**\_ esportazione CIM**](cim-export.md) per le directory a cui si accede in modalità remota.</span><span class="sxs-lookup"><span data-stu-id="4a7d2-109">To distinguish the two mounts, a [**CIM\_Export**](cim-export.md) association should always be defined for the remotely accessed/mounted directories.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="4a7d2-110">Le classi CIM (Common Information Model) DMTF (Distributed Management Task Force) sono le classi padre sulle quali vengono compilate le classi WMI.</span><span class="sxs-lookup"><span data-stu-id="4a7d2-110">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="4a7d2-111">Attualmente WMI supporta solo gli [schemi della versione CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="4a7d2-111">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="4a7d2-112">La sintassi seguente è semplificata dal codice MOF (Managed Object Format) e include tutte le proprietà ereditate.</span><span class="sxs-lookup"><span data-stu-id="4a7d2-112">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="4a7d2-113">Le proprietà sono elencate in ordine alfabetico e non in ordine MOF.</span><span class="sxs-lookup"><span data-stu-id="4a7d2-113">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="4a7d2-114">Sintassi</span><span class="sxs-lookup"><span data-stu-id="4a7d2-114">Syntax</span></span>

``` syntax
[Abstract, UUID("{75BCF4F6-DB46-11D2-B4C8-80080C7B6371}"), AMENDMENT]
class CIM_Mount : CIM_Dependency
{
  CIM_NFS       REF Dependent;
  CIM_Directory REF Antecedent;
};
```

## <a name="members"></a><span data-ttu-id="4a7d2-115">Members</span><span class="sxs-lookup"><span data-stu-id="4a7d2-115">Members</span></span>

<span data-ttu-id="4a7d2-116">La classe **CIM \_ Mount** presenta questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="4a7d2-116">The **CIM\_Mount** class has these types of members:</span></span>

-   [<span data-ttu-id="4a7d2-117">Proprietà</span><span class="sxs-lookup"><span data-stu-id="4a7d2-117">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="4a7d2-118">Proprietà</span><span class="sxs-lookup"><span data-stu-id="4a7d2-118">Properties</span></span>

<span data-ttu-id="4a7d2-119">La classe **CIM \_ Mount** presenta queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="4a7d2-119">The **CIM\_Mount** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="4a7d2-120">**Antecedente**</span><span class="sxs-lookup"><span data-stu-id="4a7d2-120">**Antecedent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4a7d2-121">Tipo di dati **: \_ directory CIM**</span><span class="sxs-lookup"><span data-stu-id="4a7d2-121">Data type: **CIM\_Directory**</span></span>
</dt> <dt>

<span data-ttu-id="4a7d2-122">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="4a7d2-122">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4a7d2-123">Qualificatori: [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1), [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("antecedente")</span><span class="sxs-lookup"><span data-stu-id="4a7d2-123">Qualifiers: [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1), [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent")</span></span>
</dt> </dl>

<span data-ttu-id="4a7d2-124">Una [**\_ directory CIM**](cim-directory.md) che descrive la directory montata.</span><span class="sxs-lookup"><span data-stu-id="4a7d2-124">A [**CIM\_Directory**](cim-directory.md) describing the directory mounted.</span></span>

</dd> <dt>

<span data-ttu-id="4a7d2-125">**Dipendente**</span><span class="sxs-lookup"><span data-stu-id="4a7d2-125">**Dependent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4a7d2-126">Tipo di dati **: \_ NFS CIM**</span><span class="sxs-lookup"><span data-stu-id="4a7d2-126">Data type: **CIM\_NFS**</span></span>
</dt> <dt>

<span data-ttu-id="4a7d2-127">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="4a7d2-127">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4a7d2-128">Qualificatori: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("dipendente")</span><span class="sxs-lookup"><span data-stu-id="4a7d2-128">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Dependent")</span></span>
</dt> </dl>

<span data-ttu-id="4a7d2-129">Un [**\_ NFS CIM**](cim-nfs.md) che descrive il file System in cui è montata la directory.</span><span class="sxs-lookup"><span data-stu-id="4a7d2-129">A [**CIM\_NFS**](cim-nfs.md) describing the FileSystem the Directory is mounted on.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="4a7d2-130">Commenti</span><span class="sxs-lookup"><span data-stu-id="4a7d2-130">Remarks</span></span>

<span data-ttu-id="4a7d2-131">**CIM \_ Il montaggio** deriva dalla [**\_ dipendenza CIM**](cim-dependency.md).</span><span class="sxs-lookup"><span data-stu-id="4a7d2-131">**CIM\_Mount** is derived from [**CIM\_Dependency**](cim-dependency.md).</span></span>

<span data-ttu-id="4a7d2-132">WMI non implementa questa classe.</span><span class="sxs-lookup"><span data-stu-id="4a7d2-132">WMI does not implement this class.</span></span>

<span data-ttu-id="4a7d2-133">Questa documentazione è derivata dalle descrizioni della classe CIM pubblicate da DMTF.</span><span class="sxs-lookup"><span data-stu-id="4a7d2-133">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="4a7d2-134">Microsoft potrebbe avere apportato modifiche per correggere gli errori secondari, rispettare gli standard di documentazione di Microsoft SDK o fornire altre informazioni.</span><span class="sxs-lookup"><span data-stu-id="4a7d2-134">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="4a7d2-135">Requisiti</span><span class="sxs-lookup"><span data-stu-id="4a7d2-135">Requirements</span></span>



| <span data-ttu-id="4a7d2-136">Requisito</span><span class="sxs-lookup"><span data-stu-id="4a7d2-136">Requirement</span></span> | <span data-ttu-id="4a7d2-137">Valore</span><span class="sxs-lookup"><span data-stu-id="4a7d2-137">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="4a7d2-138">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="4a7d2-138">Minimum supported client</span></span><br/> | <span data-ttu-id="4a7d2-139">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="4a7d2-139">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="4a7d2-140">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="4a7d2-140">Minimum supported server</span></span><br/> | <span data-ttu-id="4a7d2-141">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="4a7d2-141">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="4a7d2-142">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="4a7d2-142">Namespace</span></span><br/>                | <span data-ttu-id="4a7d2-143">\\CIMV2 radice</span><span class="sxs-lookup"><span data-stu-id="4a7d2-143">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="4a7d2-144">MOF</span><span class="sxs-lookup"><span data-stu-id="4a7d2-144">MOF</span></span><br/>                      | <dl> <span data-ttu-id="4a7d2-145"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="4a7d2-145"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="4a7d2-146">DLL</span><span class="sxs-lookup"><span data-stu-id="4a7d2-146">DLL</span></span><br/>                      | <dl> <span data-ttu-id="4a7d2-147"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="4a7d2-147"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4a7d2-148">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="4a7d2-148">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4a7d2-149">**\_Dipendenza CIM**</span><span class="sxs-lookup"><span data-stu-id="4a7d2-149">**CIM\_Dependency**</span></span>](cim-dependency.md)
</dt> </dl>

 

