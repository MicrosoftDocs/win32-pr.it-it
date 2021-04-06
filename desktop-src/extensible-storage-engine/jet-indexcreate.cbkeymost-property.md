---
description: 'Altre informazioni su: Proprietà JET_INDEXCREATE. cbKeyMost'
title: Proprietà JET_INDEXCREATE. cbKeyMost
TOCTitle: 'cbKeyMost property '
ms:assetid: P:Microsoft.Isam.Esent.Interop.JET_INDEXCREATE.cbKeyMost
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.jet_indexcreate.cbkeymost(v=EXCHG.10)
ms:contentKeyID: 55103646
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.JET_INDEXCREATE.cbKeyMost
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.JET_INDEXCREATE.cbKeyMost
- Microsoft.Isam.Esent.Interop.JET_INDEXCREATE.get_cbKeyMost
- Microsoft.Isam.Esent.Interop.JET_INDEXCREATE.set_cbKeyMost
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 321704f88da59af33f4dab99d7d681fbcbd96e1a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103883490"
---
# <a name="jet_indexcreatecbkeymost-property"></a><span data-ttu-id="3b3e9-103">Proprietà JET_INDEXCREATE. cbKeyMost</span><span class="sxs-lookup"><span data-stu-id="3b3e9-103">JET_INDEXCREATE.cbKeyMost property</span></span>

<span data-ttu-id="3b3e9-104">Ottiene o imposta la dimensione massima consentita, in byte, per le chiavi nell'indice.</span><span class="sxs-lookup"><span data-stu-id="3b3e9-104">Gets or sets the maximum allowable size, in bytes, for keys in the index.</span></span> <span data-ttu-id="3b3e9-105">Le dimensioni minime massime supportate per la chiave sono JET_cbKeyMostMin (255), ovvero le dimensioni massime della chiave legacy.</span><span class="sxs-lookup"><span data-stu-id="3b3e9-105">The minimum supported maximum key size is JET_cbKeyMostMin (255) which is the legacy maximum key size.</span></span> <span data-ttu-id="3b3e9-106">Le dimensioni massime della chiave dipendono dalle dimensioni della pagina del database [DatabasePageSize](./jet-param-enumeration.md).</span><span class="sxs-lookup"><span data-stu-id="3b3e9-106">The maximum key size is dependent on the database page size [DatabasePageSize](./jet-param-enumeration.md).</span></span> <span data-ttu-id="3b3e9-107">È possibile recuperare le dimensioni massime della [chiave con la](./systemparameters.keymost-property.md)chiave.</span><span class="sxs-lookup"><span data-stu-id="3b3e9-107">The maximum key size can be retrieved with [KeyMost](./systemparameters.keymost-property.md).</span></span> <span data-ttu-id="3b3e9-108">Questo parametro viene ignorato in Windows XP e Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="3b3e9-108">This parameter is ignored on Windows XP and Windows Server 2003.</span></span> <span data-ttu-id="3b3e9-109">A differenza dell'API non gestita, **IndexKeyMost ()** (JET_bitIndexKeyMost) non è necessario, verrà aggiunto automaticamente.</span><span class="sxs-lookup"><span data-stu-id="3b3e9-109">Unlike the unmanaged API, **IndexKeyMost()** (JET_bitIndexKeyMost) is not needed, it will be added automatically.</span></span>

<span data-ttu-id="3b3e9-110">**Spazio dei nomi:**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="3b3e9-110">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="3b3e9-111">**Assembly:**  Microsoft. ISAM. esent. Interop (in Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="3b3e9-111">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="3b3e9-112">Sintassi</span><span class="sxs-lookup"><span data-stu-id="3b3e9-112">Syntax</span></span>

``` vb
'Declaration
Public Property cbKeyMost As Integer
    Get
    Set
'Usage
Dim instance As JET_INDEXCREATE
Dim value As Integer

value = instance.cbKeyMost

instance.cbKeyMost = value
```

``` csharp
public int cbKeyMost { get; set; }
```

#### <a name="property-value"></a><span data-ttu-id="3b3e9-113">Valore proprietà</span><span class="sxs-lookup"><span data-stu-id="3b3e9-113">Property value</span></span>

<span data-ttu-id="3b3e9-114">Tipo: [System. Int32](/dotnet/api/system.int32)</span><span class="sxs-lookup"><span data-stu-id="3b3e9-114">Type: [System.Int32](/dotnet/api/system.int32)</span></span>  

## <a name="see-also"></a><span data-ttu-id="3b3e9-115">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="3b3e9-115">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="3b3e9-116">Riferimento</span><span class="sxs-lookup"><span data-stu-id="3b3e9-116">Reference</span></span>

[<span data-ttu-id="3b3e9-117">Classe JET_INDEXCREATE</span><span class="sxs-lookup"><span data-stu-id="3b3e9-117">JET_INDEXCREATE class</span></span>](./jet-indexcreate-class.md)

[<span data-ttu-id="3b3e9-118">Membri JET_INDEXCREATE</span><span class="sxs-lookup"><span data-stu-id="3b3e9-118">JET_INDEXCREATE members</span></span>](./jet-indexcreate-members.md)

[<span data-ttu-id="3b3e9-119">Spazio dei nomi Microsoft. ISAM. esent. Interop</span><span class="sxs-lookup"><span data-stu-id="3b3e9-119">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
