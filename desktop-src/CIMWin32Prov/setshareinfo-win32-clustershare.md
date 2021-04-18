---
description: Imposta i parametri della risorsa condivisa.
ms.assetid: 592d0fa6-c865-4f70-89c3-b58204a8c5a6
ms.tgt_platform: multiple
title: Metodo SetShareInfo della classe Win32_ClusterShare
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_ClusterShare.SetShareInfo
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: bda6fe36d1168045ea9f8d331ff334920ed1dd19
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106305278"
---
# <a name="setshareinfo-method-of-the-win32_clustershare-class"></a><span data-ttu-id="3ce1e-103">Metodo SetShareInfo della \_ classe ClusterShare Win32</span><span class="sxs-lookup"><span data-stu-id="3ce1e-103">SetShareInfo method of the Win32\_ClusterShare class</span></span>

<span data-ttu-id="3ce1e-104">Imposta i parametri della risorsa condivisa.</span><span class="sxs-lookup"><span data-stu-id="3ce1e-104">Sets the parameters of the shared resource.</span></span>

## <a name="syntax"></a><span data-ttu-id="3ce1e-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="3ce1e-105">Syntax</span></span>


```mof
uint32 SetShareInfo(
  [in, optional] uint32                   MaximumAllowed,
  [in, optional] string                   Description,
  [in, optional] Win32_SecurityDescriptor Access
);
```



## <a name="parameters"></a><span data-ttu-id="3ce1e-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="3ce1e-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3ce1e-107">*MaximumAllowed* \[ in, facoltativo\]</span><span class="sxs-lookup"><span data-stu-id="3ce1e-107">*MaximumAllowed* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="3ce1e-108">Limite per il numero massimo di utenti che possono usare questa risorsa contemporaneamente.</span><span class="sxs-lookup"><span data-stu-id="3ce1e-108">Limit on the maximum number of users allowed to use this resource concurrently.</span></span>

</dd> <dt>

<span data-ttu-id="3ce1e-109">*Descrizione* \[ di in, facoltativo\]</span><span class="sxs-lookup"><span data-stu-id="3ce1e-109">*Description* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="3ce1e-110">Descrive la risorsa condivisa.</span><span class="sxs-lookup"><span data-stu-id="3ce1e-110">Describes the resource being shared.</span></span>

</dd> <dt>

<span data-ttu-id="3ce1e-111">*Accesso* \[ a in, facoltativo\]</span><span class="sxs-lookup"><span data-stu-id="3ce1e-111">*Access* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="3ce1e-112">Descrittore di sicurezza per le autorizzazioni a livello di utente.</span><span class="sxs-lookup"><span data-stu-id="3ce1e-112">Security descriptor for user-level permissions.</span></span> <span data-ttu-id="3ce1e-113">Un descrittore di sicurezza contiene informazioni sulle funzionalità di autorizzazione, proprietario e accesso della risorsa.</span><span class="sxs-lookup"><span data-stu-id="3ce1e-113">A security descriptor contains information about the permission, owner, and access capabilities of the resource.</span></span> <span data-ttu-id="3ce1e-114">Per ulteriori informazioni, vedere [**Win32 \_ securityDescriptor**](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptor).</span><span class="sxs-lookup"><span data-stu-id="3ce1e-114">For more information, see [**Win32\_SecurityDescriptor**](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptor).</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="3ce1e-115">Requisiti</span><span class="sxs-lookup"><span data-stu-id="3ce1e-115">Requirements</span></span>



| <span data-ttu-id="3ce1e-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="3ce1e-116">Requirement</span></span> | <span data-ttu-id="3ce1e-117">Valore</span><span class="sxs-lookup"><span data-stu-id="3ce1e-117">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="3ce1e-118">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="3ce1e-118">Minimum supported client</span></span><br/> | <span data-ttu-id="3ce1e-119">Windows 7</span><span class="sxs-lookup"><span data-stu-id="3ce1e-119">Windows 7</span></span><br/>                                                                    |
| <span data-ttu-id="3ce1e-120">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="3ce1e-120">Minimum supported server</span></span><br/> | <span data-ttu-id="3ce1e-121">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="3ce1e-121">Windows Server 2008 R2</span></span><br/>                                                       |
| <span data-ttu-id="3ce1e-122">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="3ce1e-122">Namespace</span></span><br/>                | <span data-ttu-id="3ce1e-123">\\CIMV2 radice</span><span class="sxs-lookup"><span data-stu-id="3ce1e-123">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="3ce1e-124">MOF</span><span class="sxs-lookup"><span data-stu-id="3ce1e-124">MOF</span></span><br/>                      | <dl> <span data-ttu-id="3ce1e-125"><dt>Cimwin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="3ce1e-125"><dt>Cimwin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="3ce1e-126">DLL</span><span class="sxs-lookup"><span data-stu-id="3ce1e-126">DLL</span></span><br/>                      | <dl> <span data-ttu-id="3ce1e-127"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="3ce1e-127"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3ce1e-128">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="3ce1e-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3ce1e-129">**\_ClusterShare Win32**</span><span class="sxs-lookup"><span data-stu-id="3ce1e-129">**Win32\_ClusterShare**</span></span>](win32-clustershare.md)
</dt> </dl>

 

