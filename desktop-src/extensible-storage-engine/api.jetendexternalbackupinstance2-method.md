---
description: 'Altre informazioni su: metodo API. JetEndExternalBackupInstance2'
title: API. JetEndExternalBackupInstance2, metodo
TOCTitle: 'JetEndExternalBackupInstance2 method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.JetEndExternalBackupInstance2(Microsoft.Isam.Esent.Interop.JET_INSTANCE,Microsoft.Isam.Esent.Interop.EndExternalBackupGrbit)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.jetendexternalbackupinstance2(v=EXCHG.10)
ms:contentKeyID: 55100692
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Api.JetEndExternalBackupInstance2
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Api.JetEndExternalBackupInstance2
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 71a405c5e0ba3a398071cc317e0d42dd98c4953d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104225999"
---
# <a name="apijetendexternalbackupinstance2-method"></a><span data-ttu-id="63b1f-103">API. JetEndExternalBackupInstance2, metodo</span><span class="sxs-lookup"><span data-stu-id="63b1f-103">Api.JetEndExternalBackupInstance2 method</span></span>

<span data-ttu-id="63b1f-104">Termina una sessione di backup esterna.</span><span class="sxs-lookup"><span data-stu-id="63b1f-104">Ends an external backup session.</span></span> <span data-ttu-id="63b1f-105">Questa API è l'ultima API in una serie di API che devono essere chiamate per eseguire un backup online (non basato su VSS) riuscito.</span><span class="sxs-lookup"><span data-stu-id="63b1f-105">This API is the last API in a series of APIs that must be called to execute a successful online (non-VSS based) backup.</span></span>

<span data-ttu-id="63b1f-106">**Spazio dei nomi:**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="63b1f-106">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="63b1f-107">**Assembly:**  Microsoft. ISAM. esent. Interop (in Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="63b1f-107">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="63b1f-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="63b1f-108">Syntax</span></span>

``` vb
'Declaration
Public Shared Sub JetEndExternalBackupInstance2 ( _
    instance As JET_INSTANCE, _
    grbit As EndExternalBackupGrbit _
)
'Usage
Dim instance As JET_INSTANCE
Dim grbit As EndExternalBackupGrbitApi.JetEndExternalBackupInstance2(instance, _
    grbit)
```

``` csharp
public static void JetEndExternalBackupInstance2(
    JET_INSTANCE instance,
    EndExternalBackupGrbit grbit
)
```

#### <a name="parameters"></a><span data-ttu-id="63b1f-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="63b1f-109">Parameters</span></span>

  - <span data-ttu-id="63b1f-110">instance</span><span class="sxs-lookup"><span data-stu-id="63b1f-110">instance</span></span>  
    <span data-ttu-id="63b1f-111">Tipo: [Microsoft.ISAM.esent.Interop.JET_INSTANCE](./jet-instance-structure.md)</span><span class="sxs-lookup"><span data-stu-id="63b1f-111">Type: [Microsoft.Isam.Esent.Interop.JET_INSTANCE](./jet-instance-structure.md)</span></span>  
    
    <span data-ttu-id="63b1f-112">Istanza per la quale terminare il backup.</span><span class="sxs-lookup"><span data-stu-id="63b1f-112">The instance to end the backup for.</span></span>

<!-- end list -->

  - <span data-ttu-id="63b1f-113">grbit</span><span class="sxs-lookup"><span data-stu-id="63b1f-113">grbit</span></span>  
    <span data-ttu-id="63b1f-114">Tipo: [Microsoft. ISAM. esent. Interop. EndExternalBackupGrbit](./endexternalbackupgrbit-enumeration.md)</span><span class="sxs-lookup"><span data-stu-id="63b1f-114">Type: [Microsoft.Isam.Esent.Interop.EndExternalBackupGrbit](./endexternalbackupgrbit-enumeration.md)</span></span>  
    
    <span data-ttu-id="63b1f-115">Opzioni che specificano il modo in cui è terminato il backup.</span><span class="sxs-lookup"><span data-stu-id="63b1f-115">Options that specify how the backup ended.</span></span>

## <a name="see-also"></a><span data-ttu-id="63b1f-116">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="63b1f-116">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="63b1f-117">Riferimento</span><span class="sxs-lookup"><span data-stu-id="63b1f-117">Reference</span></span>

[<span data-ttu-id="63b1f-118">Classe API</span><span class="sxs-lookup"><span data-stu-id="63b1f-118">Api class</span></span>](./api-class.md)

[<span data-ttu-id="63b1f-119">Membri API</span><span class="sxs-lookup"><span data-stu-id="63b1f-119">Api members</span></span>](./api-members.md)

[<span data-ttu-id="63b1f-120">Spazio dei nomi Microsoft. ISAM. esent. Interop</span><span class="sxs-lookup"><span data-stu-id="63b1f-120">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
