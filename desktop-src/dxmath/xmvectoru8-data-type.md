---
description: Tipo opaco e portabile per supportare l'uso della sintassi dell'inizializzatore C/C++ per caricare \_ i valori Uint8 in un'istanza di tipo XMVECTOR.
ms.assetid: ab73ac2c-f178-1bb9-910d-9eef5fc6f5df
title: Tipo di dati XMVECTORU8 (DirectXMath. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4428cdd78206bfa17c295a9578653bb0a66f0c6b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106324358"
---
# <a name="xmvectoru8-data-type"></a><span data-ttu-id="faa41-103">Tipo di dati XMVECTORU8</span><span class="sxs-lookup"><span data-stu-id="faa41-103">XMVECTORU8 Data Type</span></span>

<span data-ttu-id="faa41-104">Tipo opaco e portabile per supportare l'uso della sintassi dell'inizializzatore C/C++ per caricare \_ i valori Uint8 in un'istanza di tipo [**XMVECTOR**](xmvector-data-type.md) .</span><span class="sxs-lookup"><span data-stu-id="faa41-104">An opaque, portable type to support the use of C/C++ initializer syntax to load uint8\_t values into an instance of [**XMVECTOR**](xmvector-data-type.md) type.</span></span>


```C++
typedef XMVECTORU8 vectoru8;
```



## <a name="remarks"></a><span data-ttu-id="faa41-105">Commenti</span><span class="sxs-lookup"><span data-stu-id="faa41-105">Remarks</span></span>

<span data-ttu-id="faa41-106">Per un elenco di funzionalità aggiuntive, ad esempio costruttori e operatori, disponibili con XMVECTORU8 durante la programmazione in C++, vedere [estensioni di XMVECTORU8](ovw-xmvectoru8-extensions.md).</span><span class="sxs-lookup"><span data-stu-id="faa41-106">For a list of additional functionality, such as constructors and operators, available using XMVECTORU8 when programming in C++, see [XMVECTORU8 Extensions](ovw-xmvectoru8-extensions.md).</span></span>

<span data-ttu-id="faa41-107">Le strutture [**XMVECTORF32**](xmvectorf32-data-type.md), [**XMVECTORU32**](xmvectoru32-data-type.md), [**XMVECTORI32**](xmvectori32-data-type.md)e **XMVECTORU8** sono fornite come meccanismo per la creazione di [**XMVECTOR**](xmvector-data-type.md) da diversi tipi di dati costanti (a virgola mobile, Unsigned Integer, Integer e byte) tramite inizializzatori.</span><span class="sxs-lookup"><span data-stu-id="faa41-107">The [**XMVECTORF32**](xmvectorf32-data-type.md), [**XMVECTORU32**](xmvectoru32-data-type.md), [**XMVECTORI32**](xmvectori32-data-type.md), and **XMVECTORU8** structures are provided as a mechanism for creating [**XMVECTOR**](xmvector-data-type.md) from different constant data types (floating point, unsigned integer, integer, and byte) using initializers.</span></span>

<span data-ttu-id="faa41-108">Questa operazione è necessaria per supportare [**XMVECTOR**](xmvector-data-type.md), in quanto non supporta gli inizializzatori, per motivi di portabilità e di ottimizzazione.</span><span class="sxs-lookup"><span data-stu-id="faa41-108">This is necessary to support [**XMVECTOR**](xmvector-data-type.md), as it does not itself support initializers, for portability and optimization reasons.</span></span>

<span data-ttu-id="faa41-109">Ad esempio:</span><span class="sxs-lookup"><span data-stu-id="faa41-109">For example:</span></span>

``` syntax
XMVECTOR data;
XMVECTORU8  byteVector = { (uint8_t)  1,(uint8_t) 16,(uint8_t)101,(uint8_t) 62,
                           (uint8_t)  4,(uint8_t)  0,(uint8_t)  2,(uint8_t) 99,
                           (uint8_t)  9,(uint8_t) 18,(uint8_t)  0,(uint8_t)  0,
                           (uint8_t)100,(uint8_t) 51,(uint8_t) 23,(uint8_t)117};

data = floatingVector;
```

<span data-ttu-id="faa41-110">**Spazio dei nomi**: usare DirectX</span><span class="sxs-lookup"><span data-stu-id="faa41-110">**Namespace**: Use DirectX</span></span>

### <a name="platform-requirements"></a><span data-ttu-id="faa41-111">Requisiti della piattaforma</span><span class="sxs-lookup"><span data-stu-id="faa41-111">Platform Requirements</span></span>

<span data-ttu-id="faa41-112">Microsoft Visual Studio 2010 o Microsoft Visual Studio 2012 con la Windows SDK per Windows 8.</span><span class="sxs-lookup"><span data-stu-id="faa41-112">Microsoft Visual Studio 2010 or Microsoft Visual Studio 2012 with the Windows SDK for Windows 8.</span></span> <span data-ttu-id="faa41-113">Supportato per le app desktop Win32, le app di Windows Store e le app Windows Phone 8.</span><span class="sxs-lookup"><span data-stu-id="faa41-113">Supported for Win32 desktop apps, Windows Store apps, and Windows Phone 8 apps.</span></span>

## <a name="requirements"></a><span data-ttu-id="faa41-114">Requisiti</span><span class="sxs-lookup"><span data-stu-id="faa41-114">Requirements</span></span>



| <span data-ttu-id="faa41-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="faa41-115">Requirement</span></span> | <span data-ttu-id="faa41-116">Valore</span><span class="sxs-lookup"><span data-stu-id="faa41-116">Value</span></span> |
|-------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="faa41-117">Intestazione</span><span class="sxs-lookup"><span data-stu-id="faa41-117">Header</span></span><br/> | <dl> <span data-ttu-id="faa41-118"><dt>DirectXMath. h</dt></span><span class="sxs-lookup"><span data-stu-id="faa41-118"><dt>DirectXMath.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="faa41-119">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="faa41-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="faa41-120">Tipi di libreria DirectXMath</span><span class="sxs-lookup"><span data-stu-id="faa41-120">DirectXMath Library Types</span></span>](ovw-xnamath-reference-types.md)
</dt> <dt>

[<span data-ttu-id="faa41-121">**Tipo di dati XMVECTOR**</span><span class="sxs-lookup"><span data-stu-id="faa41-121">**XMVECTOR Data Type**</span></span>](xmvector-data-type.md)
</dt> <dt>

[<span data-ttu-id="faa41-122">**Tipo di dati XMVECTORF32**</span><span class="sxs-lookup"><span data-stu-id="faa41-122">**XMVECTORF32 Data Type**</span></span>](xmvectorf32-data-type.md)
</dt> <dt>

[<span data-ttu-id="faa41-123">**Tipo di dati XMVECTORI32**</span><span class="sxs-lookup"><span data-stu-id="faa41-123">**XMVECTORI32 Data Type**</span></span>](xmvectori32-data-type.md)
</dt> <dt>

[<span data-ttu-id="faa41-124">**Tipo di dati XMVECTORU32**</span><span class="sxs-lookup"><span data-stu-id="faa41-124">**XMVECTORU32 Data Type**</span></span>](xmvectoru32-data-type.md)
</dt> <dt>

[<span data-ttu-id="faa41-125">Estensioni XMVECTORU8</span><span class="sxs-lookup"><span data-stu-id="faa41-125">XMVECTORU8 Extensions</span></span>](ovw-xmvectoru8-extensions.md)
</dt> </dl>

 

 




