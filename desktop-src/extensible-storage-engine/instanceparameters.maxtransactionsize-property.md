---
description: 'Altre informazioni su: Proprietà InstanceParameters. MaxTransactionSize'
title: Proprietà InstanceParameters. MaxTransactionSize
TOCTitle: 'MaxTransactionSize property '
ms:assetid: P:Microsoft.Isam.Esent.Interop.InstanceParameters.MaxTransactionSize
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.instanceparameters.maxtransactionsize(v=EXCHG.10)
ms:contentKeyID: 55103317
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.InstanceParameters.MaxTransactionSize
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.InstanceParameters.MaxTransactionSize
- Microsoft.Isam.Esent.Interop.InstanceParameters.set_MaxTransactionSize
- Microsoft.Isam.Esent.Interop.InstanceParameters.get_MaxTransactionSize
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: a370d05364142a6fca7d84265dc8d29c7ab5c808
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103882529"
---
# <a name="instanceparametersmaxtransactionsize-property"></a><span data-ttu-id="aaebc-103">Proprietà InstanceParameters. MaxTransactionSize</span><span class="sxs-lookup"><span data-stu-id="aaebc-103">InstanceParameters.MaxTransactionSize property</span></span>

<span data-ttu-id="aaebc-104">Ottiene o imposta la percentuale di archivio versioni che può essere utilizzata dalla transazione meno recente prima di [VersionStoreOutOfMemory](./jet-err-enumeration.md) (impostazione predefinita = 100).</span><span class="sxs-lookup"><span data-stu-id="aaebc-104">Gets or sets the percentage of version store that can be used by oldest transaction before [VersionStoreOutOfMemory](./jet-err-enumeration.md) (default = 100).</span></span>

<span data-ttu-id="aaebc-105">**Spazio dei nomi:**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="aaebc-105">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="aaebc-106">**Assembly:**  Microsoft. ISAM. esent. Interop (in Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="aaebc-106">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="aaebc-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="aaebc-107">Syntax</span></span>

``` vb
'Declaration
Public Property MaxTransactionSize As Integer
    Get
    Set
'Usage
Dim instance As InstanceParameters
Dim value As Integer

value = instance.MaxTransactionSize

instance.MaxTransactionSize = value
```

``` csharp
public int MaxTransactionSize { get; set; }
```

#### <a name="property-value"></a><span data-ttu-id="aaebc-108">Valore proprietà</span><span class="sxs-lookup"><span data-stu-id="aaebc-108">Property value</span></span>

<span data-ttu-id="aaebc-109">Tipo: [System. Int32](/dotnet/api/system.int32)</span><span class="sxs-lookup"><span data-stu-id="aaebc-109">Type: [System.Int32](/dotnet/api/system.int32)</span></span>  

## <a name="see-also"></a><span data-ttu-id="aaebc-110">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="aaebc-110">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="aaebc-111">Riferimento</span><span class="sxs-lookup"><span data-stu-id="aaebc-111">Reference</span></span>

[<span data-ttu-id="aaebc-112">Classe InstanceParameters</span><span class="sxs-lookup"><span data-stu-id="aaebc-112">InstanceParameters class</span></span>](./instanceparameters-class.md)

[<span data-ttu-id="aaebc-113">Membri di InstanceParameters</span><span class="sxs-lookup"><span data-stu-id="aaebc-113">InstanceParameters members</span></span>](./instanceparameters-members.md)

[<span data-ttu-id="aaebc-114">Spazio dei nomi Microsoft. ISAM. esent. Interop</span><span class="sxs-lookup"><span data-stu-id="aaebc-114">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
