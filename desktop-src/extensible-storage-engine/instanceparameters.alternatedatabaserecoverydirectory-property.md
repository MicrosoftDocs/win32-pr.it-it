---
description: 'Altre informazioni su: Proprietà InstanceParameters. AlternateDatabaseRecoveryDirectory'
title: Proprietà InstanceParameters. AlternateDatabaseRecoveryDirectory
TOCTitle: 'AlternateDatabaseRecoveryDirectory property '
ms:assetid: P:Microsoft.Isam.Esent.Interop.InstanceParameters.AlternateDatabaseRecoveryDirectory
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.instanceparameters.alternatedatabaserecoverydirectory(v=EXCHG.10)
ms:contentKeyID: 55107440
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.InstanceParameters.AlternateDatabaseRecoveryDirectory
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.InstanceParameters.AlternateDatabaseRecoveryDirectory
- Microsoft.Isam.Esent.Interop.InstanceParameters.get_AlternateDatabaseRecoveryDirectory
- Microsoft.Isam.Esent.Interop.InstanceParameters.set_AlternateDatabaseRecoveryDirectory
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 70e08c65027806990ab511ef8561b41551f0ac2c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106308524"
---
# <a name="instanceparametersalternatedatabaserecoverydirectory-property"></a><span data-ttu-id="72350-103">Proprietà InstanceParameters. AlternateDatabaseRecoveryDirectory</span><span class="sxs-lookup"><span data-stu-id="72350-103">InstanceParameters.AlternateDatabaseRecoveryDirectory property</span></span>

<span data-ttu-id="72350-104">Ottiene o imposta il percorso di file system relativo o assoluto di una cartella in cui il ripristino dell'arresto anomalo o un'operazione di ripristino è in grado di individuare i database a cui si fa riferimento nel log delle transazioni nella cartella specificata.</span><span class="sxs-lookup"><span data-stu-id="72350-104">Gets or sets the relative or absolute file system path of the a folder where crash recovery or a restore operation can find the databases referenced in the transaction log in the specified folder.</span></span>

<span data-ttu-id="72350-105">**Spazio dei nomi:**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="72350-105">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="72350-106">**Assembly:**  Microsoft. ISAM. esent. Interop (in Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="72350-106">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="72350-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="72350-107">Syntax</span></span>

``` vb
'Declaration
Public Property AlternateDatabaseRecoveryDirectory As String
    Get
    Set
'Usage
Dim instance As InstanceParameters
Dim value As String

value = instance.AlternateDatabaseRecoveryDirectory

instance.AlternateDatabaseRecoveryDirectory = value
```

``` csharp
public string AlternateDatabaseRecoveryDirectory { get; set; }
```

#### <a name="property-value"></a><span data-ttu-id="72350-108">Valore proprietà</span><span class="sxs-lookup"><span data-stu-id="72350-108">Property value</span></span>

<span data-ttu-id="72350-109">Tipo: [System. String](/dotnet/api/system.string)</span><span class="sxs-lookup"><span data-stu-id="72350-109">Type: [System.String](/dotnet/api/system.string)</span></span>  

## <a name="remarks"></a><span data-ttu-id="72350-110">Commenti</span><span class="sxs-lookup"><span data-stu-id="72350-110">Remarks</span></span>

<span data-ttu-id="72350-111">Questo parametro viene ignorato in Windows XP.</span><span class="sxs-lookup"><span data-stu-id="72350-111">This parameter is ignored on Windows XP.</span></span>

## <a name="see-also"></a><span data-ttu-id="72350-112">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="72350-112">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="72350-113">Riferimento</span><span class="sxs-lookup"><span data-stu-id="72350-113">Reference</span></span>

[<span data-ttu-id="72350-114">Classe InstanceParameters</span><span class="sxs-lookup"><span data-stu-id="72350-114">InstanceParameters class</span></span>](./instanceparameters-class.md)

[<span data-ttu-id="72350-115">Membri di InstanceParameters</span><span class="sxs-lookup"><span data-stu-id="72350-115">InstanceParameters members</span></span>](./instanceparameters-members.md)

[<span data-ttu-id="72350-116">Spazio dei nomi Microsoft. ISAM. esent. Interop</span><span class="sxs-lookup"><span data-stu-id="72350-116">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
