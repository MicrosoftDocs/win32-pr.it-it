---
description: Verifica l'esistenza di tutti i sottoscrittori temporanei nell'archivio dati. Chiamando questo metodo, è possibile verificare che tutti i sottoscrittori temporanei elencati nell'archivio dati siano attivi.
ms.assetid: fffdde33-e960-42ef-a089-8ea8a6f33d52
title: 'Metodo IEventSystem2:: VerifyTransientSubscribers'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IEventSystem2.VerifyTransientSubscribers
api_type:
- COM
api_location: ''
ms.openlocfilehash: 4415f405b95f341b645ca1dccbf254df2ffc7167
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103966072"
---
# <a name="ieventsystem2verifytransientsubscribers-method"></a><span data-ttu-id="d650c-104">Metodo IEventSystem2:: VerifyTransientSubscribers</span><span class="sxs-lookup"><span data-stu-id="d650c-104">IEventSystem2::VerifyTransientSubscribers method</span></span>

<span data-ttu-id="d650c-105">Verifica l'esistenza di tutti i sottoscrittori temporanei nell'archivio dati.</span><span class="sxs-lookup"><span data-stu-id="d650c-105">Verifies the existence of all transient subscribers in the data store.</span></span> <span data-ttu-id="d650c-106">Chiamando questo metodo, è possibile verificare che tutti i sottoscrittori temporanei elencati nell'archivio dati siano attivi.</span><span class="sxs-lookup"><span data-stu-id="d650c-106">By calling this method, you can ensure that all transient subscribers listed in the data store are active.</span></span>

## <a name="syntax"></a><span data-ttu-id="d650c-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="d650c-107">Syntax</span></span>


```C++
HRESULT VerifyTransientSubscribers();
```



## <a name="parameters"></a><span data-ttu-id="d650c-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="d650c-108">Parameters</span></span>

<span data-ttu-id="d650c-109">Questo metodo non presenta parametri.</span><span class="sxs-lookup"><span data-stu-id="d650c-109">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="d650c-110">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="d650c-110">Return value</span></span>

<span data-ttu-id="d650c-111">Questo metodo può restituire i valori restituiti standard E \_ INVALIDARG, e \_ OutOfMemory, e \_ imprevisto, e ha \_ esito negativo e S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="d650c-111">This method can return the standard return values E\_INVALIDARG, E\_OUTOFMEMORY, E\_UNEXPECTED, E\_FAIL, and S\_OK.</span></span>

## <a name="requirements"></a><span data-ttu-id="d650c-112">Requisiti</span><span class="sxs-lookup"><span data-stu-id="d650c-112">Requirements</span></span>



| <span data-ttu-id="d650c-113">Requisito</span><span class="sxs-lookup"><span data-stu-id="d650c-113">Requirement</span></span> | <span data-ttu-id="d650c-114">Valore</span><span class="sxs-lookup"><span data-stu-id="d650c-114">Value</span></span> |
|-------------------------------------|------------------------------------------------------------|
| <span data-ttu-id="d650c-115">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="d650c-115">Minimum supported client</span></span><br/> | <span data-ttu-id="d650c-116">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="d650c-116">Windows 2000 Professional \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="d650c-117">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="d650c-117">Minimum supported server</span></span><br/> | <span data-ttu-id="d650c-118">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="d650c-118">Windows 2000 Server \[desktop apps only\]</span></span><br/>       |



## <a name="see-also"></a><span data-ttu-id="d650c-119">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="d650c-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d650c-120">**IEventSystem2**</span><span class="sxs-lookup"><span data-stu-id="d650c-120">**IEventSystem2**</span></span>](ieventsystem2.md)
</dt> </dl>

 

 




