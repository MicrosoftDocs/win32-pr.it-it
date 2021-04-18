---
description: 'Altre informazioni su: Proprietà JET_ENUMCOLUMNID. ctagSequence'
title: Proprietà JET_ENUMCOLUMNID. ctagSequence
TOCTitle: 'ctagSequence property '
ms:assetid: P:Microsoft.Isam.Esent.Interop.JET_ENUMCOLUMNID.ctagSequence
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.jet_enumcolumnid.ctagsequence(v=EXCHG.10)
ms:contentKeyID: 55107537
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.JET_ENUMCOLUMNID.ctagSequence
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.JET_ENUMCOLUMNID.set_ctagSequence
- Microsoft.Isam.Esent.Interop.JET_ENUMCOLUMNID.ctagSequence
- Microsoft.Isam.Esent.Interop.JET_ENUMCOLUMNID.get_ctagSequence
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: b8e12c8c6a102cbb20862b3cc9859f7e632ade8b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106306826"
---
# <a name="jet_enumcolumnidctagsequence-property"></a><span data-ttu-id="36e34-103">Proprietà JET_ENUMCOLUMNID. ctagSequence</span><span class="sxs-lookup"><span data-stu-id="36e34-103">JET_ENUMCOLUMNID.ctagSequence property</span></span>

<span data-ttu-id="36e34-104">Ottiene o imposta il conteggio dei valori di colonna (in base a un indice in base 1) da enumerare per l'ID di colonna specificato.</span><span class="sxs-lookup"><span data-stu-id="36e34-104">Gets or sets the count of column values (by one-based index) to enumerate for the specified column ID.</span></span> <span data-ttu-id="36e34-105">Se ctagSequence è 0 (zero), rgtagSequence viene ignorato e verranno enumerati tutti i valori di colonna per l'ID di colonna specificato.</span><span class="sxs-lookup"><span data-stu-id="36e34-105">If ctagSequence is 0 (zero) then rgtagSequence is ignored and all column values for the specified column ID will be enumerated.</span></span>

<span data-ttu-id="36e34-106">**Spazio dei nomi:**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="36e34-106">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="36e34-107">**Assembly:**  Microsoft. ISAM. esent. Interop (in Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="36e34-107">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="36e34-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="36e34-108">Syntax</span></span>

``` vb
'Declaration
Public Property ctagSequence As Integer
    Get
    Set
'Usage
Dim instance As JET_ENUMCOLUMNID
Dim value As Integer

value = instance.ctagSequence

instance.ctagSequence = value
```

``` csharp
public int ctagSequence { get; set; }
```

#### <a name="property-value"></a><span data-ttu-id="36e34-109">Valore proprietà</span><span class="sxs-lookup"><span data-stu-id="36e34-109">Property value</span></span>

<span data-ttu-id="36e34-110">Tipo: [System. Int32](/dotnet/api/system.int32)</span><span class="sxs-lookup"><span data-stu-id="36e34-110">Type: [System.Int32](/dotnet/api/system.int32)</span></span>  

## <a name="see-also"></a><span data-ttu-id="36e34-111">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="36e34-111">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="36e34-112">Riferimento</span><span class="sxs-lookup"><span data-stu-id="36e34-112">Reference</span></span>

[<span data-ttu-id="36e34-113">Classe JET_ENUMCOLUMNID</span><span class="sxs-lookup"><span data-stu-id="36e34-113">JET_ENUMCOLUMNID class</span></span>](./jet-enumcolumnid-class.md)

[<span data-ttu-id="36e34-114">Membri JET_ENUMCOLUMNID</span><span class="sxs-lookup"><span data-stu-id="36e34-114">JET_ENUMCOLUMNID members</span></span>](./jet-enumcolumnid-members.md)

[<span data-ttu-id="36e34-115">Spazio dei nomi Microsoft. ISAM. esent. Interop</span><span class="sxs-lookup"><span data-stu-id="36e34-115">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
