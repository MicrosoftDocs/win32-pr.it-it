---
description: 'Altre informazioni su: campo VistaParam. CachedClosedTables'
title: Campo VistaParam. CachedClosedTables (Microsoft. ISAM. esent. Interop. vista)
TOCTitle: CachedClosedTables field
ms:assetid: F:Microsoft.Isam.Esent.Interop.Vista.VistaParam.CachedClosedTables
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.vista.vistaparam.cachedclosedtables(v=EXCHG.10)
ms:contentKeyID: 55104337
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Vista.VistaParam.CachedClosedTables
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Vista.VistaParam.CachedClosedTables
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: ff72925e34c731e57d11170753ecff13f4b96a39
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104128150"
---
# <a name="vistaparamcachedclosedtables-field"></a><span data-ttu-id="8dbc7-103">Campo VistaParam. CachedClosedTables</span><span class="sxs-lookup"><span data-stu-id="8dbc7-103">VistaParam.CachedClosedTables field</span></span>

<span data-ttu-id="8dbc7-104">Questo parametro controlla il numero di risorse dell'albero B + memorizzato nella cache dall'istanza dopo che le tabelle che rappresentano sono state chiuse dall'applicazione.</span><span class="sxs-lookup"><span data-stu-id="8dbc7-104">This parameter controls the number of B+ Tree resources cached by the instance after the tables they represent have been closed by the application.</span></span> <span data-ttu-id="8dbc7-105">I valori di grandi dimensioni per questo parametro comportano l'utilizzo di una maggiore quantità di memoria da parte del motore di database, ma aumentano la velocità con cui l'applicazione può aprire in modo casuale un numero elevato di tabelle.</span><span class="sxs-lookup"><span data-stu-id="8dbc7-105">Large values for this parameter will cause the database engine to use more memory but will increase the speed with which a large number of tables can be opened randomly by the application.</span></span> <span data-ttu-id="8dbc7-106">Questa operazione è utile per le applicazioni che dispongono di uno schema con un numero molto elevato di tabelle.</span><span class="sxs-lookup"><span data-stu-id="8dbc7-106">This is useful for applications that have a schema with a very large number of tables.</span></span>

<span data-ttu-id="8dbc7-107">**Spazio dei nomi:**  [Microsoft. ISAM. esent. Interop. vista](./microsoft.isam.esent.interop.vista-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="8dbc7-107">**Namespace:**  [Microsoft.Isam.Esent.Interop.Vista](./microsoft.isam.esent.interop.vista-namespace.md)</span></span>  
<span data-ttu-id="8dbc7-108">**Assembly:**  Microsoft. ISAM. esent. Interop (in Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="8dbc7-108">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="8dbc7-109">Sintassi</span><span class="sxs-lookup"><span data-stu-id="8dbc7-109">Syntax</span></span>

``` vb
'Declaration
Public Const CachedClosedTables As JET_param
'Usage
Dim value As JET_param

value = VistaParam.CachedClosedTables
```

``` csharp
public const JET_param CachedClosedTables
```

## <a name="see-also"></a><span data-ttu-id="8dbc7-110">Vedere anche</span><span class="sxs-lookup"><span data-stu-id="8dbc7-110">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="8dbc7-111">Riferimento</span><span class="sxs-lookup"><span data-stu-id="8dbc7-111">Reference</span></span>

[<span data-ttu-id="8dbc7-112">Classe VistaParam</span><span class="sxs-lookup"><span data-stu-id="8dbc7-112">VistaParam class</span></span>](./vistaparam-class.md)

[<span data-ttu-id="8dbc7-113">Membri di VistaParam</span><span class="sxs-lookup"><span data-stu-id="8dbc7-113">VistaParam members</span></span>](./vistaparam-members.md)

[<span data-ttu-id="8dbc7-114">Spazio dei nomi Microsoft. ISAM. esent. Interop. vista</span><span class="sxs-lookup"><span data-stu-id="8dbc7-114">Microsoft.Isam.Esent.Interop.Vista namespace</span></span>](./microsoft.isam.esent.interop.vista-namespace.md)
