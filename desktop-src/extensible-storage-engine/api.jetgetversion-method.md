---
description: 'Altre informazioni su: metodo API. JetGetVersion'
title: API. JetGetVersion, metodo
TOCTitle: 'JetGetVersion method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.JetGetVersion(Microsoft.Isam.Esent.Interop.JET_SESID,System.UInt32@)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.jetgetversion(v=EXCHG.10)
ms:contentKeyID: 55100744
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Api.JetGetVersion
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Api.JetGetVersion
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 8860b21ec2b5db3841b866aa9c1c2cc7cff300aa
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104527577"
---
# <a name="apijetgetversion-method"></a><span data-ttu-id="9d1c0-103">API. JetGetVersion, metodo</span><span class="sxs-lookup"><span data-stu-id="9d1c0-103">Api.JetGetVersion method</span></span>

<span data-ttu-id="9d1c0-104">Recupera la versione del motore di database.</span><span class="sxs-lookup"><span data-stu-id="9d1c0-104">Retrieves the version of the database engine.</span></span>

<span data-ttu-id="9d1c0-105">Questa API non è conforme a CLS.</span><span class="sxs-lookup"><span data-stu-id="9d1c0-105">This API is not CLS-compliant.</span></span> 

<span data-ttu-id="9d1c0-106">**Spazio dei nomi:**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="9d1c0-106">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="9d1c0-107">**Assembly:**  Microsoft. ISAM. esent. Interop (in Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="9d1c0-107">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="9d1c0-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="9d1c0-108">Syntax</span></span>

``` vb
'Declaration
<CLSCompliantAttribute(False)> _
Public Shared Sub JetGetVersion ( _
    sesid As JET_SESID, _
    <OutAttribute> ByRef version As UInteger _
)
'Usage
Dim sesid As JET_SESID
Dim version As UIntegerApi.JetGetVersion(sesid, version)
```

``` csharp
[CLSCompliantAttribute(false)]
public static void JetGetVersion(
    JET_SESID sesid,
    out uint version
)
```

#### <a name="parameters"></a><span data-ttu-id="9d1c0-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="9d1c0-109">Parameters</span></span>

  - <span data-ttu-id="9d1c0-110">sesid</span><span class="sxs-lookup"><span data-stu-id="9d1c0-110">sesid</span></span>  
    <span data-ttu-id="9d1c0-111">Tipo: [Microsoft.ISAM.esent.Interop.JET_SESID](./jet-sesid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="9d1c0-111">Type: [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)</span></span>  
    
    <span data-ttu-id="9d1c0-112">Sessione da utilizzare.</span><span class="sxs-lookup"><span data-stu-id="9d1c0-112">The session to use.</span></span>

<!-- end list -->

  - <span data-ttu-id="9d1c0-113">version</span><span class="sxs-lookup"><span data-stu-id="9d1c0-113">version</span></span>  
    <span data-ttu-id="9d1c0-114">Tipo: [System. UInt32](/dotnet/api/system.uint32)</span><span class="sxs-lookup"><span data-stu-id="9d1c0-114">Type: [System.UInt32](/dotnet/api/system.uint32)</span></span>  
    
    <span data-ttu-id="9d1c0-115">Restituisce il numero di versione del motore di database.</span><span class="sxs-lookup"><span data-stu-id="9d1c0-115">Returns the version number of the database engine.</span></span>

## <a name="see-also"></a><span data-ttu-id="9d1c0-116">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="9d1c0-116">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="9d1c0-117">Riferimento</span><span class="sxs-lookup"><span data-stu-id="9d1c0-117">Reference</span></span>

[<span data-ttu-id="9d1c0-118">Classe API</span><span class="sxs-lookup"><span data-stu-id="9d1c0-118">Api class</span></span>](./api-class.md)

[<span data-ttu-id="9d1c0-119">Membri API</span><span class="sxs-lookup"><span data-stu-id="9d1c0-119">Api members</span></span>](./api-members.md)

[<span data-ttu-id="9d1c0-120">Spazio dei nomi Microsoft. ISAM. esent. Interop</span><span class="sxs-lookup"><span data-stu-id="9d1c0-120">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
