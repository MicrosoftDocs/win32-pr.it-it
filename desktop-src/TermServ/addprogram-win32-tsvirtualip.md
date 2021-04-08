---
title: Metodo AddProgram della classe Win32_TSVirtualIP (Bdaiface. h)
description: Aggiunge un programma all'elenco di programmi che utilizzano la virtualizzazione IP.
ms.assetid: 4d142774-fa7a-4cfb-9305-5a61b0ef5438
ms.tgt_platform: multiple
keywords:
- Servizi Desktop remoto del metodo AddProgram
- Metodo AddProgram Servizi Desktop remoto, classe Win32_TSVirtualIP
- Classe Win32_TSVirtualIP Servizi Desktop remoto, metodo AddProgram
topic_type:
- apiref
api_name:
- Win32_TSVirtualIP.AddProgram
api_location:
- TSCfgWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4de573e8d04500917ed44d5a0453005b3aa691bf
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103740767"
---
# <a name="addprogram-method-of-the-win32_tsvirtualip-class"></a><span data-ttu-id="cf48a-106">Metodo AddProgram della \_ classe TSVirtualIP Win32</span><span class="sxs-lookup"><span data-stu-id="cf48a-106">AddProgram method of the Win32\_TSVirtualIP class</span></span>

<span data-ttu-id="cf48a-107">Aggiunge un programma all'elenco di programmi che utilizzano la virtualizzazione IP.</span><span class="sxs-lookup"><span data-stu-id="cf48a-107">Adds a program to the list of programs that use IP virtualization.</span></span>

## <a name="syntax"></a><span data-ttu-id="cf48a-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="cf48a-108">Syntax</span></span>


```mof
uint32 AddProgram(
  [in] string ProgramPath
);
```



## <a name="parameters"></a><span data-ttu-id="cf48a-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="cf48a-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="cf48a-110">*ProgramPath* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="cf48a-110">*ProgramPath* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="cf48a-111">Tipo: **stringa**</span><span class="sxs-lookup"><span data-stu-id="cf48a-111">Type: **string**</span></span>

<span data-ttu-id="cf48a-112">Il percorso e il nome file del programma da aggiungere all'elenco.</span><span class="sxs-lookup"><span data-stu-id="cf48a-112">The path and file name of the program to add to the list.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="cf48a-113">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="cf48a-113">Return value</span></span>

<span data-ttu-id="cf48a-114">Tipo: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="cf48a-114">Type: **uint32**</span></span>

<span data-ttu-id="cf48a-115">Restituisce 0 in caso di esito positivo, in caso contrario restituisce un codice di errore WMI.</span><span class="sxs-lookup"><span data-stu-id="cf48a-115">Returns 0 on success, otherwise returns a WMI error code.</span></span> <span data-ttu-id="cf48a-116">Per un elenco di questi valori, vedere [Servizi Desktop remoto codici di errore del provider WMI](terminal-services-wmi-provider-error-codes.md) .</span><span class="sxs-lookup"><span data-stu-id="cf48a-116">Refer to [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md) for a list of these values.</span></span> <span data-ttu-id="cf48a-117">Il metodo restituisce un errore se l'impostazione è sotto il controllo criteri di gruppo.</span><span class="sxs-lookup"><span data-stu-id="cf48a-117">The method returns an error if the setting is under group policy control.</span></span>

## <a name="requirements"></a><span data-ttu-id="cf48a-118">Requisiti</span><span class="sxs-lookup"><span data-stu-id="cf48a-118">Requirements</span></span>



| <span data-ttu-id="cf48a-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="cf48a-119">Requirement</span></span> | <span data-ttu-id="cf48a-120">Valore</span><span class="sxs-lookup"><span data-stu-id="cf48a-120">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="cf48a-121">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="cf48a-121">Minimum supported client</span></span><br/> | <span data-ttu-id="cf48a-122">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="cf48a-122">None supported</span></span><br/>                                                               |
| <span data-ttu-id="cf48a-123">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="cf48a-123">Minimum supported server</span></span><br/> | <span data-ttu-id="cf48a-124">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="cf48a-124">Windows Server 2008 R2</span></span><br/>                                                       |
| <span data-ttu-id="cf48a-125">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="cf48a-125">Namespace</span></span><br/>                | <span data-ttu-id="cf48a-126">Radice \\ CIMv2 \\ TerminalServices</span><span class="sxs-lookup"><span data-stu-id="cf48a-126">Root\\CIMv2\\TerminalServices</span></span><br/>                                                |
| <span data-ttu-id="cf48a-127">Intestazione</span><span class="sxs-lookup"><span data-stu-id="cf48a-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="cf48a-128"><dt>Bdaiface. h</dt></span><span class="sxs-lookup"><span data-stu-id="cf48a-128"><dt>Bdaiface.h</dt></span></span> </dl>   |
| <span data-ttu-id="cf48a-129">MOF</span><span class="sxs-lookup"><span data-stu-id="cf48a-129">MOF</span></span><br/>                      | <dl> <span data-ttu-id="cf48a-130"><dt>TSCfgWmi. mof</dt></span><span class="sxs-lookup"><span data-stu-id="cf48a-130"><dt>TSCfgWmi.mof</dt></span></span> </dl> |
| <span data-ttu-id="cf48a-131">DLL</span><span class="sxs-lookup"><span data-stu-id="cf48a-131">DLL</span></span><br/>                      | <dl> <span data-ttu-id="cf48a-132"><dt>TSCfgWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="cf48a-132"><dt>TSCfgWmi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="cf48a-133">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="cf48a-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cf48a-134">**\_TSVirtualIP Win32**</span><span class="sxs-lookup"><span data-stu-id="cf48a-134">**Win32\_TSVirtualIP**</span></span>](win32-tsvirtualip.md)
</dt> </dl>

 

 





