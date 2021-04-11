---
description: 'Altre informazioni su: Conversions. CompareOptionsFromLCMapFlags, metodo'
title: Conversions. CompareOptionsFromLCMapFlags, metodo
TOCTitle: 'CompareOptionsFromLCMapFlags method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Conversions.CompareOptionsFromLCMapFlags(System.UInt32)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.conversions.compareoptionsfromlcmapflags(v=EXCHG.10)
ms:contentKeyID: 55100975
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Conversions.CompareOptionsFromLCMapFlags
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Conversions.CompareOptionsFromLCMapFlags
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 79e0d6a92aef75f3758adc16e9c82de81b8c6962
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104226414"
---
# <a name="conversionscompareoptionsfromlcmapflags-method"></a><span data-ttu-id="e10e2-103">Conversions. CompareOptionsFromLCMapFlags, metodo</span><span class="sxs-lookup"><span data-stu-id="e10e2-103">Conversions.CompareOptionsFromLCMapFlags method</span></span>

<span data-ttu-id="e10e2-104">Flag specificati per LCMapFlags, trasformarli in opzioni di confronto.</span><span class="sxs-lookup"><span data-stu-id="e10e2-104">Given flags for LCMapFlags, turn them into compare options.</span></span> <span data-ttu-id="e10e2-105">Le opzioni sconosciute vengono ignorate.</span><span class="sxs-lookup"><span data-stu-id="e10e2-105">Unknown options are ignored.</span></span>

<span data-ttu-id="e10e2-106">Questa API non è conforme a CLS.</span><span class="sxs-lookup"><span data-stu-id="e10e2-106">This API is not CLS-compliant.</span></span> 

<span data-ttu-id="e10e2-107">**Spazio dei nomi:**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="e10e2-107">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="e10e2-108">**Assembly:**  Microsoft. ISAM. esent. Interop (in Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="e10e2-108">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="e10e2-109">Sintassi</span><span class="sxs-lookup"><span data-stu-id="e10e2-109">Syntax</span></span>

``` vb
'Declaration
<CLSCompliantAttribute(False)> _
Public Shared Function CompareOptionsFromLCMapFlags ( _
    lcmapFlags As UInteger _
) As CompareOptions
'Usage
Dim lcmapFlags As UInteger
Dim returnValue As CompareOptions

returnValue = Conversions.CompareOptionsFromLCMapFlags(lcmapFlags)
```

``` csharp
[CLSCompliantAttribute(false)]
public static CompareOptions CompareOptionsFromLCMapFlags(
    uint lcmapFlags
)
```

#### <a name="parameters"></a><span data-ttu-id="e10e2-110">Parametri</span><span class="sxs-lookup"><span data-stu-id="e10e2-110">Parameters</span></span>

  - <span data-ttu-id="e10e2-111">lcmapFlags</span><span class="sxs-lookup"><span data-stu-id="e10e2-111">lcmapFlags</span></span>  
    <span data-ttu-id="e10e2-112">Tipo: [System. UInt32](/dotnet/api/system.uint32)</span><span class="sxs-lookup"><span data-stu-id="e10e2-112">Type: [System.UInt32](/dotnet/api/system.uint32)</span></span>  
    
    <span data-ttu-id="e10e2-113">Flag LCMapString.</span><span class="sxs-lookup"><span data-stu-id="e10e2-113">LCMapString flags.</span></span>

#### <a name="return-value"></a><span data-ttu-id="e10e2-114">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="e10e2-114">Return value</span></span>

<span data-ttu-id="e10e2-115">Tipo: [System. Globalization. CompareOptions](/dotnet/api/system.globalization.compareoptions)</span><span class="sxs-lookup"><span data-stu-id="e10e2-115">Type: [System.Globalization.CompareOptions](/dotnet/api/system.globalization.compareoptions)</span></span>  
<span data-ttu-id="e10e2-116">CompareOptions che descrive i flag (noti).</span><span class="sxs-lookup"><span data-stu-id="e10e2-116">CompareOptions describing the (known) flags.</span></span>  

## <a name="see-also"></a><span data-ttu-id="e10e2-117">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="e10e2-117">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="e10e2-118">Riferimento</span><span class="sxs-lookup"><span data-stu-id="e10e2-118">Reference</span></span>

[<span data-ttu-id="e10e2-119">Classe Conversions</span><span class="sxs-lookup"><span data-stu-id="e10e2-119">Conversions class</span></span>](./conversions-class.md)

[<span data-ttu-id="e10e2-120">Membri delle conversioni</span><span class="sxs-lookup"><span data-stu-id="e10e2-120">Conversions members</span></span>](./conversions-members.md)

[<span data-ttu-id="e10e2-121">Spazio dei nomi Microsoft. ISAM. esent. Interop</span><span class="sxs-lookup"><span data-stu-id="e10e2-121">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
