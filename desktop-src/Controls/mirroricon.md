---
title: MirrorIcon (funzione)
description: Inverte le icone (mirror) in modo che vengano visualizzate correttamente in un contesto di dispositivo con mirroring.
ms.assetid: bca87037-1789-466b-9be0-914966fdad31
keywords:
- Controlli Windows per la funzione MirrorIcon
topic_type:
- apiref
api_name:
- MirrorIcon
api_location:
- Comctl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 02f180d509464b63e5ec73c5fb74e4d70386bdea
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104047993"
---
# <a name="mirroricon-function"></a><span data-ttu-id="75a42-104">MirrorIcon (funzione)</span><span class="sxs-lookup"><span data-stu-id="75a42-104">MirrorIcon function</span></span>

<span data-ttu-id="75a42-105">\[**MirrorIcon** è disponibile tramite Windows XP con Service Pack 2 (SP2).</span><span class="sxs-lookup"><span data-stu-id="75a42-105">\[**MirrorIcon** is available through Windows XP with Service Pack 2 (SP2).</span></span> <span data-ttu-id="75a42-106">Potrebbe essere modificato o non disponibile nelle versioni successive.\]</span><span class="sxs-lookup"><span data-stu-id="75a42-106">It might be altered or unavailable in subsequent versions.\]</span></span>

<span data-ttu-id="75a42-107">Inverte le icone (mirror) in modo che vengano visualizzate correttamente in un contesto di dispositivo con mirroring.</span><span class="sxs-lookup"><span data-stu-id="75a42-107">Reverses (mirrors) icons so that they are displayed correctly on a mirrored device context.</span></span>

## <a name="syntax"></a><span data-ttu-id="75a42-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="75a42-108">Syntax</span></span>


```C++
BOOL WINAPI MirrorIcon(
  _Inout_opt_ HICON *phIconSmall,
  _Inout_opt_ HICON *phIconLarge
);
```



## <a name="parameters"></a><span data-ttu-id="75a42-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="75a42-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="75a42-110">*phIconSmall* \[ in, out, facoltativo\]</span><span class="sxs-lookup"><span data-stu-id="75a42-110">*phIconSmall* \[in, out, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="75a42-111">Tipo: \**[**HICON**](/windows/desktop/WinProg/windows-data-types) \** _</span><span class="sxs-lookup"><span data-stu-id="75a42-111">Type: \**[**HICON**](/windows/desktop/WinProg/windows-data-types)\** _</span></span>

<span data-ttu-id="75a42-112">Puntatore all'handle dell'icona che fa riferimento a una versione ridotta di un'icona.</span><span class="sxs-lookup"><span data-stu-id="75a42-112">A pointer to the icon handle that references a small version of an icon.</span></span>

</dd> <dt>

<span data-ttu-id="75a42-113">_phIconLarge \* \[ in, out, facoltativo\]</span><span class="sxs-lookup"><span data-stu-id="75a42-113">_phIconLarge\* \[in, out, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="75a42-114">Tipo: \**[**HICON**](/windows/desktop/WinProg/windows-data-types) \** _</span><span class="sxs-lookup"><span data-stu-id="75a42-114">Type: \**[**HICON**](/windows/desktop/WinProg/windows-data-types)\** _</span></span>

<span data-ttu-id="75a42-115">Puntatore all'handle dell'icona che fa riferimento a una versione di grandi dimensioni di un'icona.</span><span class="sxs-lookup"><span data-stu-id="75a42-115">A pointer to the icon handle that references a large version of an icon.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="75a42-116">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="75a42-116">Return value</span></span>

<span data-ttu-id="75a42-117">Tipo: _ *[**bool**](/windows/desktop/WinProg/windows-data-types)*\*</span><span class="sxs-lookup"><span data-stu-id="75a42-117">Type: _ *[**BOOL**](/windows/desktop/WinProg/windows-data-types)*\*</span></span>

<span data-ttu-id="75a42-118">**True** se l'operazione ha esito positivo; in caso contrario, **false**.</span><span class="sxs-lookup"><span data-stu-id="75a42-118">**TRUE** if successful; otherwise, **FALSE**.</span></span>

## <a name="remarks"></a><span data-ttu-id="75a42-119">Commenti</span><span class="sxs-lookup"><span data-stu-id="75a42-119">Remarks</span></span>

<span data-ttu-id="75a42-120">**MirrorIcon** non viene esportato in base al nome o dichiarata in un file di intestazione pubblico.</span><span class="sxs-lookup"><span data-stu-id="75a42-120">**MirrorIcon** is not exported by name or declared in a public header file.</span></span> <span data-ttu-id="75a42-121">Per usarlo, è necessario usare [**GetProcAddress**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress) e richiedere l'ordinale 414 da ComCtl32.dll per ottenere un puntatore a funzione.</span><span class="sxs-lookup"><span data-stu-id="75a42-121">To use it, you must use [**GetProcAddress**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress) and request ordinal 414 from ComCtl32.dll to obtain a function pointer.</span></span>

## <a name="requirements"></a><span data-ttu-id="75a42-122">Requisiti</span><span class="sxs-lookup"><span data-stu-id="75a42-122">Requirements</span></span>



| <span data-ttu-id="75a42-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="75a42-123">Requirement</span></span> | <span data-ttu-id="75a42-124">Valore</span><span class="sxs-lookup"><span data-stu-id="75a42-124">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="75a42-125">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="75a42-125">Minimum supported client</span></span><br/> | <span data-ttu-id="75a42-126">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="75a42-126">Windows Vista \[desktop apps only\]</span></span><br/>                                                                  |
| <span data-ttu-id="75a42-127">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="75a42-127">Minimum supported server</span></span><br/> | <span data-ttu-id="75a42-128">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="75a42-128">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                            |
| <span data-ttu-id="75a42-129">DLL</span><span class="sxs-lookup"><span data-stu-id="75a42-129">DLL</span></span><br/>                      | <dl> <span data-ttu-id="75a42-130"><dt>Comctl32.dll (versione 5,81 o successiva)</dt></span><span class="sxs-lookup"><span data-stu-id="75a42-130"><dt>Comctl32.dll (version 5.81 or later)</dt></span></span> </dl> |



 

