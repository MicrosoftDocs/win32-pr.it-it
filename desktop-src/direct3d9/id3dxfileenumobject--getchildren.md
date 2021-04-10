---
description: Recupera il numero di oggetti figlio in questo oggetto dati di file.
ms.assetid: 4409819f-a346-40b1-8e12-86e8128ece47
title: 'Metodo ID3DXFileEnumObject:: GetChildren (D3DX9Xof. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXFileEnumObject.GetChildren
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: cafa79844e89602d3b88756e04ca460f611516dd
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "103762137"
---
# <a name="id3dxfileenumobjectgetchildren-method"></a><span data-ttu-id="39d06-103">Metodo ID3DXFileEnumObject:: GetChildren</span><span class="sxs-lookup"><span data-stu-id="39d06-103">ID3DXFileEnumObject::GetChildren method</span></span>

<span data-ttu-id="39d06-104">Recupera il numero di oggetti figlio in questo oggetto dati di file.</span><span class="sxs-lookup"><span data-stu-id="39d06-104">Retrieves the number of child objects in this file data object.</span></span>

## <a name="syntax"></a><span data-ttu-id="39d06-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="39d06-105">Syntax</span></span>


```C++
HRESULT GetChildren(
  [in] SIZE_T *puiChildren
);
```



## <a name="parameters"></a><span data-ttu-id="39d06-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="39d06-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="39d06-107">*puiChildren* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="39d06-107">*puiChildren* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="39d06-108">Tipo: **[ **size \_ T**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="39d06-108">Type: **[**SIZE\_T**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="39d06-109">Indirizzo di un puntatore per ricevere il numero di oggetti figlio in questo oggetto dati file.</span><span class="sxs-lookup"><span data-stu-id="39d06-109">Address of a pointer to receive the number of child objects in this file data object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="39d06-110">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="39d06-110">Return value</span></span>

<span data-ttu-id="39d06-111">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="39d06-111">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="39d06-112">Se il metodo ha esito positivo, il valore restituito è \_ OK.</span><span class="sxs-lookup"><span data-stu-id="39d06-112">If the method succeeds, the return value is S\_OK.</span></span> <span data-ttu-id="39d06-113">Se il metodo ha esito negativo, verrà restituito il valore seguente: D3DXFERR \_ BADVALUE.</span><span class="sxs-lookup"><span data-stu-id="39d06-113">If the method fails, the following value will be returned: D3DXFERR\_BADVALUE.</span></span>

## <a name="requirements"></a><span data-ttu-id="39d06-114">Requisiti</span><span class="sxs-lookup"><span data-stu-id="39d06-114">Requirements</span></span>



| <span data-ttu-id="39d06-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="39d06-115">Requirement</span></span> | <span data-ttu-id="39d06-116">Valore</span><span class="sxs-lookup"><span data-stu-id="39d06-116">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="39d06-117">Intestazione</span><span class="sxs-lookup"><span data-stu-id="39d06-117">Header</span></span><br/>  | <dl> <span data-ttu-id="39d06-118"><dt>D3DX9Xof. h</dt></span><span class="sxs-lookup"><span data-stu-id="39d06-118"><dt>D3DX9Xof.h</dt></span></span> </dl> |
| <span data-ttu-id="39d06-119">Libreria</span><span class="sxs-lookup"><span data-stu-id="39d06-119">Library</span></span><br/> | <dl> <span data-ttu-id="39d06-120"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="39d06-120"><dt>D3dx9.lib</dt></span></span> </dl>  |



## <a name="see-also"></a><span data-ttu-id="39d06-121">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="39d06-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="39d06-122">ID3DXFileEnumObject</span><span class="sxs-lookup"><span data-stu-id="39d06-122">ID3DXFileEnumObject</span></span>](id3dxfileenumobject.md)
</dt> </dl>

 

 
