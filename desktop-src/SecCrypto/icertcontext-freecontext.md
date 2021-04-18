---
description: Rilascia un \_ contesto PCCERT acquisito tramite la proprietà CertContext.
ms.assetid: fcb9e885-d26c-4866-a35d-1c940bfe8162
title: 'Metodo ICertContext:: FreeContext'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ICertContext.FreeContext
- CertContext.FreeContext
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: e1f4c216f6e417726e60d5f2e2bd67387a51d352
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106329345"
---
# <a name="icertcontextfreecontext-method"></a><span data-ttu-id="776ae-103">Metodo ICertContext:: FreeContext</span><span class="sxs-lookup"><span data-stu-id="776ae-103">ICertContext::FreeContext method</span></span>

<span data-ttu-id="776ae-104">\[CAPICOM è un componente solo a 32 bit disponibile per l'uso nei sistemi operativi seguenti: Windows Server 2008, Windows Vista e Windows XP.\]</span><span class="sxs-lookup"><span data-stu-id="776ae-104">\[CAPICOM is a 32-bit only component that is available for use in the following operating systems: Windows Server 2008, Windows Vista, and Windows XP.\]</span></span>

<span data-ttu-id="776ae-105">Il metodo **FreeContext** rilascia un \_ contesto PCCERT acquisito tramite la proprietà [**CertContext**](icertcontext-certcontext.md) .</span><span class="sxs-lookup"><span data-stu-id="776ae-105">The **FreeContext** method releases a PCCERT\_CONTEXT acquired through the [**CertContext**](icertcontext-certcontext.md) property.</span></span>

## <a name="syntax"></a><span data-ttu-id="776ae-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="776ae-106">Syntax</span></span>


```VB
CertContext.FreeContext( _
  ByVal pCertContext _
)
```



## <a name="parameters"></a><span data-ttu-id="776ae-107">Parametri</span><span class="sxs-lookup"><span data-stu-id="776ae-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="776ae-108">*pCertContext* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="776ae-108">*pCertContext* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="776ae-109">Contesto PCCERT \_ da rilasciare.</span><span class="sxs-lookup"><span data-stu-id="776ae-109">The PCCERT\_CONTEXT to be released.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="776ae-110">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="776ae-110">Return value</span></span>

<span data-ttu-id="776ae-111">Il valore restituito è un valore **HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="776ae-111">The return value is an **HRESULT**.</span></span> <span data-ttu-id="776ae-112">Un valore di S \_ OK indica l'esito positivo.</span><span class="sxs-lookup"><span data-stu-id="776ae-112">A value of S\_OK indicates success.</span></span> <span data-ttu-id="776ae-113">Qualsiasi altro valore indica che l'operazione non è riuscita.</span><span class="sxs-lookup"><span data-stu-id="776ae-113">Any other value indicates that the operation failed.</span></span>

## <a name="remarks"></a><span data-ttu-id="776ae-114">Commenti</span><span class="sxs-lookup"><span data-stu-id="776ae-114">Remarks</span></span>

<span data-ttu-id="776ae-115">Questo metodo non rilascia il contesto PCCERT \_ contenuto all'interno di un oggetto [**Certificate**](certificate.md) .</span><span class="sxs-lookup"><span data-stu-id="776ae-115">This method does not release the PCCERT\_CONTEXT contained within a [**Certificate**](certificate.md) object.</span></span> <span data-ttu-id="776ae-116">Deve essere usato solo per rilasciare un contesto PCCERT \_ acquisito tramite la proprietà [**CertContext**](icertcontext-certcontext.md) .</span><span class="sxs-lookup"><span data-stu-id="776ae-116">It should be used only to release a PCCERT\_CONTEXT acquired through the [**CertContext**](icertcontext-certcontext.md) property.</span></span>

## <a name="requirements"></a><span data-ttu-id="776ae-117">Requisiti</span><span class="sxs-lookup"><span data-stu-id="776ae-117">Requirements</span></span>



| <span data-ttu-id="776ae-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="776ae-118">Requirement</span></span> | <span data-ttu-id="776ae-119">Valore</span><span class="sxs-lookup"><span data-stu-id="776ae-119">Value</span></span> |
|----------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="776ae-120">Componente ridistribuibile</span><span class="sxs-lookup"><span data-stu-id="776ae-120">Redistributable</span></span><br/> | <span data-ttu-id="776ae-121">CAPICOM 2,0 o versioni successive in Windows Server 2003 e Windows XP</span><span class="sxs-lookup"><span data-stu-id="776ae-121">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="776ae-122">DLL</span><span class="sxs-lookup"><span data-stu-id="776ae-122">DLL</span></span><br/>             | <dl> <span data-ttu-id="776ae-123"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="776ae-123"><dt>Capicom.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="776ae-124">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="776ae-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="776ae-125">**ICertContext**</span><span class="sxs-lookup"><span data-stu-id="776ae-125">**ICertContext**</span></span>](icertcontext.md)
</dt> </dl>

 

 




