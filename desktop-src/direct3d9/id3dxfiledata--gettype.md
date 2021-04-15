---
description: Recupera l'ID modello in questo oggetto dati file.
ms.assetid: abc53dda-d3ed-461b-b3d8-a64845c44c81
title: 'Metodo ID3DXFileData:: GetType (D3DX9Xof. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXFileData.GetType
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: 566052c06d5f7e55629a26442dd774a2f80fd647
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "104401993"
---
# <a name="id3dxfiledatagettype-method"></a><span data-ttu-id="e3c55-103">Metodo ID3DXFileData:: GetType</span><span class="sxs-lookup"><span data-stu-id="e3c55-103">ID3DXFileData::GetType method</span></span>

<span data-ttu-id="e3c55-104">Recupera l'ID modello in questo oggetto dati file.</span><span class="sxs-lookup"><span data-stu-id="e3c55-104">Retrieves the template ID in this file data object.</span></span>

## <a name="syntax"></a><span data-ttu-id="e3c55-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="e3c55-105">Syntax</span></span>


```C++
HRESULT GetType(
  [in] const GUID *pType
);
```



## <a name="parameters"></a><span data-ttu-id="e3c55-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="e3c55-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e3c55-107">*pType* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="e3c55-107">*pType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e3c55-108">Tipo: **[**GUID**](guid.md) \* const**</span><span class="sxs-lookup"><span data-stu-id="e3c55-108">Type: **const [**GUID**](guid.md)\***</span></span>

<span data-ttu-id="e3c55-109">Puntatore al GUID che rappresenta il modello in questo oggetto dati file.</span><span class="sxs-lookup"><span data-stu-id="e3c55-109">Pointer to the GUID representing the template in this file data object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e3c55-110">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="e3c55-110">Return value</span></span>

<span data-ttu-id="e3c55-111">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="e3c55-111">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="e3c55-112">Se il metodo ha esito positivo, il valore restituito è \_ OK.</span><span class="sxs-lookup"><span data-stu-id="e3c55-112">If the method succeeds, the return value is S\_OK.</span></span> <span data-ttu-id="e3c55-113">Se il metodo ha esito negativo, verrà restituito il valore seguente: D3DXFERR \_ BADVALUE.</span><span class="sxs-lookup"><span data-stu-id="e3c55-113">If the method fails, the following value will be returned: D3DXFERR\_BADVALUE.</span></span>

## <a name="requirements"></a><span data-ttu-id="e3c55-114">Requisiti</span><span class="sxs-lookup"><span data-stu-id="e3c55-114">Requirements</span></span>



| <span data-ttu-id="e3c55-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="e3c55-115">Requirement</span></span> | <span data-ttu-id="e3c55-116">Valore</span><span class="sxs-lookup"><span data-stu-id="e3c55-116">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="e3c55-117">Intestazione</span><span class="sxs-lookup"><span data-stu-id="e3c55-117">Header</span></span><br/>  | <dl> <span data-ttu-id="e3c55-118"><dt>D3DX9Xof. h</dt></span><span class="sxs-lookup"><span data-stu-id="e3c55-118"><dt>D3DX9Xof.h</dt></span></span> </dl> |
| <span data-ttu-id="e3c55-119">Libreria</span><span class="sxs-lookup"><span data-stu-id="e3c55-119">Library</span></span><br/> | <dl> <span data-ttu-id="e3c55-120"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="e3c55-120"><dt>D3dx9.lib</dt></span></span> </dl>  |



## <a name="see-also"></a><span data-ttu-id="e3c55-121">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="e3c55-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e3c55-122">ID3DXFileData</span><span class="sxs-lookup"><span data-stu-id="e3c55-122">ID3DXFileData</span></span>](id3dxfiledata.md)
</dt> </dl>

 

 




