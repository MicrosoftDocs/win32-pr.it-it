---
description: Recupera il descrittore di sicurezza associato alla condivisione DDE. Questa operazione viene eseguita in genere per la modifica.
ms.assetid: 7d3cc965-45ee-40ce-a462-568200592345
title: Funzione NDdeGetShareSecurity (nddeapi. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- NDdeGetShareSecurity
- NDdeGetShareSecurityA
- NDdeGetShareSecurityW
api_type:
- DllExport
api_location:
- Nddeapi.dll
ms.openlocfilehash: dae1352d9e7c45f9ce301dd30d4e7f73d508498c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103884997"
---
# <a name="nddegetsharesecurity-function"></a><span data-ttu-id="88d0e-104">NDdeGetShareSecurity (funzione)</span><span class="sxs-lookup"><span data-stu-id="88d0e-104">NDdeGetShareSecurity function</span></span>

<span data-ttu-id="88d0e-105">\[Il DDE di rete non è più supportato.</span><span class="sxs-lookup"><span data-stu-id="88d0e-105">\[Network DDE is no longer supported.</span></span> <span data-ttu-id="88d0e-106">Nddeapi.dll è presente in Windows Vista, ma tutte le chiamate di funzione restituiscono NDDE \_ non \_ implementate.\]</span><span class="sxs-lookup"><span data-stu-id="88d0e-106">Nddeapi.dll is present on Windows Vista, but all function calls return NDDE\_NOT\_IMPLEMENTED.\]</span></span>

<span data-ttu-id="88d0e-107">Recupera il descrittore di sicurezza associato alla condivisione DDE.</span><span class="sxs-lookup"><span data-stu-id="88d0e-107">Retrieves the security descriptor associated with the DDE share.</span></span> <span data-ttu-id="88d0e-108">Questa operazione viene eseguita in genere per la modifica.</span><span class="sxs-lookup"><span data-stu-id="88d0e-108">This is done usually for editing.</span></span>

## <a name="syntax"></a><span data-ttu-id="88d0e-109">Sintassi</span><span class="sxs-lookup"><span data-stu-id="88d0e-109">Syntax</span></span>


```C++
UINT NDdeGetShareSecurity(
  _In_  LPTSTR               lpszServer,
  _In_  LPTSTR               lpszShareName,
  _In_  SECURITY_INFORMATION si,
  _Out_ PSECURITY_DESCRIPTOR pSD,
  _In_  DWORD                cbSD,
  _Out_ LPDWORD              lpcbsdRequired
);
```



## <a name="parameters"></a><span data-ttu-id="88d0e-110">Parametri</span><span class="sxs-lookup"><span data-stu-id="88d0e-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="88d0e-111">*lpszServer* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="88d0e-111">*lpszServer* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="88d0e-112">Nome del server in cui risiede l'DSDM.</span><span class="sxs-lookup"><span data-stu-id="88d0e-112">The name of the server on which the DSDM resides.</span></span>

</dd> <dt>

<span data-ttu-id="88d0e-113">*lpszShareName* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="88d0e-113">*lpszShareName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="88d0e-114">Nome della condivisione il cui descrittore di sicurezza deve essere recuperato da DSDM.</span><span class="sxs-lookup"><span data-stu-id="88d0e-114">The name of the share whose security descriptor is to be retrieved from the DSDM.</span></span> <span data-ttu-id="88d0e-115">Questo parametro non può essere **null**.</span><span class="sxs-lookup"><span data-stu-id="88d0e-115">This parameter cannot be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="88d0e-116">*si* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="88d0e-116">*si* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="88d0e-117">Valore [**delle \_ informazioni di sicurezza**](/windows/desktop/SecAuthZ/security-information) che specifica le informazioni di sicurezza da recuperare dal descrittore di sicurezza associato alla condivisione.</span><span class="sxs-lookup"><span data-stu-id="88d0e-117">A [**SECURITY\_INFORMATION**](/windows/desktop/SecAuthZ/security-information) value that specifies the security information to be retrieved from the security descriptor associated with the share.</span></span>

</dd> <dt>

<span data-ttu-id="88d0e-118">*PSD* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="88d0e-118">*pSD* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="88d0e-119">Puntatore a una struttura [**di \_ descrittori di sicurezza**](/windows/desktop/api/winnt/ns-winnt-security_descriptor) che riceve il descrittore di sicurezza relativo.</span><span class="sxs-lookup"><span data-stu-id="88d0e-119">A pointer to a [**SECURITY\_DESCRIPTOR**](/windows/desktop/api/winnt/ns-winnt-security_descriptor) structure that receives the self-relative security descriptor.</span></span> <span data-ttu-id="88d0e-120">Questo parametro può essere **NULL**.</span><span class="sxs-lookup"><span data-stu-id="88d0e-120">This parameter can be **NULL**.</span></span> <span data-ttu-id="88d0e-121">Se questo parametro è **null**, DSDM determina la dimensione delle informazioni di sicurezza richieste e restituisce il numero di byte necessari nel parametro *lpcbsdRequired* insieme al codice di errore NDDE \_ BUF \_ troppo \_ piccolo.</span><span class="sxs-lookup"><span data-stu-id="88d0e-121">If this parameter is **NULL**, the DSDM determines the size of the requested security information and returns the number of bytes needed in the *lpcbsdRequired* parameter along with the NDDE\_BUF\_TOO\_SMALL error code.</span></span>

</dd> <dt>

<span data-ttu-id="88d0e-122">*cbSD* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="88d0e-122">*cbSD* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="88d0e-123">Dimensioni del buffer *PSD* .</span><span class="sxs-lookup"><span data-stu-id="88d0e-123">The size of the *pSD* buffer.</span></span> <span data-ttu-id="88d0e-124">Se *PSD* è **null**, questo parametro deve essere zero.</span><span class="sxs-lookup"><span data-stu-id="88d0e-124">This parameter must be zero if *pSD* is **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="88d0e-125">*lpcbsdRequired* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="88d0e-125">*lpcbsdRequired* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="88d0e-126">Puntatore alla variabile che riceve le dimensioni effettive del descrittore di sicurezza recuperato.</span><span class="sxs-lookup"><span data-stu-id="88d0e-126">A pointer to the variable that receives the actual size of the retrieved security descriptor.</span></span> <span data-ttu-id="88d0e-127">Questo parametro non può essere **null**.</span><span class="sxs-lookup"><span data-stu-id="88d0e-127">This parameter cannot be **NULL**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="88d0e-128">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="88d0e-128">Return value</span></span>

<span data-ttu-id="88d0e-129">Se la funzione ha esito positivo, il valore restituito è NDDE \_ senza \_ errori.</span><span class="sxs-lookup"><span data-stu-id="88d0e-129">If the function succeeds, the return value is NDDE\_NO\_ERROR.</span></span>

<span data-ttu-id="88d0e-130">Se la funzione ha esito negativo, il valore restituito è un codice di errore, che può essere convertito in un messaggio di errore di testo chiamando [**NDdeGetErrorString**](nddegeterrorstring.md).</span><span class="sxs-lookup"><span data-stu-id="88d0e-130">If the function fails, the return value is an error code, which can be translated into a text error message by calling [**NDdeGetErrorString**](nddegeterrorstring.md).</span></span> <span data-ttu-id="88d0e-131">Se il parametro *PSD* è **null**, restituisce NDDE \_ BUF \_ troppo \_ piccolo.</span><span class="sxs-lookup"><span data-stu-id="88d0e-131">If the *pSD* parameter was **NULL**, it returns NDDE\_BUF\_TOO\_SMALL.</span></span>

## <a name="requirements"></a><span data-ttu-id="88d0e-132">Requisiti</span><span class="sxs-lookup"><span data-stu-id="88d0e-132">Requirements</span></span>



| <span data-ttu-id="88d0e-133">Requisito</span><span class="sxs-lookup"><span data-stu-id="88d0e-133">Requirement</span></span> | <span data-ttu-id="88d0e-134">Valore</span><span class="sxs-lookup"><span data-stu-id="88d0e-134">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="88d0e-135">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="88d0e-135">Minimum supported client</span></span><br/> | <span data-ttu-id="88d0e-136">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="88d0e-136">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="88d0e-137">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="88d0e-137">Minimum supported server</span></span><br/> | <span data-ttu-id="88d0e-138">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="88d0e-138">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="88d0e-139">Intestazione</span><span class="sxs-lookup"><span data-stu-id="88d0e-139">Header</span></span><br/>                   | <dl> <span data-ttu-id="88d0e-140"><dt>Nddeapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="88d0e-140"><dt>Nddeapi.h</dt></span></span> </dl>   |
| <span data-ttu-id="88d0e-141">Libreria</span><span class="sxs-lookup"><span data-stu-id="88d0e-141">Library</span></span><br/>                  | <dl> <span data-ttu-id="88d0e-142"><dt>Nddeapi. lib</dt></span><span class="sxs-lookup"><span data-stu-id="88d0e-142"><dt>Nddeapi.lib</dt></span></span> </dl> |
| <span data-ttu-id="88d0e-143">DLL</span><span class="sxs-lookup"><span data-stu-id="88d0e-143">DLL</span></span><br/>                      | <dl> <span data-ttu-id="88d0e-144"><dt>Nddeapi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="88d0e-144"><dt>Nddeapi.dll</dt></span></span> </dl> |
| <span data-ttu-id="88d0e-145">Nomi Unicode e ANSI</span><span class="sxs-lookup"><span data-stu-id="88d0e-145">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="88d0e-146">**NDdeGetShareSecurityW** (Unicode) e **NDdeGetShareSecurityA** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="88d0e-146">**NDdeGetShareSecurityW** (Unicode) and **NDdeGetShareSecurityA** (ANSI)</span></span><br/>    |



## <a name="see-also"></a><span data-ttu-id="88d0e-147">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="88d0e-147">See also</span></span>

<dl> <dt>

[<span data-ttu-id="88d0e-148">Panoramica di Dynamic Data Exchange di rete</span><span class="sxs-lookup"><span data-stu-id="88d0e-148">Network Dynamic Data Exchange Overview</span></span>](network-dynamic-data-exchange.md)
</dt> <dt>

[<span data-ttu-id="88d0e-149">Funzioni DDE di rete</span><span class="sxs-lookup"><span data-stu-id="88d0e-149">Network DDE Functions</span></span>](network-dde-functions.md)
</dt> <dt>

[<span data-ttu-id="88d0e-150">**informazioni di sicurezza \_**</span><span class="sxs-lookup"><span data-stu-id="88d0e-150">**SECURITY\_INFORMATION**</span></span>](/windows/desktop/SecAuthZ/security-information)
</dt> <dt>

[<span data-ttu-id="88d0e-151">**NDdeSetShareSecurity**</span><span class="sxs-lookup"><span data-stu-id="88d0e-151">**NDdeSetShareSecurity**</span></span>](nddesetsharesecurity.md)
</dt> </dl>

 

