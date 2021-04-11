---
title: GetProcessHandleFromHwnd (funzione)
description: Recupera un handle di processo da un handle di finestra.
ms.assetid: 173579d2-c930-402c-81c7-761b063b5b51
keywords:
- Accessibilità di Windows per la funzione GetProcessHandleFromHwnd
topic_type:
- apiref
api_name:
- GetProcessHandleFromHwnd
api_location:
- Oleacc.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bee00f36f236396816e7bb54cadbe6914f3437e6
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104119863"
---
# <a name="getprocesshandlefromhwnd-function"></a><span data-ttu-id="e2deb-104">GetProcessHandleFromHwnd (funzione)</span><span class="sxs-lookup"><span data-stu-id="e2deb-104">GetProcessHandleFromHwnd function</span></span>

<span data-ttu-id="e2deb-105">Recupera un handle di processo da un handle di finestra.</span><span class="sxs-lookup"><span data-stu-id="e2deb-105">Retrieves a process handle from a window handle.</span></span>

## <a name="syntax"></a><span data-ttu-id="e2deb-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="e2deb-106">Syntax</span></span>


```C++
HANDLE WINAPI GetProcessHandleFromHwnd(
  _In_ HWND hwnd
);
```



## <a name="parameters"></a><span data-ttu-id="e2deb-107">Parametri</span><span class="sxs-lookup"><span data-stu-id="e2deb-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e2deb-108">*HWND* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="e2deb-108">*hwnd* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e2deb-109">Tipo: **[ **HWND**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="e2deb-109">Type: **[**HWND**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="e2deb-110">Handle di finestra.</span><span class="sxs-lookup"><span data-stu-id="e2deb-110">The window handle.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e2deb-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="e2deb-111">Return value</span></span>

<span data-ttu-id="e2deb-112">Tipo: **[ **handle**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="e2deb-112">Type: **[**HANDLE**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="e2deb-113">Se l'operazione riesce, restituisce l'handle del processo a cui appartiene la finestra.</span><span class="sxs-lookup"><span data-stu-id="e2deb-113">If successful, returns the handle of the process that owns the window.</span></span>

<span data-ttu-id="e2deb-114">Se ha esito negativo, restituisce **null**.</span><span class="sxs-lookup"><span data-stu-id="e2deb-114">If not successful, returns **NULL**.</span></span>

## <a name="remarks"></a><span data-ttu-id="e2deb-115">Commenti</span><span class="sxs-lookup"><span data-stu-id="e2deb-115">Remarks</span></span>

<span data-ttu-id="e2deb-116">Nelle versioni precedenti del sistema operativo un processo poteva aprire un altro processo (ad esempio, per accedere alla sua memoria) usando [**OpenProcess**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-openprocess).</span><span class="sxs-lookup"><span data-stu-id="e2deb-116">In previous versions of the operating system, a process could open another process (to access its memory, for example) using [**OpenProcess**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-openprocess).</span></span> <span data-ttu-id="e2deb-117">Questa funzione ha esito positivo se il chiamante dispone dei privilegi appropriati; in genere il chiamante e il processo di destinazione devono essere lo stesso utente.</span><span class="sxs-lookup"><span data-stu-id="e2deb-117">This function succeeds if the caller has appropriate privileges; usually the caller and target process must be the same user.</span></span>

<span data-ttu-id="e2deb-118">In Windows Vista, tuttavia, [**OpenProcess**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-openprocess) ha esito negativo nello scenario in cui il chiamante ha uiAccess e il processo di destinazione è elevato.</span><span class="sxs-lookup"><span data-stu-id="e2deb-118">On Windows Vista, however, [**OpenProcess**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-openprocess) fails in the scenario where the caller has UIAccess, and the target process is elevated.</span></span> <span data-ttu-id="e2deb-119">In questo caso, il proprietario del processo di destinazione si trova nel gruppo Administrators, ma il processo chiamante è in esecuzione con il token con restrizioni, quindi non ha l'appartenenza a questo gruppo e viene negato l'accesso al processo con privilegi elevati.</span><span class="sxs-lookup"><span data-stu-id="e2deb-119">In this case, the owner of the target process is in the Administrators group, but the calling process is running with the restricted token, so does not have membership in this group, and is denied access to the elevated process.</span></span> <span data-ttu-id="e2deb-120">Se il chiamante ha UIAccess, tuttavia, può usare un hook di Windows per inserire il codice nel processo di destinazione e, dal processo di destinazione, restituire un handle al chiamante.</span><span class="sxs-lookup"><span data-stu-id="e2deb-120">If the caller has UIAccess, however, they can use a windows hook to inject code into the target process, and from within the target process, send a handle back to the caller.</span></span>

<span data-ttu-id="e2deb-121">**GetProcessHandleFromHwnd** è una funzione utile che usa questa tecnica per ottenere l'handle del processo a cui appartiene l'HWND specificato.</span><span class="sxs-lookup"><span data-stu-id="e2deb-121">**GetProcessHandleFromHwnd** is a convenience function that uses this technique to obtain the handle of the process that owns the specified HWND.</span></span> <span data-ttu-id="e2deb-122">Si noti che ha esito positivo solo nei casi in cui il chiamante e il processo di destinazione vengono eseguiti con lo stesso utente.</span><span class="sxs-lookup"><span data-stu-id="e2deb-122">Note that it only succeeds in cases where the caller and target process are running as the same user.</span></span> <span data-ttu-id="e2deb-123">L'handle restituito ha i privilegi seguenti: processo duplicato Gestisci processo macchina virtuale processo macchina virtuale \_ \_ lettura processo macchina virtuale \| \_ \_ \| \_ \_ \| \_ \_ scrittura \| sincronizzazione.</span><span class="sxs-lookup"><span data-stu-id="e2deb-123">The returned handle has the following privileges: PROCESS\_DUP\_HANDLE \| PROCESS\_VM\_OPERATION \| PROCESS\_VM\_READ \| PROCESS\_VM\_WRITE \| SYNCHRONIZE.</span></span> <span data-ttu-id="e2deb-124">Se sono necessari altri privilegi, potrebbe essere necessario implementare la tecnica di hook in modo esplicito anziché usare questa funzione.</span><span class="sxs-lookup"><span data-stu-id="e2deb-124">If other privileges are required, it may be necessary to implement the hooking technique explicitly instead of using this function.</span></span>

## <a name="requirements"></a><span data-ttu-id="e2deb-125">Requisiti</span><span class="sxs-lookup"><span data-stu-id="e2deb-125">Requirements</span></span>



| <span data-ttu-id="e2deb-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="e2deb-126">Requirement</span></span> | <span data-ttu-id="e2deb-127">Valore</span><span class="sxs-lookup"><span data-stu-id="e2deb-127">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="e2deb-128">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="e2deb-128">Minimum supported client</span></span><br/> | <span data-ttu-id="e2deb-129">\[Solo app desktop Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="e2deb-129">Windows XP \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="e2deb-130">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="e2deb-130">Minimum supported server</span></span><br/> | <span data-ttu-id="e2deb-131">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="e2deb-131">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="e2deb-132">DLL</span><span class="sxs-lookup"><span data-stu-id="e2deb-132">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e2deb-133"><dt>Oleacc.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e2deb-133"><dt>Oleacc.dll</dt></span></span> </dl> |



 

