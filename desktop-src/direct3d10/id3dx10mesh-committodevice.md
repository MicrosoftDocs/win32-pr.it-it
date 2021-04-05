---
description: Eseguire il commit di tutte le modifiche apportate a una mesh al dispositivo, in modo che sia possibile eseguire il rendering delle modifiche. Questa operazione deve essere chiamata dopo che i dati di una mesh vengono modificati e prima che ne venga eseguito il rendering. Non è possibile eseguire il rendering di una mesh a meno che non ne venga eseguito il commit nel dispositivo. Vedere la sezione Osservazioni.
ms.assetid: 26927553-d1d8-4745-85ad-a8a6fe949306
title: 'Metodo ID3DX10Mesh:: CommitToDevice (D3DX10. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DX10Mesh.CommitToDevice
api_type:
- COM
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 160f97a3a00ddc7bbf69989991b2794ab3d6e5e8
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "104058616"
---
# <a name="id3dx10meshcommittodevice-method"></a><span data-ttu-id="e5ab1-106">Metodo ID3DX10Mesh:: CommitToDevice</span><span class="sxs-lookup"><span data-stu-id="e5ab1-106">ID3DX10Mesh::CommitToDevice method</span></span>

<span data-ttu-id="e5ab1-107">Eseguire il commit di tutte le modifiche apportate a una mesh al dispositivo, in modo che sia possibile eseguire il rendering delle modifiche.</span><span class="sxs-lookup"><span data-stu-id="e5ab1-107">Commit any changes made to a mesh to the device so that the changes can be rendered.</span></span> <span data-ttu-id="e5ab1-108">Questa operazione deve essere chiamata dopo che i dati di una mesh vengono modificati e prima che ne venga eseguito il rendering.</span><span class="sxs-lookup"><span data-stu-id="e5ab1-108">This should be called after a mesh's data is altered and before it is rendered.</span></span> <span data-ttu-id="e5ab1-109">Non è possibile eseguire il rendering di una mesh a meno che non ne venga eseguito il commit nel dispositivo.</span><span class="sxs-lookup"><span data-stu-id="e5ab1-109">A mesh cannot be rendered unless it is committed to the device.</span></span> <span data-ttu-id="e5ab1-110">Vedere la sezione Osservazioni.</span><span class="sxs-lookup"><span data-stu-id="e5ab1-110">See remarks.</span></span>

## <a name="syntax"></a><span data-ttu-id="e5ab1-111">Sintassi</span><span class="sxs-lookup"><span data-stu-id="e5ab1-111">Syntax</span></span>


```C++
HRESULT CommitToDevice();
```



## <a name="parameters"></a><span data-ttu-id="e5ab1-112">Parametri</span><span class="sxs-lookup"><span data-stu-id="e5ab1-112">Parameters</span></span>

<span data-ttu-id="e5ab1-113">Questo metodo non presenta parametri.</span><span class="sxs-lookup"><span data-stu-id="e5ab1-113">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="e5ab1-114">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="e5ab1-114">Return value</span></span>

<span data-ttu-id="e5ab1-115">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="e5ab1-115">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="e5ab1-116">Il valore restituito è uno dei valori elencati in [codici restituiti Direct3D 10](d3d10-graphics-reference-returnvalues.md).</span><span class="sxs-lookup"><span data-stu-id="e5ab1-116">The return value is one of the values listed in [Direct3D 10 Return Codes](d3d10-graphics-reference-returnvalues.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="e5ab1-117">Commenti</span><span class="sxs-lookup"><span data-stu-id="e5ab1-117">Remarks</span></span>

<span data-ttu-id="e5ab1-118">Quando viene caricata una mesh, i dati vengono caricati nelle risorse di staging, ovvero i dati possono essere modificati ma non sottoposti a rendering.</span><span class="sxs-lookup"><span data-stu-id="e5ab1-118">When a mesh is loaded, it's data is loaded into staging resources, meaning the data can be altered but not rendered.</span></span> <span data-ttu-id="e5ab1-119">Quando viene chiamato CommitToDevice, i dati delle risorse di gestione temporanea vengono copiati nelle risorse del dispositivo in modo che possano essere sottoposti a rendering.</span><span class="sxs-lookup"><span data-stu-id="e5ab1-119">When CommitToDevice is called, the data from the staging resources are copied into device resources so that they can be rendered.</span></span> <span data-ttu-id="e5ab1-120">Sebbene i dati vengano sottoposte a commit nel dispositivo, le risorse di gestione temporanea rimangono e possono essere modificate.</span><span class="sxs-lookup"><span data-stu-id="e5ab1-120">Although the data is committed to the device, the staging resources remain and can be modified.</span></span> <span data-ttu-id="e5ab1-121">Se vengono apportate modifiche alle risorse di gestione temporanea, è necessario eseguire di nuovo il commit delle risorse di gestione temporanea sul dispositivo per poter eseguire il rendering delle modifiche sullo schermo.</span><span class="sxs-lookup"><span data-stu-id="e5ab1-121">If any modifications are made to the staging resources, the staging resources must be committed to the device again in order for those changes to be rendered on screen.</span></span>

## <a name="requirements"></a><span data-ttu-id="e5ab1-122">Requisiti</span><span class="sxs-lookup"><span data-stu-id="e5ab1-122">Requirements</span></span>



| <span data-ttu-id="e5ab1-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="e5ab1-123">Requirement</span></span> | <span data-ttu-id="e5ab1-124">Valore</span><span class="sxs-lookup"><span data-stu-id="e5ab1-124">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="e5ab1-125">Intestazione</span><span class="sxs-lookup"><span data-stu-id="e5ab1-125">Header</span></span><br/>  | <dl> <span data-ttu-id="e5ab1-126"><dt>D3DX10. h</dt></span><span class="sxs-lookup"><span data-stu-id="e5ab1-126"><dt>D3DX10.h</dt></span></span> </dl>   |
| <span data-ttu-id="e5ab1-127">Libreria</span><span class="sxs-lookup"><span data-stu-id="e5ab1-127">Library</span></span><br/> | <dl> <span data-ttu-id="e5ab1-128"><dt>D3DX10. lib</dt></span><span class="sxs-lookup"><span data-stu-id="e5ab1-128"><dt>D3DX10.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e5ab1-129">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="e5ab1-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e5ab1-130">ID3DX10Mesh</span><span class="sxs-lookup"><span data-stu-id="e5ab1-130">ID3DX10Mesh</span></span>](id3dx10mesh.md)
</dt> <dt>

[<span data-ttu-id="e5ab1-131">Interfacce D3DX</span><span class="sxs-lookup"><span data-stu-id="e5ab1-131">D3DX Interfaces</span></span>](d3d10-graphics-reference-d3dx10-interfaces.md)
</dt> </dl>

 

 




