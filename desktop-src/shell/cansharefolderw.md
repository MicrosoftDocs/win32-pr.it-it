---
description: Consente di determinare se visualizzare l'opzione Condividi questa cartella nella visualizzazione Web.
title: Funzione CanShareFolderW
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CanShareFolderW
- CanShareFolderW
api_type:
- DllExport
api_location:
- Ntshrui.dll
ms.assetid: 5fd28a14-53e7-4016-9c49-9bb14ce7808b
ms.openlocfilehash: 46df03208ecc468aac366fb0b4cfb33e1a68157e
ms.sourcegitcommit: 3caaa3c92dcb1ef12f84464d14ce6262e65e988e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 05/12/2021
ms.locfileid: "109841682"
---
# <a name="cansharefolderw-function"></a><span data-ttu-id="c1d1b-103">Funzione CanShareFolderW</span><span class="sxs-lookup"><span data-stu-id="c1d1b-103">CanShareFolderW function</span></span>

<span data-ttu-id="c1d1b-104">\[Questa funzione è disponibile tramite Windows XP con Service Pack 2 (SP2) e Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="c1d1b-104">\[This function is available through Windows XP with Service Pack 2 (SP2) and Windows Server 2003.</span></span> <span data-ttu-id="c1d1b-105">Potrebbe essere modificato o non disponibile nelle versioni successive di Windows.\]</span><span class="sxs-lookup"><span data-stu-id="c1d1b-105">It might be altered or unavailable in subsequent versions of Windows.\]</span></span>

<span data-ttu-id="c1d1b-106">Consente di determinare se visualizzare **l'opzione Condividi** questa cartella nella visualizzazione Web.</span><span class="sxs-lookup"><span data-stu-id="c1d1b-106">Used to determine whether to show the **Share this folder** option in web view.</span></span>

## <a name="syntax"></a><span data-ttu-id="c1d1b-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="c1d1b-107">Syntax</span></span>


```C++
STDAPI CanShareFolderW(
  _In_ LPCWSTR pszPath
);
```



## <a name="parameters"></a><span data-ttu-id="c1d1b-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="c1d1b-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c1d1b-109">*pszPath* \[ Pollici\]</span><span class="sxs-lookup"><span data-stu-id="c1d1b-109">*pszPath* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c1d1b-110">Tipo: **LPCWSTR**</span><span class="sxs-lookup"><span data-stu-id="c1d1b-110">Type: **LPCWSTR**</span></span>

<span data-ttu-id="c1d1b-111">Puntatore a una stringa che specifica il percorso della cartella da testare.</span><span class="sxs-lookup"><span data-stu-id="c1d1b-111">A pointer to a string that specifies the path of the folder to test.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c1d1b-112">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="c1d1b-112">Return value</span></span>

<span data-ttu-id="c1d1b-113">Tipo: **STDAPI**</span><span class="sxs-lookup"><span data-stu-id="c1d1b-113">Type: **STDAPI**</span></span>

<span data-ttu-id="c1d1b-114">I valori restituiti includono quanto segue.</span><span class="sxs-lookup"><span data-stu-id="c1d1b-114">Return values include the following.</span></span>



| <span data-ttu-id="c1d1b-115">Codice/valore restituito</span><span class="sxs-lookup"><span data-stu-id="c1d1b-115">Return code/value</span></span>                                                                        | <span data-ttu-id="c1d1b-116">Descrizione</span><span class="sxs-lookup"><span data-stu-id="c1d1b-116">Description</span></span>                                                                           |
|------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="c1d1b-117"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="c1d1b-117"><dt>**S\_OK**</dt></span></span> </dl>     | <span data-ttu-id="c1d1b-118">Il percorso a cui punta *pszPath* specifica una cartella che può essere condivisa.</span><span class="sxs-lookup"><span data-stu-id="c1d1b-118">The path pointed to by *pszPath* specifies a folder that can be shared.</span></span><br/>    |
| <dl> <span data-ttu-id="c1d1b-119"><dt>**S \_ FALSE**</dt></span><span class="sxs-lookup"><span data-stu-id="c1d1b-119"><dt>**S\_FALSE**</dt></span></span> </dl>  | <span data-ttu-id="c1d1b-120">Il percorso a cui punta *pszPath* specifica una cartella che non può essere condivisa.</span><span class="sxs-lookup"><span data-stu-id="c1d1b-120">The path pointed to by *pszPath* specifies a folder that cannot be shared.</span></span><br/> |
| <dl> <span data-ttu-id="c1d1b-121"><dt>Errore HRESULT</dt></span><span class="sxs-lookup"><span data-stu-id="c1d1b-121"><dt>HRESULT error</dt></span></span> </dl> | <span data-ttu-id="c1d1b-122">un errore.</span><span class="sxs-lookup"><span data-stu-id="c1d1b-122">An error has occurred.</span></span><br/>                                                     |



 

## <a name="remarks"></a><span data-ttu-id="c1d1b-123">Commenti</span><span class="sxs-lookup"><span data-stu-id="c1d1b-123">Remarks</span></span>

<span data-ttu-id="c1d1b-124">A questa funzione non è associato alcun file con estensione lib.</span><span class="sxs-lookup"><span data-stu-id="c1d1b-124">This function has no associated .lib file.</span></span> <span data-ttu-id="c1d1b-125">Per usarlo, è necessario usare [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) e [**GetProcAddress.**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress)</span><span class="sxs-lookup"><span data-stu-id="c1d1b-125">You must use [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) to use it.</span></span>

## <a name="requirements"></a><span data-ttu-id="c1d1b-126">Requisiti</span><span class="sxs-lookup"><span data-stu-id="c1d1b-126">Requirements</span></span>



| <span data-ttu-id="c1d1b-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="c1d1b-127">Requirement</span></span> | <span data-ttu-id="c1d1b-128">Valore</span><span class="sxs-lookup"><span data-stu-id="c1d1b-128">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="c1d1b-129">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="c1d1b-129">Minimum supported client</span></span><br/> | <span data-ttu-id="c1d1b-130">Solo app desktop di Windows XP \[\]</span><span class="sxs-lookup"><span data-stu-id="c1d1b-130">Windows XP \[desktop apps only\]</span></span><br/>                                            |
| <span data-ttu-id="c1d1b-131">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="c1d1b-131">Minimum supported server</span></span><br/> | <span data-ttu-id="c1d1b-132">Solo app desktop di Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="c1d1b-132">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="c1d1b-133">DLL</span><span class="sxs-lookup"><span data-stu-id="c1d1b-133">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c1d1b-134"><dt>Ntshrui.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c1d1b-134"><dt>Ntshrui.dll</dt></span></span> </dl> |
| <span data-ttu-id="c1d1b-135">Nomi Unicode e ANSI</span><span class="sxs-lookup"><span data-stu-id="c1d1b-135">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="c1d1b-136">**CanShareFolderW** (Unicode)</span><span class="sxs-lookup"><span data-stu-id="c1d1b-136">**CanShareFolderW** (Unicode)</span></span><br/>                                               |



## <a name="see-also"></a><span data-ttu-id="c1d1b-137">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="c1d1b-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c1d1b-138">**ShowShareFolderUI**</span><span class="sxs-lookup"><span data-stu-id="c1d1b-138">**ShowShareFolderUI**</span></span>](./showsharefolderui.md)
</dt> </dl>

 

 
