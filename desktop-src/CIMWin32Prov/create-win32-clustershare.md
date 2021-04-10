---
description: Crea una nuova \_ istanza di ClusterShare Win32.
ms.assetid: a6fde28d-f19e-4a31-8f0d-35927c75a030
ms.tgt_platform: multiple
title: Metodo Create della classe Win32_ClusterShare
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- kbSyntax
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 7cbf7c42b8523bcd12b19e9b474ecc50bd031939
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104127650"
---
# <a name="create-method-of-the-win32_clustershare-class"></a><span data-ttu-id="bd222-103">Metodo Create della classe Win32 \_ ClusterShare</span><span class="sxs-lookup"><span data-stu-id="bd222-103">Create method of the Win32\_ClusterShare class</span></span>

<span data-ttu-id="bd222-104">Crea una nuova istanza di [**\_ ClusterShare Win32**](win32-clustershare.md) .</span><span class="sxs-lookup"><span data-stu-id="bd222-104">Creates a new [**Win32\_ClusterShare**](win32-clustershare.md) instance.</span></span>

## <a name="syntax"></a><span data-ttu-id="bd222-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="bd222-105">Syntax</span></span>


```mof
static uint32 Create(
  [in]           string                   Path,
  [in]           string                   Name,
  [in]           uint32                   Type,
  [in, optional] uint32                   MaximumAllowed,
  [in, optional] string                   Description,
  [in, optional] string                   Password,
  [in, optional] Win32_SecurityDescriptor Access
);
```



## <a name="parameters"></a><span data-ttu-id="bd222-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="bd222-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="bd222-107">*Percorso* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="bd222-107">*Path* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="bd222-108">Percorso locale della condivisione di Windows.</span><span class="sxs-lookup"><span data-stu-id="bd222-108">Local path of the Windows share.</span></span>

<span data-ttu-id="bd222-109">Esempio, "C: \\ Program Files".</span><span class="sxs-lookup"><span data-stu-id="bd222-109">Example, "C:\\Program Files".</span></span>

</dd> <dt>

<span data-ttu-id="bd222-110">*Nome* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="bd222-110">*Name* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="bd222-111">Alias di un percorso configurato come una condivisione in un computer in cui è in esecuzione Windows.</span><span class="sxs-lookup"><span data-stu-id="bd222-111">The alias to a path set up as a share on a computer system running Windows.</span></span>

<span data-ttu-id="bd222-112">Esempio "public".</span><span class="sxs-lookup"><span data-stu-id="bd222-112">Example, "public".</span></span>

</dd> <dt>

<span data-ttu-id="bd222-113">*Tipo* \[ di in\]</span><span class="sxs-lookup"><span data-stu-id="bd222-113">*Type* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="bd222-114">Tipo di risorsa condivisa.</span><span class="sxs-lookup"><span data-stu-id="bd222-114">Type of resource being shared.</span></span> <span data-ttu-id="bd222-115">I tipi includono le unità disco, le code di stampa, le comunicazioni interprocesso (IPC) e i dispositivi generali.</span><span class="sxs-lookup"><span data-stu-id="bd222-115">Types include: disk drives, print queues, interprocess communications (IPC), and general devices.</span></span>

<dt>

<span data-ttu-id="bd222-116">0 (0x0)</span><span class="sxs-lookup"><span data-stu-id="bd222-116">0 (0x0)</span></span>
</dt> <dd>

<span data-ttu-id="bd222-117">Unità disco</span><span class="sxs-lookup"><span data-stu-id="bd222-117">Disk Drive</span></span>

</dd> <dt>

<span data-ttu-id="bd222-118">1 (0x1)</span><span class="sxs-lookup"><span data-stu-id="bd222-118">1 (0x1)</span></span>
</dt> <dd>

<span data-ttu-id="bd222-119">Coda di stampa</span><span class="sxs-lookup"><span data-stu-id="bd222-119">Print Queue</span></span>

</dd> <dt>

<span data-ttu-id="bd222-120">2 (0x2)</span><span class="sxs-lookup"><span data-stu-id="bd222-120">2 (0x2)</span></span>
</dt> <dd>

<span data-ttu-id="bd222-121">Dispositivo</span><span class="sxs-lookup"><span data-stu-id="bd222-121">Device</span></span>

</dd> <dt>

<span data-ttu-id="bd222-122">3 (0x3)</span><span class="sxs-lookup"><span data-stu-id="bd222-122">3 (0x3)</span></span>
</dt> <dd>

<span data-ttu-id="bd222-123">IPC</span><span class="sxs-lookup"><span data-stu-id="bd222-123">IPC</span></span>

</dd> <dt>

<span data-ttu-id="bd222-124">2147483648 (0x80000000)</span><span class="sxs-lookup"><span data-stu-id="bd222-124">2147483648 (0x80000000)</span></span>
</dt> <dd>

<span data-ttu-id="bd222-125">Amministrazione unità disco</span><span class="sxs-lookup"><span data-stu-id="bd222-125">Disk Drive Admin</span></span>

</dd> <dt>

<span data-ttu-id="bd222-126">2147483649 (0x80000001)</span><span class="sxs-lookup"><span data-stu-id="bd222-126">2147483649 (0x80000001)</span></span>
</dt> <dd>

<span data-ttu-id="bd222-127">Amministrazione coda di stampa</span><span class="sxs-lookup"><span data-stu-id="bd222-127">Print Queue Admin</span></span>

</dd> <dt>

<span data-ttu-id="bd222-128">2147483650 (0x80000002)</span><span class="sxs-lookup"><span data-stu-id="bd222-128">2147483650 (0x80000002)</span></span>
</dt> <dd>

<span data-ttu-id="bd222-129">Amministratore del dispositivo</span><span class="sxs-lookup"><span data-stu-id="bd222-129">Device Admin</span></span>

</dd> <dt>

<span data-ttu-id="bd222-130">2147483651 (0x80000003)</span><span class="sxs-lookup"><span data-stu-id="bd222-130">2147483651 (0x80000003)</span></span>
</dt> <dd>

<span data-ttu-id="bd222-131">Amministratore IPC</span><span class="sxs-lookup"><span data-stu-id="bd222-131">IPC Admin</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="bd222-132">*MaximumAllowed* \[ in, facoltativo\]</span><span class="sxs-lookup"><span data-stu-id="bd222-132">*MaximumAllowed* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="bd222-133">Limite per il numero massimo di utenti che possono usare questa risorsa contemporaneamente.</span><span class="sxs-lookup"><span data-stu-id="bd222-133">Limit on the maximum number of users allowed to use this resource concurrently.</span></span>

</dd> <dt>

<span data-ttu-id="bd222-134">*Descrizione* \[ di in, facoltativo\]</span><span class="sxs-lookup"><span data-stu-id="bd222-134">*Description* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="bd222-135">Descrizione dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="bd222-135">Description of the object.</span></span>

</dd> <dt>

<span data-ttu-id="bd222-136">*Password* \[ di in, facoltativo\]</span><span class="sxs-lookup"><span data-stu-id="bd222-136">*Password* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="bd222-137">TBD</span><span class="sxs-lookup"><span data-stu-id="bd222-137">TBD</span></span>

</dd> <dt>

<span data-ttu-id="bd222-138">*Accesso* \[ a in, facoltativo\]</span><span class="sxs-lookup"><span data-stu-id="bd222-138">*Access* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="bd222-139">Istanza incorporata facoltativa di una classe [**\_ securityDescriptor Win32**](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptor) che contiene il descrittore di sicurezza per la nuova condivisione.</span><span class="sxs-lookup"><span data-stu-id="bd222-139">Optional embedded instance of a [**Win32\_SecurityDescriptor**](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptor) class that contains the security descriptor for the new share.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="bd222-140">Requisiti</span><span class="sxs-lookup"><span data-stu-id="bd222-140">Requirements</span></span>



| <span data-ttu-id="bd222-141">Requisito</span><span class="sxs-lookup"><span data-stu-id="bd222-141">Requirement</span></span> | <span data-ttu-id="bd222-142">Valore</span><span class="sxs-lookup"><span data-stu-id="bd222-142">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="bd222-143">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="bd222-143">Minimum supported client</span></span><br/> | <span data-ttu-id="bd222-144">Windows 7</span><span class="sxs-lookup"><span data-stu-id="bd222-144">Windows 7</span></span><br/>                                                                    |
| <span data-ttu-id="bd222-145">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="bd222-145">Minimum supported server</span></span><br/> | <span data-ttu-id="bd222-146">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="bd222-146">Windows Server 2008 R2</span></span><br/>                                                       |
| <span data-ttu-id="bd222-147">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="bd222-147">Namespace</span></span><br/>                | <span data-ttu-id="bd222-148">\\CIMV2 radice</span><span class="sxs-lookup"><span data-stu-id="bd222-148">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="bd222-149">MOF</span><span class="sxs-lookup"><span data-stu-id="bd222-149">MOF</span></span><br/>                      | <dl> <span data-ttu-id="bd222-150"><dt>Cimwin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="bd222-150"><dt>Cimwin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="bd222-151">DLL</span><span class="sxs-lookup"><span data-stu-id="bd222-151">DLL</span></span><br/>                      | <dl> <span data-ttu-id="bd222-152"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="bd222-152"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="bd222-153">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="bd222-153">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bd222-154">**\_ClusterShare Win32**</span><span class="sxs-lookup"><span data-stu-id="bd222-154">**Win32\_ClusterShare**</span></span>](win32-clustershare.md)
</dt> </dl>

 

