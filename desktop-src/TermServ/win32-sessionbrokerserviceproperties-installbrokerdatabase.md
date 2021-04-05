---
title: Metodo InstallBrokerDatabase della classe Win32_SessionBrokerServiceProperties
description: Installa un database gestore connessione Desktop remoto in un server SQL centrale.
ms.assetid: 9cc6fa4a-f1eb-49eb-bec4-acaff73190e8
ms.tgt_platform: multiple
keywords:
- Servizi Desktop remoto del metodo InstallBrokerDatabase
- Metodo InstallBrokerDatabase Servizi Desktop remoto, classe Win32_SessionBrokerServiceProperties
- Classe Win32_SessionBrokerServiceProperties Servizi Desktop remoto, metodo InstallBrokerDatabase
topic_type:
- apiref
api_name:
- Win32_SessionBrokerServiceProperties.InstallBrokerDatabase
api_location:
- TssdWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: da560bd4746c41864b3c56438f841efebe71ecd7
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103740199"
---
# <a name="installbrokerdatabase-method-of-the-win32_sessionbrokerserviceproperties-class"></a><span data-ttu-id="afeab-106">Metodo InstallBrokerDatabase della \_ classe SessionBrokerServiceProperties Win32</span><span class="sxs-lookup"><span data-stu-id="afeab-106">InstallBrokerDatabase method of the Win32\_SessionBrokerServiceProperties class</span></span>

<span data-ttu-id="afeab-107">Installa un database gestore connessione Desktop remoto in un server SQL centrale.</span><span class="sxs-lookup"><span data-stu-id="afeab-107">Installs an RD connection broker database on a central SQL server.</span></span>

## <a name="syntax"></a><span data-ttu-id="afeab-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="afeab-108">Syntax</span></span>


```mof
uint32 InstallBrokerDatabase(
  [in] string newDbFilePath,
  [in] string connStringToCentralDBMaster,
  [in] string centralRdcmsDbName
);
```



## <a name="parameters"></a><span data-ttu-id="afeab-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="afeab-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="afeab-110">*newDbFilePath* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="afeab-110">*newDbFilePath* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="afeab-111">nuovo percorso del file di database.</span><span class="sxs-lookup"><span data-stu-id="afeab-111">new database file path.</span></span>

</dd> <dt>

<span data-ttu-id="afeab-112">*connStringToCentralDBMaster* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="afeab-112">*connStringToCentralDBMaster* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="afeab-113">Stringa di connessione al Master di database centrale.</span><span class="sxs-lookup"><span data-stu-id="afeab-113">Connection string to the central database master.</span></span>

</dd> <dt>

<span data-ttu-id="afeab-114">*centralRdcmsDbName* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="afeab-114">*centralRdcmsDbName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="afeab-115">Nome del database centrale.</span><span class="sxs-lookup"><span data-stu-id="afeab-115">Name of the central database.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="afeab-116">Requisiti</span><span class="sxs-lookup"><span data-stu-id="afeab-116">Requirements</span></span>



| <span data-ttu-id="afeab-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="afeab-117">Requirement</span></span> | <span data-ttu-id="afeab-118">Valore</span><span class="sxs-lookup"><span data-stu-id="afeab-118">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="afeab-119">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="afeab-119">Minimum supported client</span></span><br/> | <span data-ttu-id="afeab-120">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="afeab-120">None supported</span></span><br/>                                                              |
| <span data-ttu-id="afeab-121">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="afeab-121">Minimum supported server</span></span><br/> | <span data-ttu-id="afeab-122">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="afeab-122">Windows Server 2012</span></span><br/>                                                         |
| <span data-ttu-id="afeab-123">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="afeab-123">Namespace</span></span><br/>                | <span data-ttu-id="afeab-124">Radice \\ CIMv2 \\ TerminalServices</span><span class="sxs-lookup"><span data-stu-id="afeab-124">Root\\CIMv2\\TerminalServices</span></span><br/>                                               |
| <span data-ttu-id="afeab-125">MOF</span><span class="sxs-lookup"><span data-stu-id="afeab-125">MOF</span></span><br/>                      | <dl> <span data-ttu-id="afeab-126"><dt>TssdWmi. mof</dt></span><span class="sxs-lookup"><span data-stu-id="afeab-126"><dt>TssdWmi.mof</dt></span></span> </dl> |
| <span data-ttu-id="afeab-127">DLL</span><span class="sxs-lookup"><span data-stu-id="afeab-127">DLL</span></span><br/>                      | <dl> <span data-ttu-id="afeab-128"><dt>TssdWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="afeab-128"><dt>TssdWmi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="afeab-129">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="afeab-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="afeab-130">**\_SessionBrokerServiceProperties Win32**</span><span class="sxs-lookup"><span data-stu-id="afeab-130">**Win32\_SessionBrokerServiceProperties**</span></span>](win32-sessionbrokerserviceproperties.md)
</dt> </dl>

 

 





