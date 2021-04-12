---
title: Metodo SetBrokerHAMode della classe Win32_SessionBrokerServiceProperties
description: Esegue la migrazione dei dati da un database WID locale al nuovo database basato su SQL Server. Configura inoltre il server Broker per l'utilizzo del server SQL centrale.
ms.assetid: 8f14590d-3042-403c-a1cb-a3b257866284
ms.tgt_platform: multiple
keywords:
- Servizi Desktop remoto del metodo SetBrokerHAMode
- Metodo SetBrokerHAMode Servizi Desktop remoto, classe Win32_SessionBrokerServiceProperties
- Classe Win32_SessionBrokerServiceProperties Servizi Desktop remoto, metodo SetBrokerHAMode
topic_type:
- apiref
api_name:
- Win32_SessionBrokerServiceProperties.SetBrokerHAMode
api_location:
- TssdWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4526f8ded96086ccf223b3c8e5aad72d9e0262cc
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104119766"
---
# <a name="setbrokerhamode-method-of-the-win32_sessionbrokerserviceproperties-class"></a><span data-ttu-id="f103e-107">Metodo SetBrokerHAMode della \_ classe SessionBrokerServiceProperties Win32</span><span class="sxs-lookup"><span data-stu-id="f103e-107">SetBrokerHAMode method of the Win32\_SessionBrokerServiceProperties class</span></span>

<span data-ttu-id="f103e-108">Esegue la migrazione dei dati da un database WID locale al nuovo database basato su SQL Server.</span><span class="sxs-lookup"><span data-stu-id="f103e-108">Migrates data from a local WID database to the new SQL server-based database.</span></span> <span data-ttu-id="f103e-109">Configura inoltre il server Broker per l'utilizzo del server SQL centrale.</span><span class="sxs-lookup"><span data-stu-id="f103e-109">It also configures the broker server to use the central SQL server.</span></span>

## <a name="syntax"></a><span data-ttu-id="f103e-110">Sintassi</span><span class="sxs-lookup"><span data-stu-id="f103e-110">Syntax</span></span>


```mof
uint32 SetBrokerHAMode(
  [in] string connStringToCentralDBRdcms,
  [in] string secondaryConnStringToCentralDBRdcms,
  [in] string brokerDnsRRName,
  [in] string activeBrokerName
);
```



## <a name="parameters"></a><span data-ttu-id="f103e-111">Parametri</span><span class="sxs-lookup"><span data-stu-id="f103e-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f103e-112">*connStringToCentralDBRdcms* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="f103e-112">*connStringToCentralDBRdcms* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f103e-113">Stringa di connessione al database centrale.</span><span class="sxs-lookup"><span data-stu-id="f103e-113">Connection string to the central database.</span></span>

</dd> <dt>

<span data-ttu-id="f103e-114">*secondaryConnStringToCentralDBRdcms* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="f103e-114">*secondaryConnStringToCentralDBRdcms* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f103e-115">Stringa di connessione secondaria al database centrale.</span><span class="sxs-lookup"><span data-stu-id="f103e-115">Secondary connection string to the central database.</span></span>

<span data-ttu-id="f103e-116">**Windows server 2012 R2 e Windows server 2012:** Questo parametro non è disponibile prima di Windows Server 2016.</span><span class="sxs-lookup"><span data-stu-id="f103e-116">**Windows Server 2012 R2 and Windows Server 2012:** This parameter is not available before Windows Server 2016.</span></span>

</dd> <dt>

<span data-ttu-id="f103e-117">*brokerDnsRRName* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="f103e-117">*brokerDnsRRName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f103e-118">Nome DNS del broker.</span><span class="sxs-lookup"><span data-stu-id="f103e-118">Broker DNS name.</span></span>

</dd> <dt>

<span data-ttu-id="f103e-119">*activeBrokerName* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="f103e-119">*activeBrokerName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f103e-120">Nome del broker attivo.</span><span class="sxs-lookup"><span data-stu-id="f103e-120">Active broker name.</span></span>

<span data-ttu-id="f103e-121">**Windows server 2012 R2 e Windows server 2012:** Questo parametro non è disponibile prima di Windows Server 2016.</span><span class="sxs-lookup"><span data-stu-id="f103e-121">**Windows Server 2012 R2 and Windows Server 2012:** This parameter is not available before Windows Server 2016.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="f103e-122">Requisiti</span><span class="sxs-lookup"><span data-stu-id="f103e-122">Requirements</span></span>



| <span data-ttu-id="f103e-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="f103e-123">Requirement</span></span> | <span data-ttu-id="f103e-124">Valore</span><span class="sxs-lookup"><span data-stu-id="f103e-124">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="f103e-125">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="f103e-125">Minimum supported client</span></span><br/> | <span data-ttu-id="f103e-126">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="f103e-126">None supported</span></span><br/>                                                              |
| <span data-ttu-id="f103e-127">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="f103e-127">Minimum supported server</span></span><br/> | <span data-ttu-id="f103e-128">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="f103e-128">Windows Server 2012</span></span><br/>                                                         |
| <span data-ttu-id="f103e-129">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="f103e-129">Namespace</span></span><br/>                | <span data-ttu-id="f103e-130">Radice \\ CIMv2 \\ TerminalServices</span><span class="sxs-lookup"><span data-stu-id="f103e-130">Root\\CIMv2\\TerminalServices</span></span><br/>                                               |
| <span data-ttu-id="f103e-131">MOF</span><span class="sxs-lookup"><span data-stu-id="f103e-131">MOF</span></span><br/>                      | <dl> <span data-ttu-id="f103e-132"><dt>TssdWmi. mof</dt></span><span class="sxs-lookup"><span data-stu-id="f103e-132"><dt>TssdWmi.mof</dt></span></span> </dl> |
| <span data-ttu-id="f103e-133">DLL</span><span class="sxs-lookup"><span data-stu-id="f103e-133">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f103e-134"><dt>TssdWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f103e-134"><dt>TssdWmi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f103e-135">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="f103e-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f103e-136">**\_SessionBrokerServiceProperties Win32**</span><span class="sxs-lookup"><span data-stu-id="f103e-136">**Win32\_SessionBrokerServiceProperties**</span></span>](win32-sessionbrokerserviceproperties.md)
</dt> </dl>

 

 





