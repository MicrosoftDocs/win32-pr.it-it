---
description: Recuperare le caratteristiche dei tipi di carattere.
ms.assetid: ef7e0d18-492b-476b-945a-bfc0232a939a
title: 'Metodo ID3DX10Font:: GetTextMetrics (D3DX10. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DX10Font.GetTextMetrics
api_type:
- COM
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 72decdcf0a9573f7ad8ba0f4e363df6df3599477
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "104530937"
---
# <a name="id3dx10fontgettextmetrics-method"></a><span data-ttu-id="29c07-103">Metodo ID3DX10Font:: GetTextMetrics</span><span class="sxs-lookup"><span data-stu-id="29c07-103">ID3DX10Font::GetTextMetrics method</span></span>

<span data-ttu-id="29c07-104">Recuperare le caratteristiche dei tipi di carattere.</span><span class="sxs-lookup"><span data-stu-id="29c07-104">Retrieve font characteristics.</span></span>

## <a name="syntax"></a><span data-ttu-id="29c07-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="29c07-105">Syntax</span></span>


```C++
BOOL GetTextMetrics(
  [in] TEXTMETRIC *pTextMetrics
);
```



## <a name="parameters"></a><span data-ttu-id="29c07-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="29c07-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="29c07-107">*pTextMetrics* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="29c07-107">*pTextMetrics* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="29c07-108">Tipo: **TEXTMETRIC \***</span><span class="sxs-lookup"><span data-stu-id="29c07-108">Type: **TEXTMETRIC\***</span></span>

<span data-ttu-id="29c07-109">Puntatore a una struttura [TEXTMETRIC](/previous-versions//ms534202(v=vs.85)) che contiene le proprietà del tipo di carattere.</span><span class="sxs-lookup"><span data-stu-id="29c07-109">Pointer to a [TEXTMETRIC](/previous-versions//ms534202(v=vs.85)) structure, which contains font properties.</span></span> <span data-ttu-id="29c07-110">Se è definito Unicode, la funzione restituisce una struttura Campo TEXTMETRICW.</span><span class="sxs-lookup"><span data-stu-id="29c07-110">If Unicode is defined, the function returns a TEXTMETRICW structure.</span></span> <span data-ttu-id="29c07-111">In caso contrario, la funzione restituisce una struttura TEXTMETRICA.</span><span class="sxs-lookup"><span data-stu-id="29c07-111">Otherwise, the function returns a TEXTMETRICA structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="29c07-112">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="29c07-112">Return value</span></span>

<span data-ttu-id="29c07-113">Tipo: **[ **bool**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="29c07-113">Type: **[**BOOL**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="29c07-114">Diverso da zero se la funzione ha esito positivo; in caso contrario, 0.</span><span class="sxs-lookup"><span data-stu-id="29c07-114">Nonzero if the function is successful; otherwise 0.</span></span>

## <a name="requirements"></a><span data-ttu-id="29c07-115">Requisiti</span><span class="sxs-lookup"><span data-stu-id="29c07-115">Requirements</span></span>



| <span data-ttu-id="29c07-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="29c07-116">Requirement</span></span> | <span data-ttu-id="29c07-117">Valore</span><span class="sxs-lookup"><span data-stu-id="29c07-117">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="29c07-118">Intestazione</span><span class="sxs-lookup"><span data-stu-id="29c07-118">Header</span></span><br/>  | <dl> <span data-ttu-id="29c07-119"><dt>D3DX10. h</dt></span><span class="sxs-lookup"><span data-stu-id="29c07-119"><dt>D3DX10.h</dt></span></span> </dl>   |
| <span data-ttu-id="29c07-120">Libreria</span><span class="sxs-lookup"><span data-stu-id="29c07-120">Library</span></span><br/> | <dl> <span data-ttu-id="29c07-121"><dt>D3DX10. lib</dt></span><span class="sxs-lookup"><span data-stu-id="29c07-121"><dt>D3DX10.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="29c07-122">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="29c07-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="29c07-123">ID3DX10Font</span><span class="sxs-lookup"><span data-stu-id="29c07-123">ID3DX10Font</span></span>](id3dx10font.md)
</dt> <dt>

[<span data-ttu-id="29c07-124">Interfacce D3DX</span><span class="sxs-lookup"><span data-stu-id="29c07-124">D3DX Interfaces</span></span>](d3d10-graphics-reference-d3dx10-interfaces.md)
</dt> </dl>

 

 
