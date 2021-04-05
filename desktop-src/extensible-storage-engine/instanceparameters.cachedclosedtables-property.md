---
description: 'Altre informazioni su: Proprietà InstanceParameters. CachedClosedTables'
title: Proprietà InstanceParameters. CachedClosedTables
TOCTitle: 'CachedClosedTables property '
ms:assetid: P:Microsoft.Isam.Esent.Interop.InstanceParameters.CachedClosedTables
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.instanceparameters.cachedclosedtables(v=EXCHG.10)
ms:contentKeyID: 55103293
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.InstanceParameters.CachedClosedTables
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.InstanceParameters.get_CachedClosedTables
- Microsoft.Isam.Esent.Interop.InstanceParameters.CachedClosedTables
- Microsoft.Isam.Esent.Interop.InstanceParameters.set_CachedClosedTables
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 8f2465de2df3d25293f5298d40700512b6a086d8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103753975"
---
# <a name="instanceparameterscachedclosedtables-property"></a><span data-ttu-id="0e9f7-103">Proprietà InstanceParameters. CachedClosedTables</span><span class="sxs-lookup"><span data-stu-id="0e9f7-103">InstanceParameters.CachedClosedTables property</span></span>

<span data-ttu-id="0e9f7-104">Ottiene o imposta un valore che indica il numero di risorse dell'albero B + memorizzato nella cache dall'istanza dopo che le tabelle che rappresentano sono state chiuse dall'applicazione.</span><span class="sxs-lookup"><span data-stu-id="0e9f7-104">Gets or sets a value giving the number of B+ Tree resources cached by the instance after the tables they represent have been closed by the application.</span></span> <span data-ttu-id="0e9f7-105">I valori di grandi dimensioni per questo parametro comportano l'utilizzo di una maggiore quantità di memoria da parte del motore di database, ma aumentano la velocità con cui l'applicazione può aprire in modo casuale un numero elevato di tabelle.</span><span class="sxs-lookup"><span data-stu-id="0e9f7-105">Large values for this parameter will cause the database engine to use more memory but will increase the speed with which a large number of tables can be opened randomly by the application.</span></span> <span data-ttu-id="0e9f7-106">Questa operazione è utile per le applicazioni che dispongono di uno schema con un numero molto elevato di tabelle.</span><span class="sxs-lookup"><span data-stu-id="0e9f7-106">This is useful for applications that have a schema with a very large number of tables.</span></span> <span data-ttu-id="0e9f7-107">Supportato in Windows Vista e in alto.</span><span class="sxs-lookup"><span data-stu-id="0e9f7-107">Supported on Windows Vista and up.</span></span> <span data-ttu-id="0e9f7-108">Ignorato in Windows XP e Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="0e9f7-108">Ignored on Windows XP and Windows Server 2003.</span></span>

<span data-ttu-id="0e9f7-109">**Spazio dei nomi:**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="0e9f7-109">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="0e9f7-110">**Assembly:**  Microsoft. ISAM. esent. Interop (in Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="0e9f7-110">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="0e9f7-111">Sintassi</span><span class="sxs-lookup"><span data-stu-id="0e9f7-111">Syntax</span></span>

``` vb
'Declaration
Public Property CachedClosedTables As Integer
    Get
    Set
'Usage
Dim instance As InstanceParameters
Dim value As Integer

value = instance.CachedClosedTables

instance.CachedClosedTables = value
```

``` csharp
public int CachedClosedTables { get; set; }
```

#### <a name="property-value"></a><span data-ttu-id="0e9f7-112">Valore proprietà</span><span class="sxs-lookup"><span data-stu-id="0e9f7-112">Property value</span></span>

<span data-ttu-id="0e9f7-113">Tipo: [System. Int32](/dotnet/api/system.int32)</span><span class="sxs-lookup"><span data-stu-id="0e9f7-113">Type: [System.Int32](/dotnet/api/system.int32)</span></span>  

## <a name="see-also"></a><span data-ttu-id="0e9f7-114">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="0e9f7-114">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="0e9f7-115">Riferimento</span><span class="sxs-lookup"><span data-stu-id="0e9f7-115">Reference</span></span>

[<span data-ttu-id="0e9f7-116">Classe InstanceParameters</span><span class="sxs-lookup"><span data-stu-id="0e9f7-116">InstanceParameters class</span></span>](./instanceparameters-class.md)

[<span data-ttu-id="0e9f7-117">Membri di InstanceParameters</span><span class="sxs-lookup"><span data-stu-id="0e9f7-117">InstanceParameters members</span></span>](./instanceparameters-members.md)

[<span data-ttu-id="0e9f7-118">Spazio dei nomi Microsoft. ISAM. esent. Interop</span><span class="sxs-lookup"><span data-stu-id="0e9f7-118">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
