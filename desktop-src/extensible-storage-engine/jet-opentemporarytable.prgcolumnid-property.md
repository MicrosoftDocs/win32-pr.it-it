---
description: 'Altre informazioni su: Proprietà JET_OPENTEMPORARYTABLE. prgcolumnid'
title: Proprietà JET_OPENTEMPORARYTABLE. prgcolumnid (Microsoft. ISAM. esent. Interop. vista)
TOCTitle: 'prgcolumnid property '
ms:assetid: P:Microsoft.Isam.Esent.Interop.Vista.JET_OPENTEMPORARYTABLE.prgcolumnid
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.vista.jet_opentemporarytable.prgcolumnid(v=EXCHG.10)
ms:contentKeyID: 55104133
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Vista.JET_OPENTEMPORARYTABLE.prgcolumnid
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Vista.JET_OPENTEMPORARYTABLE.get_prgcolumnid
- Microsoft.Isam.Esent.Interop.Vista.JET_OPENTEMPORARYTABLE.set_prgcolumnid
- Microsoft.Isam.Esent.Interop.Vista.JET_OPENTEMPORARYTABLE.prgcolumnid
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: cd6516e01d08de32f7962a48d2caca69ddbf0427
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103968436"
---
# <a name="jet_opentemporarytableprgcolumnid-property"></a><span data-ttu-id="e6a09-103">Proprietà JET_OPENTEMPORARYTABLE. prgcolumnid</span><span class="sxs-lookup"><span data-stu-id="e6a09-103">JET_OPENTEMPORARYTABLE.prgcolumnid property</span></span>

<span data-ttu-id="e6a09-104">Ottiene o imposta il buffer di output che riceve la matrice di ID di colonna generati durante la creazione della tabella temporanea.</span><span class="sxs-lookup"><span data-stu-id="e6a09-104">Gets or sets the output buffer that receives the array of column IDs generated during the creation of the temporary table.</span></span> <span data-ttu-id="e6a09-105">Gli ID di colonna in questa matrice corrispondono esattamente alla matrice di input delle definizioni di colonna.</span><span class="sxs-lookup"><span data-stu-id="e6a09-105">The column IDs in this array will exactly correspond to the input array of column definitions.</span></span> <span data-ttu-id="e6a09-106">Di conseguenza, le dimensioni del buffer devono corrispondere alla dimensione di [prgcolumndef](./jet-opentemporarytable.prgcolumndef-property.md).</span><span class="sxs-lookup"><span data-stu-id="e6a09-106">As a result, the size of this buffer must correspond to the size of [prgcolumndef](./jet-opentemporarytable.prgcolumndef-property.md).</span></span>

<span data-ttu-id="e6a09-107">**Spazio dei nomi:**  [Microsoft. ISAM. esent. Interop. vista](./microsoft.isam.esent.interop.vista-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="e6a09-107">**Namespace:**  [Microsoft.Isam.Esent.Interop.Vista](./microsoft.isam.esent.interop.vista-namespace.md)</span></span>  
<span data-ttu-id="e6a09-108">**Assembly:**  Microsoft. ISAM. esent. Interop (in Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="e6a09-108">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="e6a09-109">Sintassi</span><span class="sxs-lookup"><span data-stu-id="e6a09-109">Syntax</span></span>

``` vb
'Declaration
Public Property prgcolumnid As JET_COLUMNID()
    Get
    Set
'Usage
Dim instance As JET_OPENTEMPORARYTABLE
Dim value As JET_COLUMNID()

value = instance.prgcolumnid

instance.prgcolumnid = value
```

``` csharp
public JET_COLUMNID[] prgcolumnid { get; set; }
```

#### <a name="property-value"></a><span data-ttu-id="e6a09-110">Valore proprietà</span><span class="sxs-lookup"><span data-stu-id="e6a09-110">Property value</span></span>

<span data-ttu-id="e6a09-111">Tipo \[\]</span><span class="sxs-lookup"><span data-stu-id="e6a09-111">Type: \[\]</span></span>  

## <a name="see-also"></a><span data-ttu-id="e6a09-112">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="e6a09-112">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="e6a09-113">Riferimento</span><span class="sxs-lookup"><span data-stu-id="e6a09-113">Reference</span></span>

[<span data-ttu-id="e6a09-114">Classe JET_OPENTEMPORARYTABLE</span><span class="sxs-lookup"><span data-stu-id="e6a09-114">JET_OPENTEMPORARYTABLE class</span></span>](./jet-opentemporarytable-class.md)

[<span data-ttu-id="e6a09-115">Membri JET_OPENTEMPORARYTABLE</span><span class="sxs-lookup"><span data-stu-id="e6a09-115">JET_OPENTEMPORARYTABLE members</span></span>](./jet-opentemporarytable-members.md)

[<span data-ttu-id="e6a09-116">Spazio dei nomi Microsoft. ISAM. esent. Interop. vista</span><span class="sxs-lookup"><span data-stu-id="e6a09-116">Microsoft.Isam.Esent.Interop.Vista namespace</span></span>](./microsoft.isam.esent.interop.vista-namespace.md)
