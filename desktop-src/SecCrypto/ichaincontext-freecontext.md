---
description: Rilascia un \_ \_ contesto della catena PCCERT acquisito tramite la proprietà chainContext.
ms.assetid: fa9a6171-58ff-400f-bdcc-ba32a0ae0441
title: 'Metodo IChainContext:: FreeContext'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IChainContext.FreeContext
- ChainContext.FreeContext
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 413b119f250bfbd061301391fee7741362979f65
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106329223"
---
# <a name="ichaincontextfreecontext-method"></a><span data-ttu-id="1e4a9-103">Metodo IChainContext:: FreeContext</span><span class="sxs-lookup"><span data-stu-id="1e4a9-103">IChainContext::FreeContext method</span></span>

<span data-ttu-id="1e4a9-104">\[CAPICOM è un componente solo a 32 bit disponibile per l'uso nei sistemi operativi seguenti: Windows Server 2008, Windows Vista e Windows XP.\]</span><span class="sxs-lookup"><span data-stu-id="1e4a9-104">\[CAPICOM is a 32-bit only component that is available for use in the following operating systems: Windows Server 2008, Windows Vista, and Windows XP.\]</span></span>

<span data-ttu-id="1e4a9-105">Il metodo **FreeContext** rilascia un \_ contesto della catena PCCERT \_ acquisito tramite la proprietà [**chainContext**](ichaincontext-chaincontext.md) .</span><span class="sxs-lookup"><span data-stu-id="1e4a9-105">The **FreeContext** method releases a PCCERT\_CHAIN\_CONTEXT acquired through the [**ChainContext**](ichaincontext-chaincontext.md) property.</span></span>

## <a name="syntax"></a><span data-ttu-id="1e4a9-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="1e4a9-106">Syntax</span></span>


```VB
ChainContext.FreeContext()
```



## <a name="parameters"></a><span data-ttu-id="1e4a9-107">Parametri</span><span class="sxs-lookup"><span data-stu-id="1e4a9-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1e4a9-108">*pChainContext* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="1e4a9-108">*pChainContext* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1e4a9-109">Contesto della \_ catena PCCERT \_ da rilasciare.</span><span class="sxs-lookup"><span data-stu-id="1e4a9-109">The PCCERT\_CHAIN\_CONTEXT to be released.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1e4a9-110">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="1e4a9-110">Return value</span></span>

<span data-ttu-id="1e4a9-111">Il valore restituito è un valore **HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="1e4a9-111">The return value is an **HRESULT**.</span></span> <span data-ttu-id="1e4a9-112">Un valore di S \_ OK indica l'esito positivo.</span><span class="sxs-lookup"><span data-stu-id="1e4a9-112">A value of S\_OK indicates success.</span></span> <span data-ttu-id="1e4a9-113">Qualsiasi altro valore indica che l'operazione non è riuscita.</span><span class="sxs-lookup"><span data-stu-id="1e4a9-113">Any other value indicates that the operation failed.</span></span>

## <a name="remarks"></a><span data-ttu-id="1e4a9-114">Commenti</span><span class="sxs-lookup"><span data-stu-id="1e4a9-114">Remarks</span></span>

<span data-ttu-id="1e4a9-115">Questo metodo non rilascia il contesto della \_ catena PCCERT \_ contenuto all'interno di un oggetto [**Chain**](chain.md) .</span><span class="sxs-lookup"><span data-stu-id="1e4a9-115">This method does not release the PCCERT\_CHAIN\_CONTEXT contained within a [**Chain**](chain.md) object.</span></span> <span data-ttu-id="1e4a9-116">Deve essere usato solo per rilasciare un \_ \_ contesto della catena PCCERT acquisito tramite la proprietà [**chainContext**](ichaincontext-chaincontext.md) .</span><span class="sxs-lookup"><span data-stu-id="1e4a9-116">It should be used only to release a PCCERT\_CHAIN\_CONTEXT acquired through the [**ChainContext**](ichaincontext-chaincontext.md) property.</span></span>

## <a name="requirements"></a><span data-ttu-id="1e4a9-117">Requisiti</span><span class="sxs-lookup"><span data-stu-id="1e4a9-117">Requirements</span></span>



| <span data-ttu-id="1e4a9-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="1e4a9-118">Requirement</span></span> | <span data-ttu-id="1e4a9-119">Valore</span><span class="sxs-lookup"><span data-stu-id="1e4a9-119">Value</span></span> |
|----------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="1e4a9-120">Componente ridistribuibile</span><span class="sxs-lookup"><span data-stu-id="1e4a9-120">Redistributable</span></span><br/> | <span data-ttu-id="1e4a9-121">CAPICOM 2,0 o versioni successive in Windows Server 2003 e Windows XP</span><span class="sxs-lookup"><span data-stu-id="1e4a9-121">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="1e4a9-122">DLL</span><span class="sxs-lookup"><span data-stu-id="1e4a9-122">DLL</span></span><br/>             | <dl> <span data-ttu-id="1e4a9-123"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="1e4a9-123"><dt>Capicom.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1e4a9-124">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="1e4a9-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1e4a9-125">**IChainContext**</span><span class="sxs-lookup"><span data-stu-id="1e4a9-125">**IChainContext**</span></span>](ichaincontext.md)
</dt> </dl>

 

 




