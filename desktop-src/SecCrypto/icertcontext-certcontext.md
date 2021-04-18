---
description: Imposta o Recupera il \_ contesto PCCERT di un certificato.
ms.assetid: aedd219d-43fa-4722-9af4-36172d2c18b0
title: 'Proprietà ICertContext:: CertContext'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ICertContext.CertContext
- ICertContext.get_CertContext
- ICertContext.put_CertContext
- CertContext.CertContext
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 38bd1c704ca709fc1e4b6072bb68c2105dc5db9c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106329343"
---
# <a name="icertcontextcertcontext-property"></a><span data-ttu-id="22389-103">Proprietà ICertContext:: CertContext</span><span class="sxs-lookup"><span data-stu-id="22389-103">ICertContext::CertContext property</span></span>

<span data-ttu-id="22389-104">\[CAPICOM è un componente solo a 32 bit disponibile per l'uso nei sistemi operativi seguenti: Windows Server 2008, Windows Vista e Windows XP.\]</span><span class="sxs-lookup"><span data-stu-id="22389-104">\[CAPICOM is a 32-bit only component that is available for use in the following operating systems: Windows Server 2008, Windows Vista, and Windows XP.\]</span></span>

<span data-ttu-id="22389-105">La proprietà **CertContext** imposta o Recupera il \_ contesto PCCERT di un certificato.</span><span class="sxs-lookup"><span data-stu-id="22389-105">The **CertContext** property sets or retrieves the PCCERT\_CONTEXT of a certificate.</span></span>

<span data-ttu-id="22389-106">Si tratta di una proprietà di lettura/scrittura.</span><span class="sxs-lookup"><span data-stu-id="22389-106">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="22389-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="22389-107">Syntax</span></span>


```VB
CertContext.CertContext As Long
```



## <a name="property-value"></a><span data-ttu-id="22389-108">Valore proprietà</span><span class="sxs-lookup"><span data-stu-id="22389-108">Property value</span></span>

<span data-ttu-id="22389-109">Contesto PCCERT \_ del certificato.</span><span class="sxs-lookup"><span data-stu-id="22389-109">The PCCERT\_CONTEXT of the certificate.</span></span>

## <a name="error-codes"></a><span data-ttu-id="22389-110">Codici di errore</span><span class="sxs-lookup"><span data-stu-id="22389-110">Error codes</span></span>

<span data-ttu-id="22389-111">Se i metodi di accesso alle proprietà **inseriscono \_ CertContext** e **get \_ CertContext** ha esito positivo, restituiscono S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="22389-111">If the property access methods **put\_CertContext** and **get\_CertContext** succeed, they return S\_OK.</span></span>

<span data-ttu-id="22389-112">Qualsiasi altro valore **HRESULT** indica che la chiamata non è riuscita.</span><span class="sxs-lookup"><span data-stu-id="22389-112">Any other **HRESULT** value indicates that the call failed.</span></span>

## <a name="remarks"></a><span data-ttu-id="22389-113">Commenti</span><span class="sxs-lookup"><span data-stu-id="22389-113">Remarks</span></span>

<span data-ttu-id="22389-114">Per liberare il contesto, è necessario chiamare il metodo [**FreeContext**](icertcontext-freecontext.md) o la funzione [**CertFreeCertificateContext**](/windows/desktop/api/Wincrypt/nf-wincrypt-certfreecertificatecontext) .</span><span class="sxs-lookup"><span data-stu-id="22389-114">You must call either the [**FreeContext**](icertcontext-freecontext.md) method or the [**CertFreeCertificateContext**](/windows/desktop/api/Wincrypt/nf-wincrypt-certfreecertificatecontext) function to free the context.</span></span>

<span data-ttu-id="22389-115">Se si imposta la proprietà **CertContext** , lo stato dell'intero oggetto [**certificato**](certificate.md) viene reimpostato.</span><span class="sxs-lookup"><span data-stu-id="22389-115">If you set the **CertContext** property, the state of the entire [**Certificate**](certificate.md) object is reset.</span></span>

## <a name="requirements"></a><span data-ttu-id="22389-116">Requisiti</span><span class="sxs-lookup"><span data-stu-id="22389-116">Requirements</span></span>



| <span data-ttu-id="22389-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="22389-117">Requirement</span></span> | <span data-ttu-id="22389-118">Valore</span><span class="sxs-lookup"><span data-stu-id="22389-118">Value</span></span> |
|----------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="22389-119">Componente ridistribuibile</span><span class="sxs-lookup"><span data-stu-id="22389-119">Redistributable</span></span><br/> | <span data-ttu-id="22389-120">CAPICOM 2,0 o versioni successive in Windows Server 2003 e Windows XP</span><span class="sxs-lookup"><span data-stu-id="22389-120">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="22389-121">DLL</span><span class="sxs-lookup"><span data-stu-id="22389-121">DLL</span></span><br/>             | <dl> <span data-ttu-id="22389-122"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="22389-122"><dt>Capicom.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="22389-123">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="22389-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="22389-124">**ICertContext**</span><span class="sxs-lookup"><span data-stu-id="22389-124">**ICertContext**</span></span>](icertcontext.md)
</dt> </dl>

 

 




