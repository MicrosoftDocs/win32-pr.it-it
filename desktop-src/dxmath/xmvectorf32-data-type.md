---
description: Tipo opaco e portabile per supportare l'utilizzo della sintassi dell'inizializzatore C/C++ per caricare valori a virgola mobile in un'istanza di tipo XMVECTOR.
ms.assetid: bafaa59f-fd1b-e252-cbbd-903df796fde0
title: Tipo di dati XMVECTORF32 (DirectXMath. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8e56e79ea678ede0afcac3523c09da725ede00d1
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106329183"
---
# <a name="xmvectorf32-data-type"></a><span data-ttu-id="8837b-103">Tipo di dati XMVECTORF32</span><span class="sxs-lookup"><span data-stu-id="8837b-103">XMVECTORF32 Data Type</span></span>

<span data-ttu-id="8837b-104">Tipo opaco e portabile per supportare l'utilizzo della sintassi dell'inizializzatore C/C++ per caricare valori a virgola mobile in un'istanza di tipo [**XMVECTOR**](xmvector-data-type.md) .</span><span class="sxs-lookup"><span data-stu-id="8837b-104">An opaque, portable type to support the use of C/C++ initializer syntax to load floating-point values into an instance of [**XMVECTOR**](xmvector-data-type.md) type.</span></span>


```C++
typedef XMVECTORF32 vectorf32;
```



## <a name="remarks"></a><span data-ttu-id="8837b-105">Commenti</span><span class="sxs-lookup"><span data-stu-id="8837b-105">Remarks</span></span>

<span data-ttu-id="8837b-106">Per un elenco di funzionalità aggiuntive, ad esempio costruttori e operatori, disponibili con `XMVECTORF32` durante la programmazione in C++, vedere [XMVECTORF32 Extensions](ovw-xmvectorf32-extensions.md).</span><span class="sxs-lookup"><span data-stu-id="8837b-106">For a list of additional functionality, such as constructors and operators, available using `XMVECTORF32` when programming in C++, see [XMVECTORF32 Extensions](ovw-xmvectorf32-extensions.md).</span></span>

<span data-ttu-id="8837b-107">Le strutture **XMVECTORF32**, [**XMVECTORU32**](xmvectoru32-data-type.md), [**XMVECTORI32**](xmvectori32-data-type.md)e [**XMVECTORU8**](xmvectoru8-data-type.md) sono fornite come meccanismo per la creazione di [**XMVECTOR**](xmvector-data-type.md) da diversi tipi di dati costanti (a virgola mobile, Unsigned Integer, Integer e byte) tramite inizializzatori.</span><span class="sxs-lookup"><span data-stu-id="8837b-107">The **XMVECTORF32**, [**XMVECTORU32**](xmvectoru32-data-type.md), [**XMVECTORI32**](xmvectori32-data-type.md), and [**XMVECTORU8**](xmvectoru8-data-type.md) structures are provided as a mechanism for creating [**XMVECTOR**](xmvector-data-type.md) from different constant data types (floating point, unsigned integer, integer, and byte) using initializers.</span></span>

<span data-ttu-id="8837b-108">Questa operazione è necessaria per supportare [**XMVECTOR**](xmvector-data-type.md), in quanto non supporta gli inizializzatori, per motivi di portabilità e di ottimizzazione.</span><span class="sxs-lookup"><span data-stu-id="8837b-108">This is necessary to support [**XMVECTOR**](xmvector-data-type.md), as it does not itself support initializers, for portability and optimization reasons.</span></span>

<span data-ttu-id="8837b-109">Ad esempio:</span><span class="sxs-lookup"><span data-stu-id="8837b-109">For example:</span></span>


```
XMVECTOR data;
XMVECTORF32 floatingVector = { 0.f, 0.f, 0.1f, 1.f };
data = floatingVector;
```



<span data-ttu-id="8837b-110">**Spazio dei nomi**: usare DirectX</span><span class="sxs-lookup"><span data-stu-id="8837b-110">**Namespace**: Use DirectX</span></span>

### <a name="platform-requirements"></a><span data-ttu-id="8837b-111">Requisiti della piattaforma</span><span class="sxs-lookup"><span data-stu-id="8837b-111">Platform Requirements</span></span>

<span data-ttu-id="8837b-112">Microsoft Visual Studio 2010 o Microsoft Visual Studio 2012 con la Windows SDK per Windows 8.</span><span class="sxs-lookup"><span data-stu-id="8837b-112">Microsoft Visual Studio 2010 or Microsoft Visual Studio 2012 with the Windows SDK for Windows 8.</span></span> <span data-ttu-id="8837b-113">Supportato per le app desktop Win32, le app di Windows Store e le app Windows Phone 8.</span><span class="sxs-lookup"><span data-stu-id="8837b-113">Supported for Win32 desktop apps, Windows Store apps, and Windows Phone 8 apps.</span></span>

## <a name="requirements"></a><span data-ttu-id="8837b-114">Requisiti</span><span class="sxs-lookup"><span data-stu-id="8837b-114">Requirements</span></span>



| <span data-ttu-id="8837b-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="8837b-115">Requirement</span></span> | <span data-ttu-id="8837b-116">Valore</span><span class="sxs-lookup"><span data-stu-id="8837b-116">Value</span></span> |
|-------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="8837b-117">Intestazione</span><span class="sxs-lookup"><span data-stu-id="8837b-117">Header</span></span><br/> | <dl> <span data-ttu-id="8837b-118"><dt>DirectXMath. h</dt></span><span class="sxs-lookup"><span data-stu-id="8837b-118"><dt>DirectXMath.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8837b-119">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="8837b-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8837b-120">Tipi di libreria DirectXMath</span><span class="sxs-lookup"><span data-stu-id="8837b-120">DirectXMath Library Types</span></span>](ovw-xnamath-reference-types.md)
</dt> <dt>

[<span data-ttu-id="8837b-121">**Tipo di dati XMVECTORI32**</span><span class="sxs-lookup"><span data-stu-id="8837b-121">**XMVECTORI32 Data Type**</span></span>](xmvectori32-data-type.md)
</dt> <dt>

[<span data-ttu-id="8837b-122">**Tipo di dati XMVECTOR**</span><span class="sxs-lookup"><span data-stu-id="8837b-122">**XMVECTOR Data Type**</span></span>](xmvector-data-type.md)
</dt> <dt>

[<span data-ttu-id="8837b-123">**Tipo di dati XMVECTORU32**</span><span class="sxs-lookup"><span data-stu-id="8837b-123">**XMVECTORU32 Data Type**</span></span>](xmvectoru32-data-type.md)
</dt> <dt>

[<span data-ttu-id="8837b-124">**Tipo di dati XMVECTORU8**</span><span class="sxs-lookup"><span data-stu-id="8837b-124">**XMVECTORU8 Data Type**</span></span>](xmvectoru8-data-type.md)
</dt> <dt>

[<span data-ttu-id="8837b-125">**Tipo di dati XMVECTORF32**</span><span class="sxs-lookup"><span data-stu-id="8837b-125">**XMVECTORF32 Data Type**</span></span>](xmvectorf32-data-type.md)
</dt> </dl>

 

 




