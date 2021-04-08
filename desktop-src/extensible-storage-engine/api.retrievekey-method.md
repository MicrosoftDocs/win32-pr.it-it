---
description: 'Altre informazioni su: metodo API. RetrieveKey'
title: API. RetrieveKey, metodo
TOCTitle: 'RetrieveKey method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.RetrieveKey(Microsoft.Isam.Esent.Interop.JET_SESID,Microsoft.Isam.Esent.Interop.JET_TABLEID,Microsoft.Isam.Esent.Interop.RetrieveKeyGrbit)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.retrievekey(v=EXCHG.10)
ms:contentKeyID: 55100880
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Api.RetrieveKey
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Api.RetrieveKey
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: fcabab7639a9cf3128b0b2c314ba60c2de8f8e09
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103749490"
---
# <a name="apiretrievekey-method"></a><span data-ttu-id="1363e-103">API. RetrieveKey, metodo</span><span class="sxs-lookup"><span data-stu-id="1363e-103">Api.RetrieveKey method</span></span>

<span data-ttu-id="1363e-104">Recupera la chiave per la voce di indice in corrispondenza della posizione corrente di un cursore.</span><span class="sxs-lookup"><span data-stu-id="1363e-104">Retrieves the key for the index entry at the current position of a cursor.</span></span>

<span data-ttu-id="1363e-105">**Spazio dei nomi:**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="1363e-105">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="1363e-106">**Assembly:**  Microsoft. ISAM. esent. Interop (in Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="1363e-106">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="1363e-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="1363e-107">Syntax</span></span>

``` vb
'Declaration
Public Shared Function RetrieveKey ( _
    sesid As JET_SESID, _
    tableid As JET_TABLEID, _
    grbit As RetrieveKeyGrbit _
) As Byte()
'Usage
Dim sesid As JET_SESID
Dim tableid As JET_TABLEID
Dim grbit As RetrieveKeyGrbit
Dim returnValue As Byte()

returnValue = Api.RetrieveKey(sesid, _
    tableid, grbit)
```

``` csharp
public static byte[] RetrieveKey(
    JET_SESID sesid,
    JET_TABLEID tableid,
    RetrieveKeyGrbit grbit
)
```

#### <a name="parameters"></a><span data-ttu-id="1363e-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="1363e-108">Parameters</span></span>

  - <span data-ttu-id="1363e-109">sesid</span><span class="sxs-lookup"><span data-stu-id="1363e-109">sesid</span></span>  
    <span data-ttu-id="1363e-110">Tipo: [Microsoft.ISAM.esent.Interop.JET_SESID](./jet-sesid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="1363e-110">Type: [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)</span></span>  
    
    <span data-ttu-id="1363e-111">Sessione da utilizzare.</span><span class="sxs-lookup"><span data-stu-id="1363e-111">The session to use.</span></span>

<!-- end list -->

  - <span data-ttu-id="1363e-112">TableID</span><span class="sxs-lookup"><span data-stu-id="1363e-112">tableid</span></span>  
    <span data-ttu-id="1363e-113">Tipo: [Microsoft.ISAM.esent.Interop.JET_TABLEID](./jet-tableid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="1363e-113">Type: [Microsoft.Isam.Esent.Interop.JET_TABLEID](./jet-tableid-structure.md)</span></span>  
    
    <span data-ttu-id="1363e-114">Cursore da cui recuperare la chiave.</span><span class="sxs-lookup"><span data-stu-id="1363e-114">The cursor to retrieve the key from.</span></span>

<!-- end list -->

  - <span data-ttu-id="1363e-115">grbit</span><span class="sxs-lookup"><span data-stu-id="1363e-115">grbit</span></span>  
    <span data-ttu-id="1363e-116">Tipo: [Microsoft. ISAM. esent. Interop. RetrieveKeyGrbit](./retrievekeygrbit-enumeration.md)</span><span class="sxs-lookup"><span data-stu-id="1363e-116">Type: [Microsoft.Isam.Esent.Interop.RetrieveKeyGrbit](./retrievekeygrbit-enumeration.md)</span></span>  
    
    <span data-ttu-id="1363e-117">Recupera le opzioni della chiave.</span><span class="sxs-lookup"><span data-stu-id="1363e-117">Retrieve key options.</span></span>

#### <a name="return-value"></a><span data-ttu-id="1363e-118">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="1363e-118">Return value</span></span>

<span data-ttu-id="1363e-119">Tipo \[\]</span><span class="sxs-lookup"><span data-stu-id="1363e-119">Type: \[\]</span></span>  
<span data-ttu-id="1363e-120">Chiave recuperata.</span><span class="sxs-lookup"><span data-stu-id="1363e-120">The retrieved key.</span></span>  

## <a name="see-also"></a><span data-ttu-id="1363e-121">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="1363e-121">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="1363e-122">Riferimento</span><span class="sxs-lookup"><span data-stu-id="1363e-122">Reference</span></span>

[<span data-ttu-id="1363e-123">Classe API</span><span class="sxs-lookup"><span data-stu-id="1363e-123">Api class</span></span>](./api-class.md)

[<span data-ttu-id="1363e-124">Membri API</span><span class="sxs-lookup"><span data-stu-id="1363e-124">Api members</span></span>](./api-members.md)

[<span data-ttu-id="1363e-125">Spazio dei nomi Microsoft. ISAM. esent. Interop</span><span class="sxs-lookup"><span data-stu-id="1363e-125">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
