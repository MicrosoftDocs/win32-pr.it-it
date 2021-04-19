---
description: 'Altre informazioni su: <T> interfaccia IContentEquatable'
title: Interfaccia IContentEquatable (T)
TOCTitle: IContentEquatable(T) interface
ms:assetid: T:Microsoft.Isam.Esent.Interop.IContentEquatable`1
ms:mtpsurl: https://msdn.microsoft.com/library/Hh578046(v=EXCHG.10)
ms:contentKeyID: 39511318
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.IContentEquatable`1
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.IContentEquatable`1
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 02e237714f020f5bafa3ce8b7465f1c8e2615c01
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106309158"
---
# <a name="icontentequatablet-interface"></a><span data-ttu-id="d2545-103">\<T\>Interfaccia IContentEquatable</span><span class="sxs-lookup"><span data-stu-id="d2545-103">IContentEquatable\<T\> interface</span></span>

<span data-ttu-id="d2545-104">Interfaccia per gli oggetti il cui contenuto può essere confrontato tra loro.</span><span class="sxs-lookup"><span data-stu-id="d2545-104">Interface for objects that can have their contents compared against each other.</span></span> <span data-ttu-id="d2545-105">Questa operazione deve essere utilizzata per i confronti di uguaglianza sugli oggetti di riferimento modificabili in cui l'override di Equals () e GetHashCode () non è un'idea efficace.</span><span class="sxs-lookup"><span data-stu-id="d2545-105">This should be used for equality comparisons on mutable reference objects where overriding Equals() and GetHashCode() isn't a good idea.</span></span>

<span data-ttu-id="d2545-106">**Spazio dei nomi:**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="d2545-106">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="d2545-107">**Assembly:**  Microsoft. ISAM. esent. Interop (in Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="d2545-107">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="d2545-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="d2545-108">Syntax</span></span>

``` vb
'Declaration
Public Interface IContentEquatable(Of T)
'Usage
Dim instance As IContentEquatable(Of T)
```

``` csharp
public interface IContentEquatable<T>
```

#### <a name="type-parameters"></a><span data-ttu-id="d2545-109">Parametri di tipo</span><span class="sxs-lookup"><span data-stu-id="d2545-109">Type parameters</span></span>

  - <span data-ttu-id="d2545-110">T</span><span class="sxs-lookup"><span data-stu-id="d2545-110">T</span></span>  
    <span data-ttu-id="d2545-111">Tipo di oggetti da comapre.</span><span class="sxs-lookup"><span data-stu-id="d2545-111">The type of objects to comapre.</span></span>

## <a name="see-also"></a><span data-ttu-id="d2545-112">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="d2545-112">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="d2545-113">Riferimento</span><span class="sxs-lookup"><span data-stu-id="d2545-113">Reference</span></span>

[<span data-ttu-id="d2545-114">Membri di IContentEquatable \<T\></span><span class="sxs-lookup"><span data-stu-id="d2545-114">IContentEquatable\<T\> members</span></span>](./icontentequatable-t-members.md)

[<span data-ttu-id="d2545-115">Spazio dei nomi Microsoft. ISAM. esent. Interop</span><span class="sxs-lookup"><span data-stu-id="d2545-115">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
