---
title: Metodo SetBrokerNonHAMode della classe Win32_SessionBrokerServiceProperties
description: Esegue la migrazione dei dati dalla SQL Server centrale a un database locale. Consente inoltre di configurare il server Broker per l'utilizzo del database locale.
ms.assetid: a73908be-0cc8-4512-842c-439d5cf18ed4
ms.tgt_platform: multiple
keywords:
- Servizi Desktop remoto del metodo SetBrokerNonHAMode
- Metodo SetBrokerNonHAMode Servizi Desktop remoto, classe Win32_SessionBrokerServiceProperties
- Classe Win32_SessionBrokerServiceProperties Servizi Desktop remoto, metodo SetBrokerNonHAMode
topic_type:
- apiref
api_name:
- Win32_SessionBrokerServiceProperties.SetBrokerNonHAMode
api_location:
- TssdWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0ef811bf8024f8e89f9739461dfa8499891077f3
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106301609"
---
# <a name="setbrokernonhamode-method-of-the-win32_sessionbrokerserviceproperties-class"></a><span data-ttu-id="adf4f-107">Metodo SetBrokerNonHAMode della \_ classe SessionBrokerServiceProperties Win32</span><span class="sxs-lookup"><span data-stu-id="adf4f-107">SetBrokerNonHAMode method of the Win32\_SessionBrokerServiceProperties class</span></span>

<span data-ttu-id="adf4f-108">Esegue la migrazione dei dati dalla SQL Server centrale a un database locale.</span><span class="sxs-lookup"><span data-stu-id="adf4f-108">Migrates data from central SQL Server to a local database.</span></span> <span data-ttu-id="adf4f-109">Consente inoltre di configurare il server Broker per l'utilizzo del database locale.</span><span class="sxs-lookup"><span data-stu-id="adf4f-109">It also configures the broker server to use the local database.</span></span>

## <a name="syntax"></a><span data-ttu-id="adf4f-110">Sintassi</span><span class="sxs-lookup"><span data-stu-id="adf4f-110">Syntax</span></span>


```mof
uint32 SetBrokerNonHAMode(
  [in] string connStringToCentralDBRdcms
);
```



## <a name="parameters"></a><span data-ttu-id="adf4f-111">Parametri</span><span class="sxs-lookup"><span data-stu-id="adf4f-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="adf4f-112">*connStringToCentralDBRdcms* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="adf4f-112">*connStringToCentralDBRdcms* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="adf4f-113">Stringa di connessione al database centrale.</span><span class="sxs-lookup"><span data-stu-id="adf4f-113">Connection string to the central database.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="adf4f-114">Requisiti</span><span class="sxs-lookup"><span data-stu-id="adf4f-114">Requirements</span></span>



| <span data-ttu-id="adf4f-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="adf4f-115">Requirement</span></span> | <span data-ttu-id="adf4f-116">Valore</span><span class="sxs-lookup"><span data-stu-id="adf4f-116">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="adf4f-117">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="adf4f-117">Minimum supported client</span></span><br/> | <span data-ttu-id="adf4f-118">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="adf4f-118">None supported</span></span><br/>                                                              |
| <span data-ttu-id="adf4f-119">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="adf4f-119">Minimum supported server</span></span><br/> | <span data-ttu-id="adf4f-120">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="adf4f-120">Windows Server 2012</span></span><br/>                                                         |
| <span data-ttu-id="adf4f-121">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="adf4f-121">Namespace</span></span><br/>                | <span data-ttu-id="adf4f-122">Radice \\ CIMv2 \\ TerminalServices</span><span class="sxs-lookup"><span data-stu-id="adf4f-122">Root\\CIMv2\\TerminalServices</span></span><br/>                                               |
| <span data-ttu-id="adf4f-123">MOF</span><span class="sxs-lookup"><span data-stu-id="adf4f-123">MOF</span></span><br/>                      | <dl> <span data-ttu-id="adf4f-124"><dt>TssdWmi. mof</dt></span><span class="sxs-lookup"><span data-stu-id="adf4f-124"><dt>TssdWmi.mof</dt></span></span> </dl> |
| <span data-ttu-id="adf4f-125">DLL</span><span class="sxs-lookup"><span data-stu-id="adf4f-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="adf4f-126"><dt>TssdWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="adf4f-126"><dt>TssdWmi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="adf4f-127">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="adf4f-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="adf4f-128">**\_SessionBrokerServiceProperties Win32**</span><span class="sxs-lookup"><span data-stu-id="adf4f-128">**Win32\_SessionBrokerServiceProperties**</span></span>](win32-sessionbrokerserviceproperties.md)
</dt> </dl>

 

 





