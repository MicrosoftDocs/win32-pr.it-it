---
title: Metodo DeleteSBDbConnectionString della classe Win32_SessionBrokerServiceProperties
description: Elimina le stringhe di connessione del database (primaria o secondaria) dal registro di sistema.
ms.assetid: 275dd790-bdc7-46d1-a07d-54ec6fa33e44
ms.tgt_platform: multiple
keywords:
- Servizi Desktop remoto del metodo DeleteSBDbConnectionString
- Metodo DeleteSBDbConnectionString Servizi Desktop remoto, classe Win32_SessionBrokerServiceProperties
- Classe Win32_SessionBrokerServiceProperties Servizi Desktop remoto, metodo DeleteSBDbConnectionString
topic_type:
- apiref
api_name:
- Win32_SessionBrokerServiceProperties.DeleteSBDbConnectionString
api_location:
- TssdWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d2e2a9701afebe150f0c8dc0e4bf437dd23586c3
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106301610"
---
# <a name="deletesbdbconnectionstring-method-of-the-win32_sessionbrokerserviceproperties-class"></a><span data-ttu-id="8b8ca-106">Metodo DeleteSBDbConnectionString della \_ classe SessionBrokerServiceProperties Win32</span><span class="sxs-lookup"><span data-stu-id="8b8ca-106">DeleteSBDbConnectionString method of the Win32\_SessionBrokerServiceProperties class</span></span>

<span data-ttu-id="8b8ca-107">Elimina le stringhe di connessione del database (primaria o secondaria) dal registro di sistema.</span><span class="sxs-lookup"><span data-stu-id="8b8ca-107">Deletes DB connection strings (primary or secondary) from the registry.</span></span>

## <a name="syntax"></a><span data-ttu-id="8b8ca-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="8b8ca-108">Syntax</span></span>


```mof
uint32 DeleteSBDbConnectionString(
  [in] boolean IsSecondaryConnString
);
```



## <a name="parameters"></a><span data-ttu-id="8b8ca-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="8b8ca-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8b8ca-110">*IsSecondaryConnString* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="8b8ca-110">*IsSecondaryConnString* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8b8ca-111">Se **true**, la stringa di connessione secondaria viene rimossa.</span><span class="sxs-lookup"><span data-stu-id="8b8ca-111">If **True**, secondary connection string is removed.</span></span> <span data-ttu-id="8b8ca-112">Se **false**, la stringa di connessione primaria viene rimossa.</span><span class="sxs-lookup"><span data-stu-id="8b8ca-112">If **False**, primary connection string is removed.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="8b8ca-113">Requisiti</span><span class="sxs-lookup"><span data-stu-id="8b8ca-113">Requirements</span></span>



| <span data-ttu-id="8b8ca-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="8b8ca-114">Requirement</span></span> | <span data-ttu-id="8b8ca-115">Valore</span><span class="sxs-lookup"><span data-stu-id="8b8ca-115">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="8b8ca-116">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="8b8ca-116">Minimum supported client</span></span><br/> | <span data-ttu-id="8b8ca-117">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="8b8ca-117">None supported</span></span><br/>                                                              |
| <span data-ttu-id="8b8ca-118">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="8b8ca-118">Minimum supported server</span></span><br/> | <span data-ttu-id="8b8ca-119">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="8b8ca-119">Windows Server 2016</span></span><br/>                                                         |
| <span data-ttu-id="8b8ca-120">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="8b8ca-120">Namespace</span></span><br/>                | <span data-ttu-id="8b8ca-121">Radice \\ CIMv2 \\ TerminalServices</span><span class="sxs-lookup"><span data-stu-id="8b8ca-121">Root\\CIMv2\\TerminalServices</span></span><br/>                                               |
| <span data-ttu-id="8b8ca-122">MOF</span><span class="sxs-lookup"><span data-stu-id="8b8ca-122">MOF</span></span><br/>                      | <dl> <span data-ttu-id="8b8ca-123"><dt>TssdWmi. mof</dt></span><span class="sxs-lookup"><span data-stu-id="8b8ca-123"><dt>TssdWmi.mof</dt></span></span> </dl> |
| <span data-ttu-id="8b8ca-124">DLL</span><span class="sxs-lookup"><span data-stu-id="8b8ca-124">DLL</span></span><br/>                      | <dl> <span data-ttu-id="8b8ca-125"><dt>TssdWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="8b8ca-125"><dt>TssdWmi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8b8ca-126">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="8b8ca-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8b8ca-127">**\_SessionBrokerServiceProperties Win32**</span><span class="sxs-lookup"><span data-stu-id="8b8ca-127">**Win32\_SessionBrokerServiceProperties**</span></span>](win32-sessionbrokerserviceproperties.md)
</dt> </dl>

 

 





