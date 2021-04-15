---
title: Metodo IsDbReachable della classe Win32_SessionBrokerServiceProperties
description: Controlla se il database è raggiungibile.
ms.assetid: c9774d6d-1b78-4ec1-bae2-80d41d4c9b06
ms.tgt_platform: multiple
keywords:
- Servizi Desktop remoto del metodo IsDbReachable
- Metodo IsDbReachable Servizi Desktop remoto, classe Win32_SessionBrokerServiceProperties
- Classe Win32_SessionBrokerServiceProperties Servizi Desktop remoto, metodo IsDbReachable
topic_type:
- apiref
api_name:
- Win32_SessionBrokerServiceProperties.IsDbReachable
api_location:
- TssdWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d3a59b8b0eba80dd832b3967b5e626642684f0c1
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104476690"
---
# <a name="isdbreachable-method-of-the-win32_sessionbrokerserviceproperties-class"></a><span data-ttu-id="c14b9-106">Metodo IsDbReachable della \_ classe SessionBrokerServiceProperties Win32</span><span class="sxs-lookup"><span data-stu-id="c14b9-106">IsDbReachable method of the Win32\_SessionBrokerServiceProperties class</span></span>

<span data-ttu-id="c14b9-107">Controlla se il database è raggiungibile.</span><span class="sxs-lookup"><span data-stu-id="c14b9-107">Checks if the database is reachable.</span></span>

## <a name="syntax"></a><span data-ttu-id="c14b9-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="c14b9-108">Syntax</span></span>


```mof
uint32 IsDbReachable(
  [in] string connStringToDb,
  [in] string connSecondaryStringToDb,
  [in] string activeBrokerName
);
```



## <a name="parameters"></a><span data-ttu-id="c14b9-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="c14b9-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c14b9-110">*connStringToDb* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="c14b9-110">*connStringToDb* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c14b9-111">Stringa di connessione al database.</span><span class="sxs-lookup"><span data-stu-id="c14b9-111">The connection string to the database.</span></span>

</dd> <dt>

<span data-ttu-id="c14b9-112">*connSecondaryStringToDb* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="c14b9-112">*connSecondaryStringToDb* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c14b9-113">Stringa di connessione secondaria al database centrale.</span><span class="sxs-lookup"><span data-stu-id="c14b9-113">Secondary connection string to the central database.</span></span>

<span data-ttu-id="c14b9-114">**Windows server 2012 R2 e Windows server 2012:** Questo parametro non è disponibile prima di Windows Server 2016.</span><span class="sxs-lookup"><span data-stu-id="c14b9-114">**Windows Server 2012 R2 and Windows Server 2012:** This parameter is not available before Windows Server 2016.</span></span>

</dd> <dt>

<span data-ttu-id="c14b9-115">*activeBrokerName* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="c14b9-115">*activeBrokerName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c14b9-116">Nome del broker attivo.</span><span class="sxs-lookup"><span data-stu-id="c14b9-116">Active broker name.</span></span>

<span data-ttu-id="c14b9-117">**Windows server 2012 R2 e Windows server 2012:** Questo parametro non è disponibile prima di Windows Server 2016.</span><span class="sxs-lookup"><span data-stu-id="c14b9-117">**Windows Server 2012 R2 and Windows Server 2012:** This parameter is not available before Windows Server 2016.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="c14b9-118">Requisiti</span><span class="sxs-lookup"><span data-stu-id="c14b9-118">Requirements</span></span>



| <span data-ttu-id="c14b9-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="c14b9-119">Requirement</span></span> | <span data-ttu-id="c14b9-120">Valore</span><span class="sxs-lookup"><span data-stu-id="c14b9-120">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="c14b9-121">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="c14b9-121">Minimum supported client</span></span><br/> | <span data-ttu-id="c14b9-122">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="c14b9-122">None supported</span></span><br/>                                                              |
| <span data-ttu-id="c14b9-123">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="c14b9-123">Minimum supported server</span></span><br/> | <span data-ttu-id="c14b9-124">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="c14b9-124">Windows Server 2012</span></span><br/>                                                         |
| <span data-ttu-id="c14b9-125">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="c14b9-125">Namespace</span></span><br/>                | <span data-ttu-id="c14b9-126">Radice \\ CIMv2 \\ TerminalServices</span><span class="sxs-lookup"><span data-stu-id="c14b9-126">Root\\CIMv2\\TerminalServices</span></span><br/>                                               |
| <span data-ttu-id="c14b9-127">MOF</span><span class="sxs-lookup"><span data-stu-id="c14b9-127">MOF</span></span><br/>                      | <dl> <span data-ttu-id="c14b9-128"><dt>TssdWmi. mof</dt></span><span class="sxs-lookup"><span data-stu-id="c14b9-128"><dt>TssdWmi.mof</dt></span></span> </dl> |
| <span data-ttu-id="c14b9-129">DLL</span><span class="sxs-lookup"><span data-stu-id="c14b9-129">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c14b9-130"><dt>TssdWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c14b9-130"><dt>TssdWmi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c14b9-131">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="c14b9-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c14b9-132">**\_SessionBrokerServiceProperties Win32**</span><span class="sxs-lookup"><span data-stu-id="c14b9-132">**Win32\_SessionBrokerServiceProperties**</span></span>](win32-sessionbrokerserviceproperties.md)
</dt> </dl>

 

 





