---
description: Recupera il GUID del nodo dati del file ID3DXFileSaveData.
ms.assetid: 79413eb4-4889-4148-b1a1-58a0b780403c
title: 'Metodo ID3DXFileSaveData:: GetId (D3DX9Xof. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXFileSaveData.GetId
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: b03322e03d1bedc10f9deec82c60418b5ad846b8
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "106323061"
---
# <a name="id3dxfilesavedatagetid-method"></a><span data-ttu-id="ca6ef-103">Metodo ID3DXFileSaveData:: GetId</span><span class="sxs-lookup"><span data-stu-id="ca6ef-103">ID3DXFileSaveData::GetId method</span></span>

<span data-ttu-id="ca6ef-104">Recupera il GUID del nodo dati del file [**ID3DXFileSaveData**](id3dxfilesavedata.md) .</span><span class="sxs-lookup"><span data-stu-id="ca6ef-104">Retrieves the GUID of this [**ID3DXFileSaveData**](id3dxfilesavedata.md) file data node.</span></span>

## <a name="syntax"></a><span data-ttu-id="ca6ef-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="ca6ef-105">Syntax</span></span>


```C++
HRESULT GetId(
  [out] 
            LPGUID pId
);
```



## <a name="parameters"></a><span data-ttu-id="ca6ef-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="ca6ef-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ca6ef-107">*PID* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="ca6ef-107">*pId* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="ca6ef-108">Tipo: **LPGUID**</span><span class="sxs-lookup"><span data-stu-id="ca6ef-108">Type: **LPGUID**</span></span>

<span data-ttu-id="ca6ef-109">Puntatore a un GUID per ricevere l'ID del nodo dati del file.</span><span class="sxs-lookup"><span data-stu-id="ca6ef-109">Pointer to a GUID to receive the ID of this file data node.</span></span> <span data-ttu-id="ca6ef-110">Se l'oggetto non dispone di un ID, il valore del parametro restituito sarà GUID \_ null.</span><span class="sxs-lookup"><span data-stu-id="ca6ef-110">If the object has no ID, the returned parameter value will be GUID\_NULL.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ca6ef-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="ca6ef-111">Return value</span></span>

<span data-ttu-id="ca6ef-112">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="ca6ef-112">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="ca6ef-113">Se il metodo ha esito positivo, il valore restituito è \_ OK.</span><span class="sxs-lookup"><span data-stu-id="ca6ef-113">If the method succeeds, the return value is S\_OK.</span></span> <span data-ttu-id="ca6ef-114">Se il metodo ha esito negativo, verrà restituito il valore seguente: D3DXFERR \_ BADVALUE.</span><span class="sxs-lookup"><span data-stu-id="ca6ef-114">If the method fails, the following value will be returned: D3DXFERR\_BADVALUE.</span></span>

## <a name="requirements"></a><span data-ttu-id="ca6ef-115">Requisiti</span><span class="sxs-lookup"><span data-stu-id="ca6ef-115">Requirements</span></span>



| <span data-ttu-id="ca6ef-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="ca6ef-116">Requirement</span></span> | <span data-ttu-id="ca6ef-117">Valore</span><span class="sxs-lookup"><span data-stu-id="ca6ef-117">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="ca6ef-118">Intestazione</span><span class="sxs-lookup"><span data-stu-id="ca6ef-118">Header</span></span><br/>  | <dl> <span data-ttu-id="ca6ef-119"><dt>D3DX9Xof. h</dt></span><span class="sxs-lookup"><span data-stu-id="ca6ef-119"><dt>D3DX9Xof.h</dt></span></span> </dl> |
| <span data-ttu-id="ca6ef-120">Libreria</span><span class="sxs-lookup"><span data-stu-id="ca6ef-120">Library</span></span><br/> | <dl> <span data-ttu-id="ca6ef-121"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="ca6ef-121"><dt>D3dx9.lib</dt></span></span> </dl>  |



## <a name="see-also"></a><span data-ttu-id="ca6ef-122">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="ca6ef-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ca6ef-123">ID3DXFileSaveData</span><span class="sxs-lookup"><span data-stu-id="ca6ef-123">ID3DXFileSaveData</span></span>](id3dxfilesavedata.md)
</dt> </dl>

 

 




