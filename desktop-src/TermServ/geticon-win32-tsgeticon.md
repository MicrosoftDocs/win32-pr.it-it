---
title: Metodo GetIcon della classe Win32_TSGetIcon
description: Restituisce il contenuto dell'icona specificata.
ms.assetid: 9448181c-27b8-40eb-9369-8abe1422243b
ms.tgt_platform: multiple
keywords:
- Metodo GetIcon Servizi Desktop remoto
- Metodo GetIcon Servizi Desktop remoto, classe Win32_TSGetIcon
- Classe Win32_TSGetIcon Servizi Desktop remoto, Metodo GetIcon
topic_type:
- apiref
api_name:
- Win32_TSGetIcon.GetIcon
api_location:
- TsPubWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 92cd20cad668b0e3a6bba191c83ecdca2934ca17
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103963847"
---
# <a name="geticon-method-of-the-win32_tsgeticon-class"></a><span data-ttu-id="fab34-106">Metodo GetIcon della classe Win32 \_ TSGetIcon</span><span class="sxs-lookup"><span data-stu-id="fab34-106">GetIcon method of the Win32\_TSGetIcon class</span></span>

<span data-ttu-id="fab34-107">Restituisce il contenuto dell'icona specificata.</span><span class="sxs-lookup"><span data-stu-id="fab34-107">Returns the contents of the specified icon.</span></span>

## <a name="syntax"></a><span data-ttu-id="fab34-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="fab34-108">Syntax</span></span>


```mof
uint32 GetIcon(
  [in]  string FilePath,
  [in]  sint32 Index,
  [out] uint8  IconContents[]
);
```



## <a name="parameters"></a><span data-ttu-id="fab34-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="fab34-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="fab34-110">*FilePath* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="fab34-110">*FilePath* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fab34-111">Specifica il percorso del file che contiene l'icona.</span><span class="sxs-lookup"><span data-stu-id="fab34-111">Specifies the path to the file that contains the icon</span></span>

</dd> <dt>

<span data-ttu-id="fab34-112">*Indice* \[ di in\]</span><span class="sxs-lookup"><span data-stu-id="fab34-112">*Index* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fab34-113">Specifica l'indice dell'icona nel file.</span><span class="sxs-lookup"><span data-stu-id="fab34-113">Specifies the index of the icon in the file.</span></span>

</dd> <dt>

<span data-ttu-id="fab34-114">*IconContents* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="fab34-114">*IconContents* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="fab34-115">Al termine, contiene il contenuto dell'icona.</span><span class="sxs-lookup"><span data-stu-id="fab34-115">On successful completion contains the contents of the icon.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="fab34-116">Requisiti</span><span class="sxs-lookup"><span data-stu-id="fab34-116">Requirements</span></span>



| <span data-ttu-id="fab34-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="fab34-117">Requirement</span></span> | <span data-ttu-id="fab34-118">Valore</span><span class="sxs-lookup"><span data-stu-id="fab34-118">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="fab34-119">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="fab34-119">Minimum supported client</span></span><br/> | <span data-ttu-id="fab34-120">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="fab34-120">None supported</span></span><br/>                                                               |
| <span data-ttu-id="fab34-121">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="fab34-121">Minimum supported server</span></span><br/> | <span data-ttu-id="fab34-122">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="fab34-122">Windows Server 2012</span></span><br/>                                                          |
| <span data-ttu-id="fab34-123">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="fab34-123">Namespace</span></span><br/>                | <span data-ttu-id="fab34-124">Radice \\ CIMv2 \\ TerminalServices</span><span class="sxs-lookup"><span data-stu-id="fab34-124">Root\\CIMv2\\TerminalServices</span></span><br/>                                                |
| <span data-ttu-id="fab34-125">MOF</span><span class="sxs-lookup"><span data-stu-id="fab34-125">MOF</span></span><br/>                      | <dl> <span data-ttu-id="fab34-126"><dt>TsAllow. mof</dt></span><span class="sxs-lookup"><span data-stu-id="fab34-126"><dt>TsAllow.mof</dt></span></span> </dl>  |
| <span data-ttu-id="fab34-127">DLL</span><span class="sxs-lookup"><span data-stu-id="fab34-127">DLL</span></span><br/>                      | <dl> <span data-ttu-id="fab34-128"><dt>TsPubWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="fab34-128"><dt>TsPubWmi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="fab34-129">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="fab34-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fab34-130">**\_TSGetIcon Win32**</span><span class="sxs-lookup"><span data-stu-id="fab34-130">**Win32\_TSGetIcon**</span></span>](win32-tsgeticon.md)
</dt> </dl>

 

 





