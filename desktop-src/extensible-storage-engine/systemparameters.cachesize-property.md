---
description: 'Altre informazioni su: Proprietà SystemParameters. CacheSize'
title: Proprietà SystemParameters. CacheSize
TOCTitle: 'CacheSize property '
ms:assetid: P:Microsoft.Isam.Esent.Interop.SystemParameters.CacheSize
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.systemparameters.cachesize(v=EXCHG.10)
ms:contentKeyID: 55104109
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.SystemParameters.CacheSize
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.SystemParameters.CacheSize
- Microsoft.Isam.Esent.Interop.SystemParameters.set_CacheSize
- Microsoft.Isam.Esent.Interop.SystemParameters.get_CacheSize
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 0981f02df3b807ab56fa20922d1e245f00c2df34
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104233753"
---
# <a name="systemparameterscachesize-property"></a><span data-ttu-id="ec947-103">Proprietà SystemParameters. CacheSize</span><span class="sxs-lookup"><span data-stu-id="ec947-103">SystemParameters.CacheSize property</span></span>

<span data-ttu-id="ec947-104">Ottiene o imposta le dimensioni della cache del database in pagine.</span><span class="sxs-lookup"><span data-stu-id="ec947-104">Gets or sets the size of the database cache in pages.</span></span> <span data-ttu-id="ec947-105">Per impostazione predefinita, le dimensioni della cache del database vengono ottimizzate automaticamente, impostando questa proprietà su un valore diverso da zero, la cache verrà adattata alle dimensioni di destinazione.</span><span class="sxs-lookup"><span data-stu-id="ec947-105">By default the database cache will automatically tune its size, setting this property to a non-zero value will cause the cache to adjust itself to the target size.</span></span>

<span data-ttu-id="ec947-106">**Spazio dei nomi:**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="ec947-106">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="ec947-107">**Assembly:**  Microsoft. ISAM. esent. Interop (in Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="ec947-107">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="ec947-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="ec947-108">Syntax</span></span>

``` vb
'Declaration
Public Shared Property CacheSize As Integer
    Get
    Set
'Usage
Dim value As Integer

value = SystemParameters.CacheSize

SystemParameters.CacheSize = value
```

``` csharp
public static int CacheSize { get; set; }
```

#### <a name="property-value"></a><span data-ttu-id="ec947-109">Valore proprietà</span><span class="sxs-lookup"><span data-stu-id="ec947-109">Property value</span></span>

<span data-ttu-id="ec947-110">Tipo: [System. Int32](/dotnet/api/system.int32)</span><span class="sxs-lookup"><span data-stu-id="ec947-110">Type: [System.Int32](/dotnet/api/system.int32)</span></span>  

## <a name="see-also"></a><span data-ttu-id="ec947-111">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="ec947-111">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="ec947-112">Riferimento</span><span class="sxs-lookup"><span data-stu-id="ec947-112">Reference</span></span>

[<span data-ttu-id="ec947-113">SystemParameters (classe)</span><span class="sxs-lookup"><span data-stu-id="ec947-113">SystemParameters class</span></span>](./systemparameters-class.md)

[<span data-ttu-id="ec947-114">Membri SystemParameters</span><span class="sxs-lookup"><span data-stu-id="ec947-114">SystemParameters members</span></span>](./systemparameters-members.md)

[<span data-ttu-id="ec947-115">Spazio dei nomi Microsoft. ISAM. esent. Interop</span><span class="sxs-lookup"><span data-stu-id="ec947-115">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
