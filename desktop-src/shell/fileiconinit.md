---
description: Inizializza o reinizializza l'elenco di immagini di sistema.
ms.assetid: 4e661326-157e-4c75-86df-cd213e01c3e5
title: FileIconInit (funzione)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FileIconInit
api_type:
- DllExport
api_location:
- Shell32.dll
ms.openlocfilehash: 090f35cc576caf6f99a8d5822a0304f15383e8db
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104345416"
---
# <a name="fileiconinit-function"></a><span data-ttu-id="bfde4-103">FileIconInit (funzione)</span><span class="sxs-lookup"><span data-stu-id="bfde4-103">FileIconInit function</span></span>

<span data-ttu-id="bfde4-104">Inizializza o reinizializza l'elenco di immagini di sistema.</span><span class="sxs-lookup"><span data-stu-id="bfde4-104">Initializes or reinitializes the system image list.</span></span>

## <a name="syntax"></a><span data-ttu-id="bfde4-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="bfde4-105">Syntax</span></span>


```C++
BOOL FileIconInit(
  _In_ BOOL fRestoreCache
);
```



## <a name="parameters"></a><span data-ttu-id="bfde4-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="bfde4-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="bfde4-107">*fRestoreCache* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="bfde4-107">*fRestoreCache* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="bfde4-108">Tipo: **bool**</span><span class="sxs-lookup"><span data-stu-id="bfde4-108">Type: **BOOL**</span></span>

<span data-ttu-id="bfde4-109">**True** per ripristinare la cache dell'immagine di sistema dal disco; In caso contrario, **false** .</span><span class="sxs-lookup"><span data-stu-id="bfde4-109">**TRUE** to restore the system image cache from disk; **FALSE** otherwise.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="bfde4-110">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="bfde4-110">Return value</span></span>

<span data-ttu-id="bfde4-111">Tipo: **bool**</span><span class="sxs-lookup"><span data-stu-id="bfde4-111">Type: **BOOL**</span></span>

<span data-ttu-id="bfde4-112">**True** se la cache è stata aggiornata correttamente, **false** se l'inizializzazione non è riuscita.</span><span class="sxs-lookup"><span data-stu-id="bfde4-112">**TRUE** if the cache was successfully refreshed, **FALSE** if the initialization failed.</span></span>

## <a name="remarks"></a><span data-ttu-id="bfde4-113">Commenti</span><span class="sxs-lookup"><span data-stu-id="bfde4-113">Remarks</span></span>

<span data-ttu-id="bfde4-114">Se si utilizzano elenchi di immagini di sistema nel proprio processo, è necessario chiamare **FileIconInit** negli orari seguenti:</span><span class="sxs-lookup"><span data-stu-id="bfde4-114">If you are using system image lists in your own process, you must call **FileIconInit** at the following times:</span></span>

-   <span data-ttu-id="bfde4-115">All'avvio.</span><span class="sxs-lookup"><span data-stu-id="bfde4-115">On launch.</span></span>
-   <span data-ttu-id="bfde4-116">In risposta a un messaggio [**WM \_ SETTINGCHANGE**](../winmsg/wm-settingchange.md) quando viene impostato il flag [**SPI \_ SETNONCLIENTMETRICS**](/windows/win32/api/winuser/nf-winuser-systemparametersinfoa) .</span><span class="sxs-lookup"><span data-stu-id="bfde4-116">In response to a [**WM\_SETTINGCHANGE**](../winmsg/wm-settingchange.md) message when the [**SPI\_SETNONCLIENTMETRICS**](/windows/win32/api/winuser/nf-winuser-systemparametersinfoa) flag is set.</span></span>

<span data-ttu-id="bfde4-117">**FileIconInit** non è incluso in un file di intestazione.</span><span class="sxs-lookup"><span data-stu-id="bfde4-117">**FileIconInit** is not included in a header file.</span></span> <span data-ttu-id="bfde4-118">È necessario chiamarlo direttamente da Shell32.dll, usando il numero ordinale 660.</span><span class="sxs-lookup"><span data-stu-id="bfde4-118">You must call it directly from Shell32.dll, using ordinal 660.</span></span>

## <a name="requirements"></a><span data-ttu-id="bfde4-119">Requisiti</span><span class="sxs-lookup"><span data-stu-id="bfde4-119">Requirements</span></span>



| <span data-ttu-id="bfde4-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="bfde4-120">Requirement</span></span> | <span data-ttu-id="bfde4-121">Valore</span><span class="sxs-lookup"><span data-stu-id="bfde4-121">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="bfde4-122">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="bfde4-122">Minimum supported client</span></span><br/> | <span data-ttu-id="bfde4-123">\[Solo app desktop Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="bfde4-123">Windows XP \[desktop apps only\]</span></span><br/>                                            |
| <span data-ttu-id="bfde4-124">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="bfde4-124">Minimum supported server</span></span><br/> | <span data-ttu-id="bfde4-125">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="bfde4-125">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="bfde4-126">DLL</span><span class="sxs-lookup"><span data-stu-id="bfde4-126">DLL</span></span><br/>                      | <dl> <span data-ttu-id="bfde4-127"><dt>Shell32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="bfde4-127"><dt>Shell32.dll</dt></span></span> </dl> |



 

 
