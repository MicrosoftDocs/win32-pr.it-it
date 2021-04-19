---
description: Recupera l'oggetto di enumerazione in questo oggetto dati del file.
ms.assetid: 383560e2-1888-4e37-9883-2ddbcb101cf6
title: 'Metodo ID3DXFileData:: getenum (D3DX9Xof. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXFileData.GetEnum
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: 7dd565f6f76d42159d77d8b83c638c75648f293b
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "106323071"
---
# <a name="id3dxfiledatagetenum-method"></a><span data-ttu-id="2b418-103">Metodo ID3DXFileData:: getenum</span><span class="sxs-lookup"><span data-stu-id="2b418-103">ID3DXFileData::GetEnum method</span></span>

<span data-ttu-id="2b418-104">Recupera l'oggetto di enumerazione in questo oggetto dati del file.</span><span class="sxs-lookup"><span data-stu-id="2b418-104">Retrieves the enumeration object in this file data object.</span></span>

## <a name="syntax"></a><span data-ttu-id="2b418-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="2b418-105">Syntax</span></span>


```C++
HRESULT GetEnum(
  [in] ID3DXFileEnumObject **ppObj
);
```



## <a name="parameters"></a><span data-ttu-id="2b418-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="2b418-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2b418-107">*ppObj* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="2b418-107">*ppObj* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2b418-108">Tipo: **[ **ID3DXFileEnumObject**](id3dxfileenumobject.md)\*\***</span><span class="sxs-lookup"><span data-stu-id="2b418-108">Type: **[**ID3DXFileEnumObject**](id3dxfileenumobject.md)\*\***</span></span>

<span data-ttu-id="2b418-109">Indirizzo di un puntatore per ricevere l'oggetto di enumerazione in questo oggetto dati del file.</span><span class="sxs-lookup"><span data-stu-id="2b418-109">Address of a pointer to receive the enumeration object in this file data object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2b418-110">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="2b418-110">Return value</span></span>

<span data-ttu-id="2b418-111">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="2b418-111">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="2b418-112">Se il metodo ha esito positivo, il valore restituito è \_ OK.</span><span class="sxs-lookup"><span data-stu-id="2b418-112">If the method succeeds, the return value is S\_OK.</span></span> <span data-ttu-id="2b418-113">Se il metodo ha esito negativo, verrà restituito il valore seguente: D3DXFERR \_ BADVALUE.</span><span class="sxs-lookup"><span data-stu-id="2b418-113">If the method fails, the following value will be returned: D3DXFERR\_BADVALUE.</span></span>

## <a name="requirements"></a><span data-ttu-id="2b418-114">Requisiti</span><span class="sxs-lookup"><span data-stu-id="2b418-114">Requirements</span></span>



| <span data-ttu-id="2b418-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="2b418-115">Requirement</span></span> | <span data-ttu-id="2b418-116">Valore</span><span class="sxs-lookup"><span data-stu-id="2b418-116">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="2b418-117">Intestazione</span><span class="sxs-lookup"><span data-stu-id="2b418-117">Header</span></span><br/>  | <dl> <span data-ttu-id="2b418-118"><dt>D3DX9Xof. h</dt></span><span class="sxs-lookup"><span data-stu-id="2b418-118"><dt>D3DX9Xof.h</dt></span></span> </dl> |
| <span data-ttu-id="2b418-119">Libreria</span><span class="sxs-lookup"><span data-stu-id="2b418-119">Library</span></span><br/> | <dl> <span data-ttu-id="2b418-120"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="2b418-120"><dt>D3dx9.lib</dt></span></span> </dl>  |



## <a name="see-also"></a><span data-ttu-id="2b418-121">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="2b418-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2b418-122">ID3DXFileData</span><span class="sxs-lookup"><span data-stu-id="2b418-122">ID3DXFileData</span></span>](id3dxfiledata.md)
</dt> </dl>

 

 




