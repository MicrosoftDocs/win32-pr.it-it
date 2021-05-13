---
description: Recupera un enumeratore che restituirà un puntatore a un elenco di identificatori di elemento (PIDL) per ogni visualizzazione estesa.
title: Metodo IShellFolderViewType::EnumViews
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IShellFolderViewType.EnumViews
api_type:
- COM
api_location:
- Shell32.dll
ms.assetid: e44cd774-1d16-4faa-b5ca-fcaf2740cdca
ms.openlocfilehash: 1627bb134066821444788ca44a3527278a02f4c7
ms.sourcegitcommit: 3caaa3c92dcb1ef12f84464d14ce6262e65e988e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 05/12/2021
ms.locfileid: "109842772"
---
# <a name="ishellfolderviewtypeenumviews-method"></a><span data-ttu-id="c4294-103">Metodo IShellFolderViewType::EnumViews</span><span class="sxs-lookup"><span data-stu-id="c4294-103">IShellFolderViewType::EnumViews method</span></span>

<span data-ttu-id="c4294-104">Recupera un enumeratore che restituirà un puntatore a un elenco di identificatori di elemento (PIDL) per ogni visualizzazione estesa.</span><span class="sxs-lookup"><span data-stu-id="c4294-104">Retrieves an enumerator that will return one pointer to an item identifier list (PIDL) for every extended view.</span></span>

## <a name="syntax"></a><span data-ttu-id="c4294-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="c4294-105">Syntax</span></span>


```C++
HRESULT EnumViews(
  [in]  ULONG       grfFlags,
  [out] IEnumIDList **ppenum
);
```



## <a name="parameters"></a><span data-ttu-id="c4294-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="c4294-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c4294-107">*grfFlags* \[ Pollici\]</span><span class="sxs-lookup"><span data-stu-id="c4294-107">*grfFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c4294-108">Tipo: **ULONG**</span><span class="sxs-lookup"><span data-stu-id="c4294-108">Type: **ULONG**</span></span>

<span data-ttu-id="c4294-109">Flag che indicano gli elementi da includere nell'enumerazione .</span><span class="sxs-lookup"><span data-stu-id="c4294-109">Flags indicating which items to include in the enumeration.</span></span> <span data-ttu-id="c4294-110">Per un elenco dei valori possibili, vedere il [**tipo enumerato SHCONTF.**](/windows/win32/api/shobjidl_core/ne-shobjidl_core-_shcontf)</span><span class="sxs-lookup"><span data-stu-id="c4294-110">For a list of possible values, see the [**SHCONTF**](/windows/win32/api/shobjidl_core/ne-shobjidl_core-_shcontf) enumerated type.</span></span> <span data-ttu-id="c4294-111">Questo parametro può essere ignorato.</span><span class="sxs-lookup"><span data-stu-id="c4294-111">This parameter may be ignored.</span></span>

</dd> <dt>

<span data-ttu-id="c4294-112">*ppenum* \[ Cambio\]</span><span class="sxs-lookup"><span data-stu-id="c4294-112">*ppenum* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="c4294-113">Tipo: **[ **IEnumIDList**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ienumidlist)\*\***</span><span class="sxs-lookup"><span data-stu-id="c4294-113">Type: **[**IEnumIDList**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ienumidlist)\*\***</span></span>

<span data-ttu-id="c4294-114">Indirizzo di una variabile puntatore di tipo [**IEnumIDList**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ienumidlist) che riceve l'enumeratore.</span><span class="sxs-lookup"><span data-stu-id="c4294-114">The address of a pointer variable of type [**IEnumIDList**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ienumidlist) that receives the enumerator.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c4294-115">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="c4294-115">Return value</span></span>

<span data-ttu-id="c4294-116">Tipo: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="c4294-116">Type: **HRESULT**</span></span>

<span data-ttu-id="c4294-117">Se questo metodo ha esito positivo, restituisce **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="c4294-117">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="c4294-118">In caso contrario, restituisce un **codice di errore HRESULT.**</span><span class="sxs-lookup"><span data-stu-id="c4294-118">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="c4294-119">Commenti</span><span class="sxs-lookup"><span data-stu-id="c4294-119">Remarks</span></span>

<span data-ttu-id="c4294-120">Le visualizzazioni vengono rappresentate all'utente come cartelle nascoste dalla directory radice (rappresentate da PIDL).</span><span class="sxs-lookup"><span data-stu-id="c4294-120">Views are represented to the user as hidden folders off the root directory (represented by PIDLs).</span></span> <span data-ttu-id="c4294-121">Se appropriato, la visualizzazione predefinita (all'di fuori della cartella radice) viene rappresentata come **NULL** o come PIDL vuoto.</span><span class="sxs-lookup"><span data-stu-id="c4294-121">Whenever appropriate, the default view (off the root folder) is represented as the **NULL**, or empty, PIDL.</span></span>

## <a name="requirements"></a><span data-ttu-id="c4294-122">Requisiti</span><span class="sxs-lookup"><span data-stu-id="c4294-122">Requirements</span></span>



| <span data-ttu-id="c4294-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="c4294-123">Requirement</span></span> | <span data-ttu-id="c4294-124">Valore</span><span class="sxs-lookup"><span data-stu-id="c4294-124">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="c4294-125">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="c4294-125">Minimum supported client</span></span><br/> | <span data-ttu-id="c4294-126">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="c4294-126">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="c4294-127">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="c4294-127">Minimum supported server</span></span><br/> | <span data-ttu-id="c4294-128">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="c4294-128">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="c4294-129">DLL</span><span class="sxs-lookup"><span data-stu-id="c4294-129">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c4294-130"><dt>Shell32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c4294-130"><dt>Shell32.dll</dt></span></span> </dl> |



 

 




