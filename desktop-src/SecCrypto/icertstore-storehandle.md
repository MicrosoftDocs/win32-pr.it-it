---
description: Imposta o recupera l'handle HCERTSTORE di un archivio certificati.
ms.assetid: 3ff8b4c7-4a9a-4cc1-b0ea-da442ebce157
title: 'Proprietà ICertStore:: StoreHandle'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ICertStore.StoreHandle
- ICertStore.get_StoreHandle
- ICertStore.put_StoreHandle
- CertStore.StoreHandle
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 86f57159a2fdd444f22593ec66fa99510a5260b1
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106328604"
---
# <a name="icertstorestorehandle-property"></a><span data-ttu-id="f96ac-103">Proprietà ICertStore:: StoreHandle</span><span class="sxs-lookup"><span data-stu-id="f96ac-103">ICertStore::StoreHandle property</span></span>

<span data-ttu-id="f96ac-104">\[CAPICOM è un componente solo a 32 bit disponibile per l'uso nei sistemi operativi seguenti: Windows Server 2008, Windows Vista e Windows XP.\]</span><span class="sxs-lookup"><span data-stu-id="f96ac-104">\[CAPICOM is a 32-bit only component that is available for use in the following operating systems: Windows Server 2008, Windows Vista, and Windows XP.\]</span></span>

<span data-ttu-id="f96ac-105">La proprietà **storeHandle** imposta o recupera l'handle HCERTSTORE di un archivio certificati.</span><span class="sxs-lookup"><span data-stu-id="f96ac-105">The **StoreHandle** property sets or retrieves the HCERTSTORE handle of a certificate store.</span></span>

<span data-ttu-id="f96ac-106">Si tratta di una proprietà di lettura/scrittura.</span><span class="sxs-lookup"><span data-stu-id="f96ac-106">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="f96ac-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="f96ac-107">Syntax</span></span>


```VB
CertStore.StoreHandle As Long
```



## <a name="property-value"></a><span data-ttu-id="f96ac-108">Valore proprietà</span><span class="sxs-lookup"><span data-stu-id="f96ac-108">Property value</span></span>

<span data-ttu-id="f96ac-109">Handle HCERTSTORE dell'archivio certificati.</span><span class="sxs-lookup"><span data-stu-id="f96ac-109">The HCERTSTORE handle of the certificate store.</span></span>

## <a name="error-codes"></a><span data-ttu-id="f96ac-110">Codici di errore</span><span class="sxs-lookup"><span data-stu-id="f96ac-110">Error codes</span></span>

<span data-ttu-id="f96ac-111">Se i metodi di accesso alle proprietà **inseriscono \_ storeHandle** e **get \_ storeHandle** ha esito positivo, restituiscono S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="f96ac-111">If the property access methods **put\_StoreHandle** and **get\_StoreHandle** succeed, they return S\_OK.</span></span>

<span data-ttu-id="f96ac-112">Qualsiasi altro valore **HRESULT** indica che la chiamata non è riuscita.</span><span class="sxs-lookup"><span data-stu-id="f96ac-112">Any other **HRESULT** value indicates that the call failed.</span></span>

## <a name="remarks"></a><span data-ttu-id="f96ac-113">Commenti</span><span class="sxs-lookup"><span data-stu-id="f96ac-113">Remarks</span></span>

<span data-ttu-id="f96ac-114">Per liberare il contesto, è necessario chiamare il metodo [**CloseHandle**](icertstore-closehandle.md) o la funzione [**CertCloseStore**](/windows/desktop/api/Wincrypt/nf-wincrypt-certclosestore) .</span><span class="sxs-lookup"><span data-stu-id="f96ac-114">You must call either the [**CloseHandle**](icertstore-closehandle.md) method or the [**CertCloseStore**](/windows/desktop/api/Wincrypt/nf-wincrypt-certclosestore) function to free the context.</span></span>

<span data-ttu-id="f96ac-115">Se si imposta la proprietà **storeHandle** , lo stato dell'intero oggetto [**Store**](store.md) viene reimpostato.</span><span class="sxs-lookup"><span data-stu-id="f96ac-115">If you set the **StoreHandle** property, the state of the entire [**Store**](store.md) object is reset.</span></span>

## <a name="requirements"></a><span data-ttu-id="f96ac-116">Requisiti</span><span class="sxs-lookup"><span data-stu-id="f96ac-116">Requirements</span></span>



| <span data-ttu-id="f96ac-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="f96ac-117">Requirement</span></span> | <span data-ttu-id="f96ac-118">Valore</span><span class="sxs-lookup"><span data-stu-id="f96ac-118">Value</span></span> |
|----------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="f96ac-119">Componente ridistribuibile</span><span class="sxs-lookup"><span data-stu-id="f96ac-119">Redistributable</span></span><br/> | <span data-ttu-id="f96ac-120">CAPICOM 2,0 o versioni successive in Windows Server 2003 e Windows XP</span><span class="sxs-lookup"><span data-stu-id="f96ac-120">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="f96ac-121">DLL</span><span class="sxs-lookup"><span data-stu-id="f96ac-121">DLL</span></span><br/>             | <dl> <span data-ttu-id="f96ac-122"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f96ac-122"><dt>Capicom.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f96ac-123">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="f96ac-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f96ac-124">**ICertStore**</span><span class="sxs-lookup"><span data-stu-id="f96ac-124">**ICertStore**</span></span>](icertstore.md)
</dt> </dl>

 

 




