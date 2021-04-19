---
description: 'Altre informazioni su: JET_LGPOS. CompareTo (metodo)'
title: Metodo JET_LGPOS. CompareTo
TOCTitle: 'CompareTo method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.JET_LGPOS.CompareTo(Microsoft.Isam.Esent.Interop.JET_LGPOS)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.jet_lgpos.compareto(v=EXCHG.10)
ms:contentKeyID: 39514516
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.JET_LGPOS.CompareTo
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.JET_LGPOS.CompareTo
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 83012ed755ab876618147c013e99868927e16f1f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106315125"
---
# <a name="jet_lgposcompareto-method"></a><span data-ttu-id="89680-103">Metodo JET_LGPOS. CompareTo</span><span class="sxs-lookup"><span data-stu-id="89680-103">JET_LGPOS.CompareTo method</span></span>

<span data-ttu-id="89680-104">Confronta la posizione del log con un'altra posizione del log e determina se questa istanza è precedente, uguale o successiva all'altra istanza.</span><span class="sxs-lookup"><span data-stu-id="89680-104">Compares this log position to another log position and determines whether this instance is before, the same as or after the other instance.</span></span>

<span data-ttu-id="89680-105">**Spazio dei nomi:**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="89680-105">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="89680-106">**Assembly:**  Microsoft. ISAM. esent. Interop (in Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="89680-106">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="89680-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="89680-107">Syntax</span></span>

``` vb
'Declaration
Public Function CompareTo ( _
    other As JET_LGPOS _
) As Integer
'Usage
Dim instance As JET_LGPOS
Dim other As JET_LGPOS
Dim returnValue As Integer

returnValue = instance.CompareTo(other)
```

``` csharp
public int CompareTo(
    JET_LGPOS other
)
```

#### <a name="parameters"></a><span data-ttu-id="89680-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="89680-108">Parameters</span></span>

  - <span data-ttu-id="89680-109">altro</span><span class="sxs-lookup"><span data-stu-id="89680-109">other</span></span>  
    <span data-ttu-id="89680-110">Tipo: [Microsoft.ISAM.esent.Interop.JET_LGPOS](./jet-lgpos-structure2.md)</span><span class="sxs-lookup"><span data-stu-id="89680-110">Type: [Microsoft.Isam.Esent.Interop.JET_LGPOS](./jet-lgpos-structure2.md)</span></span>  
    
    <span data-ttu-id="89680-111">Posizione del log da confrontare con l'istanza corrente.</span><span class="sxs-lookup"><span data-stu-id="89680-111">The log position to compare to the current instance.</span></span>

#### <a name="return-value"></a><span data-ttu-id="89680-112">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="89680-112">Return value</span></span>

<span data-ttu-id="89680-113">Tipo: [System. Int32](/dotnet/api/system.int32)</span><span class="sxs-lookup"><span data-stu-id="89680-113">Type: [System.Int32](/dotnet/api/system.int32)</span></span>  
<span data-ttu-id="89680-114">Numero con segno che indica le posizioni relative di questa istanza e il parametro del valore.</span><span class="sxs-lookup"><span data-stu-id="89680-114">A signed number indicating the relative positions of this instance and the value parameter.</span></span>  

#### <a name="implements"></a><span data-ttu-id="89680-115">Implementazioni</span><span class="sxs-lookup"><span data-stu-id="89680-115">Implements</span></span>

[<span data-ttu-id="89680-116">IComparable \<T\> . CompareTo (T)</span><span class="sxs-lookup"><span data-stu-id="89680-116">IComparable\<T\>.CompareTo(T)</span></span>](/dotnet/api/system.icomparable-1.compareto#System_IComparable_1_CompareTo__0_)  

## <a name="see-also"></a><span data-ttu-id="89680-117">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="89680-117">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="89680-118">Riferimento</span><span class="sxs-lookup"><span data-stu-id="89680-118">Reference</span></span>

[<span data-ttu-id="89680-119">Struttura JET_LGPOS</span><span class="sxs-lookup"><span data-stu-id="89680-119">JET_LGPOS structure</span></span>](./jet-lgpos-structure2.md)

[<span data-ttu-id="89680-120">Membri JET_LGPOS</span><span class="sxs-lookup"><span data-stu-id="89680-120">JET_LGPOS members</span></span>](./jet-lgpos-members.md)

[<span data-ttu-id="89680-121">Spazio dei nomi Microsoft. ISAM. esent. Interop</span><span class="sxs-lookup"><span data-stu-id="89680-121">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
