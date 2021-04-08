---
description: 'Altre informazioni su: Proprietà JET_ENUMCOLUMNID. rgtagSequence'
title: Proprietà JET_ENUMCOLUMNID. rgtagSequence
TOCTitle: 'rgtagSequence property '
ms:assetid: P:Microsoft.Isam.Esent.Interop.JET_ENUMCOLUMNID.rgtagSequence
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.jet_enumcolumnid.rgtagsequence(v=EXCHG.10)
ms:contentKeyID: 55103529
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.JET_ENUMCOLUMNID.rgtagSequence
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.JET_ENUMCOLUMNID.set_rgtagSequence
- Microsoft.Isam.Esent.Interop.JET_ENUMCOLUMNID.get_rgtagSequence
- Microsoft.Isam.Esent.Interop.JET_ENUMCOLUMNID.rgtagSequence
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 1d61d69fb9f22a31f07ee2eb0b4116a13761d961
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103749858"
---
# <a name="jet_enumcolumnidrgtagsequence-property"></a><span data-ttu-id="2298c-103">Proprietà JET_ENUMCOLUMNID. rgtagSequence</span><span class="sxs-lookup"><span data-stu-id="2298c-103">JET_ENUMCOLUMNID.rgtagSequence property</span></span>

<span data-ttu-id="2298c-104">Ottiene o imposta la matrice di indici in base uno in una matrice di valori di colonna per una colonna specificata.</span><span class="sxs-lookup"><span data-stu-id="2298c-104">Gets or sets the array of one-based indices into the array of column values for a given column.</span></span> <span data-ttu-id="2298c-105">Un singolo elemento è un itagSequence definito in JET_RETRIEVECOLUMN.</span><span class="sxs-lookup"><span data-stu-id="2298c-105">A single element is an itagSequence which is defined in JET_RETRIEVECOLUMN.</span></span> <span data-ttu-id="2298c-106">Un itagSequence di 0 (zero) indica "Skip".</span><span class="sxs-lookup"><span data-stu-id="2298c-106">An itagSequence of 0 (zero) means "skip".</span></span> <span data-ttu-id="2298c-107">Un itagSequence di 1 indica che restituisce il primo valore della colonna, 2 indica il secondo e così via.</span><span class="sxs-lookup"><span data-stu-id="2298c-107">An itagSequence of 1 means return the first column value of the column, 2 means the second, and so on.</span></span>

<span data-ttu-id="2298c-108">**Spazio dei nomi:**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="2298c-108">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="2298c-109">**Assembly:**  Microsoft. ISAM. esent. Interop (in Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="2298c-109">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="2298c-110">Sintassi</span><span class="sxs-lookup"><span data-stu-id="2298c-110">Syntax</span></span>

``` vb
'Declaration
Public Property rgtagSequence As Integer()
    Get
    Set
'Usage
Dim instance As JET_ENUMCOLUMNID
Dim value As Integer()

value = instance.rgtagSequence

instance.rgtagSequence = value
```

``` csharp
public int[] rgtagSequence { get; set; }
```

#### <a name="property-value"></a><span data-ttu-id="2298c-111">Valore proprietà</span><span class="sxs-lookup"><span data-stu-id="2298c-111">Property value</span></span>

<span data-ttu-id="2298c-112">Tipo \[\]</span><span class="sxs-lookup"><span data-stu-id="2298c-112">Type: \[\]</span></span>  

## <a name="see-also"></a><span data-ttu-id="2298c-113">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="2298c-113">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="2298c-114">Riferimento</span><span class="sxs-lookup"><span data-stu-id="2298c-114">Reference</span></span>

[<span data-ttu-id="2298c-115">Classe JET_ENUMCOLUMNID</span><span class="sxs-lookup"><span data-stu-id="2298c-115">JET_ENUMCOLUMNID class</span></span>](./jet-enumcolumnid-class.md)

[<span data-ttu-id="2298c-116">Membri JET_ENUMCOLUMNID</span><span class="sxs-lookup"><span data-stu-id="2298c-116">JET_ENUMCOLUMNID members</span></span>](./jet-enumcolumnid-members.md)

[<span data-ttu-id="2298c-117">Spazio dei nomi Microsoft. ISAM. esent. Interop</span><span class="sxs-lookup"><span data-stu-id="2298c-117">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
