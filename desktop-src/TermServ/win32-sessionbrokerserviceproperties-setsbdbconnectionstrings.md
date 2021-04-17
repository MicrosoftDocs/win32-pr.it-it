---
title: Metodo SetSBDbConnectionStrings della classe Win32_SessionBrokerServiceProperties
description: Salva le stringhe di connessione del database, sia primarie che secondarie, nel registro di sistema.
ms.assetid: a9a20eca-22d9-495c-b976-2952c97be67e
ms.tgt_platform: multiple
keywords:
- Servizi Desktop remoto del metodo SetSBDbConnectionStrings
- Metodo SetSBDbConnectionStrings Servizi Desktop remoto, classe Win32_SessionBrokerServiceProperties
- Classe Win32_SessionBrokerServiceProperties Servizi Desktop remoto, metodo SetSBDbConnectionStrings
topic_type:
- apiref
api_name:
- Win32_SessionBrokerServiceProperties.SetSBDbConnectionStrings
api_location:
- RDMS.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2e4aa02cabe89e434fb8b24b308bbe2ec51fa5f4
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104476685"
---
# <a name="setsbdbconnectionstrings-method-of-the-win32_sessionbrokerserviceproperties-class"></a><span data-ttu-id="d34e1-106">Metodo SetSBDbConnectionStrings della \_ classe SessionBrokerServiceProperties Win32</span><span class="sxs-lookup"><span data-stu-id="d34e1-106">SetSBDbConnectionStrings method of the Win32\_SessionBrokerServiceProperties class</span></span>

<span data-ttu-id="d34e1-107">Salva le stringhe di connessione del database, sia primarie che secondarie, nel registro di sistema.</span><span class="sxs-lookup"><span data-stu-id="d34e1-107">Saves DB connection strings, both primary and secondary, in the registry.</span></span>

## <a name="syntax"></a><span data-ttu-id="d34e1-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="d34e1-108">Syntax</span></span>


```mof
uint32 SetSBDbConnectionStrings(
  [in] string connStringToCentralDBRdcms,
  [in] string secondaryConnStringToCentralDBRdcms
);
```



## <a name="parameters"></a><span data-ttu-id="d34e1-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="d34e1-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d34e1-110">*connStringToCentralDBRdcms* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="d34e1-110">*connStringToCentralDBRdcms* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d34e1-111">Stringa di connessione primaria.</span><span class="sxs-lookup"><span data-stu-id="d34e1-111">The primary connection string.</span></span>

</dd> <dt>

<span data-ttu-id="d34e1-112">*secondaryConnStringToCentralDBRdcms* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="d34e1-112">*secondaryConnStringToCentralDBRdcms* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d34e1-113">Stringa di connessione secondaria.</span><span class="sxs-lookup"><span data-stu-id="d34e1-113">The secondary connection string.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="d34e1-114">Requisiti</span><span class="sxs-lookup"><span data-stu-id="d34e1-114">Requirements</span></span>



| <span data-ttu-id="d34e1-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="d34e1-115">Requirement</span></span> | <span data-ttu-id="d34e1-116">Valore</span><span class="sxs-lookup"><span data-stu-id="d34e1-116">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="d34e1-117">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="d34e1-117">Minimum supported client</span></span><br/> | <span data-ttu-id="d34e1-118">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="d34e1-118">None supported</span></span><br/>                                                              |
| <span data-ttu-id="d34e1-119">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="d34e1-119">Minimum supported server</span></span><br/> | <span data-ttu-id="d34e1-120">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="d34e1-120">Windows Server 2016</span></span><br/>                                                         |
| <span data-ttu-id="d34e1-121">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="d34e1-121">Namespace</span></span><br/>                | <span data-ttu-id="d34e1-122">Radice \\ CIMv2 \\ TerminalServices</span><span class="sxs-lookup"><span data-stu-id="d34e1-122">Root\\CIMv2\\TerminalServices</span></span><br/>                                               |
| <span data-ttu-id="d34e1-123">MOF</span><span class="sxs-lookup"><span data-stu-id="d34e1-123">MOF</span></span><br/>                      | <dl> <span data-ttu-id="d34e1-124"><dt>TssdWmi. mof</dt></span><span class="sxs-lookup"><span data-stu-id="d34e1-124"><dt>TssdWmi.mof</dt></span></span> </dl> |
| <span data-ttu-id="d34e1-125">DLL</span><span class="sxs-lookup"><span data-stu-id="d34e1-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="d34e1-126"><dt>RDMS.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d34e1-126"><dt>RDMS.dll</dt></span></span> </dl>    |



## <a name="see-also"></a><span data-ttu-id="d34e1-127">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="d34e1-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d34e1-128">**\_SessionBrokerServiceProperties Win32**</span><span class="sxs-lookup"><span data-stu-id="d34e1-128">**Win32\_SessionBrokerServiceProperties**</span></span>](win32-sessionbrokerserviceproperties.md)
</dt> </dl>

 

 





