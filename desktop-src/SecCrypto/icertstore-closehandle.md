---
description: Chiude un handle HCERTSTORE acquisito tramite la proprietà StoreHandle.
ms.assetid: 1b0d3d9b-09e0-4035-88ac-2887b3ab60c9
title: 'Metodo ICertStore:: CloseHandle'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ICertStore.CloseHandle
- CertStore.CloseHandle
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: bb1e9ab032b76b8ef02de786d1fc39af0b0d54b4
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106333972"
---
# <a name="icertstoreclosehandle-method"></a><span data-ttu-id="186be-103">Metodo ICertStore:: CloseHandle</span><span class="sxs-lookup"><span data-stu-id="186be-103">ICertStore::CloseHandle method</span></span>

<span data-ttu-id="186be-104">\[CAPICOM è un componente solo a 32 bit disponibile per l'uso nei sistemi operativi seguenti: Windows Server 2008, Windows Vista e Windows XP.\]</span><span class="sxs-lookup"><span data-stu-id="186be-104">\[CAPICOM is a 32-bit only component that is available for use in the following operating systems: Windows Server 2008, Windows Vista, and Windows XP.\]</span></span>

<span data-ttu-id="186be-105">Il metodo **CloseHandle** chiude un handle HCERTSTORE acquisito tramite la proprietà [**storeHandle**](icertstore-storehandle.md) .</span><span class="sxs-lookup"><span data-stu-id="186be-105">The **CloseHandle** method closes an HCERTSTORE handle acquired through the [**StoreHandle**](icertstore-storehandle.md) property.</span></span>

## <a name="syntax"></a><span data-ttu-id="186be-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="186be-106">Syntax</span></span>


```VB
CertStore.CloseHandle( _
  ByVal hCertStore _
)
```



## <a name="parameters"></a><span data-ttu-id="186be-107">Parametri</span><span class="sxs-lookup"><span data-stu-id="186be-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="186be-108">*hCertStore* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="186be-108">*hCertStore* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="186be-109">Handle HCERTSTORE da chiudere.</span><span class="sxs-lookup"><span data-stu-id="186be-109">The HCERTSTORE handle to be closed.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="186be-110">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="186be-110">Return value</span></span>

<span data-ttu-id="186be-111">Il valore restituito è un valore **HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="186be-111">The return value is an **HRESULT**.</span></span> <span data-ttu-id="186be-112">Un valore di **S \_ OK** indica l'esito positivo.</span><span class="sxs-lookup"><span data-stu-id="186be-112">A value of **S\_OK** indicates success.</span></span> <span data-ttu-id="186be-113">Qualsiasi altro valore indica che l'operazione non è riuscita.</span><span class="sxs-lookup"><span data-stu-id="186be-113">Any other value indicates that the operation failed.</span></span>

## <a name="remarks"></a><span data-ttu-id="186be-114">Commenti</span><span class="sxs-lookup"><span data-stu-id="186be-114">Remarks</span></span>

<span data-ttu-id="186be-115">Questo metodo non rilascia l'handle HCERTSTORE contenuto in un oggetto [**Store**](store.md) .</span><span class="sxs-lookup"><span data-stu-id="186be-115">This method does not release the HCERTSTORE handle contained within a [**Store**](store.md) object.</span></span> <span data-ttu-id="186be-116">Deve essere usato solo per rilasciare un handle HCERTSTORE acquisito tramite la proprietà [**storeHandle**](icertstore-storehandle.md) .</span><span class="sxs-lookup"><span data-stu-id="186be-116">It should be used only to release a HCERTSTORE handle acquired through the [**StoreHandle**](icertstore-storehandle.md) property.</span></span>

## <a name="requirements"></a><span data-ttu-id="186be-117">Requisiti</span><span class="sxs-lookup"><span data-stu-id="186be-117">Requirements</span></span>



| <span data-ttu-id="186be-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="186be-118">Requirement</span></span> | <span data-ttu-id="186be-119">Valore</span><span class="sxs-lookup"><span data-stu-id="186be-119">Value</span></span> |
|----------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="186be-120">Componente ridistribuibile</span><span class="sxs-lookup"><span data-stu-id="186be-120">Redistributable</span></span><br/> | <span data-ttu-id="186be-121">CAPICOM 2,0 o versioni successive in Windows Server 2003 e Windows XP</span><span class="sxs-lookup"><span data-stu-id="186be-121">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="186be-122">DLL</span><span class="sxs-lookup"><span data-stu-id="186be-122">DLL</span></span><br/>             | <dl> <span data-ttu-id="186be-123"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="186be-123"><dt>Capicom.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="186be-124">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="186be-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="186be-125">**ICertStore**</span><span class="sxs-lookup"><span data-stu-id="186be-125">**ICertStore**</span></span>](icertstore.md)
</dt> </dl>

 

 




