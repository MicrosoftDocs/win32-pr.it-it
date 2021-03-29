---
description: Consente di visualizzare la scheda condivisione cartelle nella finestra delle proprietà per la cartella specificata.
ms.assetid: e622e4bb-eaf7-494f-b2a2-78ba1311a496
title: ShowShareFolderUI (funzione)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ShowShareFolderUI
- ShowShareFolderUIW
api_type:
- DllExport
api_location:
- Ntshrui.dll
ms.openlocfilehash: e6270f72d1574a21b98ac9ee3151af1f34f08a72
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104346426"
---
# <a name="showsharefolderui-function"></a><span data-ttu-id="ebd4f-103">ShowShareFolderUI (funzione)</span><span class="sxs-lookup"><span data-stu-id="ebd4f-103">ShowShareFolderUI function</span></span>

<span data-ttu-id="ebd4f-104">Consente di visualizzare la scheda **condivisione cartelle** nella finestra delle proprietà per la cartella specificata.</span><span class="sxs-lookup"><span data-stu-id="ebd4f-104">Displays the **Folder Sharing** tab on the properties sheet for the specified folder.</span></span>

## <a name="syntax"></a><span data-ttu-id="ebd4f-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="ebd4f-105">Syntax</span></span>


```C++
HRESULT ShowShareFolderUI(
  _In_ HWND    hwndParent,
  _In_ LPCWSTR pszPath
);
```



## <a name="parameters"></a><span data-ttu-id="ebd4f-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="ebd4f-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ebd4f-107">*hwndParent* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="ebd4f-107">*hwndParent* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ebd4f-108">Tipo: **HWND**</span><span class="sxs-lookup"><span data-stu-id="ebd4f-108">Type: **HWND**</span></span>

<span data-ttu-id="ebd4f-109">Handle per la finestra padre della finestra delle proprietà.</span><span class="sxs-lookup"><span data-stu-id="ebd4f-109">A handle to the parent window for the property sheet.</span></span>

</dd> <dt>

<span data-ttu-id="ebd4f-110">*pszPath* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="ebd4f-110">*pszPath* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ebd4f-111">Tipo: **LPCWSTR**</span><span class="sxs-lookup"><span data-stu-id="ebd4f-111">Type: **LPCWSTR**</span></span>

<span data-ttu-id="ebd4f-112">Puntatore a una stringa che specifica il percorso alla cartella che visualizza la scheda **condivisione cartelle** .</span><span class="sxs-lookup"><span data-stu-id="ebd4f-112">A pointer to a string that specifies the path to the folder that displays its **Folder Sharing** tab.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ebd4f-113">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="ebd4f-113">Return value</span></span>

<span data-ttu-id="ebd4f-114">Tipo: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="ebd4f-114">Type: **HRESULT**</span></span>

<span data-ttu-id="ebd4f-115">Questa funzione restituisce sempre S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="ebd4f-115">This function always returns S\_OK.</span></span>

## <a name="remarks"></a><span data-ttu-id="ebd4f-116">Commenti</span><span class="sxs-lookup"><span data-stu-id="ebd4f-116">Remarks</span></span>

<span data-ttu-id="ebd4f-117">A questa funzione non è associato alcun file con estensione LIB.</span><span class="sxs-lookup"><span data-stu-id="ebd4f-117">This function has no associated .lib file.</span></span> <span data-ttu-id="ebd4f-118">Per usarlo, è necessario usare [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) e [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) .</span><span class="sxs-lookup"><span data-stu-id="ebd4f-118">You must use [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) to use it.</span></span>

## <a name="requirements"></a><span data-ttu-id="ebd4f-119">Requisiti</span><span class="sxs-lookup"><span data-stu-id="ebd4f-119">Requirements</span></span>



| <span data-ttu-id="ebd4f-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="ebd4f-120">Requirement</span></span> | <span data-ttu-id="ebd4f-121">Valore</span><span class="sxs-lookup"><span data-stu-id="ebd4f-121">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="ebd4f-122">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="ebd4f-122">Minimum supported client</span></span><br/> | <span data-ttu-id="ebd4f-123">\[Solo app desktop Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="ebd4f-123">Windows XP \[desktop apps only\]</span></span><br/>                                            |
| <span data-ttu-id="ebd4f-124">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="ebd4f-124">Minimum supported server</span></span><br/> | <span data-ttu-id="ebd4f-125">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="ebd4f-125">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="ebd4f-126">DLL</span><span class="sxs-lookup"><span data-stu-id="ebd4f-126">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ebd4f-127"><dt>Ntshrui.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ebd4f-127"><dt>Ntshrui.dll</dt></span></span> </dl> |
| <span data-ttu-id="ebd4f-128">Nomi Unicode e ANSI</span><span class="sxs-lookup"><span data-stu-id="ebd4f-128">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="ebd4f-129">**ShowShareFolderUIW** (Unicode)</span><span class="sxs-lookup"><span data-stu-id="ebd4f-129">**ShowShareFolderUIW** (Unicode)</span></span><br/>                                            |



## <a name="see-also"></a><span data-ttu-id="ebd4f-130">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="ebd4f-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ebd4f-131">**CanShareFolderW**</span><span class="sxs-lookup"><span data-stu-id="ebd4f-131">**CanShareFolderW**</span></span>](cansharefolderw.md)
</dt> </dl>

 

 
