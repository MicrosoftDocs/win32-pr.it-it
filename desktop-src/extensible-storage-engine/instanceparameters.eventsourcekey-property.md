---
description: 'Altre informazioni su: Proprietà InstanceParameters. EventSourceKey'
title: Proprietà InstanceParameters. EventSourceKey
TOCTitle: 'EventSourceKey property '
ms:assetid: P:Microsoft.Isam.Esent.Interop.InstanceParameters.EventSourceKey
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.instanceparameters.eventsourcekey(v=EXCHG.10)
ms:contentKeyID: 55107449
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.InstanceParameters.EventSourceKey
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.InstanceParameters.set_EventSourceKey
- Microsoft.Isam.Esent.Interop.InstanceParameters.EventSourceKey
- Microsoft.Isam.Esent.Interop.InstanceParameters.get_EventSourceKey
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: d1dc80943095611737d0c9704bcc0e82ffee506f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103966995"
---
# <a name="instanceparameterseventsourcekey-property"></a><span data-ttu-id="d1327-103">Proprietà InstanceParameters. EventSourceKey</span><span class="sxs-lookup"><span data-stu-id="d1327-103">InstanceParameters.EventSourceKey property</span></span>

<span data-ttu-id="d1327-104">Ottiene o imposta il nome del registro eventi utilizzato dal motore di database per i messaggi del log eventi.</span><span class="sxs-lookup"><span data-stu-id="d1327-104">Gets or sets the name of the event log the database engine uses for its event log messages.</span></span> <span data-ttu-id="d1327-105">Per impostazione predefinita, tutti i messaggi del registro eventi vengono inviati al registro eventi dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="d1327-105">By default, all event log messages will go to the Application event log.</span></span> <span data-ttu-id="d1327-106">Se viene configurato il nome della chiave del registro di sistema per un altro log eventi, i messaggi del registro eventi verranno invece inseriti.</span><span class="sxs-lookup"><span data-stu-id="d1327-106">If the registry key name for another event log is configured then the event log messages will go there instead.</span></span>

<span data-ttu-id="d1327-107">**Spazio dei nomi:**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="d1327-107">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="d1327-108">**Assembly:**  Microsoft. ISAM. esent. Interop (in Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="d1327-108">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="d1327-109">Sintassi</span><span class="sxs-lookup"><span data-stu-id="d1327-109">Syntax</span></span>

``` vb
'Declaration
Public Property EventSourceKey As String
    Get
    Set
'Usage
Dim instance As InstanceParameters
Dim value As String

value = instance.EventSourceKey

instance.EventSourceKey = value
```

``` csharp
public string EventSourceKey { get; set; }
```

#### <a name="property-value"></a><span data-ttu-id="d1327-110">Valore proprietà</span><span class="sxs-lookup"><span data-stu-id="d1327-110">Property value</span></span>

<span data-ttu-id="d1327-111">Tipo: [System. String](/dotnet/api/system.string)</span><span class="sxs-lookup"><span data-stu-id="d1327-111">Type: [System.String](/dotnet/api/system.string)</span></span>  

## <a name="see-also"></a><span data-ttu-id="d1327-112">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="d1327-112">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="d1327-113">Riferimento</span><span class="sxs-lookup"><span data-stu-id="d1327-113">Reference</span></span>

[<span data-ttu-id="d1327-114">Classe InstanceParameters</span><span class="sxs-lookup"><span data-stu-id="d1327-114">InstanceParameters class</span></span>](./instanceparameters-class.md)

[<span data-ttu-id="d1327-115">Membri di InstanceParameters</span><span class="sxs-lookup"><span data-stu-id="d1327-115">InstanceParameters members</span></span>](./instanceparameters-members.md)

[<span data-ttu-id="d1327-116">Spazio dei nomi Microsoft. ISAM. esent. Interop</span><span class="sxs-lookup"><span data-stu-id="d1327-116">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
