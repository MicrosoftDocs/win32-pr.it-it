---
description: Imposta le informazioni sulla condivisione DDE. Questa operazione viene in genere eseguita dopo la modifica.
ms.assetid: 002c73ce-7b35-4e8e-bb7e-0e1393b97ccc
title: Funzione NDdeShareSetInfo (nddeapi. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- NDdeShareSetInfo
- NDdeShareSetInfoA
- NDdeShareSetInfoW
api_type:
- DllExport
api_location:
- Nddeapi.dll
ms.openlocfilehash: cee7660a58e8f2747a800650b79db20f95504f87
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106305709"
---
# <a name="nddesharesetinfo-function"></a><span data-ttu-id="296f7-104">NDdeShareSetInfo (funzione)</span><span class="sxs-lookup"><span data-stu-id="296f7-104">NDdeShareSetInfo function</span></span>

<span data-ttu-id="296f7-105">\[Il DDE di rete non è più supportato.</span><span class="sxs-lookup"><span data-stu-id="296f7-105">\[Network DDE is no longer supported.</span></span> <span data-ttu-id="296f7-106">Nddeapi.dll è presente in Windows Vista, ma tutte le chiamate di funzione restituiscono NDDE \_ non \_ implementate.\]</span><span class="sxs-lookup"><span data-stu-id="296f7-106">Nddeapi.dll is present on Windows Vista, but all function calls return NDDE\_NOT\_IMPLEMENTED.\]</span></span>

<span data-ttu-id="296f7-107">Imposta le informazioni sulla condivisione DDE.</span><span class="sxs-lookup"><span data-stu-id="296f7-107">Sets DDE share information.</span></span> <span data-ttu-id="296f7-108">Questa operazione viene in genere eseguita dopo la modifica.</span><span class="sxs-lookup"><span data-stu-id="296f7-108">This is usually done after editing.</span></span>

## <a name="syntax"></a><span data-ttu-id="296f7-109">Sintassi</span><span class="sxs-lookup"><span data-stu-id="296f7-109">Syntax</span></span>


```C++
UINT NDdeShareSetInfo(
  _In_ LPTSTR lpszServer,
  _In_ LPTSTR lpszShareName,
  _In_ UINT   nLevel,
  _In_ LPBYTE lpBuffer,
  _In_ DWORD  cBufSize,
  _In_ WORD   sParmNum
);
```



## <a name="parameters"></a><span data-ttu-id="296f7-110">Parametri</span><span class="sxs-lookup"><span data-stu-id="296f7-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="296f7-111">*lpszServer* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="296f7-111">*lpszServer* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="296f7-112">Nome del server di cui è necessario modificare il DSDM.</span><span class="sxs-lookup"><span data-stu-id="296f7-112">The name of the server whose DSDM is to be modified.</span></span>

</dd> <dt>

<span data-ttu-id="296f7-113">*lpszShareName* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="296f7-113">*lpszShareName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="296f7-114">Nome del nome della condivisione di cui è necessario modificare le informazioni.</span><span class="sxs-lookup"><span data-stu-id="296f7-114">The name of the share name whose information is to be modified.</span></span> <span data-ttu-id="296f7-115">Questo parametro non può essere **null**.</span><span class="sxs-lookup"><span data-stu-id="296f7-115">This parameter cannot be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="296f7-116">*nLevel* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="296f7-116">*nLevel* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="296f7-117">Livello di informazioni.</span><span class="sxs-lookup"><span data-stu-id="296f7-117">The information level.</span></span> <span data-ttu-id="296f7-118">Questo parametro deve essere 2.</span><span class="sxs-lookup"><span data-stu-id="296f7-118">This parameter must be 2.</span></span>

</dd> <dt>

<span data-ttu-id="296f7-119">*lpBuffer* \[in\]</span><span class="sxs-lookup"><span data-stu-id="296f7-119">*lpBuffer* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="296f7-120">Puntatore alla struttura [**NDDESHAREINFO**](nddeshareinfo-str.md) che specifica le informazioni sulla condivisione DDE da archiviare in DSDM.</span><span class="sxs-lookup"><span data-stu-id="296f7-120">A pointer to the [**NDDESHAREINFO**](nddeshareinfo-str.md) structure that specifies the DDE share information to be stored in the DSDM.</span></span> <span data-ttu-id="296f7-121">Attualmente, le informazioni sulla condivisione DDE vengono modificate nel suo complesso, ovvero non vengono apportate modifiche parziali.</span><span class="sxs-lookup"><span data-stu-id="296f7-121">Currently the DDE share information is modified as a whole, that is, no partial edits are made.</span></span> <span data-ttu-id="296f7-122">Questo parametro non può essere **null**.</span><span class="sxs-lookup"><span data-stu-id="296f7-122">This parameter cannot be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="296f7-123">*cBufSize* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="296f7-123">*cBufSize* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="296f7-124">Dimensioni in byte del buffer *lpBuffer* .</span><span class="sxs-lookup"><span data-stu-id="296f7-124">The size of the *lpBuffer* buffer, in bytes.</span></span>

</dd> <dt>

<span data-ttu-id="296f7-125">*sParmNum* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="296f7-125">*sParmNum* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="296f7-126">Indice del parametro da modificare.</span><span class="sxs-lookup"><span data-stu-id="296f7-126">The parameter index to be modified.</span></span> <span data-ttu-id="296f7-127">L'implementazione corrente non supporta la modifica parziale; Pertanto, questo parametro deve essere zero.</span><span class="sxs-lookup"><span data-stu-id="296f7-127">The current implementation does not support partial modification; therefore, this parameter must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="296f7-128">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="296f7-128">Return value</span></span>

<span data-ttu-id="296f7-129">Se la funzione ha esito positivo, il valore restituito è NDDE \_ senza \_ errori.</span><span class="sxs-lookup"><span data-stu-id="296f7-129">If the function succeeds, the return value is NDDE\_NO\_ERROR.</span></span>

<span data-ttu-id="296f7-130">Se la funzione ha esito negativo, il valore restituito è un codice di errore, che può essere convertito in un messaggio di errore di testo chiamando [**NDdeGetErrorString**](nddegeterrorstring.md).</span><span class="sxs-lookup"><span data-stu-id="296f7-130">If the function fails, the return value is an error code, which can be translated into a text error message by calling [**NDdeGetErrorString**](nddegeterrorstring.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="296f7-131">Requisiti</span><span class="sxs-lookup"><span data-stu-id="296f7-131">Requirements</span></span>



| <span data-ttu-id="296f7-132">Requisito</span><span class="sxs-lookup"><span data-stu-id="296f7-132">Requirement</span></span> | <span data-ttu-id="296f7-133">Valore</span><span class="sxs-lookup"><span data-stu-id="296f7-133">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="296f7-134">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="296f7-134">Minimum supported client</span></span><br/> | <span data-ttu-id="296f7-135">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="296f7-135">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="296f7-136">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="296f7-136">Minimum supported server</span></span><br/> | <span data-ttu-id="296f7-137">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="296f7-137">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="296f7-138">Intestazione</span><span class="sxs-lookup"><span data-stu-id="296f7-138">Header</span></span><br/>                   | <dl> <span data-ttu-id="296f7-139"><dt>Nddeapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="296f7-139"><dt>Nddeapi.h</dt></span></span> </dl>   |
| <span data-ttu-id="296f7-140">Libreria</span><span class="sxs-lookup"><span data-stu-id="296f7-140">Library</span></span><br/>                  | <dl> <span data-ttu-id="296f7-141"><dt>Nddeapi. lib</dt></span><span class="sxs-lookup"><span data-stu-id="296f7-141"><dt>Nddeapi.lib</dt></span></span> </dl> |
| <span data-ttu-id="296f7-142">DLL</span><span class="sxs-lookup"><span data-stu-id="296f7-142">DLL</span></span><br/>                      | <dl> <span data-ttu-id="296f7-143"><dt>Nddeapi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="296f7-143"><dt>Nddeapi.dll</dt></span></span> </dl> |
| <span data-ttu-id="296f7-144">Nomi Unicode e ANSI</span><span class="sxs-lookup"><span data-stu-id="296f7-144">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="296f7-145">**NDdeShareSetInfoW** (Unicode) e **NDdeShareSetInfoA** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="296f7-145">**NDdeShareSetInfoW** (Unicode) and **NDdeShareSetInfoA** (ANSI)</span></span><br/>            |



## <a name="see-also"></a><span data-ttu-id="296f7-146">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="296f7-146">See also</span></span>

<dl> <dt>

[<span data-ttu-id="296f7-147">Panoramica di Dynamic Data Exchange di rete</span><span class="sxs-lookup"><span data-stu-id="296f7-147">Network Dynamic Data Exchange Overview</span></span>](network-dynamic-data-exchange.md)
</dt> <dt>

[<span data-ttu-id="296f7-148">Funzioni DDE di rete</span><span class="sxs-lookup"><span data-stu-id="296f7-148">Network DDE Functions</span></span>](network-dde-functions.md)
</dt> <dt>

[<span data-ttu-id="296f7-149">**NDDESHAREINFO**</span><span class="sxs-lookup"><span data-stu-id="296f7-149">**NDDESHAREINFO**</span></span>](nddeshareinfo-str.md)
</dt> <dt>

[<span data-ttu-id="296f7-150">**NDdeShareGetInfo**</span><span class="sxs-lookup"><span data-stu-id="296f7-150">**NDdeShareGetInfo**</span></span>](nddesharegetinfo.md)
</dt> </dl>

 

 




