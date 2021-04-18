---
title: parola chiave declare_guid
description: La \_ parola chiave Declare GUID indica a MIDL di creare una variabile GUID nel file di intestazione generato.
keywords:
- declare_guid parola chiave MIDL
topic_type:
- apiref
api_name:
- declare_guid
api_type:
- NA
ms.topic: reference
ms.date: 02/05/2021
ms.openlocfilehash: 495acd64e79544d067ff124a88289219919a7fb6
ms.sourcegitcommit: 5b98bf8c68922f8f03c14f793fbe17504900559c
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/12/2021
ms.locfileid: "106320440"
---
# <a name="declare_guid-keyword"></a><span data-ttu-id="028ba-104">dichiarare \_ GUID (parola chiave)</span><span class="sxs-lookup"><span data-stu-id="028ba-104">declare\_guid keyword</span></span>

<span data-ttu-id="028ba-105">La parola chiave **Declare \_ GUID** indica a MIDL di creare una variabile GUID nel file di intestazione generato.</span><span class="sxs-lookup"><span data-stu-id="028ba-105">The **declare\_guid** keyword instructs MIDL to emit a GUID variable into the generated header file.</span></span>

``` syntax
declare_guid(variable-name, guid)
```

## <a name="parameters"></a><span data-ttu-id="028ba-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="028ba-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="028ba-107">*nome variabile*</span><span class="sxs-lookup"><span data-stu-id="028ba-107">*variable-name*</span></span> 
</dt> <dd>

<span data-ttu-id="028ba-108">Specifica un nome di variabile per l'identificatore nel file di intestazione generato.</span><span class="sxs-lookup"><span data-stu-id="028ba-108">Specifies a variable name for the identifier in the generated header file.</span></span>

</dd> <dt>

<span data-ttu-id="028ba-109">*guid*</span><span class="sxs-lookup"><span data-stu-id="028ba-109">*guid*</span></span>
</dt> <dd>

<span data-ttu-id="028ba-110">Specifica il [GUID](/windows/win32/api/guiddef/ns-guiddef-guid) che si applicherà al nome della variabile nel file di intestazione generato.</span><span class="sxs-lookup"><span data-stu-id="028ba-110">Specifies the [GUID](/windows/win32/api/guiddef/ns-guiddef-guid) that will apply to the variable name in the generated header file.</span></span>

</dd> </dl>

## <a name="examples"></a><span data-ttu-id="028ba-111">Esempio</span><span class="sxs-lookup"><span data-stu-id="028ba-111">Examples</span></span>

``` syntax
declare_guid(SID_Widget, 5144C348-169E-4359-A79D-5482461D9929)  
```

## <a name="remarks"></a><span data-ttu-id="028ba-112">Commenti</span><span class="sxs-lookup"><span data-stu-id="028ba-112">Remarks</span></span>

<span data-ttu-id="028ba-113">L'utilizzo di `declare_guid` equivale all'utilizzo `cpp_quote` di per generare una chiamata della `EXTERN_GUID` macro.</span><span class="sxs-lookup"><span data-stu-id="028ba-113">Using `declare_guid` is equivalent to using `cpp_quote` to generate an invocation of the `EXTERN_GUID` macro.</span></span>

<span data-ttu-id="028ba-114">L'esempio precedente restituisce l'output seguente:</span><span class="sxs-lookup"><span data-stu-id="028ba-114">The above example results in the following output:</span></span>

```C
cpp_quote("EXTERN_GUID(SID_Widget, 0x5144c348, 0x169e, 0x4359, 0xa7, 0x9d, 0x54, 0x82, 0x46, 0x1d, 0x99, 0x29);")
```

<span data-ttu-id="028ba-115">L' `declare_guid` istruzione viene fornita come praticità.</span><span class="sxs-lookup"><span data-stu-id="028ba-115">The `declare_guid` statement is provided as a convenience.</span></span> <span data-ttu-id="028ba-116">Ha il vantaggio di usare la stessa sintassi GUID dell' [ `uuid` attributo](uuid.md).</span><span class="sxs-lookup"><span data-stu-id="028ba-116">It has the advantage of using the same GUID syntax as the [`uuid` attribute](uuid.md).</span></span>

## <a name="see-also"></a><span data-ttu-id="028ba-117">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="028ba-117">See also</span></span>

<dl> <dt>

[<span data-ttu-id="028ba-118">File di definizione dell'interfaccia (IDL)</span><span class="sxs-lookup"><span data-stu-id="028ba-118">Interface Definition (IDL) File</span></span>](interface-definition-idl-file.md)
</dt> <dt>

[<span data-ttu-id="028ba-119">**cpp_quote**</span><span class="sxs-lookup"><span data-stu-id="028ba-119">**cpp_quote**</span></span>](cpp-quote.md)
</dt> <dt>

[<span data-ttu-id="028ba-120">**uuid (attributo)**</span><span class="sxs-lookup"><span data-stu-id="028ba-120">**uuid attribute**</span></span>](uuid.md)
</dt> <dt>

[<span data-ttu-id="028ba-121">**Struttura GUID**</span><span class="sxs-lookup"><span data-stu-id="028ba-121">**GUID structure**</span></span>](/windows/win32/api/guiddef/ns-guiddef-guid)
</dt> </dl>
