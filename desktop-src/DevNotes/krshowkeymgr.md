---
description: Visualizza la finestra di dialogo Gestione chiavi nell'interfaccia utente.
ms.assetid: 65c2763f-42d5-4534-94f7-e753f6486014
title: KRShowKeyMgr (funzione)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- KRShowKeyMgr
api_type:
- DllExport
api_location:
- Keymgr.dll
ms.openlocfilehash: 59b6b38cf7e78755c7d5c481a22a0a8b3854c8a6
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106324700"
---
# <a name="krshowkeymgr-function"></a><span data-ttu-id="25702-103">KRShowKeyMgr (funzione)</span><span class="sxs-lookup"><span data-stu-id="25702-103">KRShowKeyMgr function</span></span>

<span data-ttu-id="25702-104">\[Questa funzione è inclusa solo in Windows XP.</span><span class="sxs-lookup"><span data-stu-id="25702-104">\[This function is included only in Windows XP.</span></span> <span data-ttu-id="25702-105">Non è attualmente incluso in nessun'altra versione di Windows, né dovrebbe essere incluso nelle versioni future di Windows.\]</span><span class="sxs-lookup"><span data-stu-id="25702-105">It is not currently included in any other version of Windows, nor is it expected to be included in any future versions of Windows.\]</span></span>

<span data-ttu-id="25702-106">Visualizza la finestra di dialogo Gestione chiavi nell'interfaccia utente.</span><span class="sxs-lookup"><span data-stu-id="25702-106">Brings up the key manager dialog into the user interface.</span></span>

## <a name="syntax"></a><span data-ttu-id="25702-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="25702-107">Syntax</span></span>


```C++
void KRShowKeyMgr(
   HWND      hwParent,
   HINSTANCE hInstance,
   LPWSTR    pszCmdLine,
   int       CmdShow
);
```



## <a name="parameters"></a><span data-ttu-id="25702-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="25702-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="25702-109">*hwParent*</span><span class="sxs-lookup"><span data-stu-id="25702-109">*hwParent*</span></span> 
</dt> <dd>

<span data-ttu-id="25702-110">Handle per la finestra padre della finestra di dialogo.</span><span class="sxs-lookup"><span data-stu-id="25702-110">A handle to the parent window of the dialog.</span></span> <span data-ttu-id="25702-111">Questo parametro può essere **NULL**.</span><span class="sxs-lookup"><span data-stu-id="25702-111">This parameter can be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="25702-112">*hInstance*</span><span class="sxs-lookup"><span data-stu-id="25702-112">*hInstance*</span></span> 
</dt> <dd>

<span data-ttu-id="25702-113">Questo parametro non viene utilizzato e deve essere impostato su **null**.</span><span class="sxs-lookup"><span data-stu-id="25702-113">This parameter is not used and should be set to **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="25702-114">*pszCmdLine*</span><span class="sxs-lookup"><span data-stu-id="25702-114">*pszCmdLine*</span></span> 
</dt> <dd>

<span data-ttu-id="25702-115">Questo parametro non viene utilizzato e deve essere impostato su **null**.</span><span class="sxs-lookup"><span data-stu-id="25702-115">This parameter is not used and should be set to **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="25702-116">*CmdShow*</span><span class="sxs-lookup"><span data-stu-id="25702-116">*CmdShow*</span></span> 
</dt> <dd>

<span data-ttu-id="25702-117">Questo parametro non viene utilizzato e deve essere impostato su **null**.</span><span class="sxs-lookup"><span data-stu-id="25702-117">This parameter is not used and should be set to **NULL**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="25702-118">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="25702-118">Return value</span></span>

<span data-ttu-id="25702-119">Questa funzione non restituisce un valore.</span><span class="sxs-lookup"><span data-stu-id="25702-119">This function does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="25702-120">Commenti</span><span class="sxs-lookup"><span data-stu-id="25702-120">Remarks</span></span>

<span data-ttu-id="25702-121">A questa funzione non è associato alcun file di intestazione o libreria di importazione. è necessario chiamarla usando le funzioni [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) e [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) .</span><span class="sxs-lookup"><span data-stu-id="25702-121">This function has no associated import library or header file; you must call it using the [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) functions.</span></span>

## <a name="requirements"></a><span data-ttu-id="25702-122">Requisiti</span><span class="sxs-lookup"><span data-stu-id="25702-122">Requirements</span></span>



| <span data-ttu-id="25702-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="25702-123">Requirement</span></span> | <span data-ttu-id="25702-124">Valore</span><span class="sxs-lookup"><span data-stu-id="25702-124">Value</span></span> |
|----------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="25702-125">DLL</span><span class="sxs-lookup"><span data-stu-id="25702-125">DLL</span></span><br/> | <dl> <span data-ttu-id="25702-126"><dt>Keymgr.dll</dt></span><span class="sxs-lookup"><span data-stu-id="25702-126"><dt>Keymgr.dll</dt></span></span> </dl> |



 

 
