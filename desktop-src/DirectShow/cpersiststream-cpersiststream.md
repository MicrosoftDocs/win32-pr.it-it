---
description: 'Costruttore CPersistStream.CPersistStream : metodo costruttore.'
ms.assetid: 48143a61-5ba7-4bf9-bffa-244f2769144d
title: Costruttore CPersistStream.CPersistStream (Pstream.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CPersistStream.CPersistStream
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 9e3be9233d76929ebfcb79121c60ef6c1af35b56
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108085609"
---
# <a name="cpersiststreamcpersiststream-constructor"></a><span data-ttu-id="707e3-103">Costruttore CPersistStream.CPersistStream</span><span class="sxs-lookup"><span data-stu-id="707e3-103">CPersistStream.CPersistStream constructor</span></span>

<span data-ttu-id="707e3-104">Metodo del costruttore.</span><span class="sxs-lookup"><span data-stu-id="707e3-104">Constructor method.</span></span>

## <a name="syntax"></a><span data-ttu-id="707e3-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="707e3-105">Syntax</span></span>


```C++
CPersistStream(
   IUnknown *pUnk,
   HRESULT  *phr
);
```



## <a name="parameters"></a><span data-ttu-id="707e3-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="707e3-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="707e3-107">*Punk*</span><span class="sxs-lookup"><span data-stu-id="707e3-107">*pUnk*</span></span> 
</dt> <dd>

<span data-ttu-id="707e3-108">Puntatore **all'interfaccia IUnknown** dell'oggetto delegante.</span><span class="sxs-lookup"><span data-stu-id="707e3-108">Pointer to the **IUnknown** interface of the delegating object.</span></span>

</dd> <dt>

<span data-ttu-id="707e3-109">*Phr*</span><span class="sxs-lookup"><span data-stu-id="707e3-109">*phr*</span></span> 
</dt> <dd>

<span data-ttu-id="707e3-110">Puntatore al valore restituito COM generale.</span><span class="sxs-lookup"><span data-stu-id="707e3-110">Pointer to the general COM return value.</span></span> <span data-ttu-id="707e3-111">Questo valore viene modificato solo se questa funzione ha esito negativo.</span><span class="sxs-lookup"><span data-stu-id="707e3-111">This value is changed only if this function fails.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="707e3-112">Requisiti</span><span class="sxs-lookup"><span data-stu-id="707e3-112">Requirements</span></span>



| <span data-ttu-id="707e3-113">Requisito</span><span class="sxs-lookup"><span data-stu-id="707e3-113">Requirement</span></span> | <span data-ttu-id="707e3-114">Valore</span><span class="sxs-lookup"><span data-stu-id="707e3-114">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="707e3-115">Intestazione</span><span class="sxs-lookup"><span data-stu-id="707e3-115">Header</span></span><br/>  | <dl> <span data-ttu-id="707e3-116"><dt>Pstream.h (include Streams.h)</dt></span><span class="sxs-lookup"><span data-stu-id="707e3-116"><dt>Pstream.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="707e3-117">Libreria</span><span class="sxs-lookup"><span data-stu-id="707e3-117">Library</span></span><br/> | <dl> <span data-ttu-id="707e3-118"><dt>Strmbase.lib (build di vendita al dettaglio); </dt> <dt>Strmbasd.lib (build di debug)</dt></span><span class="sxs-lookup"><span data-stu-id="707e3-118"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="707e3-119">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="707e3-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="707e3-120">**Classe CPersistStream**</span><span class="sxs-lookup"><span data-stu-id="707e3-120">**CPersistStream Class**</span></span>](cpersiststream.md)
</dt> </dl>

 

 




