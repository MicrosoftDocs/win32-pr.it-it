---
description: Tipo opaco e portabile per supportare l'utilizzo della sintassi dell'inizializzatore C/C++ per caricare valori integer in un'istanza di tipo XMVECTOR.
ms.assetid: 6564030e-b6e9-0c4f-4e2a-4132e4264c94
title: Tipo di dati XMVECTORI32 (DirectXMath. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7ac36caf97a62037223840e9220876f1c7a1f09a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106333232"
---
# <a name="xmvectori32-data-type"></a><span data-ttu-id="a86d2-103">Tipo di dati XMVECTORI32</span><span class="sxs-lookup"><span data-stu-id="a86d2-103">XMVECTORI32 Data Type</span></span>

<span data-ttu-id="a86d2-104">Tipo opaco e portabile per supportare l'utilizzo della sintassi dell'inizializzatore C/C++ per caricare valori integer in un'istanza di tipo [**XMVECTOR**](xmvector-data-type.md) .</span><span class="sxs-lookup"><span data-stu-id="a86d2-104">An opaque, portable type to support the use of C/C++ initializer syntax to load integer values into an instance of [**XMVECTOR**](xmvector-data-type.md) type.</span></span>


```C++
typedef XMVECTORI32 vectori32;
```



## <a name="remarks"></a><span data-ttu-id="a86d2-105">Commenti</span><span class="sxs-lookup"><span data-stu-id="a86d2-105">Remarks</span></span>

<span data-ttu-id="a86d2-106">Per un elenco di funzionalità aggiuntive, ad esempio costruttori e operatori, disponibili con `XMVECTORI32` durante la programmazione in C++, vedere [XMVECTORI32 Extensions](ovw-xmvectori32-extensions.md).</span><span class="sxs-lookup"><span data-stu-id="a86d2-106">For a list of additional functionality, such as constructors and operators, available using `XMVECTORI32` when programming in C++, see [XMVECTORI32 Extensions](ovw-xmvectori32-extensions.md).</span></span>

<span data-ttu-id="a86d2-107">Le strutture [**XMVECTORF32**](xmvectorf32-data-type.md), [**XMVECTORU32**](xmvectoru32-data-type.md), **XMVECTORI32** e [**XMVECTORU8**](xmvectoru8-data-type.md) sono fornite come meccanismo per la creazione di [**XMVECTOR**](xmvector-data-type.md) da diversi tipi di dati costanti (a virgola mobile, Unsigned Integer, Integer e byte) tramite inizializzatori.</span><span class="sxs-lookup"><span data-stu-id="a86d2-107">The [**XMVECTORF32**](xmvectorf32-data-type.md), [**XMVECTORU32**](xmvectoru32-data-type.md), **XMVECTORI32**, and [**XMVECTORU8**](xmvectoru8-data-type.md) structures are provided as a mechanism for creating [**XMVECTOR**](xmvector-data-type.md) from different constant data types (floating point, unsigned integer, integer, and byte) using initializers.</span></span>

<span data-ttu-id="a86d2-108">Questa operazione è necessaria per supportare [**XMVECTOR**](xmvector-data-type.md), in quanto non supporta gli inizializzatori, per motivi di portabilità e di ottimizzazione.</span><span class="sxs-lookup"><span data-stu-id="a86d2-108">This is necessary to support [**XMVECTOR**](xmvector-data-type.md), as it does not itself support initializers, for portability and optimization reasons.</span></span>

<span data-ttu-id="a86d2-109">Ad esempio:</span><span class="sxs-lookup"><span data-stu-id="a86d2-109">For example:</span></span>


```
XMVECTOR data;
XMVECTORI32 intVector = { -1, 5, 33, 0 };
data = intVector;
```



<span data-ttu-id="a86d2-110">**Spazio dei nomi**: usare DirectX</span><span class="sxs-lookup"><span data-stu-id="a86d2-110">**Namespace**: Use DirectX</span></span>

### <a name="platform-requirements"></a><span data-ttu-id="a86d2-111">Requisiti della piattaforma</span><span class="sxs-lookup"><span data-stu-id="a86d2-111">Platform Requirements</span></span>

<span data-ttu-id="a86d2-112">Microsoft Visual Studio 2010 o Microsoft Visual Studio 2012 con la Windows SDK per Windows 8.</span><span class="sxs-lookup"><span data-stu-id="a86d2-112">Microsoft Visual Studio 2010 or Microsoft Visual Studio 2012 with the Windows SDK for Windows 8.</span></span> <span data-ttu-id="a86d2-113">Supportato per le app desktop Win32, le app di Windows Store e le app Windows Phone 8.</span><span class="sxs-lookup"><span data-stu-id="a86d2-113">Supported for Win32 desktop apps, Windows Store apps, and Windows Phone 8 apps.</span></span>

## <a name="requirements"></a><span data-ttu-id="a86d2-114">Requisiti</span><span class="sxs-lookup"><span data-stu-id="a86d2-114">Requirements</span></span>



| <span data-ttu-id="a86d2-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="a86d2-115">Requirement</span></span> | <span data-ttu-id="a86d2-116">Valore</span><span class="sxs-lookup"><span data-stu-id="a86d2-116">Value</span></span> |
|-------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="a86d2-117">Intestazione</span><span class="sxs-lookup"><span data-stu-id="a86d2-117">Header</span></span><br/> | <dl> <span data-ttu-id="a86d2-118"><dt>DirectXMath. h</dt></span><span class="sxs-lookup"><span data-stu-id="a86d2-118"><dt>DirectXMath.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a86d2-119">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="a86d2-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a86d2-120">Tipi di libreria DirectXMath</span><span class="sxs-lookup"><span data-stu-id="a86d2-120">DirectXMath Library Types</span></span>](ovw-xnamath-reference-types.md)
</dt> <dt>

[<span data-ttu-id="a86d2-121">**Tipo di dati XMVECTOR**</span><span class="sxs-lookup"><span data-stu-id="a86d2-121">**XMVECTOR Data Type**</span></span>](xmvector-data-type.md)
</dt> <dt>

[<span data-ttu-id="a86d2-122">**Tipo di dati XMVECTORF32**</span><span class="sxs-lookup"><span data-stu-id="a86d2-122">**XMVECTORF32 Data Type**</span></span>](xmvectorf32-data-type.md)
</dt> <dt>

[<span data-ttu-id="a86d2-123">**Tipo di dati XMVECTORU32**</span><span class="sxs-lookup"><span data-stu-id="a86d2-123">**XMVECTORU32 Data Type**</span></span>](xmvectoru32-data-type.md)
</dt> <dt>

[<span data-ttu-id="a86d2-124">**Tipo di dati XMVECTORU8**</span><span class="sxs-lookup"><span data-stu-id="a86d2-124">**XMVECTORU8 Data Type**</span></span>](xmvectoru8-data-type.md)
</dt> <dt>

[<span data-ttu-id="a86d2-125">**Tipo di dati XMVECTORI32**</span><span class="sxs-lookup"><span data-stu-id="a86d2-125">**XMVECTORI32 Data Type**</span></span>](xmvectori32-data-type.md)
</dt> </dl>

 

 




