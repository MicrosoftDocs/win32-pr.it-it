---
description: Ottiene l'ID di interfaccia di un riferimento agile a un oggetto.
ms.assetid: 627A7EE4-CFEF-47F6-BA99-51BEB78C5D55
title: 'Metodo IAgileReference:: Resolve'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAgileReference.Resolve
api_type:
- COM
api_location:
- objidl.h
ms.openlocfilehash: 1c3ac95802a44f4305abb24566744ad98c67b174
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106307080"
---
# <a name="iagilereferenceresolve-method"></a><span data-ttu-id="4e1c7-103">Metodo IAgileReference:: Resolve</span><span class="sxs-lookup"><span data-stu-id="4e1c7-103">IAgileReference::Resolve method</span></span>

<span data-ttu-id="4e1c7-104">Ottiene l'ID di interfaccia di un riferimento agile a un oggetto.</span><span class="sxs-lookup"><span data-stu-id="4e1c7-104">Gets the interface ID of an agile reference to an object.</span></span>

## <a name="syntax"></a><span data-ttu-id="4e1c7-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="4e1c7-105">Syntax</span></span>


```C++
HRESULT Resolve(
  [in]          REFIID riid,
  [out, retval] void   **ppvObjectReference
);
```



## <a name="parameters"></a><span data-ttu-id="4e1c7-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="4e1c7-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4e1c7-107">*riid* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="4e1c7-107">*riid* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4e1c7-108">ID di interfaccia dell'interfaccia da recuperare dal riferimento agile.</span><span class="sxs-lookup"><span data-stu-id="4e1c7-108">The interface ID of the interface to be retrieved from the agile reference.</span></span> <span data-ttu-id="4e1c7-109">Non è necessario che corrisponda all'interfaccia registrata.</span><span class="sxs-lookup"><span data-stu-id="4e1c7-109">It is not required to be the same as the registered interface.</span></span>

</dd> <dt>

<span data-ttu-id="4e1c7-110">*ppvObjectReference* \[ out, retval\]</span><span class="sxs-lookup"><span data-stu-id="4e1c7-110">*ppvObjectReference* \[out, retval\]</span></span>
</dt> <dd>

<span data-ttu-id="4e1c7-111">Al termine, \* *ppvObjectReference* è un puntatore all'interfaccia specificata da *riid*.</span><span class="sxs-lookup"><span data-stu-id="4e1c7-111">On successful completion, \**ppvObjectReference* is a pointer to the interface specified by *riid*.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4e1c7-112">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="4e1c7-112">Return value</span></span>

<span data-ttu-id="4e1c7-113">Questo metodo può restituire uno di questi valori.</span><span class="sxs-lookup"><span data-stu-id="4e1c7-113">This method can return one of these values.</span></span>



| <span data-ttu-id="4e1c7-114">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="4e1c7-114">Return value</span></span>                                                                              | <span data-ttu-id="4e1c7-115">Descrizione</span><span class="sxs-lookup"><span data-stu-id="4e1c7-115">Description</span></span>                                                                    |
|-------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="4e1c7-116"><dt>\_OK</dt></span><span class="sxs-lookup"><span data-stu-id="4e1c7-116"><dt>S\_OK</dt></span></span> </dl>          | <span data-ttu-id="4e1c7-117">Metodo completato correttamente.</span><span class="sxs-lookup"><span data-stu-id="4e1c7-117">The method completed successfully.</span></span><br/>                                  |
| <dl> <span data-ttu-id="4e1c7-118"><dt>E \_ NOinterface</dt></span><span class="sxs-lookup"><span data-stu-id="4e1c7-118"><dt>E\_NOINTERFACE</dt></span></span> </dl> | <span data-ttu-id="4e1c7-119">L'interfaccia richiesta non è implementata nell'oggetto registrato.</span><span class="sxs-lookup"><span data-stu-id="4e1c7-119">The requested interface isn't implemented on the registered object.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="4e1c7-120">Commenti</span><span class="sxs-lookup"><span data-stu-id="4e1c7-120">Remarks</span></span>

<span data-ttu-id="4e1c7-121">Chiamare la funzione [**RoGetAgileReference**](/windows/desktop/api/ComBaseApi/nf-combaseapi-rogetagilereference) per creare un riferimento agile a un oggetto.</span><span class="sxs-lookup"><span data-stu-id="4e1c7-121">Call the [**RoGetAgileReference**](/windows/desktop/api/ComBaseApi/nf-combaseapi-rogetagilereference) function to create an agile reference to an object.</span></span> <span data-ttu-id="4e1c7-122">Chiamare il metodo **Resolve** per localizzare l'oggetto nell'Apartment in cui viene chiamata la **risoluzione** .</span><span class="sxs-lookup"><span data-stu-id="4e1c7-122">Call the **Resolve** method to localize the object into the apartment in which **Resolve** is called.</span></span>

## <a name="requirements"></a><span data-ttu-id="4e1c7-123">Requisiti</span><span class="sxs-lookup"><span data-stu-id="4e1c7-123">Requirements</span></span>



| <span data-ttu-id="4e1c7-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="4e1c7-124">Requirement</span></span> | <span data-ttu-id="4e1c7-125">Valore</span><span class="sxs-lookup"><span data-stu-id="4e1c7-125">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------|
| <span data-ttu-id="4e1c7-126">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="4e1c7-126">Minimum supported client</span></span><br/> | <span data-ttu-id="4e1c7-127">App \[ desktop di Windows 8.1 app \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="4e1c7-127">Windows 8.1 \[desktop apps \| UWP apps\]</span></span><br/>            |
| <span data-ttu-id="4e1c7-128">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="4e1c7-128">Minimum supported server</span></span><br/> | <span data-ttu-id="4e1c7-129">App desktop di Windows Server 2012 R2 \[ \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="4e1c7-129">Windows Server 2012 R2 \[desktop apps \| UWP apps\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="4e1c7-130">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="4e1c7-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4e1c7-131">**IAgileReference**</span><span class="sxs-lookup"><span data-stu-id="4e1c7-131">**IAgileReference**</span></span>](/windows/desktop/api/objidl/nn-objidl-iagilereference)
</dt> <dt>

[<span data-ttu-id="4e1c7-132">**RoGetAgileReference**</span><span class="sxs-lookup"><span data-stu-id="4e1c7-132">**RoGetAgileReference**</span></span>](/windows/desktop/api/ComBaseApi/nf-combaseapi-rogetagilereference)
</dt> </dl>

 

 




