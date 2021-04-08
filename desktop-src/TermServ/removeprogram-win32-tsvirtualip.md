---
title: Metodo RemoveProgram della classe Win32_TSVirtualIP (Bdaiface. h)
description: Rimuove un programma dall'elenco di programmi che utilizzano la virtualizzazione IP.
ms.assetid: 2a8069a0-2c48-40d3-a850-0cdfce4fbc82
ms.tgt_platform: multiple
keywords:
- Servizi Desktop remoto del metodo RemoveProgram
- Metodo RemoveProgram Servizi Desktop remoto, classe Win32_TSVirtualIP
- Classe Win32_TSVirtualIP Servizi Desktop remoto, metodo RemoveProgram
topic_type:
- apiref
api_name:
- Win32_TSVirtualIP.RemoveProgram
api_location:
- TSCfgWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d6241664b6e56c3d387673b6a1cc50e43b413336
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103743626"
---
# <a name="removeprogram-method-of-the-win32_tsvirtualip-class"></a><span data-ttu-id="d1668-106">Metodo RemoveProgram della \_ classe TSVirtualIP Win32</span><span class="sxs-lookup"><span data-stu-id="d1668-106">RemoveProgram method of the Win32\_TSVirtualIP class</span></span>

<span data-ttu-id="d1668-107">Rimuove un programma dall'elenco di programmi che utilizzano la virtualizzazione IP.</span><span class="sxs-lookup"><span data-stu-id="d1668-107">Removes a program from the list of programs that use IP virtualization.</span></span>

## <a name="syntax"></a><span data-ttu-id="d1668-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="d1668-108">Syntax</span></span>


```mof
uint32 RemoveProgram(
  [in] string ProgramPath
);
```



## <a name="parameters"></a><span data-ttu-id="d1668-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="d1668-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d1668-110">*ProgramPath* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="d1668-110">*ProgramPath* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d1668-111">Tipo: **stringa**</span><span class="sxs-lookup"><span data-stu-id="d1668-111">Type: **string**</span></span>

<span data-ttu-id="d1668-112">Percorso e nome file del programma da rimuovere dall'elenco.</span><span class="sxs-lookup"><span data-stu-id="d1668-112">The path and file name of the program to remove from the list.</span></span> <span data-ttu-id="d1668-113">Se il programma non viene trovato, viene restituito un errore.</span><span class="sxs-lookup"><span data-stu-id="d1668-113">If the program is not found, an error is returned.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d1668-114">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="d1668-114">Return value</span></span>

<span data-ttu-id="d1668-115">Tipo: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="d1668-115">Type: **uint32**</span></span>

<span data-ttu-id="d1668-116">Restituisce 0 in caso di esito positivo, in caso contrario restituisce un codice di errore WMI.</span><span class="sxs-lookup"><span data-stu-id="d1668-116">Returns 0 on success, otherwise returns a WMI error code.</span></span> <span data-ttu-id="d1668-117">Per un elenco di questi valori, vedere [Servizi Desktop remoto codici di errore del provider WMI](terminal-services-wmi-provider-error-codes.md) .</span><span class="sxs-lookup"><span data-stu-id="d1668-117">Refer to [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md) for a list of these values.</span></span> <span data-ttu-id="d1668-118">Il metodo restituisce un errore se l'impostazione è sotto il controllo criteri di gruppo.</span><span class="sxs-lookup"><span data-stu-id="d1668-118">The method returns an error if the setting is under group policy control.</span></span>

## <a name="requirements"></a><span data-ttu-id="d1668-119">Requisiti</span><span class="sxs-lookup"><span data-stu-id="d1668-119">Requirements</span></span>



| <span data-ttu-id="d1668-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="d1668-120">Requirement</span></span> | <span data-ttu-id="d1668-121">Valore</span><span class="sxs-lookup"><span data-stu-id="d1668-121">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="d1668-122">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="d1668-122">Minimum supported client</span></span><br/> | <span data-ttu-id="d1668-123">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="d1668-123">None supported</span></span><br/>                                                               |
| <span data-ttu-id="d1668-124">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="d1668-124">Minimum supported server</span></span><br/> | <span data-ttu-id="d1668-125">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="d1668-125">Windows Server 2008 R2</span></span><br/>                                                       |
| <span data-ttu-id="d1668-126">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="d1668-126">Namespace</span></span><br/>                | <span data-ttu-id="d1668-127">Radice \\ CIMv2 \\ TerminalServices</span><span class="sxs-lookup"><span data-stu-id="d1668-127">Root\\CIMv2\\TerminalServices</span></span><br/>                                                |
| <span data-ttu-id="d1668-128">Intestazione</span><span class="sxs-lookup"><span data-stu-id="d1668-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="d1668-129"><dt>Bdaiface. h</dt></span><span class="sxs-lookup"><span data-stu-id="d1668-129"><dt>Bdaiface.h</dt></span></span> </dl>   |
| <span data-ttu-id="d1668-130">MOF</span><span class="sxs-lookup"><span data-stu-id="d1668-130">MOF</span></span><br/>                      | <dl> <span data-ttu-id="d1668-131"><dt>TSCfgWmi. mof</dt></span><span class="sxs-lookup"><span data-stu-id="d1668-131"><dt>TSCfgWmi.mof</dt></span></span> </dl> |
| <span data-ttu-id="d1668-132">DLL</span><span class="sxs-lookup"><span data-stu-id="d1668-132">DLL</span></span><br/>                      | <dl> <span data-ttu-id="d1668-133"><dt>TSCfgWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d1668-133"><dt>TSCfgWmi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d1668-134">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="d1668-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d1668-135">**\_TSVirtualIP Win32**</span><span class="sxs-lookup"><span data-stu-id="d1668-135">**Win32\_TSVirtualIP**</span></span>](win32-tsvirtualip.md)
</dt> </dl>

 

 





