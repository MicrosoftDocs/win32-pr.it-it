---
description: Chiude un archivio certificati aperto.
ms.assetid: 14db819a-b220-47d4-9030-72157e0e5019
title: Store. Close (metodo)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Store.Close
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 2e3deb127ec8b19d9ec5c625f07cfaa2685b776c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106331703"
---
# <a name="storeclose-method"></a><span data-ttu-id="21ac2-103">Store. Close (metodo)</span><span class="sxs-lookup"><span data-stu-id="21ac2-103">Store.Close method</span></span>

<span data-ttu-id="21ac2-104">\[Il metodo **Close** è disponibile per l'uso nei sistemi operativi specificati nella sezione requisiti.</span><span class="sxs-lookup"><span data-stu-id="21ac2-104">\[The **Close** method is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="21ac2-105">Usare invece la [**classe X509Store**](/previous-versions/windows/embedded/hh424027(v=msdn.10)) nello spazio dei nomi [**System. Security. Cryptography. X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) .\]</span><span class="sxs-lookup"><span data-stu-id="21ac2-105">Instead, use the [**X509Store Class**](/previous-versions/windows/embedded/hh424027(v=msdn.10)) in the [**System.Security.Cryptography.X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) namespace.\]</span></span>

<span data-ttu-id="21ac2-106">Il metodo **Close** chiude un [*archivio certificati*](../secgloss/c-gly.md)aperto.</span><span class="sxs-lookup"><span data-stu-id="21ac2-106">The **Close** method closes an open [*certificate store*](../secgloss/c-gly.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="21ac2-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="21ac2-107">Syntax</span></span>


```VB
Store.Close()
```



## <a name="parameters"></a><span data-ttu-id="21ac2-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="21ac2-108">Parameters</span></span>

<span data-ttu-id="21ac2-109">Questo metodo non presenta parametri.</span><span class="sxs-lookup"><span data-stu-id="21ac2-109">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="21ac2-110">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="21ac2-110">Return value</span></span>

<span data-ttu-id="21ac2-111">Questo metodo non restituisce valori.</span><span class="sxs-lookup"><span data-stu-id="21ac2-111">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="21ac2-112">Commenti</span><span class="sxs-lookup"><span data-stu-id="21ac2-112">Remarks</span></span>

<span data-ttu-id="21ac2-113">Quando viene chiamato il metodo **Close** , l'oggetto [**Store**](store.md) viene eliminato definitivamente.</span><span class="sxs-lookup"><span data-stu-id="21ac2-113">After the **Close** method is called, the [**Store**](store.md) object is destroyed.</span></span>

## <a name="requirements"></a><span data-ttu-id="21ac2-114">Requisiti</span><span class="sxs-lookup"><span data-stu-id="21ac2-114">Requirements</span></span>



| <span data-ttu-id="21ac2-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="21ac2-115">Requirement</span></span> | <span data-ttu-id="21ac2-116">Valore</span><span class="sxs-lookup"><span data-stu-id="21ac2-116">Value</span></span> |
|----------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="21ac2-117">Componente ridistribuibile</span><span class="sxs-lookup"><span data-stu-id="21ac2-117">Redistributable</span></span><br/> | <span data-ttu-id="21ac2-118">CAPICOM 2,1 o versioni successive in Windows Server 2003 e Windows XP</span><span class="sxs-lookup"><span data-stu-id="21ac2-118">CAPICOM 2.1 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="21ac2-119">DLL</span><span class="sxs-lookup"><span data-stu-id="21ac2-119">DLL</span></span><br/>             | <dl> <span data-ttu-id="21ac2-120"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="21ac2-120"><dt>Capicom.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="21ac2-121">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="21ac2-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="21ac2-122">**Store**</span><span class="sxs-lookup"><span data-stu-id="21ac2-122">**Store**</span></span>](store.md)
</dt> <dt>

[<span data-ttu-id="21ac2-123">**Oggetti Cryptography**</span><span class="sxs-lookup"><span data-stu-id="21ac2-123">**Cryptography Objects**</span></span>](cryptography-objects.md)
</dt> <dt>

[<span data-ttu-id="21ac2-124">**Aprire**</span><span class="sxs-lookup"><span data-stu-id="21ac2-124">**Open**</span></span>](store-open.md)
</dt> </dl>

 

 
