---
description: Puntatore a una funzione che viene chiamata dal punto di ingresso della DLL.
ms.assetid: 30196657-38ab-42ca-b673-b0894999e566
title: Puntatore alla funzione LPFNInitRoutine (ComBase. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- LPFNInitRoutine
api_type:
- UserDefined
api_location:
- Combase.h
ms.openlocfilehash: 375660399180196e2434030ea7551733affc4062
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106327417"
---
# <a name="lpfninitroutine-function-pointer"></a><span data-ttu-id="175fb-103">Puntatore alla funzione LPFNInitRoutine</span><span class="sxs-lookup"><span data-stu-id="175fb-103">LPFNInitRoutine function pointer</span></span>

<span data-ttu-id="175fb-104">Puntatore a una funzione che viene chiamata dal punto di ingresso della DLL.</span><span class="sxs-lookup"><span data-stu-id="175fb-104">Pointer to a function that gets called from the DLL entry point.</span></span>

## <a name="syntax"></a><span data-ttu-id="175fb-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="175fb-105">Syntax</span></span>


```C++
typedef void ( CALLBACK *LPFNInitRoutine)(
         BOOL  bLoading,
   const CLSID *rclsid
);
```



## <a name="parameters"></a><span data-ttu-id="175fb-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="175fb-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="175fb-107">*bLoading*</span><span class="sxs-lookup"><span data-stu-id="175fb-107">*bLoading*</span></span> 
</dt> <dd>

<span data-ttu-id="175fb-108">**True** quando la dll viene caricata, **false** quando la dll viene scaricata.</span><span class="sxs-lookup"><span data-stu-id="175fb-108">**TRUE** when the DLL is loaded, **FALSE** when the DLL is unloaded.</span></span>

</dd> <dt>

<span data-ttu-id="175fb-109">*rclsid*</span><span class="sxs-lookup"><span data-stu-id="175fb-109">*rclsid*</span></span> 
</dt> <dd>

<span data-ttu-id="175fb-110">Puntatore al CLISD dell'oggetto, specificato nella variabile membro [**\_ CLSID CFactoryTemplate:: m**](cfactorytemplate-m-clsid.md) .</span><span class="sxs-lookup"><span data-stu-id="175fb-110">Pointer to the object's CLISD, specified in the [**CFactoryTemplate::m\_ClsID**](cfactorytemplate-m-clsid.md) member variable.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="175fb-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="175fb-111">Return value</span></span>

<span data-ttu-id="175fb-112">Questo puntatore a funzione non restituisce un valore.</span><span class="sxs-lookup"><span data-stu-id="175fb-112">This function pointer does not return a value.</span></span>

## <a name="requirements"></a><span data-ttu-id="175fb-113">Requisiti</span><span class="sxs-lookup"><span data-stu-id="175fb-113">Requirements</span></span>



| <span data-ttu-id="175fb-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="175fb-114">Requirement</span></span> | <span data-ttu-id="175fb-115">Valore</span><span class="sxs-lookup"><span data-stu-id="175fb-115">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="175fb-116">Intestazione</span><span class="sxs-lookup"><span data-stu-id="175fb-116">Header</span></span><br/> | <dl> <span data-ttu-id="175fb-117"><dt>ComBase. h (Includi Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="175fb-117"><dt>Combase.h (include Streams.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="175fb-118">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="175fb-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="175fb-119">**Classe CFactoryTemplate**</span><span class="sxs-lookup"><span data-stu-id="175fb-119">**CFactoryTemplate Class**</span></span>](cfactorytemplate.md)
</dt> </dl>

 

 




