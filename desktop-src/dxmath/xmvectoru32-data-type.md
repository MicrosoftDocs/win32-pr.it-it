---
description: Tipo opaco e portabile per supportare l'utilizzo della sintassi dell'inizializzatore C/C++ per caricare \_ i valori UInt32 t in un'istanza di tipo XMVECTOR.
ms.assetid: 1ac1f48a-cd7f-7741-933f-c341fc42a21c
title: Tipo di dati XMVECTORU32 (DirectXMath. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 90c7a64d42bc4638573b987642c0cd77c37cc12d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106329170"
---
# <a name="xmvectoru32-data-type"></a><span data-ttu-id="aeaf1-103">Tipo di dati XMVECTORU32</span><span class="sxs-lookup"><span data-stu-id="aeaf1-103">XMVECTORU32 Data Type</span></span>

<span data-ttu-id="aeaf1-104">Tipo opaco e portabile per supportare l'utilizzo della sintassi dell'inizializzatore C/C++ per caricare \_ i valori UInt32 t in un'istanza di tipo [**XMVECTOR**](xmvector-data-type.md) .</span><span class="sxs-lookup"><span data-stu-id="aeaf1-104">An opaque, portable type to support the use of C/C++ initializer syntax to load uint32\_t values into an instance of [**XMVECTOR**](xmvector-data-type.md) type.</span></span>


```C++
typedef XMVECTOR32 vectoru32;
```



## <a name="remarks"></a><span data-ttu-id="aeaf1-105">Commenti</span><span class="sxs-lookup"><span data-stu-id="aeaf1-105">Remarks</span></span>

<span data-ttu-id="aeaf1-106">Per un elenco di funzionalità aggiuntive, ad esempio costruttori e operatori, disponibili con XMVECTORU32 durante la programmazione in C++, vedere [estensioni di XMVECTORU32](ovw-xmvectoru32-extensions.md).</span><span class="sxs-lookup"><span data-stu-id="aeaf1-106">For a list of additional functionality, such as constructors and operators, available using XMVECTORU32 when programming in C++, see [XMVECTORU32 Extensions](ovw-xmvectoru32-extensions.md).</span></span>

<span data-ttu-id="aeaf1-107">Le strutture [**XMVECTORF32**](xmvectorf32-data-type.md), **XMVECTORU32**, [**XMVECTORI32**](xmvectori32-data-type.md)e [**XMVECTORU8**](xmvectoru8-data-type.md) sono fornite come meccanismo per la creazione di [**XMVECTOR**](xmvector-data-type.md) da diversi tipi di dati costanti (a virgola mobile, Unsigned Integer, Integer e byte) tramite inizializzatori.</span><span class="sxs-lookup"><span data-stu-id="aeaf1-107">The [**XMVECTORF32**](xmvectorf32-data-type.md), **XMVECTORU32**, [**XMVECTORI32**](xmvectori32-data-type.md), and [**XMVECTORU8**](xmvectoru8-data-type.md) structures are provided as a mechanism for creating [**XMVECTOR**](xmvector-data-type.md) from different constant data types (floating point, unsigned integer, integer, and byte) using initializers.</span></span>

<span data-ttu-id="aeaf1-108">Questa operazione è necessaria per supportare [**XMVECTOR**](xmvector-data-type.md), in quanto non supporta gli inizializzatori, per motivi di portabilità e di ottimizzazione.</span><span class="sxs-lookup"><span data-stu-id="aeaf1-108">This is necessary to support [**XMVECTOR**](xmvector-data-type.md), as it does not itself support initializers, for portability and optimization reasons.</span></span>

<span data-ttu-id="aeaf1-109">Ad esempio:</span><span class="sxs-lookup"><span data-stu-id="aeaf1-109">For example:</span></span>

``` syntax
XMVECTOR data;
XMVECTORU32 uintVector = { 0xf7000000, 0x8310000, 0x1000000, 0 };
data = uintVector;
```

<span data-ttu-id="aeaf1-110">**Spazio dei nomi**: usare DirectX</span><span class="sxs-lookup"><span data-stu-id="aeaf1-110">**Namespace**: Use DirectX</span></span>

### <a name="platform-requirements"></a><span data-ttu-id="aeaf1-111">Requisiti della piattaforma</span><span class="sxs-lookup"><span data-stu-id="aeaf1-111">Platform Requirements</span></span>

<span data-ttu-id="aeaf1-112">Microsoft Visual Studio 2010 o Microsoft Visual Studio 2012 con la Windows SDK per Windows 8.</span><span class="sxs-lookup"><span data-stu-id="aeaf1-112">Microsoft Visual Studio 2010 or Microsoft Visual Studio 2012 with the Windows SDK for Windows 8.</span></span> <span data-ttu-id="aeaf1-113">Supportato per le app desktop Win32, le app di Windows Store e le app Windows Phone 8.</span><span class="sxs-lookup"><span data-stu-id="aeaf1-113">Supported for Win32 desktop apps, Windows Store apps, and Windows Phone 8 apps.</span></span>

## <a name="requirements"></a><span data-ttu-id="aeaf1-114">Requisiti</span><span class="sxs-lookup"><span data-stu-id="aeaf1-114">Requirements</span></span>



| <span data-ttu-id="aeaf1-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="aeaf1-115">Requirement</span></span> | <span data-ttu-id="aeaf1-116">Valore</span><span class="sxs-lookup"><span data-stu-id="aeaf1-116">Value</span></span> |
|-------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="aeaf1-117">Intestazione</span><span class="sxs-lookup"><span data-stu-id="aeaf1-117">Header</span></span><br/> | <dl> <span data-ttu-id="aeaf1-118"><dt>DirectXMath. h</dt></span><span class="sxs-lookup"><span data-stu-id="aeaf1-118"><dt>Directxmath.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="aeaf1-119">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="aeaf1-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="aeaf1-120">Tipi di libreria DirectXMath</span><span class="sxs-lookup"><span data-stu-id="aeaf1-120">DirectXMath Library Types</span></span>](ovw-xnamath-reference-types.md)
</dt> <dt>

[<span data-ttu-id="aeaf1-121">**Tipo di dati XMVECTORI32**</span><span class="sxs-lookup"><span data-stu-id="aeaf1-121">**XMVECTORI32 Data Type**</span></span>](xmvectori32-data-type.md)
</dt> <dt>

[<span data-ttu-id="aeaf1-122">**Tipo di dati XMVECTORF32**</span><span class="sxs-lookup"><span data-stu-id="aeaf1-122">**XMVECTORF32 Data Type**</span></span>](xmvectorf32-data-type.md)
</dt> <dt>

[<span data-ttu-id="aeaf1-123">**Tipo di dati XMVECTOR**</span><span class="sxs-lookup"><span data-stu-id="aeaf1-123">**XMVECTOR Data Type**</span></span>](xmvector-data-type.md)
</dt> <dt>

[<span data-ttu-id="aeaf1-124">**Tipo di dati XMVECTORU8**</span><span class="sxs-lookup"><span data-stu-id="aeaf1-124">**XMVECTORU8 Data Type**</span></span>](xmvectoru8-data-type.md)
</dt> <dt>

[<span data-ttu-id="aeaf1-125">Estensioni XMVECTORU32</span><span class="sxs-lookup"><span data-stu-id="aeaf1-125">XMVECTORU32 Extensions</span></span>](ovw-xmvectoru32-extensions.md)
</dt> </dl>

 

 




