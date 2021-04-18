---
description: Elimina una condivisione DDE da gestione database di condivisione DDE (DSDM).
ms.assetid: 3240f4b1-2625-46bc-9bbe-27737c59df81
title: Funzione NDdeShareDel (nddeapi. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- NDdeShareDel
- NDdeShareDelA
- NDdeShareDelW
api_type:
- DllExport
api_location:
- Nddeapi.dll
ms.openlocfilehash: 2d57307c157c532e124699b6bfb2ed666f374722
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106305711"
---
# <a name="nddesharedel-function"></a><span data-ttu-id="35a55-103">NDdeShareDel (funzione)</span><span class="sxs-lookup"><span data-stu-id="35a55-103">NDdeShareDel function</span></span>

<span data-ttu-id="35a55-104">\[Il DDE di rete non è più supportato.</span><span class="sxs-lookup"><span data-stu-id="35a55-104">\[Network DDE is no longer supported.</span></span> <span data-ttu-id="35a55-105">Nddeapi.dll è presente in Windows Vista, ma tutte le chiamate di funzione restituiscono NDDE \_ non \_ implementate.\]</span><span class="sxs-lookup"><span data-stu-id="35a55-105">Nddeapi.dll is present on Windows Vista, but all function calls return NDDE\_NOT\_IMPLEMENTED.\]</span></span>

<span data-ttu-id="35a55-106">Elimina una condivisione DDE da gestione database di condivisione DDE (DSDM).</span><span class="sxs-lookup"><span data-stu-id="35a55-106">Deletes a DDE share from the DDE share database manager (DSDM).</span></span>

## <a name="syntax"></a><span data-ttu-id="35a55-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="35a55-107">Syntax</span></span>


```C++
UINT NDdeShareDel(
  _In_ LPTSTR lpszServer,
  _In_ LPTSTR lpszShareName,
  _In_ UINT   wReserved
);
```



## <a name="parameters"></a><span data-ttu-id="35a55-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="35a55-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="35a55-109">*lpszServer* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="35a55-109">*lpszServer* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="35a55-110">Nome del server di cui è necessario modificare il DSDM.</span><span class="sxs-lookup"><span data-stu-id="35a55-110">The name of the server whose DSDM is to be modified.</span></span>

</dd> <dt>

<span data-ttu-id="35a55-111">*lpszShareName* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="35a55-111">*lpszShareName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="35a55-112">Nome della condivisione da eliminare da DSDM.</span><span class="sxs-lookup"><span data-stu-id="35a55-112">The name of the share to be deleted from the DSDM.</span></span> <span data-ttu-id="35a55-113">Questo parametro non può essere **null**.</span><span class="sxs-lookup"><span data-stu-id="35a55-113">This parameter cannot be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="35a55-114">*wReserved* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="35a55-114">*wReserved* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="35a55-115">Riservato.</span><span class="sxs-lookup"><span data-stu-id="35a55-115">Reserved.</span></span> <span data-ttu-id="35a55-116">Questo parametro deve essere zero.</span><span class="sxs-lookup"><span data-stu-id="35a55-116">This parameter must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="35a55-117">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="35a55-117">Return value</span></span>

<span data-ttu-id="35a55-118">Se la funzione ha esito positivo, il valore restituito è NDDE \_ senza \_ errori.</span><span class="sxs-lookup"><span data-stu-id="35a55-118">If the function succeeds, the return value is NDDE\_NO\_ERROR.</span></span>

<span data-ttu-id="35a55-119">Se la funzione ha esito negativo, il valore restituito è un codice di errore che può essere convertito in un messaggio di errore di testo chiamando [**NDdeGetErrorString**](nddegeterrorstring.md).</span><span class="sxs-lookup"><span data-stu-id="35a55-119">If the function fails, the return value is an error code which can be translated into a text error message by calling [**NDdeGetErrorString**](nddegeterrorstring.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="35a55-120">Commenti</span><span class="sxs-lookup"><span data-stu-id="35a55-120">Remarks</span></span>

<span data-ttu-id="35a55-121">Per eliminare una condivisione DDE dal DSDM, è necessario disporre del privilegio appropriato.</span><span class="sxs-lookup"><span data-stu-id="35a55-121">To delete a DDE share from the DSDM, you must have the appropriate privilege.</span></span> <span data-ttu-id="35a55-122">Il creatore della condivisione dispone del privilegio DELETE.</span><span class="sxs-lookup"><span data-stu-id="35a55-122">The share creator has delete privilege.</span></span>

## <a name="requirements"></a><span data-ttu-id="35a55-123">Requisiti</span><span class="sxs-lookup"><span data-stu-id="35a55-123">Requirements</span></span>



| <span data-ttu-id="35a55-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="35a55-124">Requirement</span></span> | <span data-ttu-id="35a55-125">Valore</span><span class="sxs-lookup"><span data-stu-id="35a55-125">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="35a55-126">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="35a55-126">Minimum supported client</span></span><br/> | <span data-ttu-id="35a55-127">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="35a55-127">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="35a55-128">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="35a55-128">Minimum supported server</span></span><br/> | <span data-ttu-id="35a55-129">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="35a55-129">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="35a55-130">Intestazione</span><span class="sxs-lookup"><span data-stu-id="35a55-130">Header</span></span><br/>                   | <dl> <span data-ttu-id="35a55-131"><dt>Nddeapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="35a55-131"><dt>Nddeapi.h</dt></span></span> </dl>   |
| <span data-ttu-id="35a55-132">Libreria</span><span class="sxs-lookup"><span data-stu-id="35a55-132">Library</span></span><br/>                  | <dl> <span data-ttu-id="35a55-133"><dt>Nddeapi. lib</dt></span><span class="sxs-lookup"><span data-stu-id="35a55-133"><dt>Nddeapi.lib</dt></span></span> </dl> |
| <span data-ttu-id="35a55-134">DLL</span><span class="sxs-lookup"><span data-stu-id="35a55-134">DLL</span></span><br/>                      | <dl> <span data-ttu-id="35a55-135"><dt>Nddeapi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="35a55-135"><dt>Nddeapi.dll</dt></span></span> </dl> |
| <span data-ttu-id="35a55-136">Nomi Unicode e ANSI</span><span class="sxs-lookup"><span data-stu-id="35a55-136">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="35a55-137">**NDdeShareDelW** (Unicode) e **NDdeShareDelA** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="35a55-137">**NDdeShareDelW** (Unicode) and **NDdeShareDelA** (ANSI)</span></span><br/>                    |



## <a name="see-also"></a><span data-ttu-id="35a55-138">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="35a55-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="35a55-139">Panoramica di Dynamic Data Exchange di rete</span><span class="sxs-lookup"><span data-stu-id="35a55-139">Network Dynamic Data Exchange Overview</span></span>](network-dynamic-data-exchange.md)
</dt> <dt>

[<span data-ttu-id="35a55-140">Funzioni DDE di rete</span><span class="sxs-lookup"><span data-stu-id="35a55-140">Network DDE Functions</span></span>](network-dde-functions.md)
</dt> </dl>

 

 




