---
title: Metodo SetActiveServer della classe Win32_RDMSEnvironment
description: Imposta il nome di dominio completo dell'ambiente Desktop remoto Management Services (RDBMS) sul nodo corrente.
ms.assetid: ed7b71cf-c3a4-4d2f-856a-31332f94fac9
ms.tgt_platform: multiple
keywords:
- Servizi Desktop remoto del metodo SetActiveServer
- Metodo SetActiveServer Servizi Desktop remoto, classe Win32_RDMSEnvironment
- Classe Win32_RDMSEnvironment Servizi Desktop remoto, metodo SetActiveServer
topic_type:
- apiref
api_name:
- Win32_RDMSEnvironment.SetActiveServer
api_location:
- RDMS.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7f11b378b15e271200c730691c3654fd10e80f3a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104476420"
---
# <a name="setactiveserver-method-of-the-win32_rdmsenvironment-class"></a><span data-ttu-id="08bd6-106">Metodo SetActiveServer della \_ classe RDMSEnvironment Win32</span><span class="sxs-lookup"><span data-stu-id="08bd6-106">SetActiveServer method of the Win32\_RDMSEnvironment class</span></span>

<span data-ttu-id="08bd6-107">Imposta il nome di dominio completo dell'ambiente Desktop remoto Management Services (RDBMS) sul nodo corrente.</span><span class="sxs-lookup"><span data-stu-id="08bd6-107">Sets the FQDN of the Remote Desktop Management Services (RDMS) environment to the current node.</span></span>

## <a name="syntax"></a><span data-ttu-id="08bd6-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="08bd6-108">Syntax</span></span>


```mof
uint32 SetActiveServer();
```



## <a name="parameters"></a><span data-ttu-id="08bd6-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="08bd6-109">Parameters</span></span>

<span data-ttu-id="08bd6-110">Questo metodo non presenta parametri.</span><span class="sxs-lookup"><span data-stu-id="08bd6-110">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="08bd6-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="08bd6-111">Return value</span></span>

<span data-ttu-id="08bd6-112">Restituisce 0 in caso di esito positivo, in caso contrario restituisce un codice di errore WMI.</span><span class="sxs-lookup"><span data-stu-id="08bd6-112">Returns 0 on success, otherwise returns a WMI error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="08bd6-113">Requisiti</span><span class="sxs-lookup"><span data-stu-id="08bd6-113">Requirements</span></span>



| <span data-ttu-id="08bd6-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="08bd6-114">Requirement</span></span> | <span data-ttu-id="08bd6-115">Valore</span><span class="sxs-lookup"><span data-stu-id="08bd6-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="08bd6-116">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="08bd6-116">Minimum supported client</span></span><br/> | <span data-ttu-id="08bd6-117">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="08bd6-117">None supported</span></span><br/>                                                                   |
| <span data-ttu-id="08bd6-118">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="08bd6-118">Minimum supported server</span></span><br/> | <span data-ttu-id="08bd6-119">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="08bd6-119">Windows Server 2012</span></span><br/>                                                              |
| <span data-ttu-id="08bd6-120">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="08bd6-120">Namespace</span></span><br/>                | <span data-ttu-id="08bd6-121">Radice \\ CIMv2 \\ RDBMS</span><span class="sxs-lookup"><span data-stu-id="08bd6-121">Root\\CIMv2\\rdms</span></span><br/>                                                                |
| <span data-ttu-id="08bd6-122">MOF</span><span class="sxs-lookup"><span data-stu-id="08bd6-122">MOF</span></span><br/>                      | <dl> <span data-ttu-id="08bd6-123"><dt>RDManagement. mof</dt></span><span class="sxs-lookup"><span data-stu-id="08bd6-123"><dt>RDManagement.mof</dt></span></span> </dl> |
| <span data-ttu-id="08bd6-124">DLL</span><span class="sxs-lookup"><span data-stu-id="08bd6-124">DLL</span></span><br/>                      | <dl> <span data-ttu-id="08bd6-125"><dt>RDMS.dll</dt></span><span class="sxs-lookup"><span data-stu-id="08bd6-125"><dt>RDMS.dll</dt></span></span> </dl>         |



## <a name="see-also"></a><span data-ttu-id="08bd6-126">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="08bd6-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="08bd6-127">**\_RDMSEnvironment Win32**</span><span class="sxs-lookup"><span data-stu-id="08bd6-127">**Win32\_RDMSEnvironment**</span></span>](win32-rdmsenvironment.md)
</dt> </dl>

 

 





