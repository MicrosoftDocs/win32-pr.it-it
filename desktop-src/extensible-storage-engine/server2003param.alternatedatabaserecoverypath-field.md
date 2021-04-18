---
description: 'Altre informazioni su: campo Server2003Param. AlternateDatabaseRecoveryPath'
title: Campo Server2003Param. AlternateDatabaseRecoveryPath (Microsoft. ISAM. esent. Interop. Server2003)
TOCTitle: AlternateDatabaseRecoveryPath field
ms:assetid: F:Microsoft.Isam.Esent.Interop.Server2003.Server2003Param.AlternateDatabaseRecoveryPath
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.server2003.server2003param.alternatedatabaserecoverypath(v=EXCHG.10)
ms:contentKeyID: 55104217
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Server2003.Server2003Param.AlternateDatabaseRecoveryPath
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Server2003.Server2003Param.AlternateDatabaseRecoveryPath
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 770ac27596b4385d0012cb65847754b4deb7e9fc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106308489"
---
# <a name="server2003paramalternatedatabaserecoverypath-field"></a><span data-ttu-id="88a35-103">Campo Server2003Param. AlternateDatabaseRecoveryPath</span><span class="sxs-lookup"><span data-stu-id="88a35-103">Server2003Param.AlternateDatabaseRecoveryPath field</span></span>

<span data-ttu-id="88a35-104">Il percorso completo di ogni database viene reso permanente nei log delle transazioni in fase di esecuzione.</span><span class="sxs-lookup"><span data-stu-id="88a35-104">The full path to each database is persisted in the transaction logs at run time.</span></span> <span data-ttu-id="88a35-105">In genere, è necessario che questi database rimangano nel percorso originale affinché la riproduzione delle transazioni funzioni correttamente.</span><span class="sxs-lookup"><span data-stu-id="88a35-105">Ordinarily, these databases must remain at the original location for transaction replay to function correctly.</span></span> <span data-ttu-id="88a35-106">Questo parametro può essere utilizzato per forzare il ripristino dell'arresto anomalo del sistema o un'operazione di ripristino per la ricerca dei database a cui si fa riferimento nel log delle transazioni nella cartella specificata.</span><span class="sxs-lookup"><span data-stu-id="88a35-106">This parameter can be used to force crash recovery or a restore operation to look for the databases referenced in the transaction log in the specified folder.</span></span>

<span data-ttu-id="88a35-107">**Spazio dei nomi:**  [Microsoft. ISAM. esent. Interop. Server2003](./microsoft.isam.esent.interop.server2003-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="88a35-107">**Namespace:**  [Microsoft.Isam.Esent.Interop.Server2003](./microsoft.isam.esent.interop.server2003-namespace.md)</span></span>  
<span data-ttu-id="88a35-108">**Assembly:**  Microsoft. ISAM. esent. Interop (in Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="88a35-108">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="88a35-109">Sintassi</span><span class="sxs-lookup"><span data-stu-id="88a35-109">Syntax</span></span>

``` vb
'Declaration
Public Const AlternateDatabaseRecoveryPath As JET_param
'Usage
Dim value As JET_param

value = Server2003Param.AlternateDatabaseRecoveryPath
```

``` csharp
public const JET_param AlternateDatabaseRecoveryPath
```

## <a name="see-also"></a><span data-ttu-id="88a35-110">Vedere anche</span><span class="sxs-lookup"><span data-stu-id="88a35-110">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="88a35-111">Riferimento</span><span class="sxs-lookup"><span data-stu-id="88a35-111">Reference</span></span>

[<span data-ttu-id="88a35-112">Classe Server2003Param</span><span class="sxs-lookup"><span data-stu-id="88a35-112">Server2003Param class</span></span>](./server2003param-class.md)

[<span data-ttu-id="88a35-113">Membri di Server2003Param</span><span class="sxs-lookup"><span data-stu-id="88a35-113">Server2003Param members</span></span>](./server2003param-members.md)

[<span data-ttu-id="88a35-114">Spazio dei nomi Microsoft. ISAM. esent. Interop. Server2003</span><span class="sxs-lookup"><span data-stu-id="88a35-114">Microsoft.Isam.Esent.Interop.Server2003 namespace</span></span>](./microsoft.isam.esent.interop.server2003-namespace.md)
