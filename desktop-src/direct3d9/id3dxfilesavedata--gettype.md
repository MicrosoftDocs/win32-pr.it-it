---
description: Recupera l'ID modello del nodo dati del file.
ms.assetid: ff0662da-b4f8-4ed2-81d4-6771e91da262
title: 'Metodo ID3DXFileSaveData:: GetType (D3DX9Xof. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXFileSaveData.GetType
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: b774f71b4be111efcdbdaf8bc41b40d4b0efaa95
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "106323543"
---
# <a name="id3dxfilesavedatagettype-method"></a><span data-ttu-id="ddb98-103">Metodo ID3DXFileSaveData:: GetType</span><span class="sxs-lookup"><span data-stu-id="ddb98-103">ID3DXFileSaveData::GetType method</span></span>

<span data-ttu-id="ddb98-104">Recupera l'ID modello del nodo dati del file.</span><span class="sxs-lookup"><span data-stu-id="ddb98-104">Retrieves the template ID of this file data node.</span></span>

## <a name="syntax"></a><span data-ttu-id="ddb98-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="ddb98-105">Syntax</span></span>


```C++
HRESULT GetType(
  [in] GUID *type
);
```



## <a name="parameters"></a><span data-ttu-id="ddb98-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="ddb98-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ddb98-107">*tipo* \[ di in\]</span><span class="sxs-lookup"><span data-stu-id="ddb98-107">*type* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ddb98-108">Tipo: **[ **GUID**](guid.md)\***</span><span class="sxs-lookup"><span data-stu-id="ddb98-108">Type: **[**GUID**](guid.md)\***</span></span>

<span data-ttu-id="ddb98-109">Puntatore al GUID che rappresenta il modello in questo nodo dati del file.</span><span class="sxs-lookup"><span data-stu-id="ddb98-109">Pointer to the GUID representing the template in this file data node.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ddb98-110">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="ddb98-110">Return value</span></span>

<span data-ttu-id="ddb98-111">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="ddb98-111">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="ddb98-112">Se il metodo ha esito positivo, il valore restituito è \_ OK.</span><span class="sxs-lookup"><span data-stu-id="ddb98-112">If the method succeeds, the return value is S\_OK.</span></span> <span data-ttu-id="ddb98-113">Se il metodo ha esito negativo, il valore restituito può essere uno dei seguenti: D3DXFERR \_ BADOBJECT, D3DXFERR \_ BADVALUE.</span><span class="sxs-lookup"><span data-stu-id="ddb98-113">If the method fails, the return value can be one of the following: D3DXFERR\_BADOBJECT, D3DXFERR\_BADVALUE.</span></span>

## <a name="requirements"></a><span data-ttu-id="ddb98-114">Requisiti</span><span class="sxs-lookup"><span data-stu-id="ddb98-114">Requirements</span></span>



| <span data-ttu-id="ddb98-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="ddb98-115">Requirement</span></span> | <span data-ttu-id="ddb98-116">Valore</span><span class="sxs-lookup"><span data-stu-id="ddb98-116">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="ddb98-117">Intestazione</span><span class="sxs-lookup"><span data-stu-id="ddb98-117">Header</span></span><br/>  | <dl> <span data-ttu-id="ddb98-118"><dt>D3DX9Xof. h</dt></span><span class="sxs-lookup"><span data-stu-id="ddb98-118"><dt>D3DX9Xof.h</dt></span></span> </dl> |
| <span data-ttu-id="ddb98-119">Libreria</span><span class="sxs-lookup"><span data-stu-id="ddb98-119">Library</span></span><br/> | <dl> <span data-ttu-id="ddb98-120"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="ddb98-120"><dt>D3dx9.lib</dt></span></span> </dl>  |



## <a name="see-also"></a><span data-ttu-id="ddb98-121">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="ddb98-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ddb98-122">ID3DXFileSaveData</span><span class="sxs-lookup"><span data-stu-id="ddb98-122">ID3DXFileSaveData</span></span>](id3dxfilesavedata.md)
</dt> </dl>

 

 




