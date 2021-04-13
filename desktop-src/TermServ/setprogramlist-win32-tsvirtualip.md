---
title: Metodo seprogrammer della classe Win32_TSVirtualIP
description: Sovrascrive l'elenco di programmi che usano la virtualizzazione IP.
ms.assetid: 4137c9b0-5b4d-4ab6-af2e-2cd98ba53563
ms.tgt_platform: multiple
keywords:
- Metodo seprogrammer Servizi Desktop remoto
- Metodo seprogramname Servizi Desktop remoto, classe Win32_TSVirtualIP
- Classe Win32_TSVirtualIP Servizi Desktop remoto, metodo seprogramname
topic_type:
- apiref
api_name:
- Win32_TSVirtualIP.SetProgramList
api_location:
- TSCfgWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5a64f86c5d530b3393ac1be8858a7ce57ee70ab9
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104518022"
---
# <a name="setprogramlist-method-of-the-win32_tsvirtualip-class"></a><span data-ttu-id="3bc48-106">Metodo seprogrammer della classe Win32 \_ TSVirtualIP</span><span class="sxs-lookup"><span data-stu-id="3bc48-106">SetProgramList method of the Win32\_TSVirtualIP class</span></span>

<span data-ttu-id="3bc48-107">Sovrascrive l'elenco di programmi che usano la virtualizzazione IP.</span><span class="sxs-lookup"><span data-stu-id="3bc48-107">Overwrites the list of programs that use IP virtualization.</span></span>

## <a name="syntax"></a><span data-ttu-id="3bc48-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="3bc48-108">Syntax</span></span>


```mof
unint32 SetProgramList(
  [in] string ProgramList[]
);
```



## <a name="parameters"></a><span data-ttu-id="3bc48-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="3bc48-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3bc48-110">*Programmatore* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="3bc48-110">*ProgramList* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3bc48-111">Tipo: **stringa \[ \]**</span><span class="sxs-lookup"><span data-stu-id="3bc48-111">Type: **string\[\]**</span></span>

<span data-ttu-id="3bc48-112">Matrice di stringhe che contengono il percorso e i nomi file dei programmi che utilizzano la virtualizzazione IP.</span><span class="sxs-lookup"><span data-stu-id="3bc48-112">An array of strings that contain the path and file names of the programs that use IP virtualization.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3bc48-113">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="3bc48-113">Return value</span></span>

<span data-ttu-id="3bc48-114">Tipo: **unint32**</span><span class="sxs-lookup"><span data-stu-id="3bc48-114">Type: **unint32**</span></span>

<span data-ttu-id="3bc48-115">Restituisce 0 in caso di esito positivo, in caso contrario restituisce un codice di errore WMI.</span><span class="sxs-lookup"><span data-stu-id="3bc48-115">Returns 0 on success, otherwise returns a WMI error code.</span></span> <span data-ttu-id="3bc48-116">Per un elenco di questi valori, vedere [Servizi Desktop remoto codici di errore del provider WMI](terminal-services-wmi-provider-error-codes.md) .</span><span class="sxs-lookup"><span data-stu-id="3bc48-116">Refer to [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md) for a list of these values.</span></span> <span data-ttu-id="3bc48-117">Il metodo restituisce un errore se l'impostazione è sotto il controllo criteri di gruppo.</span><span class="sxs-lookup"><span data-stu-id="3bc48-117">The method returns an error if the setting is under group policy control.</span></span>

## <a name="requirements"></a><span data-ttu-id="3bc48-118">Requisiti</span><span class="sxs-lookup"><span data-stu-id="3bc48-118">Requirements</span></span>



| <span data-ttu-id="3bc48-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="3bc48-119">Requirement</span></span> | <span data-ttu-id="3bc48-120">Valore</span><span class="sxs-lookup"><span data-stu-id="3bc48-120">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="3bc48-121">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="3bc48-121">Minimum supported client</span></span><br/> | <span data-ttu-id="3bc48-122">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="3bc48-122">None supported</span></span><br/>                                                               |
| <span data-ttu-id="3bc48-123">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="3bc48-123">Minimum supported server</span></span><br/> | <span data-ttu-id="3bc48-124">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="3bc48-124">Windows Server 2008 R2</span></span><br/>                                                       |
| <span data-ttu-id="3bc48-125">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="3bc48-125">Namespace</span></span><br/>                | <span data-ttu-id="3bc48-126">Radice \\ CIMv2 \\ TerminalServices</span><span class="sxs-lookup"><span data-stu-id="3bc48-126">Root\\CIMv2\\TerminalServices</span></span><br/>                                                |
| <span data-ttu-id="3bc48-127">MOF</span><span class="sxs-lookup"><span data-stu-id="3bc48-127">MOF</span></span><br/>                      | <dl> <span data-ttu-id="3bc48-128"><dt>TSCfgWmi. mof</dt></span><span class="sxs-lookup"><span data-stu-id="3bc48-128"><dt>TSCfgWmi.mof</dt></span></span> </dl> |
| <span data-ttu-id="3bc48-129">DLL</span><span class="sxs-lookup"><span data-stu-id="3bc48-129">DLL</span></span><br/>                      | <dl> <span data-ttu-id="3bc48-130"><dt>TSCfgWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="3bc48-130"><dt>TSCfgWmi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3bc48-131">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="3bc48-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3bc48-132">**\_TSVirtualIP Win32**</span><span class="sxs-lookup"><span data-stu-id="3bc48-132">**Win32\_TSVirtualIP**</span></span>](win32-tsvirtualip.md)
</dt> </dl>

 

 





