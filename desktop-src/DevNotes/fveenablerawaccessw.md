---
description: Abilita o Disabilita la lettura e la scrittura dei settori del disco.
ms.assetid: 885e4db1-a131-4727-80ab-3be8c591b766
title: FveEnableRawAccessW (funzione)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FveEnableRawAccessW
api_type:
- DllExport
api_location:
- Fveapi.dll
ms.openlocfilehash: 5b4a367c3566c1475f856783d800ec43e21071e2
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103877546"
---
# <a name="fveenablerawaccessw-function"></a><span data-ttu-id="419eb-103">FveEnableRawAccessW (funzione)</span><span class="sxs-lookup"><span data-stu-id="419eb-103">FveEnableRawAccessW function</span></span>

<span data-ttu-id="419eb-104">Abilita o Disabilita la lettura e la scrittura dei settori del disco.</span><span class="sxs-lookup"><span data-stu-id="419eb-104">Enables or disables reading and writing of disk sectors.</span></span>

## <a name="syntax"></a><span data-ttu-id="419eb-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="419eb-105">Syntax</span></span>


```C++
HRESULT FveEnableRawAccessW(
  _In_ PCWSTR VolumeName,
  _In_ BOOL   Enabled
);
```



## <a name="parameters"></a><span data-ttu-id="419eb-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="419eb-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="419eb-107">*VolumeName* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="419eb-107">*VolumeName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="419eb-108">Identificatore univoco del volume del disco.</span><span class="sxs-lookup"><span data-stu-id="419eb-108">A unique identifier for the disk volume.</span></span>

</dd> <dt>

<span data-ttu-id="419eb-109">*Abilitato* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="419eb-109">*Enabled* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="419eb-110">Se **true**, consente l'accesso al volume non elaborato.</span><span class="sxs-lookup"><span data-stu-id="419eb-110">If **TRUE**, allows access to the raw volume.</span></span> <span data-ttu-id="419eb-111">Se **false**, non è consentito l'accesso al volume non elaborato.</span><span class="sxs-lookup"><span data-stu-id="419eb-111">If **FALSE**, no access is allowed to the raw volume.</span></span> <span data-ttu-id="419eb-112">Se l'accesso non elaborato è già stato abilitato ma questo valore è **false**, il volume viene rimontato e riconvalidato.</span><span class="sxs-lookup"><span data-stu-id="419eb-112">If raw access has already been enabled but this value is **FALSE**, the volume is remounted and revalidated.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="419eb-113">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="419eb-113">Return value</span></span>

<span data-ttu-id="419eb-114">Questa funzione restituisce uno dei codici seguenti o un altro codice di errore se ha esito negativo.</span><span class="sxs-lookup"><span data-stu-id="419eb-114">This function returns one of the following codes or another error code if it fails.</span></span>



| <span data-ttu-id="419eb-115">Codice/valore restituito</span><span class="sxs-lookup"><span data-stu-id="419eb-115">Return code/value</span></span>                                                                                                                                                           | <span data-ttu-id="419eb-116">Descrizione</span><span class="sxs-lookup"><span data-stu-id="419eb-116">Description</span></span>                                                                        |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="419eb-117"><dt>**S \_ OK**</dt> <dt>0 (0x0)</dt></span><span class="sxs-lookup"><span data-stu-id="419eb-117"><dt>**S\_OK**</dt> <dt>0 (0x0)</dt></span></span> </dl>                           | <span data-ttu-id="419eb-118">La funzione è stata completata.</span><span class="sxs-lookup"><span data-stu-id="419eb-118">The function was successful.</span></span><br/>                                            |
| <dl> <span data-ttu-id="419eb-119"><dt>**S \_ FALSE**</dt> <dt>1 (0x1)</dt></span><span class="sxs-lookup"><span data-stu-id="419eb-119"><dt>**S\_FALSE**</dt> <dt>1 (0x1)</dt></span></span> </dl>                        | <span data-ttu-id="419eb-120">Enabled è **false** e il volume non è già in modalità di accesso non elaborato.</span><span class="sxs-lookup"><span data-stu-id="419eb-120">Enabled is **FALSE** and the volume was not already in raw access mode.</span></span><br/> |
| <dl> <span data-ttu-id="419eb-121"><dt>**E \_ ACCESSDENIED**</dt> <dt>2147942405 (0x80070005)</dt></span><span class="sxs-lookup"><span data-stu-id="419eb-121"><dt>**E\_ACCESSDENIED**</dt> <dt>2147942405 (0x80070005)</dt></span></span> </dl> | <span data-ttu-id="419eb-122">Il volume non può essere bloccato.</span><span class="sxs-lookup"><span data-stu-id="419eb-122">The volume cannot be locked.</span></span><br/>                                            |



 

## <a name="requirements"></a><span data-ttu-id="419eb-123">Requisiti</span><span class="sxs-lookup"><span data-stu-id="419eb-123">Requirements</span></span>



| <span data-ttu-id="419eb-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="419eb-124">Requirement</span></span> | <span data-ttu-id="419eb-125">Valore</span><span class="sxs-lookup"><span data-stu-id="419eb-125">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="419eb-126">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="419eb-126">Minimum supported client</span></span><br/> | <span data-ttu-id="419eb-127">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="419eb-127">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="419eb-128">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="419eb-128">Minimum supported server</span></span><br/> | <span data-ttu-id="419eb-129">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="419eb-129">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="419eb-130">DLL</span><span class="sxs-lookup"><span data-stu-id="419eb-130">DLL</span></span><br/>                      | <dl> <span data-ttu-id="419eb-131"><dt>Fveapi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="419eb-131"><dt>Fveapi.dll</dt></span></span> </dl> |



 

 




