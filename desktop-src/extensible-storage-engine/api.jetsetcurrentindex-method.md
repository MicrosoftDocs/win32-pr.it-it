---
description: 'Altre informazioni su: metodo API. JetSetCurrentIndex'
title: API. JetSetCurrentIndex, metodo
TOCTitle: 'JetSetCurrentIndex method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.JetSetCurrentIndex(Microsoft.Isam.Esent.Interop.JET_SESID,Microsoft.Isam.Esent.Interop.JET_TABLEID,System.String)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.jetsetcurrentindex(v=EXCHG.10)
ms:contentKeyID: 55100803
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Api.JetSetCurrentIndex
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Api.JetSetCurrentIndex
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: ed3c069962fe879e250f90e34744780dfe2eb862
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106318827"
---
# <a name="apijetsetcurrentindex-method"></a><span data-ttu-id="d4b97-103">API. JetSetCurrentIndex, metodo</span><span class="sxs-lookup"><span data-stu-id="d4b97-103">Api.JetSetCurrentIndex method</span></span>

<span data-ttu-id="d4b97-104">Imposta l'indice corrente di un cursore.</span><span class="sxs-lookup"><span data-stu-id="d4b97-104">Set the current index of a cursor.</span></span>

<span data-ttu-id="d4b97-105">**Spazio dei nomi:**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="d4b97-105">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="d4b97-106">**Assembly:**  Microsoft. ISAM. esent. Interop (in Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="d4b97-106">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="d4b97-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="d4b97-107">Syntax</span></span>

``` vb
'Declaration
Public Shared Sub JetSetCurrentIndex ( _
    sesid As JET_SESID, _
    tableid As JET_TABLEID, _
    index As String _
)
'Usage
Dim sesid As JET_SESID
Dim tableid As JET_TABLEID
Dim index As StringApi.JetSetCurrentIndex(sesid, tableid, _
    index)
```

``` csharp
public static void JetSetCurrentIndex(
    JET_SESID sesid,
    JET_TABLEID tableid,
    string index
)
```

#### <a name="parameters"></a><span data-ttu-id="d4b97-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="d4b97-108">Parameters</span></span>

  - <span data-ttu-id="d4b97-109">sesid</span><span class="sxs-lookup"><span data-stu-id="d4b97-109">sesid</span></span>  
    <span data-ttu-id="d4b97-110">Tipo: [Microsoft.ISAM.esent.Interop.JET_SESID](./jet-sesid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="d4b97-110">Type: [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)</span></span>  
    
    <span data-ttu-id="d4b97-111">Sessione da utilizzare.</span><span class="sxs-lookup"><span data-stu-id="d4b97-111">The session to use.</span></span>

<!-- end list -->

  - <span data-ttu-id="d4b97-112">TableID</span><span class="sxs-lookup"><span data-stu-id="d4b97-112">tableid</span></span>  
    <span data-ttu-id="d4b97-113">Tipo: [Microsoft.ISAM.esent.Interop.JET_TABLEID](./jet-tableid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="d4b97-113">Type: [Microsoft.Isam.Esent.Interop.JET_TABLEID](./jet-tableid-structure.md)</span></span>  
    
    <span data-ttu-id="d4b97-114">Cursore su cui impostare l'indice.</span><span class="sxs-lookup"><span data-stu-id="d4b97-114">The cursor to set the index on.</span></span>

<!-- end list -->

  - <span data-ttu-id="d4b97-115">indice</span><span class="sxs-lookup"><span data-stu-id="d4b97-115">index</span></span>  
    <span data-ttu-id="d4b97-116">Tipo: [System. String](/dotnet/api/system.string)</span><span class="sxs-lookup"><span data-stu-id="d4b97-116">Type: [System.String](/dotnet/api/system.string)</span></span>  
    
    <span data-ttu-id="d4b97-117">Nome dell'indice da selezionare.</span><span class="sxs-lookup"><span data-stu-id="d4b97-117">The name of the index to be selected.</span></span> <span data-ttu-id="d4b97-118">Se è null o vuoto, verrà selezionato l'indice primario.</span><span class="sxs-lookup"><span data-stu-id="d4b97-118">If this is null or empty the primary index will be selected.</span></span>

## <a name="see-also"></a><span data-ttu-id="d4b97-119">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="d4b97-119">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="d4b97-120">Riferimento</span><span class="sxs-lookup"><span data-stu-id="d4b97-120">Reference</span></span>

[<span data-ttu-id="d4b97-121">Classe API</span><span class="sxs-lookup"><span data-stu-id="d4b97-121">Api class</span></span>](./api-class.md)

[<span data-ttu-id="d4b97-122">Membri API</span><span class="sxs-lookup"><span data-stu-id="d4b97-122">Api members</span></span>](./api-members.md)

[<span data-ttu-id="d4b97-123">Spazio dei nomi Microsoft. ISAM. esent. Interop</span><span class="sxs-lookup"><span data-stu-id="d4b97-123">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
