---
description: Recupera un enumeratore che restituirà un puntatore a un elenco di identificatori di elemento (PIDL) per ogni visualizzazione estesa.
title: 'Metodo IShellFolderViewType:: EnumViews'
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
ms.openlocfilehash: 4ccaac7baf99608e097b8f8b67c8eac30f60ed3a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104993824"
---
# <a name="ishellfolderviewtypeenumviews-method"></a><span data-ttu-id="bf0f5-103">Metodo IShellFolderViewType:: EnumViews</span><span class="sxs-lookup"><span data-stu-id="bf0f5-103">IShellFolderViewType::EnumViews method</span></span>

<span data-ttu-id="bf0f5-104">Recupera un enumeratore che restituirà un puntatore a un elenco di identificatori di elemento (PIDL) per ogni visualizzazione estesa.</span><span class="sxs-lookup"><span data-stu-id="bf0f5-104">Retrieves an enumerator that will return one pointer to an item identifier list (PIDL) for every extended view.</span></span>

## <a name="syntax"></a><span data-ttu-id="bf0f5-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="bf0f5-105">Syntax</span></span>


```C++
HRESULT EnumViews(
  [in]  ULONG       grfFlags,
  [out] IEnumIDList **ppenum
);
```



## <a name="parameters"></a><span data-ttu-id="bf0f5-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="bf0f5-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="bf0f5-107">*grfFlags* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="bf0f5-107">*grfFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="bf0f5-108">Tipo: **ULONG**</span><span class="sxs-lookup"><span data-stu-id="bf0f5-108">Type: **ULONG**</span></span>

<span data-ttu-id="bf0f5-109">Flag che indicano gli elementi da includere nell'enumerazione.</span><span class="sxs-lookup"><span data-stu-id="bf0f5-109">Flags indicating which items to include in the enumeration.</span></span> <span data-ttu-id="bf0f5-110">Per un elenco di valori possibili, vedere il tipo enumerato [**SHCONTF**](/windows/win32/api/shobjidl_core/ne-shobjidl_core-_shcontf) .</span><span class="sxs-lookup"><span data-stu-id="bf0f5-110">For a list of possible values, see the [**SHCONTF**](/windows/win32/api/shobjidl_core/ne-shobjidl_core-_shcontf) enumerated type.</span></span> <span data-ttu-id="bf0f5-111">Questo parametro può essere ignorato.</span><span class="sxs-lookup"><span data-stu-id="bf0f5-111">This parameter may be ignored.</span></span>

</dd> <dt>

<span data-ttu-id="bf0f5-112">*ppEnum* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="bf0f5-112">*ppenum* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="bf0f5-113">Tipo: **[ **IEnumIDList**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ienumidlist)\*\***</span><span class="sxs-lookup"><span data-stu-id="bf0f5-113">Type: **[**IEnumIDList**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ienumidlist)\*\***</span></span>

<span data-ttu-id="bf0f5-114">Indirizzo di una variabile puntatore di tipo [**IEnumIDList**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ienumidlist) che riceve l'enumeratore.</span><span class="sxs-lookup"><span data-stu-id="bf0f5-114">The address of a pointer variable of type [**IEnumIDList**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ienumidlist) that receives the enumerator.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="bf0f5-115">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="bf0f5-115">Return value</span></span>

<span data-ttu-id="bf0f5-116">Tipo: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="bf0f5-116">Type: **HRESULT**</span></span>

<span data-ttu-id="bf0f5-117">Se questo metodo ha esito positivo, restituisce **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="bf0f5-117">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="bf0f5-118">In caso contrario, restituisce un codice di errore **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="bf0f5-118">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="bf0f5-119">Commenti</span><span class="sxs-lookup"><span data-stu-id="bf0f5-119">Remarks</span></span>

<span data-ttu-id="bf0f5-120">Le visualizzazioni sono rappresentate all'utente come cartelle nascoste dalla directory radice (rappresentata da PIDL).</span><span class="sxs-lookup"><span data-stu-id="bf0f5-120">Views are represented to the user as hidden folders off the root directory (represented by PIDLs).</span></span> <span data-ttu-id="bf0f5-121">Quando appropriato, la visualizzazione predefinita (disattivata nella cartella radice) viene rappresentata come **valore null** o vuoto, PIDL.</span><span class="sxs-lookup"><span data-stu-id="bf0f5-121">Whenever appropriate, the default view (off the root folder) is represented as the **NULL**, or empty, PIDL.</span></span>

## <a name="requirements"></a><span data-ttu-id="bf0f5-122">Requisiti</span><span class="sxs-lookup"><span data-stu-id="bf0f5-122">Requirements</span></span>



| <span data-ttu-id="bf0f5-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="bf0f5-123">Requirement</span></span> | <span data-ttu-id="bf0f5-124">Valore</span><span class="sxs-lookup"><span data-stu-id="bf0f5-124">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="bf0f5-125">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="bf0f5-125">Minimum supported client</span></span><br/> | <span data-ttu-id="bf0f5-126">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="bf0f5-126">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="bf0f5-127">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="bf0f5-127">Minimum supported server</span></span><br/> | <span data-ttu-id="bf0f5-128">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="bf0f5-128">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="bf0f5-129">DLL</span><span class="sxs-lookup"><span data-stu-id="bf0f5-129">DLL</span></span><br/>                      | <dl> <span data-ttu-id="bf0f5-130"><dt>Shell32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="bf0f5-130"><dt>Shell32.dll</dt></span></span> </dl> |



 

 




