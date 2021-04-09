---
description: 'Altre informazioni su: campo VistaGrbits. IndexCrossProduct'
title: Campo VistaGrbits. IndexCrossProduct (Microsoft. ISAM. esent. Interop. vista)
TOCTitle: IndexCrossProduct field
ms:assetid: F:Microsoft.Isam.Esent.Interop.Vista.VistaGrbits.IndexCrossProduct
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.vista.vistagrbits.indexcrossproduct(v=EXCHG.10)
ms:contentKeyID: 55104426
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Vista.VistaGrbits.IndexCrossProduct
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Vista.VistaGrbits.IndexCrossProduct
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: f1b16f741c63d455d18a887331505080aef62990
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103968705"
---
# <a name="vistagrbitsindexcrossproduct-field"></a><span data-ttu-id="8c0d6-103">Campo VistaGrbits. IndexCrossProduct</span><span class="sxs-lookup"><span data-stu-id="8c0d6-103">VistaGrbits.IndexCrossProduct field</span></span>

<span data-ttu-id="8c0d6-104">Se si specifica questo flag per un indice con più di una colonna chiave che è una colonna multivalore, verrà creata una voce di indice per ogni risultato di un prodotto incrociato di tutti i valori in tali colonne chiave.</span><span class="sxs-lookup"><span data-stu-id="8c0d6-104">Specifying this flag for an index that has more than one key column that is a multi-valued column will result in an index entry being created for each result of a cross product of all the values in those key columns.</span></span> <span data-ttu-id="8c0d6-105">In caso contrario, l'indice avrebbe solo una voce per ogni multivalore nella colonna chiave più significativa che è una colonna multivalore e ognuna di queste voci di indice utilizzerebbe il primo multivalore da qualsiasi altra colonna chiave con colonne multivalore.</span><span class="sxs-lookup"><span data-stu-id="8c0d6-105">Otherwise, the index would only have one entry for each multi-value in the most significant key column that is a multi-valued column and each of those index entries would use the first multi-value from any other key columns that are multi-valued columns.</span></span> <span data-ttu-id="8c0d6-106">Se, ad esempio, si specifica questo flag per un indice sulla colonna A con i valori "Red" e "Blue" e sulla colonna B con i valori "1" e "2", verranno create le voci di indice seguenti: "Red", "1"; "rosso", "2"; "blu", "1"; "blu", "2".</span><span class="sxs-lookup"><span data-stu-id="8c0d6-106">For example, if you specified this flag for an index over column A that has the values "red" and "blue" and over column B that has the values "1" and "2" then the following index entries would be created: "red", "1"; "red", "2"; "blue", "1"; "blue", "2".</span></span> <span data-ttu-id="8c0d6-107">In caso contrario, verranno create le voci di indice seguenti: "Red", "1"; "blu", "1".</span><span class="sxs-lookup"><span data-stu-id="8c0d6-107">Otherwise, the following index entries would be created: "red", "1"; "blue", "1".</span></span>

<span data-ttu-id="8c0d6-108">**Spazio dei nomi:**  [Microsoft. ISAM. esent. Interop. vista](./microsoft.isam.esent.interop.vista-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="8c0d6-108">**Namespace:**  [Microsoft.Isam.Esent.Interop.Vista](./microsoft.isam.esent.interop.vista-namespace.md)</span></span>  
<span data-ttu-id="8c0d6-109">**Assembly:**  Microsoft. ISAM. esent. Interop (in Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="8c0d6-109">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="8c0d6-110">Sintassi</span><span class="sxs-lookup"><span data-stu-id="8c0d6-110">Syntax</span></span>

``` vb
'Declaration
Public Const IndexCrossProduct As CreateIndexGrbit
'Usage
Dim value As CreateIndexGrbit

value = VistaGrbits.IndexCrossProduct
```

``` csharp
public const CreateIndexGrbit IndexCrossProduct
```

## <a name="see-also"></a><span data-ttu-id="8c0d6-111">Vedere anche</span><span class="sxs-lookup"><span data-stu-id="8c0d6-111">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="8c0d6-112">Riferimento</span><span class="sxs-lookup"><span data-stu-id="8c0d6-112">Reference</span></span>

[<span data-ttu-id="8c0d6-113">Classe VistaGrbits</span><span class="sxs-lookup"><span data-stu-id="8c0d6-113">VistaGrbits class</span></span>](./vistagrbits-class.md)

[<span data-ttu-id="8c0d6-114">Membri di VistaGrbits</span><span class="sxs-lookup"><span data-stu-id="8c0d6-114">VistaGrbits members</span></span>](./vistagrbits-members.md)

[<span data-ttu-id="8c0d6-115">Spazio dei nomi Microsoft. ISAM. esent. Interop. vista</span><span class="sxs-lookup"><span data-stu-id="8c0d6-115">Microsoft.Isam.Esent.Interop.Vista namespace</span></span>](./microsoft.isam.esent.interop.vista-namespace.md)
