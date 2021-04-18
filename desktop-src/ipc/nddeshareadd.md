---
description: Crea e aggiunge una nuova condivisione DDE alla gestione del database di condivisione DDE (DSDM).
ms.assetid: c9814919-412e-4f13-98cc-373b69545734
title: Funzione NDdeShareAdd (nddeapi. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- NDdeShareAdd
- NDdeShareAddA
- NDdeShareAddW
api_type:
- DllExport
api_location:
- Nddeapi.dll
ms.openlocfilehash: 282ff7ed3e1564044591966fb4233b2eda1d3227
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106316917"
---
# <a name="nddeshareadd-function"></a><span data-ttu-id="cea24-103">NDdeShareAdd (funzione)</span><span class="sxs-lookup"><span data-stu-id="cea24-103">NDdeShareAdd function</span></span>

<span data-ttu-id="cea24-104">\[Il DDE di rete non è più supportato.</span><span class="sxs-lookup"><span data-stu-id="cea24-104">\[Network DDE is no longer supported.</span></span> <span data-ttu-id="cea24-105">Nddeapi.dll è presente in Windows Vista, ma tutte le chiamate di funzione restituiscono NDDE \_ non \_ implementate.\]</span><span class="sxs-lookup"><span data-stu-id="cea24-105">Nddeapi.dll is present on Windows Vista, but all function calls return NDDE\_NOT\_IMPLEMENTED.\]</span></span>

<span data-ttu-id="cea24-106">Crea e aggiunge una nuova condivisione DDE alla gestione del database di condivisione DDE (DSDM).</span><span class="sxs-lookup"><span data-stu-id="cea24-106">Creates and adds a new DDE share to the DDE share database manager (DSDM).</span></span>

## <a name="syntax"></a><span data-ttu-id="cea24-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="cea24-107">Syntax</span></span>


```C++
UINT NDdeShareAdd(
  _In_ LPTSTR               lpszServer,
  _In_ UINT                 nLevel,
  _In_ PSECURITY_DESCRIPTOR pSD,
  _In_ LPBYTE               lpBuffer,
  _In_ DWORD                cBufSize
);
```



## <a name="parameters"></a><span data-ttu-id="cea24-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="cea24-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="cea24-109">*lpszServer* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="cea24-109">*lpszServer* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="cea24-110">Nome del server di cui è necessario modificare il DSDM.</span><span class="sxs-lookup"><span data-stu-id="cea24-110">The name of the server whose DSDM is to be modified.</span></span>

</dd> <dt>

<span data-ttu-id="cea24-111">*nLevel* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="cea24-111">*nLevel* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="cea24-112">Livello di informazioni.</span><span class="sxs-lookup"><span data-stu-id="cea24-112">The information level.</span></span> <span data-ttu-id="cea24-113">Questo parametro deve essere 2.</span><span class="sxs-lookup"><span data-stu-id="cea24-113">This parameter must be 2.</span></span>

</dd> <dt>

<span data-ttu-id="cea24-114">*PSD* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="cea24-114">*pSD* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="cea24-115">Puntatore a una struttura [**di \_ descrittori di sicurezza**](/windows/desktop/api/winnt/ns-winnt-security_descriptor) da associare a questa condivisione e in base a cui verranno eseguiti i controlli di accesso per i successivi avvii a questa condivisione.</span><span class="sxs-lookup"><span data-stu-id="cea24-115">A pointer to a [**SECURITY\_DESCRIPTOR**](/windows/desktop/api/winnt/ns-winnt-security_descriptor) structure to be associated with this share and against which access checks will be performed on subsequent initiates to this share.</span></span> <span data-ttu-id="cea24-116">Questo parametro può essere **null**, nel qual caso DSDM crea un descrittore di sicurezza predefinito che concede al proprietario il "controllo completo" e "Read and link" a tutti.</span><span class="sxs-lookup"><span data-stu-id="cea24-116">This parameter can be **NULL**, in which case the DSDM creates a default security descriptor that grants "Full Control" to the owner and "Read and Link" to everyone.</span></span>

</dd> <dt>

<span data-ttu-id="cea24-117">*lpBuffer* \[in\]</span><span class="sxs-lookup"><span data-stu-id="cea24-117">*lpBuffer* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="cea24-118">Puntatore alla struttura [**NDDESHAREINFO**](nddeshareinfo-str.md) che definisce l'elenco ApplicationTopic associato alla condivisione DDE creata e ad altri parametri.</span><span class="sxs-lookup"><span data-stu-id="cea24-118">A pointer to the [**NDDESHAREINFO**](nddeshareinfo-str.md) structure that defines the ApplicationTopic list associated with the DDE share being created as well as other parameters.</span></span> <span data-ttu-id="cea24-119">Questo parametro non può essere **null**.</span><span class="sxs-lookup"><span data-stu-id="cea24-119">This parameter cannot be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="cea24-120">*cBufSize* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="cea24-120">*cBufSize* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="cea24-121">Dimensioni in byte della struttura *lpBuffer* .</span><span class="sxs-lookup"><span data-stu-id="cea24-121">The size of the *lpBuffer* structure, in bytes.</span></span> <span data-ttu-id="cea24-122">Questo parametro non può essere zero.</span><span class="sxs-lookup"><span data-stu-id="cea24-122">This parameter cannot be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="cea24-123">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="cea24-123">Return value</span></span>

<span data-ttu-id="cea24-124">Se la funzione ha esito positivo, il valore restituito è NDDE \_ senza \_ errori.</span><span class="sxs-lookup"><span data-stu-id="cea24-124">If the function succeeds, the return value is NDDE\_NO\_ERROR.</span></span>

<span data-ttu-id="cea24-125">Se la funzione ha esito negativo, il valore restituito è un codice di errore, che può essere convertito in un messaggio di errore di testo chiamando [**NDdeGetErrorString**](nddegeterrorstring.md).</span><span class="sxs-lookup"><span data-stu-id="cea24-125">If the function fails, the return value is an error code, which can be translated into a text error message by calling [**NDdeGetErrorString**](nddegeterrorstring.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="cea24-126">Commenti</span><span class="sxs-lookup"><span data-stu-id="cea24-126">Remarks</span></span>

<span data-ttu-id="cea24-127">Prima che un client possa connettersi alla condivisione DDE, deve essere considerato attendibile con [**NDdeSetTrustedShare**](nddesettrustedshare.md).</span><span class="sxs-lookup"><span data-stu-id="cea24-127">Before a client can connect to the DDE share, it must be trusted with [**NDdeSetTrustedShare**](nddesettrustedshare.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="cea24-128">Requisiti</span><span class="sxs-lookup"><span data-stu-id="cea24-128">Requirements</span></span>



| <span data-ttu-id="cea24-129">Requisito</span><span class="sxs-lookup"><span data-stu-id="cea24-129">Requirement</span></span> | <span data-ttu-id="cea24-130">Valore</span><span class="sxs-lookup"><span data-stu-id="cea24-130">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="cea24-131">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="cea24-131">Minimum supported client</span></span><br/> | <span data-ttu-id="cea24-132">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="cea24-132">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="cea24-133">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="cea24-133">Minimum supported server</span></span><br/> | <span data-ttu-id="cea24-134">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="cea24-134">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="cea24-135">Intestazione</span><span class="sxs-lookup"><span data-stu-id="cea24-135">Header</span></span><br/>                   | <dl> <span data-ttu-id="cea24-136"><dt>Nddeapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="cea24-136"><dt>Nddeapi.h</dt></span></span> </dl>   |
| <span data-ttu-id="cea24-137">Libreria</span><span class="sxs-lookup"><span data-stu-id="cea24-137">Library</span></span><br/>                  | <dl> <span data-ttu-id="cea24-138"><dt>Nddeapi. lib</dt></span><span class="sxs-lookup"><span data-stu-id="cea24-138"><dt>Nddeapi.lib</dt></span></span> </dl> |
| <span data-ttu-id="cea24-139">DLL</span><span class="sxs-lookup"><span data-stu-id="cea24-139">DLL</span></span><br/>                      | <dl> <span data-ttu-id="cea24-140"><dt>Nddeapi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="cea24-140"><dt>Nddeapi.dll</dt></span></span> </dl> |
| <span data-ttu-id="cea24-141">Nomi Unicode e ANSI</span><span class="sxs-lookup"><span data-stu-id="cea24-141">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="cea24-142">**NDdeShareAddW** (Unicode) e **NDdeShareAddA** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="cea24-142">**NDdeShareAddW** (Unicode) and **NDdeShareAddA** (ANSI)</span></span><br/>                    |



## <a name="see-also"></a><span data-ttu-id="cea24-143">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="cea24-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cea24-144">Panoramica di Dynamic Data Exchange di rete</span><span class="sxs-lookup"><span data-stu-id="cea24-144">Network Dynamic Data Exchange Overview</span></span>](network-dynamic-data-exchange.md)
</dt> <dt>

[<span data-ttu-id="cea24-145">Funzioni DDE di rete</span><span class="sxs-lookup"><span data-stu-id="cea24-145">Network DDE Functions</span></span>](network-dde-functions.md)
</dt> <dt>

[<span data-ttu-id="cea24-146">**NDDESHAREINFO**</span><span class="sxs-lookup"><span data-stu-id="cea24-146">**NDDESHAREINFO**</span></span>](nddeshareinfo-str.md)
</dt> <dt>

[<span data-ttu-id="cea24-147">**NDdeSetTrustedShare**</span><span class="sxs-lookup"><span data-stu-id="cea24-147">**NDdeSetTrustedShare**</span></span>](nddesettrustedshare.md)
</dt> </dl>

 

