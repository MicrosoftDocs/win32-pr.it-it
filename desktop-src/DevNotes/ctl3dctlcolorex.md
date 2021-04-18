---
description: Gestisce il \_ messaggio WM CTLCOLOR per le applicazioni che usano CTL3D.
ms.assetid: 8626a559-4856-4e7d-bf9c-edc48613b8f4
title: Ctl3dCtlColorEx (funzione)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Ctl3dCtlColorEx
api_type:
- DllExport
api_location:
- Ctl3d32.dll
ms.openlocfilehash: 57df7ed5e439d75b2edbf71e743cac069f0ed75b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106331469"
---
# <a name="ctl3dctlcolorex-function"></a><span data-ttu-id="abd48-103">Ctl3dCtlColorEx (funzione)</span><span class="sxs-lookup"><span data-stu-id="abd48-103">Ctl3dCtlColorEx function</span></span>

<span data-ttu-id="abd48-104">Gestisce il messaggio **WM \_ CTLCOLOR** per le applicazioni che usano CTL3D.</span><span class="sxs-lookup"><span data-stu-id="abd48-104">Handles the **WM\_CTLCOLOR** message for applications that use CTL3D.</span></span>

## <a name="syntax"></a><span data-ttu-id="abd48-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="abd48-105">Syntax</span></span>


```C++
HBRUSH Ctl3dCtlColorEx(
   UINT   wm,
   WPARAM wParam,
   LPARAM lParam
);
```



## <a name="parameters"></a><span data-ttu-id="abd48-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="abd48-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="abd48-107">*wm*</span><span class="sxs-lookup"><span data-stu-id="abd48-107">*wm*</span></span> 
</dt> <dd>

<span data-ttu-id="abd48-108">Messaggio **WM \_ CTLCOLOR** per l'applicazione.</span><span class="sxs-lookup"><span data-stu-id="abd48-108">The **WM\_CTLCOLOR** message for the application.</span></span>

</dd> <dt>

<span data-ttu-id="abd48-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="abd48-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="abd48-110">Handle per il contesto di visualizzazione (DC).</span><span class="sxs-lookup"><span data-stu-id="abd48-110">A handle to the display context (DC).</span></span>

</dd> <dt>

<span data-ttu-id="abd48-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="abd48-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="abd48-112">Handle per una finestra figlio (controllo).</span><span class="sxs-lookup"><span data-stu-id="abd48-112">A handle to a child window (control).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="abd48-113">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="abd48-113">Return value</span></span>

<span data-ttu-id="abd48-114">Restituisce un handle al pennello appropriato se la funzione ha esito positivo; in caso contrario, restituisce `(HBRUSH)(0)` un valore che indica che si è verificato un errore.</span><span class="sxs-lookup"><span data-stu-id="abd48-114">Returns a handle to the appropriate brush if the function succeeds; otherwise, it returns `(HBRUSH)(0)` indicating that an error occurred.</span></span>

## <a name="remarks"></a><span data-ttu-id="abd48-115">Commenti</span><span class="sxs-lookup"><span data-stu-id="abd48-115">Remarks</span></span>

<span data-ttu-id="abd48-116">A questa funzione non è associato alcun file di intestazione o libreria di importazione. è necessario chiamarla usando le funzioni [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) e [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) .</span><span class="sxs-lookup"><span data-stu-id="abd48-116">This function has no associated import library or header file; you must call it using the [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) functions.</span></span>

## <a name="requirements"></a><span data-ttu-id="abd48-117">Requisiti</span><span class="sxs-lookup"><span data-stu-id="abd48-117">Requirements</span></span>



| <span data-ttu-id="abd48-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="abd48-118">Requirement</span></span> | <span data-ttu-id="abd48-119">Valore</span><span class="sxs-lookup"><span data-stu-id="abd48-119">Value</span></span> |
|----------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="abd48-120">DLL</span><span class="sxs-lookup"><span data-stu-id="abd48-120">DLL</span></span><br/> | <dl> <span data-ttu-id="abd48-121"><dt>Ctl3d32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="abd48-121"><dt>Ctl3d32.dll</dt></span></span> </dl> |



 

 
