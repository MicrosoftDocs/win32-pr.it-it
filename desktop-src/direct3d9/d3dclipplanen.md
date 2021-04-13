---
description: Definisce gli schemi di bit che abilitano i piani di ritaglio definiti dall'utente. Queste macro sono definite come praticità quando si impostano i valori per lo \_ stato di rendering CLIPPLANEENABLE di D3DRS.
ms.assetid: 5bca2401-a3fb-4b1c-bb59-621b15da10f1
title: Macro D3DCLIPPLANEn (D3D9Types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DCLIPPLANEn
api_type:
- HeaderDef
api_location:
- D3D9Types.h
ms.openlocfilehash: 4508f1654a357eb80b3847b7562e230c6a9be4d0
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "104401942"
---
# <a name="d3dclipplanen-macro"></a><span data-ttu-id="f2ef2-104">D3DCLIPPLANEn (macro)</span><span class="sxs-lookup"><span data-stu-id="f2ef2-104">D3DCLIPPLANEn macro</span></span>

<span data-ttu-id="f2ef2-105">Definisce gli schemi di bit che abilitano i piani di ritaglio definiti dall'utente.</span><span class="sxs-lookup"><span data-stu-id="f2ef2-105">Defines bit patterns that enable user-defined clipping planes.</span></span> <span data-ttu-id="f2ef2-106">Queste macro sono definite come praticità quando si impostano i valori per lo \_ stato di rendering CLIPPLANEENABLE di D3DRS.</span><span class="sxs-lookup"><span data-stu-id="f2ef2-106">These macros are defined as a convenience when setting values for the D3DRS\_CLIPPLANEENABLE render state.</span></span>

## <a name="syntax"></a><span data-ttu-id="f2ef2-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="f2ef2-107">Syntax</span></span>


```C++
void D3DCLIPPLANEn(void);
```



## <a name="parameters"></a><span data-ttu-id="f2ef2-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="f2ef2-108">Parameters</span></span>

<span data-ttu-id="f2ef2-109">Questa macro non contiene parametri.</span><span class="sxs-lookup"><span data-stu-id="f2ef2-109">This macro has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="f2ef2-110">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="f2ef2-110">Return value</span></span>

<span data-ttu-id="f2ef2-111">Questa macro non restituisce un valore.</span><span class="sxs-lookup"><span data-stu-id="f2ef2-111">This macro does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="f2ef2-112">Commenti</span><span class="sxs-lookup"><span data-stu-id="f2ef2-112">Remarks</span></span>

<span data-ttu-id="f2ef2-113">I piani di ritaglio definiti dall'utente sono abilitati quando il valore impostato nello \_ stato di rendering CLIPPLANEENABLE di D3DRS contiene uno o più bit impostati, ovvero non è 0.</span><span class="sxs-lookup"><span data-stu-id="f2ef2-113">User-defined clipping planes are enabled when the value set in the D3DRS\_CLIPPLANEENABLE render state contains one or more set bits (that is, is not 0).</span></span> <span data-ttu-id="f2ef2-114">Il valore dello stato di rendering non è importante; il sistema non interpreta il valore come numero.</span><span class="sxs-lookup"><span data-stu-id="f2ef2-114">The value of the render-state is not important; the system does not interpret the value as a number.</span></span> <span data-ttu-id="f2ef2-115">Il valore Abilita invece il piano di ritaglio il cui bit corrispondente è impostato.</span><span class="sxs-lookup"><span data-stu-id="f2ef2-115">Rather, the value enables the clipping plane whose corresponding bit is set.</span></span> <span data-ttu-id="f2ef2-116">Il bit 0 controlla lo stato del primo piano di ritaglio (in corrispondenza dell'indice 0), il bit 1 il secondo piano e così via.</span><span class="sxs-lookup"><span data-stu-id="f2ef2-116">Bit 0 controls the state of the first clipping plane (at index 0), bit 1 the second plane, and so on.</span></span>

<span data-ttu-id="f2ef2-117">Gli schemi di bit creati da queste macro possono essere combinati utilizzando un'operazione OR logica per abilitare simultaneamente più piani di ritaglio.</span><span class="sxs-lookup"><span data-stu-id="f2ef2-117">The bit patterns that these macros create can be combined by using a logical OR operation to simultaneously enable multiple clipping planes.</span></span> <span data-ttu-id="f2ef2-118">Se si omette una di queste macro dalla combinazione, il piano di ritaglio viene disabilitato in corrispondenza di tale indice.</span><span class="sxs-lookup"><span data-stu-id="f2ef2-118">Omitting one of these macros from the combination effectively disables the clipping plane at that index.</span></span>

## <a name="requirements"></a><span data-ttu-id="f2ef2-119">Requisiti</span><span class="sxs-lookup"><span data-stu-id="f2ef2-119">Requirements</span></span>



| <span data-ttu-id="f2ef2-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="f2ef2-120">Requirement</span></span> | <span data-ttu-id="f2ef2-121">Valore</span><span class="sxs-lookup"><span data-stu-id="f2ef2-121">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="f2ef2-122">Intestazione</span><span class="sxs-lookup"><span data-stu-id="f2ef2-122">Header</span></span><br/> | <dl> <span data-ttu-id="f2ef2-123"><dt>D3D9Types. h</dt></span><span class="sxs-lookup"><span data-stu-id="f2ef2-123"><dt>D3D9Types.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f2ef2-124">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="f2ef2-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f2ef2-125">Macro</span><span class="sxs-lookup"><span data-stu-id="f2ef2-125">Macros</span></span>](dx9-graphics-reference-d3d-macros.md)
</dt> </dl>

 

 




