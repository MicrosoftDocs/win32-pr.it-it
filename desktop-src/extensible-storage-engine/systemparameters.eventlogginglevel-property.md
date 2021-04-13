---
description: 'Altre informazioni su: Proprietà SystemParameters. EventLoggingLevel'
title: Proprietà SystemParameters. EventLoggingLevel
TOCTitle: 'EventLoggingLevel property '
ms:assetid: P:Microsoft.Isam.Esent.Interop.SystemParameters.EventLoggingLevel
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.systemparameters.eventlogginglevel(v=EXCHG.10)
ms:contentKeyID: 55104119
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.SystemParameters.EventLoggingLevel
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.SystemParameters.set_EventLoggingLevel
- Microsoft.Isam.Esent.Interop.SystemParameters.EventLoggingLevel
- Microsoft.Isam.Esent.Interop.SystemParameters.get_EventLoggingLevel
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 6e70ef2c0adff6982a34c8e11cc2140f51229299
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104350406"
---
# <a name="systemparameterseventlogginglevel-property"></a><span data-ttu-id="9d746-103">Proprietà SystemParameters. EventLoggingLevel</span><span class="sxs-lookup"><span data-stu-id="9d746-103">SystemParameters.EventLoggingLevel property</span></span>

<span data-ttu-id="9d746-104">Ottiene o imposta il livello di dettaglio dei messaggi EventLog emessi al log eventi dal motore di database.</span><span class="sxs-lookup"><span data-stu-id="9d746-104">Gets or sets the detail level of eventlog messages that are emitted to the eventlog by the database engine.</span></span> <span data-ttu-id="9d746-105">I numeri più alti comporteranno messaggi EventLog più dettagliati.</span><span class="sxs-lookup"><span data-stu-id="9d746-105">Higher numbers will result in more detailed eventlog messages.</span></span>

<span data-ttu-id="9d746-106">**Spazio dei nomi:**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="9d746-106">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="9d746-107">**Assembly:**  Microsoft. ISAM. esent. Interop (in Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="9d746-107">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="9d746-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="9d746-108">Syntax</span></span>

``` vb
'Declaration
Public Shared Property EventLoggingLevel As Integer
    Get
    Set
'Usage
Dim value As Integer

value = SystemParameters.EventLoggingLevel

SystemParameters.EventLoggingLevel = value
```

``` csharp
public static int EventLoggingLevel { get; set; }
```

#### <a name="property-value"></a><span data-ttu-id="9d746-109">Valore proprietà</span><span class="sxs-lookup"><span data-stu-id="9d746-109">Property value</span></span>

<span data-ttu-id="9d746-110">Tipo: [System. Int32](/dotnet/api/system.int32)</span><span class="sxs-lookup"><span data-stu-id="9d746-110">Type: [System.Int32](/dotnet/api/system.int32)</span></span>  

## <a name="see-also"></a><span data-ttu-id="9d746-111">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="9d746-111">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="9d746-112">Riferimento</span><span class="sxs-lookup"><span data-stu-id="9d746-112">Reference</span></span>

[<span data-ttu-id="9d746-113">SystemParameters (classe)</span><span class="sxs-lookup"><span data-stu-id="9d746-113">SystemParameters class</span></span>](./systemparameters-class.md)

[<span data-ttu-id="9d746-114">Membri SystemParameters</span><span class="sxs-lookup"><span data-stu-id="9d746-114">SystemParameters members</span></span>](./systemparameters-members.md)

[<span data-ttu-id="9d746-115">Spazio dei nomi Microsoft. ISAM. esent. Interop</span><span class="sxs-lookup"><span data-stu-id="9d746-115">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
