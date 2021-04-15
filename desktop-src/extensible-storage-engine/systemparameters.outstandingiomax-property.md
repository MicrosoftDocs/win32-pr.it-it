---
description: 'Altre informazioni su: Proprietà SystemParameters. OutstandingIOMax'
title: Proprietà SystemParameters. OutstandingIOMax
TOCTitle: 'OutstandingIOMax property '
ms:assetid: P:Microsoft.Isam.Esent.Interop.SystemParameters.OutstandingIOMax
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.systemparameters.outstandingiomax(v=EXCHG.10)
ms:contentKeyID: 55104045
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.SystemParameters.OutstandingIOMax
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.SystemParameters.get_OutstandingIOMax
- Microsoft.Isam.Esent.Interop.SystemParameters.OutstandingIOMax
- Microsoft.Isam.Esent.Interop.SystemParameters.set_OutstandingIOMax
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 7faf7af3aec16bc81fada5c8742b4c60595bedad
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104529286"
---
# <a name="systemparametersoutstandingiomax-property"></a><span data-ttu-id="896f1-103">Proprietà SystemParameters. OutstandingIOMax</span><span class="sxs-lookup"><span data-stu-id="896f1-103">SystemParameters.OutstandingIOMax property</span></span>

<span data-ttu-id="896f1-104">Questo parametro controlla il numero di I/o di file di database che possono essere accodati per singolo disco nel sistema operativo host alla volta.</span><span class="sxs-lookup"><span data-stu-id="896f1-104">This parameter controls how many database file I/Os can be queued per-disk in the host operating system at one time.</span></span> <span data-ttu-id="896f1-105">Un valore più elevato per questo parametro può migliorare significativamente le prestazioni di un'applicazione di database di grandi dimensioni.</span><span class="sxs-lookup"><span data-stu-id="896f1-105">A larger value for this parameter can significantly help the performance of a large database application.</span></span>

<span data-ttu-id="896f1-106">**Spazio dei nomi:**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="896f1-106">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="896f1-107">**Assembly:**  Microsoft. ISAM. esent. Interop (in Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="896f1-107">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="896f1-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="896f1-108">Syntax</span></span>

``` vb
'Declaration
Public Shared Property OutstandingIOMax As Integer
    Get
    Set
'Usage
Dim value As Integer

value = SystemParameters.OutstandingIOMax

SystemParameters.OutstandingIOMax = value
```

``` csharp
public static int OutstandingIOMax { get; set; }
```

#### <a name="property-value"></a><span data-ttu-id="896f1-109">Valore proprietà</span><span class="sxs-lookup"><span data-stu-id="896f1-109">Property value</span></span>

<span data-ttu-id="896f1-110">Tipo: [System. Int32](/dotnet/api/system.int32)</span><span class="sxs-lookup"><span data-stu-id="896f1-110">Type: [System.Int32](/dotnet/api/system.int32)</span></span>  

## <a name="see-also"></a><span data-ttu-id="896f1-111">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="896f1-111">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="896f1-112">Riferimento</span><span class="sxs-lookup"><span data-stu-id="896f1-112">Reference</span></span>

[<span data-ttu-id="896f1-113">SystemParameters (classe)</span><span class="sxs-lookup"><span data-stu-id="896f1-113">SystemParameters class</span></span>](./systemparameters-class.md)

[<span data-ttu-id="896f1-114">Membri SystemParameters</span><span class="sxs-lookup"><span data-stu-id="896f1-114">SystemParameters members</span></span>](./systemparameters-members.md)

[<span data-ttu-id="896f1-115">Spazio dei nomi Microsoft. ISAM. esent. Interop</span><span class="sxs-lookup"><span data-stu-id="896f1-115">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
