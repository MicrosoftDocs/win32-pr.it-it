---
description: La funzione GetProperty restituisce un handle per una proprietà specificata.
ms.assetid: e77ca20a-55df-4d31-aa6d-2c00695f1d6e
title: Funzione GetProperty (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GetProperty
api_type:
- DllExport
api_location:
- Nmapi.dll
ms.openlocfilehash: 297d68d68731181ed56324a4e1d174467f622e13
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103966463"
---
# <a name="getproperty-function"></a><span data-ttu-id="62a83-103">GetProperty (funzione)</span><span class="sxs-lookup"><span data-stu-id="62a83-103">GetProperty function</span></span>

<span data-ttu-id="62a83-104">La funzione **GetProperty** restituisce un handle per una proprietà specificata.</span><span class="sxs-lookup"><span data-stu-id="62a83-104">The **GetProperty** function returns a handle to a given property.</span></span>

## <a name="syntax"></a><span data-ttu-id="62a83-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="62a83-105">Syntax</span></span>


```C++
HPROPERTY WINAPI GetProperty(
  _In_ HPROTOCOL hProtocol,
  _In_ LPSTR     PropertyName
);
```



## <a name="parameters"></a><span data-ttu-id="62a83-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="62a83-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="62a83-107">*hProtocol* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="62a83-107">*hProtocol* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="62a83-108">Handle per il protocollo.</span><span class="sxs-lookup"><span data-stu-id="62a83-108">Handle to the protocol.</span></span>

</dd> <dt>

<span data-ttu-id="62a83-109">*PropertyName* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="62a83-109">*PropertyName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="62a83-110">Nome della proprietà (ad esempio, **checksum**).</span><span class="sxs-lookup"><span data-stu-id="62a83-110">Name of the property (for example, **Checksum**).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="62a83-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="62a83-111">Return value</span></span>

<span data-ttu-id="62a83-112">Se la funzione ha esito positivo, il valore restituito è l'handle della proprietà.</span><span class="sxs-lookup"><span data-stu-id="62a83-112">If the function is successful, the return value is the handle to the property.</span></span>

<span data-ttu-id="62a83-113">Se la funzione ha esito negativo, il valore restituito è **null**.</span><span class="sxs-lookup"><span data-stu-id="62a83-113">If the function is unsuccessful, the return value is **NULL**.</span></span>

## <a name="remarks"></a><span data-ttu-id="62a83-114">Commenti</span><span class="sxs-lookup"><span data-stu-id="62a83-114">Remarks</span></span>

<span data-ttu-id="62a83-115">La funzione **GetProperty** può essere utilizzata per ottenere l'handle della proprietà necessario per individuare le istanze della proprietà.</span><span class="sxs-lookup"><span data-stu-id="62a83-115">The **GetProperty** function can be used to obtain the property handle needed to locate instances of the property.</span></span> <span data-ttu-id="62a83-116">Le funzioni utilizzate per individuare le istanze di proprietà sono [FindPropertyInstance](findpropertyinstance.md) (che individua la prima istanza) e [FindPropertyInstanceRestart](findpropertyinstancerestart.md) (che individua l'istanza successiva).</span><span class="sxs-lookup"><span data-stu-id="62a83-116">The functions used to locate property instances are [FindPropertyInstance](findpropertyinstance.md) (which locates the first instance) and [FindPropertyInstanceRestart](findpropertyinstancerestart.md) (which locates the next instance).</span></span>

<span data-ttu-id="62a83-117">Gli [*esperti*](e.md) e i [*parser*](p.md) possono chiamare la funzione **GetProperty** .</span><span class="sxs-lookup"><span data-stu-id="62a83-117">[*Experts*](e.md) and [*parsers*](p.md) can call the **GetProperty** function.</span></span>

## <a name="requirements"></a><span data-ttu-id="62a83-118">Requisiti</span><span class="sxs-lookup"><span data-stu-id="62a83-118">Requirements</span></span>



| <span data-ttu-id="62a83-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="62a83-119">Requirement</span></span> | <span data-ttu-id="62a83-120">Valore</span><span class="sxs-lookup"><span data-stu-id="62a83-120">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="62a83-121">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="62a83-121">Minimum supported client</span></span><br/> | <span data-ttu-id="62a83-122">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="62a83-122">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="62a83-123">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="62a83-123">Minimum supported server</span></span><br/> | <span data-ttu-id="62a83-124">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="62a83-124">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="62a83-125">Intestazione</span><span class="sxs-lookup"><span data-stu-id="62a83-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="62a83-126"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="62a83-126"><dt>Netmon.h</dt></span></span> </dl>  |
| <span data-ttu-id="62a83-127">Libreria</span><span class="sxs-lookup"><span data-stu-id="62a83-127">Library</span></span><br/>                  | <dl> <span data-ttu-id="62a83-128"><dt>Nmap. lib</dt></span><span class="sxs-lookup"><span data-stu-id="62a83-128"><dt>Nmapi.lib</dt></span></span> </dl> |
| <span data-ttu-id="62a83-129">DLL</span><span class="sxs-lookup"><span data-stu-id="62a83-129">DLL</span></span><br/>                      | <dl> <span data-ttu-id="62a83-130"><dt>Nmapi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="62a83-130"><dt>Nmapi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="62a83-131">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="62a83-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="62a83-132">FindPropertyInstance</span><span class="sxs-lookup"><span data-stu-id="62a83-132">FindPropertyInstance</span></span>](findpropertyinstance.md)
</dt> <dt>

[<span data-ttu-id="62a83-133">FindPropertyInstanceRestart</span><span class="sxs-lookup"><span data-stu-id="62a83-133">FindPropertyInstanceRestart</span></span>](findpropertyinstancerestart.md)
</dt> </dl>

 

 




