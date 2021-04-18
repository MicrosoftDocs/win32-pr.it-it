---
description: 'Altre informazioni su: Proprietà InstanceParameters. MaxTemporaryTables'
title: Proprietà InstanceParameters. MaxTemporaryTables
TOCTitle: 'MaxTemporaryTables property '
ms:assetid: P:Microsoft.Isam.Esent.Interop.InstanceParameters.MaxTemporaryTables
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.instanceparameters.maxtemporarytables(v=EXCHG.10)
ms:contentKeyID: 55103560
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.InstanceParameters.MaxTemporaryTables
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.InstanceParameters.set_MaxTemporaryTables
- Microsoft.Isam.Esent.Interop.InstanceParameters.MaxTemporaryTables
- Microsoft.Isam.Esent.Interop.InstanceParameters.get_MaxTemporaryTables
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: e5802e512a4ea6a4916ae54c24357dbdad057540
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106315161"
---
# <a name="instanceparametersmaxtemporarytables-property"></a><span data-ttu-id="7ba77-103">Proprietà InstanceParameters. MaxTemporaryTables</span><span class="sxs-lookup"><span data-stu-id="7ba77-103">InstanceParameters.MaxTemporaryTables property</span></span>

<span data-ttu-id="7ba77-104">Ottiene o imposta il numero di risorse della tabella temporanea utilizzate da un'istanza di.</span><span class="sxs-lookup"><span data-stu-id="7ba77-104">Gets or sets the number of temporary table resources for use by an instance.</span></span> <span data-ttu-id="7ba77-105">Questa impostazione influirà sul numero di tabelle temporanee che possono essere usate contemporaneamente.</span><span class="sxs-lookup"><span data-stu-id="7ba77-105">This setting will affect how many temporary tables can be used at the same time.</span></span> <span data-ttu-id="7ba77-106">Se questo parametro di sistema è impostato su zero, non verrà creato alcun database temporaneo e le attività che richiedono l'utilizzo del database temporaneo avranno esito negativo.</span><span class="sxs-lookup"><span data-stu-id="7ba77-106">If this system parameter is set to zero then no temporary database will be created and any activity that requires use of the temporary database will fail.</span></span> <span data-ttu-id="7ba77-107">Questa impostazione può essere utile per evitare l'i/O necessario per creare il database temporaneo se è noto che non verrà utilizzato.</span><span class="sxs-lookup"><span data-stu-id="7ba77-107">This setting can be useful to avoid the I/O required to create the temporary database if it is known that it will not be used.</span></span>

<span data-ttu-id="7ba77-108">**Spazio dei nomi:**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="7ba77-108">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="7ba77-109">**Assembly:**  Microsoft. ISAM. esent. Interop (in Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="7ba77-109">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="7ba77-110">Sintassi</span><span class="sxs-lookup"><span data-stu-id="7ba77-110">Syntax</span></span>

``` vb
'Declaration
Public Property MaxTemporaryTables As Integer
    Get
    Set
'Usage
Dim instance As InstanceParameters
Dim value As Integer

value = instance.MaxTemporaryTables

instance.MaxTemporaryTables = value
```

``` csharp
public int MaxTemporaryTables { get; set; }
```

#### <a name="property-value"></a><span data-ttu-id="7ba77-111">Valore proprietà</span><span class="sxs-lookup"><span data-stu-id="7ba77-111">Property value</span></span>

<span data-ttu-id="7ba77-112">Tipo: [System. Int32](/dotnet/api/system.int32)</span><span class="sxs-lookup"><span data-stu-id="7ba77-112">Type: [System.Int32](/dotnet/api/system.int32)</span></span>  

## <a name="remarks"></a><span data-ttu-id="7ba77-113">Commenti</span><span class="sxs-lookup"><span data-stu-id="7ba77-113">Remarks</span></span>

<span data-ttu-id="7ba77-114">Per l'utilizzo di una tabella temporanea è inoltre necessaria una risorsa Cursor.</span><span class="sxs-lookup"><span data-stu-id="7ba77-114">The use of a temporary table also requires a cursor resource.</span></span>

## <a name="see-also"></a><span data-ttu-id="7ba77-115">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="7ba77-115">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="7ba77-116">Riferimento</span><span class="sxs-lookup"><span data-stu-id="7ba77-116">Reference</span></span>

[<span data-ttu-id="7ba77-117">Classe InstanceParameters</span><span class="sxs-lookup"><span data-stu-id="7ba77-117">InstanceParameters class</span></span>](./instanceparameters-class.md)

[<span data-ttu-id="7ba77-118">Membri di InstanceParameters</span><span class="sxs-lookup"><span data-stu-id="7ba77-118">InstanceParameters members</span></span>](./instanceparameters-members.md)

[<span data-ttu-id="7ba77-119">Spazio dei nomi Microsoft. ISAM. esent. Interop</span><span class="sxs-lookup"><span data-stu-id="7ba77-119">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
