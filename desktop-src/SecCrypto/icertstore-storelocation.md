---
description: Imposta o Recupera il \_ percorso dell'archivio CAPICOM \_ di un archivio certificati.
ms.assetid: 2bb76f51-f092-4dbe-93e9-1fdc185c7c50
title: 'Proprietà ICertStore:: StoreLocation'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ICertStore.StoreLocation
- ICertStore.get_StoreLocation
- ICertStore.put_StoreLocation
- CertStore.StoreLocation
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 97bca7ed9dae20c129d202910b40f7c26d54a576
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106328600"
---
# <a name="icertstorestorelocation-property"></a><span data-ttu-id="9fc0d-103">Proprietà ICertStore:: StoreLocation</span><span class="sxs-lookup"><span data-stu-id="9fc0d-103">ICertStore::StoreLocation property</span></span>

<span data-ttu-id="9fc0d-104">\[CAPICOM è un componente solo a 32 bit disponibile per l'uso nei sistemi operativi seguenti: Windows Server 2008, Windows Vista e Windows XP.\]</span><span class="sxs-lookup"><span data-stu-id="9fc0d-104">\[CAPICOM is a 32-bit only component that is available for use in the following operating systems: Windows Server 2008, Windows Vista, and Windows XP.\]</span></span>

<span data-ttu-id="9fc0d-105">La proprietà **StoreLocation** imposta o Recupera il [**\_ \_ percorso dell'archivio CAPICOM**](capicom-store-location.md) di un archivio certificati.</span><span class="sxs-lookup"><span data-stu-id="9fc0d-105">The **StoreLocation** property sets or retrieves the [**CAPICOM\_STORE\_LOCATION**](capicom-store-location.md) of a certificate store.</span></span>

<span data-ttu-id="9fc0d-106">Si tratta di una proprietà di lettura/scrittura.</span><span class="sxs-lookup"><span data-stu-id="9fc0d-106">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="9fc0d-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="9fc0d-107">Syntax</span></span>


```VB
CertStore.StoreLocation As CAPICOM_STORE_LOCATION
```



## <a name="property-value"></a><span data-ttu-id="9fc0d-108">Valore proprietà</span><span class="sxs-lookup"><span data-stu-id="9fc0d-108">Property value</span></span>

<span data-ttu-id="9fc0d-109">Percorso dell'archivio certificati.</span><span class="sxs-lookup"><span data-stu-id="9fc0d-109">The location of the certificate store.</span></span>

## <a name="error-codes"></a><span data-ttu-id="9fc0d-110">Codici di errore</span><span class="sxs-lookup"><span data-stu-id="9fc0d-110">Error codes</span></span>

<span data-ttu-id="9fc0d-111">Se i metodi di accesso alle proprietà **inseriscono \_ StoreLocation** e **get \_ StoreLocation** ha esito positivo, restituiscono S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="9fc0d-111">If the property access methods **put\_StoreLocation** and **get\_StoreLocation** succeed, they return S\_OK.</span></span>

<span data-ttu-id="9fc0d-112">Qualsiasi altro valore **HRESULT** indica che la chiamata non è riuscita.</span><span class="sxs-lookup"><span data-stu-id="9fc0d-112">Any other **HRESULT** value indicates that the call failed.</span></span>

## <a name="requirements"></a><span data-ttu-id="9fc0d-113">Requisiti</span><span class="sxs-lookup"><span data-stu-id="9fc0d-113">Requirements</span></span>



| <span data-ttu-id="9fc0d-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="9fc0d-114">Requirement</span></span> | <span data-ttu-id="9fc0d-115">Valore</span><span class="sxs-lookup"><span data-stu-id="9fc0d-115">Value</span></span> |
|----------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="9fc0d-116">Componente ridistribuibile</span><span class="sxs-lookup"><span data-stu-id="9fc0d-116">Redistributable</span></span><br/> | <span data-ttu-id="9fc0d-117">CAPICOM 2,0 o versioni successive in Windows Server 2003 e Windows XP</span><span class="sxs-lookup"><span data-stu-id="9fc0d-117">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="9fc0d-118">DLL</span><span class="sxs-lookup"><span data-stu-id="9fc0d-118">DLL</span></span><br/>             | <dl> <span data-ttu-id="9fc0d-119"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="9fc0d-119"><dt>Capicom.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9fc0d-120">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="9fc0d-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9fc0d-121">**ICertStore**</span><span class="sxs-lookup"><span data-stu-id="9fc0d-121">**ICertStore**</span></span>](icertstore.md)
</dt> </dl>

 

 




