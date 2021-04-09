---
description: Libera una chiave, un hash o un oggetto provider.
ms.assetid: 73fa0a08-4654-4515-bdb2-9951936b689a
title: Funzione SslFreeObject (Sslprovider. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SslFreeObject
api_type:
- DllExport
api_location:
- Ncrypt.dll
ms.openlocfilehash: e7d10059942080e7794da7e6b87613189dcf9844
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103880853"
---
# <a name="sslfreeobject-function"></a><span data-ttu-id="6caf5-103">SslFreeObject (funzione)</span><span class="sxs-lookup"><span data-stu-id="6caf5-103">SslFreeObject function</span></span>

<span data-ttu-id="6caf5-104">La funzione **SslFreeObject** libera una chiave, un hash o un oggetto provider.</span><span class="sxs-lookup"><span data-stu-id="6caf5-104">The **SslFreeObject** function frees a key, hash, or provider object.</span></span>

## <a name="syntax"></a><span data-ttu-id="6caf5-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="6caf5-105">Syntax</span></span>


```C++
SECURITY_STATUS WINAPI SslFreeObject(
  _In_ NCRYPT_HANDLE hObject,
  _In_ DWORD         dwFlags
);
```



## <a name="parameters"></a><span data-ttu-id="6caf5-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="6caf5-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6caf5-107">*hObject* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="6caf5-107">*hObject* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6caf5-108">Handle dell'oggetto da liberare.</span><span class="sxs-lookup"><span data-stu-id="6caf5-108">The handle of the object to free.</span></span>

</dd> <dt>

<span data-ttu-id="6caf5-109">*dwFlags* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="6caf5-109">*dwFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6caf5-110">Questo parametro è riservato per usi futuri.</span><span class="sxs-lookup"><span data-stu-id="6caf5-110">This parameter is reserved for future use.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6caf5-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="6caf5-111">Return value</span></span>

<span data-ttu-id="6caf5-112">Se la funzione ha esito positivo, restituisce zero.</span><span class="sxs-lookup"><span data-stu-id="6caf5-112">If the function succeeds, it returns zero.</span></span>

<span data-ttu-id="6caf5-113">Se la funzione ha esito negativo, restituisce un valore di errore diverso da zero.</span><span class="sxs-lookup"><span data-stu-id="6caf5-113">If the function fails, it returns a nonzero error value.</span></span>

<span data-ttu-id="6caf5-114">I codici restituiti possibili includono, ma non sono limitati a, quanto segue.</span><span class="sxs-lookup"><span data-stu-id="6caf5-114">Possible return codes include, but are not limited to, the following.</span></span>



| <span data-ttu-id="6caf5-115">Codice/valore restituito</span><span class="sxs-lookup"><span data-stu-id="6caf5-115">Return code/value</span></span>                                                                                                                                                       | <span data-ttu-id="6caf5-116">Descrizione</span><span class="sxs-lookup"><span data-stu-id="6caf5-116">Description</span></span>                                  |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------|
| <dl> <span data-ttu-id="6caf5-117"><dt>**Nte \_ 0x80090026L \_ handle non valido**</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="6caf5-117"><dt>**NTE\_INVALID\_HANDLE**</dt> <dt>0x80090026L</dt></span></span> </dl>    | <span data-ttu-id="6caf5-118">Handle interno non valido.</span><span class="sxs-lookup"><span data-stu-id="6caf5-118">An internal handle is not valid.</span></span><br/>  |
| <dl> <span data-ttu-id="6caf5-119"><dt>**Stato \_ di 0xC0000008L \_ handle non valido**</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="6caf5-119"><dt>**STATUS\_INVALID\_HANDLE**</dt> <dt>0xC0000008L</dt></span></span> </dl> | <span data-ttu-id="6caf5-120">Handle fornito non valido.</span><span class="sxs-lookup"><span data-stu-id="6caf5-120">The provided handle is not valid.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="6caf5-121">Requisiti</span><span class="sxs-lookup"><span data-stu-id="6caf5-121">Requirements</span></span>



| <span data-ttu-id="6caf5-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="6caf5-122">Requirement</span></span> | <span data-ttu-id="6caf5-123">Valore</span><span class="sxs-lookup"><span data-stu-id="6caf5-123">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="6caf5-124">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="6caf5-124">Minimum supported client</span></span><br/> | <span data-ttu-id="6caf5-125">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="6caf5-125">Windows Vista \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="6caf5-126">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="6caf5-126">Minimum supported server</span></span><br/> | <span data-ttu-id="6caf5-127">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="6caf5-127">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="6caf5-128">Intestazione</span><span class="sxs-lookup"><span data-stu-id="6caf5-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="6caf5-129"><dt>Sslprovider. h</dt></span><span class="sxs-lookup"><span data-stu-id="6caf5-129"><dt>Sslprovider.h</dt></span></span> </dl> |
| <span data-ttu-id="6caf5-130">DLL</span><span class="sxs-lookup"><span data-stu-id="6caf5-130">DLL</span></span><br/>                      | <dl> <span data-ttu-id="6caf5-131"><dt>Ncrypt.dll</dt></span><span class="sxs-lookup"><span data-stu-id="6caf5-131"><dt>Ncrypt.dll</dt></span></span> </dl>    |



 

 




