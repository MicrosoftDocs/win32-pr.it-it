---
description: Imposta le informazioni sul parametro specificato.
ms.assetid: fe3fe5cf-e8b8-40ca-9e12-9d92489982a7
title: 'Metodo IPStore:: SetProvParam (PStore. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IPStore.SetProvParam
api_type:
- COM
api_location:
- Pstorec.dll
ms.openlocfilehash: edbbb7bd2f5d889568623390d805659e1cf840f2
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106324799"
---
# <a name="ipstoresetprovparam-method"></a><span data-ttu-id="41d1e-103">Metodo IPStore:: SetProvParam</span><span class="sxs-lookup"><span data-stu-id="41d1e-103">IPStore::SetProvParam method</span></span>

<span data-ttu-id="41d1e-104">\[L'archiviazione protetta (PStore) è disponibile per l'uso in Windows Server 2003 e Windows XP.</span><span class="sxs-lookup"><span data-stu-id="41d1e-104">\[Protected Storage (Pstore) is available for use in Windows Server 2003 and Windows XP.</span></span> <span data-ttu-id="41d1e-105">È disponibile solo per le operazioni di sola lettura in Windows Server 2008 e Windows Vista, ma potrebbe non essere disponibile nelle versioni successive.</span><span class="sxs-lookup"><span data-stu-id="41d1e-105">It is only available for read-only operations in Windows Server 2008 and Windows Vista, but may be unavailable in subsequent versions.</span></span> <span data-ttu-id="41d1e-106">PStore usa un'implementazione precedente della protezione dei dati.</span><span class="sxs-lookup"><span data-stu-id="41d1e-106">Pstore uses an older implementation of data protection.</span></span> <span data-ttu-id="41d1e-107">Gli sviluppatori sono vivamente invitati a sfruttare i vantaggi della protezione dei dati più avanzata fornita dalle funzioni [**CryptProtectData**](/windows/win32/api/dpapi/nf-dpapi-cryptprotectdata) e [**CryptUnprotectData**](/windows/win32/api/dpapi/nf-dpapi-cryptunprotectdata) .\]</span><span class="sxs-lookup"><span data-stu-id="41d1e-107">Developers are strongly encouraged to take advantage of the stronger data protection provided by the [**CryptProtectData**](/windows/win32/api/dpapi/nf-dpapi-cryptprotectdata) and [**CryptUnprotectData**](/windows/win32/api/dpapi/nf-dpapi-cryptunprotectdata) functions.\]</span></span>

<span data-ttu-id="41d1e-108">Imposta le informazioni sul parametro specificato.</span><span class="sxs-lookup"><span data-stu-id="41d1e-108">Sets the specified parameter information.</span></span>

## <a name="syntax"></a><span data-ttu-id="41d1e-109">Sintassi</span><span class="sxs-lookup"><span data-stu-id="41d1e-109">Syntax</span></span>


```C++
HRESULT SetProvParam(
  [in] DWORD dwParam,
  [in] DWORD cbData,
       BYTE  *pbData,
       DWORD *dwFlags
);
```



## <a name="parameters"></a><span data-ttu-id="41d1e-110">Parametri</span><span class="sxs-lookup"><span data-stu-id="41d1e-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="41d1e-111">*dwParam* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="41d1e-111">*dwParam* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="41d1e-112">Contiene **la \_ \_ \_ \_ cache di scaricamento PW di PST PP** per scaricare la cache della password utente.</span><span class="sxs-lookup"><span data-stu-id="41d1e-112">Contains **PST\_PP\_FLUSH\_PW\_CACHE** to flush the user password cache.</span></span>

</dd> <dt>

<span data-ttu-id="41d1e-113">*cbData* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="41d1e-113">*cbData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="41d1e-114">Lunghezza della password nel buffer.</span><span class="sxs-lookup"><span data-stu-id="41d1e-114">The length of the password in the buffer.</span></span>

</dd> <dt>

<span data-ttu-id="41d1e-115">*pbData*</span><span class="sxs-lookup"><span data-stu-id="41d1e-115">*pbData*</span></span> 
</dt> <dd>

<span data-ttu-id="41d1e-116">Puntatore a un buffer che contiene la password dell'utente.</span><span class="sxs-lookup"><span data-stu-id="41d1e-116">A pointer to a buffer that contains the user's password.</span></span> <span data-ttu-id="41d1e-117">Deve essere impostato su **null**.</span><span class="sxs-lookup"><span data-stu-id="41d1e-117">This must be set to **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="41d1e-118">*dwFlags*</span><span class="sxs-lookup"><span data-stu-id="41d1e-118">*dwFlags*</span></span> 
</dt> <dd>

<span data-ttu-id="41d1e-119">Riservato: deve essere impostato su zero.</span><span class="sxs-lookup"><span data-stu-id="41d1e-119">Reserved: Must be set to zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="41d1e-120">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="41d1e-120">Return value</span></span>

<span data-ttu-id="41d1e-121">Il valore restituito è un valore **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="41d1e-121">The return value is an **HRESULT** value.</span></span> <span data-ttu-id="41d1e-122">Il valore **pst \_ E \_ OK** indica che la funzione ha avuto esito positivo.</span><span class="sxs-lookup"><span data-stu-id="41d1e-122">A value of **PST\_E\_OK** indicates the function was successful.</span></span>

## <a name="requirements"></a><span data-ttu-id="41d1e-123">Requisiti</span><span class="sxs-lookup"><span data-stu-id="41d1e-123">Requirements</span></span>



| <span data-ttu-id="41d1e-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="41d1e-124">Requirement</span></span> | <span data-ttu-id="41d1e-125">Valore</span><span class="sxs-lookup"><span data-stu-id="41d1e-125">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="41d1e-126">Intestazione</span><span class="sxs-lookup"><span data-stu-id="41d1e-126">Header</span></span><br/> | <dl> <span data-ttu-id="41d1e-127"><dt>PStore. h</dt></span><span class="sxs-lookup"><span data-stu-id="41d1e-127"><dt>Pstore.h</dt></span></span> </dl>    |
| <span data-ttu-id="41d1e-128">DLL</span><span class="sxs-lookup"><span data-stu-id="41d1e-128">DLL</span></span><br/>    | <dl> <span data-ttu-id="41d1e-129"><dt>Pstorec.dll</dt></span><span class="sxs-lookup"><span data-stu-id="41d1e-129"><dt>Pstorec.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="41d1e-130">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="41d1e-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="41d1e-131">**IPStore**</span><span class="sxs-lookup"><span data-stu-id="41d1e-131">**IPStore**</span></span>](ipstore.md)
</dt> </dl>

 

 
