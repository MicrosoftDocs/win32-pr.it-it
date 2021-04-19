---
description: Imposta o Recupera il \_ \_ contesto della catena PCCERT di un certificato.
ms.assetid: 1b33ecd5-88c9-4654-9d2d-95a0be4283c6
title: 'Proprietà IChainContext:: ChainContext'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IChainContext.ChainContext
- IChainContext.get_ChainContext
- IChainContext.put_ChainContext
- ChainContext.ChainContext
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 36b2f6f5811c844e4e43544f5b56b8de66cb3bf7
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106324764"
---
# <a name="ichaincontextchaincontext-property"></a><span data-ttu-id="74cb7-103">Proprietà IChainContext:: ChainContext</span><span class="sxs-lookup"><span data-stu-id="74cb7-103">IChainContext::ChainContext property</span></span>

<span data-ttu-id="74cb7-104">\[CAPICOM è un componente solo a 32 bit disponibile per l'uso nei sistemi operativi seguenti: Windows Server 2008, Windows Vista e Windows XP.\]</span><span class="sxs-lookup"><span data-stu-id="74cb7-104">\[CAPICOM is a 32-bit only component that is available for use in the following operating systems: Windows Server 2008, Windows Vista, and Windows XP.\]</span></span>

<span data-ttu-id="74cb7-105">La proprietà **chainContext** imposta o Recupera il \_ contesto della catena PCCERT \_ di un certificato.</span><span class="sxs-lookup"><span data-stu-id="74cb7-105">The **ChainContext** property sets or retrieves the PCCERT\_CHAIN\_CONTEXT of a certificate.</span></span>

<span data-ttu-id="74cb7-106">Si tratta di una proprietà di lettura/scrittura.</span><span class="sxs-lookup"><span data-stu-id="74cb7-106">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="74cb7-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="74cb7-107">Syntax</span></span>


```VB
' Data type: Long

ChainContext.ChainContext As Long
```



## <a name="property-value"></a><span data-ttu-id="74cb7-108">Valore proprietà</span><span class="sxs-lookup"><span data-stu-id="74cb7-108">Property value</span></span>

<span data-ttu-id="74cb7-109">\_ \_ Contesto della catena PCCERT del certificato.</span><span class="sxs-lookup"><span data-stu-id="74cb7-109">The PCCERT\_CHAIN\_CONTEXT of the certificate.</span></span>

## <a name="error-codes"></a><span data-ttu-id="74cb7-110">Codici di errore</span><span class="sxs-lookup"><span data-stu-id="74cb7-110">Error codes</span></span>

<span data-ttu-id="74cb7-111">Se i metodi di accesso alle proprietà **inseriscono \_ chainContext** e **get \_ chainContext** ha esito positivo, restituiscono S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="74cb7-111">If the property access methods **put\_ChainContext** and **get\_ChainContext** succeed, they return S\_OK.</span></span>

<span data-ttu-id="74cb7-112">Qualsiasi altro valore **HRESULT** indica che la chiamata non è riuscita.</span><span class="sxs-lookup"><span data-stu-id="74cb7-112">Any other **HRESULT** value indicates that the call failed.</span></span>

## <a name="remarks"></a><span data-ttu-id="74cb7-113">Commenti</span><span class="sxs-lookup"><span data-stu-id="74cb7-113">Remarks</span></span>

<span data-ttu-id="74cb7-114">Per liberare il contesto, è necessario chiamare il metodo [**FreeContext**](ichaincontext-freecontext.md) o la funzione [**CertFreeCertificateChain**](/windows/desktop/api/Wincrypt/nf-wincrypt-certfreecertificatechain) .</span><span class="sxs-lookup"><span data-stu-id="74cb7-114">You must call either the [**FreeContext**](ichaincontext-freecontext.md) method or the [**CertFreeCertificateChain**](/windows/desktop/api/Wincrypt/nf-wincrypt-certfreecertificatechain) function to free the context.</span></span>

<span data-ttu-id="74cb7-115">Se si imposta la proprietà **chainContext** , lo stato dell'intero oggetto [**Chain**](chain.md) viene reimpostato.</span><span class="sxs-lookup"><span data-stu-id="74cb7-115">If you set the **ChainContext** property, the state of the entire [**Chain**](chain.md) object is reset.</span></span>

## <a name="requirements"></a><span data-ttu-id="74cb7-116">Requisiti</span><span class="sxs-lookup"><span data-stu-id="74cb7-116">Requirements</span></span>



| <span data-ttu-id="74cb7-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="74cb7-117">Requirement</span></span> | <span data-ttu-id="74cb7-118">Valore</span><span class="sxs-lookup"><span data-stu-id="74cb7-118">Value</span></span> |
|----------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="74cb7-119">Componente ridistribuibile</span><span class="sxs-lookup"><span data-stu-id="74cb7-119">Redistributable</span></span><br/> | <span data-ttu-id="74cb7-120">CAPICOM 2,0 o versioni successive in Windows Server 2003 e Windows XP</span><span class="sxs-lookup"><span data-stu-id="74cb7-120">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="74cb7-121">DLL</span><span class="sxs-lookup"><span data-stu-id="74cb7-121">DLL</span></span><br/>             | <dl> <span data-ttu-id="74cb7-122"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="74cb7-122"><dt>Capicom.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="74cb7-123">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="74cb7-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="74cb7-124">**IChainContext**</span><span class="sxs-lookup"><span data-stu-id="74cb7-124">**IChainContext**</span></span>](ichaincontext.md)
</dt> </dl>

 

 




