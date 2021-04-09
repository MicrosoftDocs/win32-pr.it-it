---
description: 'Altre informazioni su: Proprietà InstanceParameters. CleanupMismatchedLogFiles'
title: Proprietà InstanceParameters. CleanupMismatchedLogFiles
TOCTitle: 'CleanupMismatchedLogFiles property '
ms:assetid: P:Microsoft.Isam.Esent.Interop.InstanceParameters.CleanupMismatchedLogFiles
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.instanceparameters.cleanupmismatchedlogfiles(v=EXCHG.10)
ms:contentKeyID: 55103296
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.InstanceParameters.CleanupMismatchedLogFiles
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.InstanceParameters.set_CleanupMismatchedLogFiles
- Microsoft.Isam.Esent.Interop.InstanceParameters.get_CleanupMismatchedLogFiles
- Microsoft.Isam.Esent.Interop.InstanceParameters.CleanupMismatchedLogFiles
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 0e80bb8877335e26cb233a09b2fa3ec3a6f12615
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104130558"
---
# <a name="instanceparameterscleanupmismatchedlogfiles-property"></a><span data-ttu-id="ef5fc-103">Proprietà InstanceParameters. CleanupMismatchedLogFiles</span><span class="sxs-lookup"><span data-stu-id="ef5fc-103">InstanceParameters.CleanupMismatchedLogFiles property</span></span>

<span data-ttu-id="ef5fc-104">Ottiene o imposta un valore che indica se JetInit ha esito negativo quando il motore di database è configurato per iniziare a utilizzare i file di log delle transazioni su disco con dimensioni diverse da quelle configurate.</span><span class="sxs-lookup"><span data-stu-id="ef5fc-104">Gets or sets a value indicating whether JetInit fails when the database engine is configured to start using transaction log files on disk that are of a different size than what is configured.</span></span> <span data-ttu-id="ef5fc-105">In genere, [JetInit (JET_INSTANCE)](./api.jetinit-method.md) recupererà correttamente i database, ma avrà esito negativo con [LogFileSizeMismatchDatabasesConsistent](./jet-err-enumeration.md) per indicare che le dimensioni del file di log non sono configurate correttamente.</span><span class="sxs-lookup"><span data-stu-id="ef5fc-105">Normally, [JetInit(JET_INSTANCE)](./api.jetinit-method.md) will successfully recover the databases but will fail with [LogFileSizeMismatchDatabasesConsistent](./jet-err-enumeration.md) to indicate that the log file size is misconfigured.</span></span> <span data-ttu-id="ef5fc-106">Tuttavia, quando questo parametro è impostato su true, il motore di database eliminerà automaticamente tutti i vecchi file di log, avviando un nuovo set di file di log delle transazioni usando le dimensioni del file di log configurate.</span><span class="sxs-lookup"><span data-stu-id="ef5fc-106">However, when this parameter is set to true then the database engine will silently delete all the old log files, start a new set of transaction log files using the configured log file size.</span></span> <span data-ttu-id="ef5fc-107">Questo parametro è utile quando l'applicazione desidera modificare in modo trasparente le dimensioni del file del log delle transazioni, ma continua a funzionare in modo trasparente negli scenari di aggiornamento e ripristino.</span><span class="sxs-lookup"><span data-stu-id="ef5fc-107">This parameter is useful when the application wishes to transparently change its transaction log file size yet still work transparently in upgrade and restore scenarios.</span></span>

<span data-ttu-id="ef5fc-108">**Spazio dei nomi:**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="ef5fc-108">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="ef5fc-109">**Assembly:**  Microsoft. ISAM. esent. Interop (in Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="ef5fc-109">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="ef5fc-110">Sintassi</span><span class="sxs-lookup"><span data-stu-id="ef5fc-110">Syntax</span></span>

``` vb
'Declaration
Public Property CleanupMismatchedLogFiles As Boolean
    Get
    Set
'Usage
Dim instance As InstanceParameters
Dim value As Boolean

value = instance.CleanupMismatchedLogFiles

instance.CleanupMismatchedLogFiles = value
```

``` csharp
public bool CleanupMismatchedLogFiles { get; set; }
```

#### <a name="property-value"></a><span data-ttu-id="ef5fc-111">Valore proprietà</span><span class="sxs-lookup"><span data-stu-id="ef5fc-111">Property value</span></span>

<span data-ttu-id="ef5fc-112">Tipo: [System. Boolean](/dotnet/api/system.boolean)</span><span class="sxs-lookup"><span data-stu-id="ef5fc-112">Type: [System.Boolean](/dotnet/api/system.boolean)</span></span>  

## <a name="see-also"></a><span data-ttu-id="ef5fc-113">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="ef5fc-113">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="ef5fc-114">Riferimento</span><span class="sxs-lookup"><span data-stu-id="ef5fc-114">Reference</span></span>

[<span data-ttu-id="ef5fc-115">Classe InstanceParameters</span><span class="sxs-lookup"><span data-stu-id="ef5fc-115">InstanceParameters class</span></span>](./instanceparameters-class.md)

[<span data-ttu-id="ef5fc-116">Membri di InstanceParameters</span><span class="sxs-lookup"><span data-stu-id="ef5fc-116">InstanceParameters members</span></span>](./instanceparameters-members.md)

[<span data-ttu-id="ef5fc-117">Spazio dei nomi Microsoft. ISAM. esent. Interop</span><span class="sxs-lookup"><span data-stu-id="ef5fc-117">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
