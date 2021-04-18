---
description: 'Altre informazioni su: Proprietà InstanceParameters. LogBuffers'
title: Proprietà InstanceParameters. LogBuffers
TOCTitle: 'LogBuffers property '
ms:assetid: P:Microsoft.Isam.Esent.Interop.InstanceParameters.LogBuffers
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.instanceparameters.logbuffers(v=EXCHG.10)
ms:contentKeyID: 55107472
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.InstanceParameters.LogBuffers
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.InstanceParameters.get_LogBuffers
- Microsoft.Isam.Esent.Interop.InstanceParameters.LogBuffers
- Microsoft.Isam.Esent.Interop.InstanceParameters.set_LogBuffers
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 7f58e43ea38792549d384328dc0fd6c5d31616e3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106316500"
---
# <a name="instanceparameterslogbuffers-property"></a><span data-ttu-id="0c6f3-103">Proprietà InstanceParameters. LogBuffers</span><span class="sxs-lookup"><span data-stu-id="0c6f3-103">InstanceParameters.LogBuffers property</span></span>

<span data-ttu-id="0c6f3-104">Ottiene o imposta la quantità di memoria utilizzata per memorizzare nella cache i record del log prima che vengano scritti nel file di log delle transazioni.</span><span class="sxs-lookup"><span data-stu-id="0c6f3-104">Gets or sets the amount of memory used to cache log records before they are written to the transaction log file.</span></span> <span data-ttu-id="0c6f3-105">L'unità per questo parametro è la dimensione settoriale del volume che include i file di log delle transazioni.</span><span class="sxs-lookup"><span data-stu-id="0c6f3-105">The unit for this parameter is the sector size of the volume that holds the transaction log files.</span></span> <span data-ttu-id="0c6f3-106">La dimensione del settore è quasi sempre di 512 byte, quindi è sicuro presupporre che le dimensioni dell'unità.</span><span class="sxs-lookup"><span data-stu-id="0c6f3-106">The sector size is almost always 512 bytes, so it is safe to assume that size for the unit.</span></span> <span data-ttu-id="0c6f3-107">Questo parametro ha un effetto sulle prestazioni.</span><span class="sxs-lookup"><span data-stu-id="0c6f3-107">This parameter has an impact on performance.</span></span> <span data-ttu-id="0c6f3-108">Quando il motore di database è sottoposto a un carico di aggiornamento intenso, questo buffer può essere pieno molto rapidamente.</span><span class="sxs-lookup"><span data-stu-id="0c6f3-108">When the database engine is under heavy update load, this buffer can become full very rapidly.</span></span> <span data-ttu-id="0c6f3-109">Una dimensione della cache maggiore per il file di log delle transazioni è essenziale per le prestazioni di aggiornamento ottimali in una condizione di carico elevato.</span><span class="sxs-lookup"><span data-stu-id="0c6f3-109">A larger cache size for the transaction log file is critical for good update performance under such a high load condition.</span></span> <span data-ttu-id="0c6f3-110">Il valore predefinito è troppo piccolo per questo caso.</span><span class="sxs-lookup"><span data-stu-id="0c6f3-110">The default is known to be too small for this case.</span></span> <span data-ttu-id="0c6f3-111">Non impostare questo parametro su un numero di buffer maggiore (in byte) della metà delle dimensioni di un file di log delle transazioni.</span><span class="sxs-lookup"><span data-stu-id="0c6f3-111">Do not set this parameter to a number of buffers that is larger (in bytes) than half the size of a transaction log file.</span></span>

<span data-ttu-id="0c6f3-112">**Spazio dei nomi:**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="0c6f3-112">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="0c6f3-113">**Assembly:**  Microsoft. ISAM. esent. Interop (in Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="0c6f3-113">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="0c6f3-114">Sintassi</span><span class="sxs-lookup"><span data-stu-id="0c6f3-114">Syntax</span></span>

``` vb
'Declaration
Public Property LogBuffers As Integer
    Get
    Set
'Usage
Dim instance As InstanceParameters
Dim value As Integer

value = instance.LogBuffers

instance.LogBuffers = value
```

``` csharp
public int LogBuffers { get; set; }
```

#### <a name="property-value"></a><span data-ttu-id="0c6f3-115">Valore proprietà</span><span class="sxs-lookup"><span data-stu-id="0c6f3-115">Property value</span></span>

<span data-ttu-id="0c6f3-116">Tipo: [System. Int32](/dotnet/api/system.int32)</span><span class="sxs-lookup"><span data-stu-id="0c6f3-116">Type: [System.Int32](/dotnet/api/system.int32)</span></span>  

## <a name="see-also"></a><span data-ttu-id="0c6f3-117">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="0c6f3-117">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="0c6f3-118">Riferimento</span><span class="sxs-lookup"><span data-stu-id="0c6f3-118">Reference</span></span>

[<span data-ttu-id="0c6f3-119">Classe InstanceParameters</span><span class="sxs-lookup"><span data-stu-id="0c6f3-119">InstanceParameters class</span></span>](./instanceparameters-class.md)

[<span data-ttu-id="0c6f3-120">Membri di InstanceParameters</span><span class="sxs-lookup"><span data-stu-id="0c6f3-120">InstanceParameters members</span></span>](./instanceparameters-members.md)

[<span data-ttu-id="0c6f3-121">Spazio dei nomi Microsoft. ISAM. esent. Interop</span><span class="sxs-lookup"><span data-stu-id="0c6f3-121">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
