---
description: Gestisce le modifiche dei colori di sistema per le applicazioni che usano CTL3D.
ms.assetid: b1eadb7d-39a5-47e9-9ae5-62bd33557f6b
title: Ctl3dColorChange (funzione)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Ctl3dColorChange
api_type:
- DllExport
api_location:
- Ctl3d32.dll
ms.openlocfilehash: 7e7b0d4480fde480ea24a6c2c0dd8a7a849fbc75
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106328854"
---
# <a name="ctl3dcolorchange-function"></a><span data-ttu-id="807a6-103">Ctl3dColorChange (funzione)</span><span class="sxs-lookup"><span data-stu-id="807a6-103">Ctl3dColorChange function</span></span>

<span data-ttu-id="807a6-104">Gestisce le modifiche dei colori di sistema per le applicazioni che usano CTL3D.</span><span class="sxs-lookup"><span data-stu-id="807a6-104">Handles system color changes for applications that use CTL3D.</span></span>

## <a name="syntax"></a><span data-ttu-id="807a6-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="807a6-105">Syntax</span></span>


```C++
BOOL Ctl3dColorChange(void);
```



## <a name="parameters"></a><span data-ttu-id="807a6-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="807a6-106">Parameters</span></span>

<span data-ttu-id="807a6-107">Questa funzione non ha parametri.</span><span class="sxs-lookup"><span data-stu-id="807a6-107">This function has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="807a6-108">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="807a6-108">Return value</span></span>

<span data-ttu-id="807a6-109">Restituisce **true** se la funzione ha esito positivo; in caso contrario, restituisce **false**.</span><span class="sxs-lookup"><span data-stu-id="807a6-109">Returns **TRUE** if the function succeeds; otherwise, it returns **FALSE**.</span></span>

## <a name="remarks"></a><span data-ttu-id="807a6-110">Commenti</span><span class="sxs-lookup"><span data-stu-id="807a6-110">Remarks</span></span>

<span data-ttu-id="807a6-111">A questa funzione non è associato alcun file di intestazione o libreria di importazione. è necessario chiamarla usando le funzioni [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) e [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) .</span><span class="sxs-lookup"><span data-stu-id="807a6-111">This function has no associated import library or header file; you must call it using the [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) functions.</span></span>

<span data-ttu-id="807a6-112">Questa funzione deve essere chiamata nella procedura della finestra principale dell'applicazione per il messaggio **WM \_ SYSCOLORCHANGE** , come illustrato di seguito.</span><span class="sxs-lookup"><span data-stu-id="807a6-112">This function should be called in the application's main window procedure for the **WM\_SYSCOLORCHANGE** message, as shown below.</span></span>

## <a name="examples"></a><span data-ttu-id="807a6-113">Esempio</span><span class="sxs-lookup"><span data-stu-id="807a6-113">Examples</span></span>

``` syntax
case WM_SYSCOLORCHANGE:
   Ctl3dColorChange();
   break;
```

## <a name="requirements"></a><span data-ttu-id="807a6-114">Requisiti</span><span class="sxs-lookup"><span data-stu-id="807a6-114">Requirements</span></span>



| <span data-ttu-id="807a6-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="807a6-115">Requirement</span></span> | <span data-ttu-id="807a6-116">Valore</span><span class="sxs-lookup"><span data-stu-id="807a6-116">Value</span></span> |
|----------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="807a6-117">DLL</span><span class="sxs-lookup"><span data-stu-id="807a6-117">DLL</span></span><br/> | <dl> <span data-ttu-id="807a6-118"><dt>Ctl3d32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="807a6-118"><dt>Ctl3d32.dll</dt></span></span> </dl> |



 

 
