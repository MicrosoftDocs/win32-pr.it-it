---
title: Metodo Export della classe Win32_TSVm
description: Recupera le informazioni di monitoraggio della sessione della macchina virtuale.
ms.assetid: 7996651c-aa7c-4fde-84a6-928b27c8c5b8
ms.tgt_platform: multiple
keywords:
- Esporta il metodo Servizi Desktop remoto
- Metodo Export Servizi Desktop remoto, classe Win32_TSVm
- Classe Win32_TSVm Servizi Desktop remoto, metodo Export
topic_type:
- apiref
api_name:
- Win32_TSVm.Export
api_location:
- TSVmHostWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c72d94b24af5563f9cdb668e269c260e8fe19049
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106301230"
---
# <a name="export-method-of-the-win32_tsvm-class"></a><span data-ttu-id="a3078-106">Metodo Export della classe Win32 \_ TSVm</span><span class="sxs-lookup"><span data-stu-id="a3078-106">Export method of the Win32\_TSVm class</span></span>

<span data-ttu-id="a3078-107">Recupera le informazioni di monitoraggio della sessione della macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="a3078-107">Retrieves the virtual machine session monitoring information.</span></span>

## <a name="syntax"></a><span data-ttu-id="a3078-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="a3078-108">Syntax</span></span>


```mof
uint32 Export(
  [in]  string ExportFolderPath,
  [out] string ExportJobObjectPath
);
```



## <a name="parameters"></a><span data-ttu-id="a3078-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="a3078-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a3078-110">*ExportFolderPath* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="a3078-110">*ExportFolderPath* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a3078-111">Percorso in cui verrà esportata la macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="a3078-111">Path to where the virtual machine will be exported.</span></span>

</dd> <dt>

<span data-ttu-id="a3078-112">*ExportJobObjectPath* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="a3078-112">*ExportJobObjectPath* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="a3078-113">In seguito all'esito positivo restituisce il percorso dell'oggetto HyperV ConcreteJob.</span><span class="sxs-lookup"><span data-stu-id="a3078-113">On a success returns the HyperV ConcreteJob object path.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a3078-114">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="a3078-114">Return value</span></span>

<span data-ttu-id="a3078-115">Restituisce 0 in caso di esito positivo, in caso contrario restituisce un codice di errore WMI.</span><span class="sxs-lookup"><span data-stu-id="a3078-115">Returns 0 on success, otherwise returns a WMI error code.</span></span> <span data-ttu-id="a3078-116">Per un elenco di questi valori, vedere [Servizi Desktop remoto codici di errore del provider WMI](terminal-services-wmi-provider-error-codes.md) .</span><span class="sxs-lookup"><span data-stu-id="a3078-116">Refer to [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md) for a list of these values.</span></span>

## <a name="requirements"></a><span data-ttu-id="a3078-117">Requisiti</span><span class="sxs-lookup"><span data-stu-id="a3078-117">Requirements</span></span>



| <span data-ttu-id="a3078-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="a3078-118">Requirement</span></span> | <span data-ttu-id="a3078-119">Valore</span><span class="sxs-lookup"><span data-stu-id="a3078-119">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------|
| <span data-ttu-id="a3078-120">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="a3078-120">Minimum supported client</span></span><br/> | <span data-ttu-id="a3078-121">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="a3078-121">None supported</span></span><br/>                                                                  |
| <span data-ttu-id="a3078-122">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="a3078-122">Minimum supported server</span></span><br/> | <span data-ttu-id="a3078-123">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="a3078-123">Windows Server 2012</span></span><br/>                                                             |
| <span data-ttu-id="a3078-124">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="a3078-124">Namespace</span></span><br/>                | <span data-ttu-id="a3078-125">Radice \\ CIMv2 \\ TerminalServices</span><span class="sxs-lookup"><span data-stu-id="a3078-125">Root\\CIMv2\\TerminalServices</span></span><br/>                                                   |
| <span data-ttu-id="a3078-126">MOF</span><span class="sxs-lookup"><span data-stu-id="a3078-126">MOF</span></span><br/>                      | <dl> <span data-ttu-id="a3078-127"><dt>TSVmHost. mof</dt></span><span class="sxs-lookup"><span data-stu-id="a3078-127"><dt>TSVmHost.mof</dt></span></span> </dl>    |
| <span data-ttu-id="a3078-128">DLL</span><span class="sxs-lookup"><span data-stu-id="a3078-128">DLL</span></span><br/>                      | <dl> <span data-ttu-id="a3078-129"><dt>TSVmHostWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a3078-129"><dt>TSVmHostWmi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a3078-130">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="a3078-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a3078-131">**\_TSVm Win32**</span><span class="sxs-lookup"><span data-stu-id="a3078-131">**Win32\_TSVm**</span></span>](win32-tsvm.md)
</dt> </dl>

 

 





