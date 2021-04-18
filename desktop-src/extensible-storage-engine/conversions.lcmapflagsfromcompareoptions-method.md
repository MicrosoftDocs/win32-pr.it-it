---
description: 'Altre informazioni su: Conversions. LCMapFlagsFromCompareOptions, metodo'
title: Conversions. LCMapFlagsFromCompareOptions, metodo
TOCTitle: 'LCMapFlagsFromCompareOptions method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Conversions.LCMapFlagsFromCompareOptions(System.Globalization.CompareOptions)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.conversions.lcmapflagsfromcompareoptions(v=EXCHG.10)
ms:contentKeyID: 55100974
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Conversions.LCMapFlagsFromCompareOptions
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Conversions.LCMapFlagsFromCompareOptions
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 55c034bb0e4e48217c5294d83f65b48245a5e455
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106308554"
---
# <a name="conversionslcmapflagsfromcompareoptions-method"></a><span data-ttu-id="690de-103">Conversions. LCMapFlagsFromCompareOptions, metodo</span><span class="sxs-lookup"><span data-stu-id="690de-103">Conversions.LCMapFlagsFromCompareOptions method</span></span>

<span data-ttu-id="690de-104">Assegnare a CompareOptions, trasformarli in flag da LCMapString.</span><span class="sxs-lookup"><span data-stu-id="690de-104">Give CompareOptions, turn them into flags from LCMapString.</span></span> <span data-ttu-id="690de-105">Le opzioni sconosciute vengono ignorate.</span><span class="sxs-lookup"><span data-stu-id="690de-105">Unknown options are ignored.</span></span>

<span data-ttu-id="690de-106">Questa API non è conforme a CLS.</span><span class="sxs-lookup"><span data-stu-id="690de-106">This API is not CLS-compliant.</span></span> 

<span data-ttu-id="690de-107">**Spazio dei nomi:**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="690de-107">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="690de-108">**Assembly:**  Microsoft. ISAM. esent. Interop (in Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="690de-108">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="690de-109">Sintassi</span><span class="sxs-lookup"><span data-stu-id="690de-109">Syntax</span></span>

``` vb
'Declaration
<CLSCompliantAttribute(False)> _
Public Shared Function LCMapFlagsFromCompareOptions ( _
    compareOptions As CompareOptions _
) As UInteger
'Usage
Dim compareOptions As CompareOptions
Dim returnValue As UInteger

returnValue = Conversions.LCMapFlagsFromCompareOptions(compareOptions)
```

``` csharp
[CLSCompliantAttribute(false)]
public static uint LCMapFlagsFromCompareOptions(
    CompareOptions compareOptions
)
```

#### <a name="parameters"></a><span data-ttu-id="690de-110">Parametri</span><span class="sxs-lookup"><span data-stu-id="690de-110">Parameters</span></span>

  - <span data-ttu-id="690de-111">compareOptions</span><span class="sxs-lookup"><span data-stu-id="690de-111">compareOptions</span></span>  
    <span data-ttu-id="690de-112">Tipo: [System. Globalization. CompareOptions](/dotnet/api/system.globalization.compareoptions)</span><span class="sxs-lookup"><span data-stu-id="690de-112">Type: [System.Globalization.CompareOptions](/dotnet/api/system.globalization.compareoptions)</span></span>  
    
    <span data-ttu-id="690de-113">Opzioni da convertire.</span><span class="sxs-lookup"><span data-stu-id="690de-113">The options to convert.</span></span>

#### <a name="return-value"></a><span data-ttu-id="690de-114">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="690de-114">Return value</span></span>

<span data-ttu-id="690de-115">Tipo: [System. UInt32](/dotnet/api/system.uint32)</span><span class="sxs-lookup"><span data-stu-id="690de-115">Type: [System.UInt32](/dotnet/api/system.uint32)</span></span>  
<span data-ttu-id="690de-116">Flag LCMapString che corrispondono alle opzioni di confronto.</span><span class="sxs-lookup"><span data-stu-id="690de-116">The LCMapString flags that match the compare options.</span></span> <span data-ttu-id="690de-117">Le opzioni non supportate vengono ignorate.</span><span class="sxs-lookup"><span data-stu-id="690de-117">Unsupported options are ignored.</span></span>  

## <a name="see-also"></a><span data-ttu-id="690de-118">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="690de-118">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="690de-119">Riferimento</span><span class="sxs-lookup"><span data-stu-id="690de-119">Reference</span></span>

[<span data-ttu-id="690de-120">Classe Conversions</span><span class="sxs-lookup"><span data-stu-id="690de-120">Conversions class</span></span>](./conversions-class.md)

[<span data-ttu-id="690de-121">Membri delle conversioni</span><span class="sxs-lookup"><span data-stu-id="690de-121">Conversions members</span></span>](./conversions-members.md)

[<span data-ttu-id="690de-122">Spazio dei nomi Microsoft. ISAM. esent. Interop</span><span class="sxs-lookup"><span data-stu-id="690de-122">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
