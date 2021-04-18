---
description: Imposta il descrittore di sicurezza associato alla condivisione DDE.
ms.assetid: 8bb8c466-3dd7-49a6-8ba5-632001b8a47f
title: Funzione NDdeSetShareSecurity (nddeapi. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- NDdeSetShareSecurity
- NDdeSetShareSecurityA
- NDdeSetShareSecurityW
api_type:
- DllExport
api_location:
- Nddeapi.dll
ms.openlocfilehash: 112752bcd0953fbbc358c75080cb2749273ed95d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106315053"
---
# <a name="nddesetsharesecurity-function"></a><span data-ttu-id="ab90c-103">NDdeSetShareSecurity (funzione)</span><span class="sxs-lookup"><span data-stu-id="ab90c-103">NDdeSetShareSecurity function</span></span>

<span data-ttu-id="ab90c-104">\[Il DDE di rete non è più supportato.</span><span class="sxs-lookup"><span data-stu-id="ab90c-104">\[Network DDE is no longer supported.</span></span> <span data-ttu-id="ab90c-105">Nddeapi.dll è presente in Windows Vista, ma tutte le chiamate di funzione restituiscono NDDE \_ non \_ implementate.\]</span><span class="sxs-lookup"><span data-stu-id="ab90c-105">Nddeapi.dll is present on Windows Vista, but all function calls return NDDE\_NOT\_IMPLEMENTED.\]</span></span>

<span data-ttu-id="ab90c-106">Imposta il descrittore di sicurezza associato alla condivisione DDE.</span><span class="sxs-lookup"><span data-stu-id="ab90c-106">Sets the security descriptor associated with the DDE share.</span></span> <span data-ttu-id="ab90c-107">Questa operazione viene eseguita in genere dopo la modifica del DACL assegnato alla condivisione DDE.</span><span class="sxs-lookup"><span data-stu-id="ab90c-107">This is done usually after editing the DACL assigned to the DDE share.</span></span>

## <a name="syntax"></a><span data-ttu-id="ab90c-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="ab90c-108">Syntax</span></span>


```C++
UINT NDdeSetShareSecurity(
  _In_ LPTSTR               lpszServer,
  _In_ LPTSTR               lpszShareName,
  _In_ SECURITY_INFORMATION si,
  _In_ PSECURITY_DESCRIPTOR pSD
);
```



## <a name="parameters"></a><span data-ttu-id="ab90c-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="ab90c-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ab90c-110">*lpszServer* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="ab90c-110">*lpszServer* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ab90c-111">Nome del server di cui è necessario modificare il DSDM.</span><span class="sxs-lookup"><span data-stu-id="ab90c-111">The name of the server whose DSDM is to be modified.</span></span>

</dd> <dt>

<span data-ttu-id="ab90c-112">*lpszShareName* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="ab90c-112">*lpszShareName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ab90c-113">Nome della condivisione di cui è necessario modificare il descrittore di sicurezza.</span><span class="sxs-lookup"><span data-stu-id="ab90c-113">The name of the share whose security descriptor is to be modified.</span></span> <span data-ttu-id="ab90c-114">Questo parametro non può essere **null**.</span><span class="sxs-lookup"><span data-stu-id="ab90c-114">This parameter cannot be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="ab90c-115">*si* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="ab90c-115">*si* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ab90c-116">Valore [**delle \_ informazioni di sicurezza**](/windows/desktop/SecAuthZ/security-information) che identifica le informazioni di sicurezza da recuperare.</span><span class="sxs-lookup"><span data-stu-id="ab90c-116">A [**SECURITY\_INFORMATION**](/windows/desktop/SecAuthZ/security-information) value that identifies the security information to retrieve.</span></span>

</dd> <dt>

<span data-ttu-id="ab90c-117">*PSD* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="ab90c-117">*pSD* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ab90c-118">Puntatore a una struttura [**di \_ descrittori di sicurezza**](/windows/desktop/api/winnt/ns-winnt-security_descriptor) che contiene informazioni sulla sicurezza.</span><span class="sxs-lookup"><span data-stu-id="ab90c-118">A pointer to a [**SECURITY\_DESCRIPTOR**](/windows/desktop/api/winnt/ns-winnt-security_descriptor) structure that contains security information.</span></span> <span data-ttu-id="ab90c-119">Questo parametro non può essere **null** e deve puntare a un descrittore di sicurezza valido.</span><span class="sxs-lookup"><span data-stu-id="ab90c-119">This parameter cannot be **NULL** and should point to a valid security descriptor.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ab90c-120">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="ab90c-120">Return value</span></span>

<span data-ttu-id="ab90c-121">Se la funzione ha esito positivo, il valore restituito è NDDE \_ senza \_ errori.</span><span class="sxs-lookup"><span data-stu-id="ab90c-121">If the function succeeds, the return value is NDDE\_NO\_ERROR.</span></span>

<span data-ttu-id="ab90c-122">Se la funzione ha esito negativo, il valore restituito è un codice di errore, che può essere convertito in un messaggio di errore di testo chiamando [**NDdeGetErrorString**](nddegeterrorstring.md).</span><span class="sxs-lookup"><span data-stu-id="ab90c-122">If the function fails, the return value is an error code, which can be translated into a text error message by calling [**NDdeGetErrorString**](nddegeterrorstring.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="ab90c-123">Commenti</span><span class="sxs-lookup"><span data-stu-id="ab90c-123">Remarks</span></span>

<span data-ttu-id="ab90c-124">Per modificare il [**\_ descrittore di sicurezza**](/windows/desktop/api/winnt/ns-winnt-security_descriptor) associato a una condivisione DDE in DSDM, l'utente deve disporre dei privilegi appropriati. l'autore della condivisione dispone di questo privilegio.</span><span class="sxs-lookup"><span data-stu-id="ab90c-124">To modify the [**SECURITY\_DESCRIPTOR**](/windows/desktop/api/winnt/ns-winnt-security_descriptor) associated with a DDE share in the DSDM, the user must have appropriate privilege; the share creator has this privilege.</span></span>

## <a name="requirements"></a><span data-ttu-id="ab90c-125">Requisiti</span><span class="sxs-lookup"><span data-stu-id="ab90c-125">Requirements</span></span>



| <span data-ttu-id="ab90c-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="ab90c-126">Requirement</span></span> | <span data-ttu-id="ab90c-127">Valore</span><span class="sxs-lookup"><span data-stu-id="ab90c-127">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="ab90c-128">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="ab90c-128">Minimum supported client</span></span><br/> | <span data-ttu-id="ab90c-129">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="ab90c-129">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="ab90c-130">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="ab90c-130">Minimum supported server</span></span><br/> | <span data-ttu-id="ab90c-131">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="ab90c-131">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="ab90c-132">Intestazione</span><span class="sxs-lookup"><span data-stu-id="ab90c-132">Header</span></span><br/>                   | <dl> <span data-ttu-id="ab90c-133"><dt>Nddeapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="ab90c-133"><dt>Nddeapi.h</dt></span></span> </dl>   |
| <span data-ttu-id="ab90c-134">Libreria</span><span class="sxs-lookup"><span data-stu-id="ab90c-134">Library</span></span><br/>                  | <dl> <span data-ttu-id="ab90c-135"><dt>Nddeapi. lib</dt></span><span class="sxs-lookup"><span data-stu-id="ab90c-135"><dt>Nddeapi.lib</dt></span></span> </dl> |
| <span data-ttu-id="ab90c-136">DLL</span><span class="sxs-lookup"><span data-stu-id="ab90c-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ab90c-137"><dt>Nddeapi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ab90c-137"><dt>Nddeapi.dll</dt></span></span> </dl> |
| <span data-ttu-id="ab90c-138">Nomi Unicode e ANSI</span><span class="sxs-lookup"><span data-stu-id="ab90c-138">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="ab90c-139">**NDdeSetShareSecurityW** (Unicode) e **NDdeSetShareSecurityA** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="ab90c-139">**NDdeSetShareSecurityW** (Unicode) and **NDdeSetShareSecurityA** (ANSI)</span></span><br/>    |



## <a name="see-also"></a><span data-ttu-id="ab90c-140">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="ab90c-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ab90c-141">Panoramica di Dynamic Data Exchange di rete</span><span class="sxs-lookup"><span data-stu-id="ab90c-141">Network Dynamic Data Exchange Overview</span></span>](network-dynamic-data-exchange.md)
</dt> <dt>

[<span data-ttu-id="ab90c-142">Funzioni DDE di rete</span><span class="sxs-lookup"><span data-stu-id="ab90c-142">Network DDE Functions</span></span>](network-dde-functions.md)
</dt> <dt>

[<span data-ttu-id="ab90c-143">**informazioni di sicurezza \_**</span><span class="sxs-lookup"><span data-stu-id="ab90c-143">**SECURITY\_INFORMATION**</span></span>](/windows/desktop/SecAuthZ/security-information)
</dt> <dt>

[<span data-ttu-id="ab90c-144">**NDdeGetShareSecurity**</span><span class="sxs-lookup"><span data-stu-id="ab90c-144">**NDdeGetShareSecurity**</span></span>](nddegetsharesecurity.md)
</dt> </dl>

 

