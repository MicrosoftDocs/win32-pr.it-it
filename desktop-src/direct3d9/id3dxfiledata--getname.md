---
description: Recupera il nome di questo oggetto dati file.
ms.assetid: 182529cb-144c-4ed8-94bf-6688598e9ea7
title: 'Metodo ID3DXFileData:: GetName (D3DX9Xof. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXFileData.GetName
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: e27fc3e95280f29a33d4ececffc7c229563462a0
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "106323070"
---
# <a name="id3dxfiledatagetname-method"></a><span data-ttu-id="d8145-103">Metodo ID3DXFileData:: GetName</span><span class="sxs-lookup"><span data-stu-id="d8145-103">ID3DXFileData::GetName method</span></span>

<span data-ttu-id="d8145-104">Recupera il nome di questo oggetto dati file.</span><span class="sxs-lookup"><span data-stu-id="d8145-104">Retrieves the name of this file data object.</span></span>

## <a name="syntax"></a><span data-ttu-id="d8145-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="d8145-105">Syntax</span></span>


```C++
HRESULT GetName(
  [in]      LPSTR  szName,
  [in, out] SIZE_T *puiSize
);
```



## <a name="parameters"></a><span data-ttu-id="d8145-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="d8145-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d8145-107">*szName* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="d8145-107">*szName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d8145-108">Tipo: **[ **LPSTR**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="d8145-108">Type: **[**LPSTR**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="d8145-109">Indirizzo di un puntatore per la ricezione del nome di questo oggetto dati file.</span><span class="sxs-lookup"><span data-stu-id="d8145-109">Address of a pointer to receive the name of this file data object.</span></span> <span data-ttu-id="d8145-110">Se questo parametro è **null**, puiSize restituirà la dimensione della stringa.</span><span class="sxs-lookup"><span data-stu-id="d8145-110">If this parameter is **NULL**, then puiSize will return the size of the string.</span></span> <span data-ttu-id="d8145-111">Se szName punta alla memoria valida, il nome di questo oggetto dati file verrà copiato in szName fino al numero di caratteri specificato da puiSize.</span><span class="sxs-lookup"><span data-stu-id="d8145-111">If szName points to valid memory, the name of this file data object will be copied into szName up to the number of characters given by puiSize.</span></span>

</dd> <dt>

<span data-ttu-id="d8145-112">*puiSize* \[ in uscita\]</span><span class="sxs-lookup"><span data-stu-id="d8145-112">*puiSize* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="d8145-113">Tipo: **[ **size \_ T**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="d8145-113">Type: **[**SIZE\_T**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="d8145-114">Puntatore alla dimensione della stringa che rappresenta il nome di questo oggetto dati file.</span><span class="sxs-lookup"><span data-stu-id="d8145-114">Pointer to the size of the string that represents the name of this file data object.</span></span> <span data-ttu-id="d8145-115">Questo parametro può essere **null** se szName fornisce un riferimento al nome.</span><span class="sxs-lookup"><span data-stu-id="d8145-115">This parameter can be **NULL** if szName provides a reference to the name.</span></span> <span data-ttu-id="d8145-116">Questo parametro restituirà la dimensione della stringa se szName è **null**.</span><span class="sxs-lookup"><span data-stu-id="d8145-116">This parameter will return the size of the string if szName is **NULL**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d8145-117">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="d8145-117">Return value</span></span>

<span data-ttu-id="d8145-118">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="d8145-118">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="d8145-119">Se il metodo ha esito positivo, il valore restituito è \_ OK.</span><span class="sxs-lookup"><span data-stu-id="d8145-119">If the method succeeds, the return value is S\_OK.</span></span> <span data-ttu-id="d8145-120">Se il metodo ha esito negativo, verrà restituito il valore seguente: D3DXFERR \_ BADVALUE.</span><span class="sxs-lookup"><span data-stu-id="d8145-120">If the method fails, the following value will be returned: D3DXFERR\_BADVALUE.</span></span>

## <a name="remarks"></a><span data-ttu-id="d8145-121">Commenti</span><span class="sxs-lookup"><span data-stu-id="d8145-121">Remarks</span></span>

<span data-ttu-id="d8145-122">Affinché questo metodo abbia esito positivo, szName o *puiSize* deve essere non **null**.</span><span class="sxs-lookup"><span data-stu-id="d8145-122">For this method to succeed, either szName or *puiSize* must be non-**NULL**.</span></span>

## <a name="requirements"></a><span data-ttu-id="d8145-123">Requisiti</span><span class="sxs-lookup"><span data-stu-id="d8145-123">Requirements</span></span>



| <span data-ttu-id="d8145-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="d8145-124">Requirement</span></span> | <span data-ttu-id="d8145-125">Valore</span><span class="sxs-lookup"><span data-stu-id="d8145-125">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="d8145-126">Intestazione</span><span class="sxs-lookup"><span data-stu-id="d8145-126">Header</span></span><br/>  | <dl> <span data-ttu-id="d8145-127"><dt>D3DX9Xof. h</dt></span><span class="sxs-lookup"><span data-stu-id="d8145-127"><dt>D3DX9Xof.h</dt></span></span> </dl> |
| <span data-ttu-id="d8145-128">Libreria</span><span class="sxs-lookup"><span data-stu-id="d8145-128">Library</span></span><br/> | <dl> <span data-ttu-id="d8145-129"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="d8145-129"><dt>D3dx9.lib</dt></span></span> </dl>  |



## <a name="see-also"></a><span data-ttu-id="d8145-130">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="d8145-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d8145-131">ID3DXFileData</span><span class="sxs-lookup"><span data-stu-id="d8145-131">ID3DXFileData</span></span>](id3dxfiledata.md)
</dt> </dl>

 

 
