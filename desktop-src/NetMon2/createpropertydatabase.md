---
description: La funzione CreatePropertyDatabase crea un database delle proprietà in cui sono archiviate le proprietà di un protocollo.
ms.assetid: 0a3be6ae-d7ce-4315-b4f2-b46bcfa25b69
title: Funzione CreatePropertyDatabase (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CreatePropertyDatabase
api_type:
- DllExport
api_location:
- Nmapi.dll
ms.openlocfilehash: 2955aa3367648c4e9e23fd748fa27d6343ef78a1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106311628"
---
# <a name="createpropertydatabase-function"></a><span data-ttu-id="c08b2-103">CreatePropertyDatabase (funzione)</span><span class="sxs-lookup"><span data-stu-id="c08b2-103">CreatePropertyDatabase function</span></span>

<span data-ttu-id="c08b2-104">La funzione **CreatePropertyDatabase** crea un database delle proprietà in cui sono archiviate le proprietà di un protocollo.</span><span class="sxs-lookup"><span data-stu-id="c08b2-104">The **CreatePropertyDatabase** function creates a property database that stores the properties of a protocol.</span></span>

## <a name="syntax"></a><span data-ttu-id="c08b2-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="c08b2-105">Syntax</span></span>


```C++
DWORD WINAPI CreatePropertyDatabase(
  _In_ HPROTOCOL hProtocol,
  _In_ DWORD     nProperties
);
```



## <a name="parameters"></a><span data-ttu-id="c08b2-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="c08b2-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c08b2-107">*hProtocol* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="c08b2-107">*hProtocol* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c08b2-108">Handle del protocollo associato al database.</span><span class="sxs-lookup"><span data-stu-id="c08b2-108">Handle of the protocol that is associated with the database.</span></span> <span data-ttu-id="c08b2-109">Quando Network Monitor chiama la funzione [Register](register-parser.md) , network monitor passa l'handle del protocollo alla DLL del parser.</span><span class="sxs-lookup"><span data-stu-id="c08b2-109">When Network Monitor calls the [Register](register-parser.md) function, Network Monitor passes the protocol handle to the parser DLL.</span></span>

</dd> <dt>

<span data-ttu-id="c08b2-110">*nProperties* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="c08b2-110">*nProperties* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c08b2-111">Numero di proprietà archiviate nel database.</span><span class="sxs-lookup"><span data-stu-id="c08b2-111">Number of properties stored in the database.</span></span> <span data-ttu-id="c08b2-112">Impostare questo parametro sul numero di proprietà supportate dal protocollo.</span><span class="sxs-lookup"><span data-stu-id="c08b2-112">Set this parameter to the number of properties that the protocol supports.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c08b2-113">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="c08b2-113">Return value</span></span>

<span data-ttu-id="c08b2-114">Se la funzione ha esito positivo, il valore restituito è NMERR \_ Success.</span><span class="sxs-lookup"><span data-stu-id="c08b2-114">If the function is successful, the return value is NMERR\_SUCCESS.</span></span>

<span data-ttu-id="c08b2-115">Se la funzione ha esito negativo, il valore restituito è un codice di errore.</span><span class="sxs-lookup"><span data-stu-id="c08b2-115">If the function is unsuccessful, the return value is an error code.</span></span>



| <span data-ttu-id="c08b2-116">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="c08b2-116">Return code</span></span>                                                                                             | <span data-ttu-id="c08b2-117">Descrizione</span><span class="sxs-lookup"><span data-stu-id="c08b2-117">Description</span></span>                                                                    |
|---------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="c08b2-118"><dt>**\_errore interno \_ NMERR**</dt></span><span class="sxs-lookup"><span data-stu-id="c08b2-118"><dt>**NMERR\_INTERNAL\_ERROR**</dt></span></span> </dl>   | <span data-ttu-id="c08b2-119">Si è verificato un errore interno.</span><span class="sxs-lookup"><span data-stu-id="c08b2-119">An internal error has occurred.</span></span><br/>                                     |
| <dl> <span data-ttu-id="c08b2-120"><dt>**\_HPOTOCOL NMERR non valido \_**</dt></span><span class="sxs-lookup"><span data-stu-id="c08b2-120"><dt>**NMERR\_INVALID\_HPOTOCOL**</dt></span></span> </dl> | <span data-ttu-id="c08b2-121">L'handle per il protocollo specificato in *hProtocol* non è valido.</span><span class="sxs-lookup"><span data-stu-id="c08b2-121">The handle to the protocol specified in *hProtocol* is invalid.</span></span><br/>     |
| <dl> <span data-ttu-id="c08b2-122"><dt>**\_ \_ \_ memoria insufficiente NMERR**</dt></span><span class="sxs-lookup"><span data-stu-id="c08b2-122"><dt>**NMERR\_OUT\_OF\_MEMORY**</dt></span></span> </dl>   | <span data-ttu-id="c08b2-123">Network Monitor non dispone di memoria sufficiente per creare il database.</span><span class="sxs-lookup"><span data-stu-id="c08b2-123">Network Monitor does not have enough memory to create the database.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="c08b2-124">Commenti</span><span class="sxs-lookup"><span data-stu-id="c08b2-124">Remarks</span></span>

<span data-ttu-id="c08b2-125">La funzione **CreatePropertyDatabase** deve essere chiamata solo quando si implementa la funzione [Register](register-parser.md) .</span><span class="sxs-lookup"><span data-stu-id="c08b2-125">The **CreatePropertyDatabase** function should be called only when implementing the [Register](register-parser.md) function.</span></span> <span data-ttu-id="c08b2-126">Il parser USA **CreatePropertyDatabase** per creare un database di proprietà che descrive le proprietà di un protocollo.</span><span class="sxs-lookup"><span data-stu-id="c08b2-126">The parser uses **CreatePropertyDatabase** to create a property database that describes the properties of a protocol.</span></span> <span data-ttu-id="c08b2-127">Network Monitor utilizza il database per interpretare le informazioni all'interno del protocollo.</span><span class="sxs-lookup"><span data-stu-id="c08b2-127">Network Monitor uses the database to interpret the information within the protocol.</span></span>

<span data-ttu-id="c08b2-128">La funzione **CreatePropertyDatabase** alloca le strutture che Network Monitor necessario per mantenere un database di proprietà.</span><span class="sxs-lookup"><span data-stu-id="c08b2-128">The **CreatePropertyDatabase** function allocates the structures that Network Monitor needs to maintain a property database.</span></span>

## <a name="requirements"></a><span data-ttu-id="c08b2-129">Requisiti</span><span class="sxs-lookup"><span data-stu-id="c08b2-129">Requirements</span></span>



| <span data-ttu-id="c08b2-130">Requisito</span><span class="sxs-lookup"><span data-stu-id="c08b2-130">Requirement</span></span> | <span data-ttu-id="c08b2-131">Valore</span><span class="sxs-lookup"><span data-stu-id="c08b2-131">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="c08b2-132">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="c08b2-132">Minimum supported client</span></span><br/> | <span data-ttu-id="c08b2-133">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="c08b2-133">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="c08b2-134">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="c08b2-134">Minimum supported server</span></span><br/> | <span data-ttu-id="c08b2-135">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="c08b2-135">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="c08b2-136">Intestazione</span><span class="sxs-lookup"><span data-stu-id="c08b2-136">Header</span></span><br/>                   | <dl> <span data-ttu-id="c08b2-137"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="c08b2-137"><dt>Netmon.h</dt></span></span> </dl>  |
| <span data-ttu-id="c08b2-138">Libreria</span><span class="sxs-lookup"><span data-stu-id="c08b2-138">Library</span></span><br/>                  | <dl> <span data-ttu-id="c08b2-139"><dt>Nmap. lib</dt></span><span class="sxs-lookup"><span data-stu-id="c08b2-139"><dt>Nmapi.lib</dt></span></span> </dl> |
| <span data-ttu-id="c08b2-140">DLL</span><span class="sxs-lookup"><span data-stu-id="c08b2-140">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c08b2-141"><dt>Nmapi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c08b2-141"><dt>Nmapi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c08b2-142">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="c08b2-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c08b2-143">Registra</span><span class="sxs-lookup"><span data-stu-id="c08b2-143">Register</span></span>](register-parser.md)
</dt> </dl>

 

 




