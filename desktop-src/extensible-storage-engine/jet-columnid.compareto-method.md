---
description: 'Altre informazioni su: JET_COLUMNID. CompareTo (metodo)'
title: Metodo JET_COLUMNID. CompareTo
TOCTitle: 'CompareTo method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.JET_COLUMNID.CompareTo(Microsoft.Isam.Esent.Interop.JET_COLUMNID)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.jet_columnid.compareto(v=EXCHG.10)
ms:contentKeyID: 39509744
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.JET_COLUMNID.CompareTo
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.JET_COLUMNID.CompareTo
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 7eea24875b0639f7f5b7968084a3fff2aa7cccec
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104130175"
---
# <a name="jet_columnidcompareto-method"></a><span data-ttu-id="9c83f-103">Metodo JET_COLUMNID. CompareTo</span><span class="sxs-lookup"><span data-stu-id="9c83f-103">JET_COLUMNID.CompareTo method</span></span>

<span data-ttu-id="9c83f-104">Confronta questo ColumnID con un altro ColumnID e determina se questa istanza è precedente, uguale o successiva all'altra istanza.</span><span class="sxs-lookup"><span data-stu-id="9c83f-104">Compares this columnid to another columnid and determines whether this instance is before, the same as or after the other instance.</span></span>

<span data-ttu-id="9c83f-105">**Spazio dei nomi:**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="9c83f-105">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="9c83f-106">**Assembly:**  Microsoft. ISAM. esent. Interop (in Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="9c83f-106">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="9c83f-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="9c83f-107">Syntax</span></span>

``` vb
'Declaration
Public Function CompareTo ( _
    other As JET_COLUMNID _
) As Integer
'Usage
Dim instance As JET_COLUMNID
Dim other As JET_COLUMNID
Dim returnValue As Integer

returnValue = instance.CompareTo(other)
```

``` csharp
public int CompareTo(
    JET_COLUMNID other
)
```

#### <a name="parameters"></a><span data-ttu-id="9c83f-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="9c83f-108">Parameters</span></span>

  - <span data-ttu-id="9c83f-109">altro</span><span class="sxs-lookup"><span data-stu-id="9c83f-109">other</span></span>  
    <span data-ttu-id="9c83f-110">Tipo: [Microsoft.ISAM.esent.Interop.JET_COLUMNID](./jet-columnid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="9c83f-110">Type: [Microsoft.Isam.Esent.Interop.JET_COLUMNID](./jet-columnid-structure.md)</span></span>  
    
    <span data-ttu-id="9c83f-111">ColumnID da confrontare con l'istanza corrente.</span><span class="sxs-lookup"><span data-stu-id="9c83f-111">The columnid to compare to the current instance.</span></span>

#### <a name="return-value"></a><span data-ttu-id="9c83f-112">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="9c83f-112">Return value</span></span>

<span data-ttu-id="9c83f-113">Tipo: [System. Int32](/dotnet/api/system.int32)</span><span class="sxs-lookup"><span data-stu-id="9c83f-113">Type: [System.Int32](/dotnet/api/system.int32)</span></span>  
<span data-ttu-id="9c83f-114">Numero con segno che indica le posizioni relative di questa istanza e il parametro del valore.</span><span class="sxs-lookup"><span data-stu-id="9c83f-114">A signed number indicating the relative positions of this instance and the value parameter.</span></span>  

#### <a name="implements"></a><span data-ttu-id="9c83f-115">Implementazioni</span><span class="sxs-lookup"><span data-stu-id="9c83f-115">Implements</span></span>

[<span data-ttu-id="9c83f-116">IComparable \<T\> . CompareTo (T)</span><span class="sxs-lookup"><span data-stu-id="9c83f-116">IComparable\<T\>.CompareTo(T)</span></span>](/dotnet/api/system.icomparable-1.compareto#System_IComparable_1_CompareTo__0_)  

## <a name="see-also"></a><span data-ttu-id="9c83f-117">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="9c83f-117">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="9c83f-118">Riferimento</span><span class="sxs-lookup"><span data-stu-id="9c83f-118">Reference</span></span>

[<span data-ttu-id="9c83f-119">Struttura JET_COLUMNID</span><span class="sxs-lookup"><span data-stu-id="9c83f-119">JET_COLUMNID structure</span></span>](./jet-columnid-structure.md)

[<span data-ttu-id="9c83f-120">Membri JET_COLUMNID</span><span class="sxs-lookup"><span data-stu-id="9c83f-120">JET_COLUMNID members</span></span>](./jet-columnid-members.md)

[<span data-ttu-id="9c83f-121">Spazio dei nomi Microsoft. ISAM. esent. Interop</span><span class="sxs-lookup"><span data-stu-id="9c83f-121">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
