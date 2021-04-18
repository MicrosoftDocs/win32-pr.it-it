---
description: Recupera il numero di elementi figlio in questo oggetto dati del file.
ms.assetid: ebc6905b-a453-4a15-adae-956ce7034084
title: 'Metodo ID3DXFileData:: GetChildren (D3DX9Xof. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXFileData.GetChildren
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: dd6932801f3d4b079efa6f1ed2688505dbd7828b
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "106322988"
---
# <a name="id3dxfiledatagetchildren-method"></a><span data-ttu-id="3c6ee-103">Metodo ID3DXFileData:: GetChildren</span><span class="sxs-lookup"><span data-stu-id="3c6ee-103">ID3DXFileData::GetChildren method</span></span>

<span data-ttu-id="3c6ee-104">Recupera il numero di elementi figlio in questo oggetto dati del file.</span><span class="sxs-lookup"><span data-stu-id="3c6ee-104">Retrieves the number of children in this file data object.</span></span>

## <a name="syntax"></a><span data-ttu-id="3c6ee-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="3c6ee-105">Syntax</span></span>


```C++
HRESULT GetChildren(
  [in] SIZE_T *puiChildren
);
```



## <a name="parameters"></a><span data-ttu-id="3c6ee-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="3c6ee-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3c6ee-107">*puiChildren* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="3c6ee-107">*puiChildren* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3c6ee-108">Tipo: **[ **size \_ T**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="3c6ee-108">Type: **[**SIZE\_T**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="3c6ee-109">Indirizzo di un puntatore per ricevere il numero di elementi figlio in questo oggetto dati file.</span><span class="sxs-lookup"><span data-stu-id="3c6ee-109">Address of a pointer to receive the number of children in this file data object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3c6ee-110">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="3c6ee-110">Return value</span></span>

<span data-ttu-id="3c6ee-111">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="3c6ee-111">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="3c6ee-112">Se il metodo ha esito positivo, il valore restituito è \_ OK.</span><span class="sxs-lookup"><span data-stu-id="3c6ee-112">If the method succeeds, the return value is S\_OK.</span></span> <span data-ttu-id="3c6ee-113">Se il metodo ha esito negativo, verrà restituito il valore seguente: D3DXFERR \_ BADVALUE.</span><span class="sxs-lookup"><span data-stu-id="3c6ee-113">If the method fails, the following value will be returned: D3DXFERR\_BADVALUE.</span></span>

## <a name="requirements"></a><span data-ttu-id="3c6ee-114">Requisiti</span><span class="sxs-lookup"><span data-stu-id="3c6ee-114">Requirements</span></span>



| <span data-ttu-id="3c6ee-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="3c6ee-115">Requirement</span></span> | <span data-ttu-id="3c6ee-116">Valore</span><span class="sxs-lookup"><span data-stu-id="3c6ee-116">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="3c6ee-117">Intestazione</span><span class="sxs-lookup"><span data-stu-id="3c6ee-117">Header</span></span><br/>  | <dl> <span data-ttu-id="3c6ee-118"><dt>D3DX9Xof. h</dt></span><span class="sxs-lookup"><span data-stu-id="3c6ee-118"><dt>D3DX9Xof.h</dt></span></span> </dl> |
| <span data-ttu-id="3c6ee-119">Libreria</span><span class="sxs-lookup"><span data-stu-id="3c6ee-119">Library</span></span><br/> | <dl> <span data-ttu-id="3c6ee-120"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="3c6ee-120"><dt>D3dx9.lib</dt></span></span> </dl>  |



## <a name="see-also"></a><span data-ttu-id="3c6ee-121">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="3c6ee-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3c6ee-122">ID3DXFileData</span><span class="sxs-lookup"><span data-stu-id="3c6ee-122">ID3DXFileData</span></span>](id3dxfiledata.md)
</dt> </dl>

 

 
