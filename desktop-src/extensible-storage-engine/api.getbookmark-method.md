---
description: 'Altre informazioni su: API. GetBookmark (metodo)'
title: API. GetBookmark, metodo
TOCTitle: 'GetBookmark method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.GetBookmark(Microsoft.Isam.Esent.Interop.JET_SESID,Microsoft.Isam.Esent.Interop.JET_TABLEID)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.getbookmark(v=EXCHG.10)
ms:contentKeyID: 55100654
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Api.GetBookmark
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Api.GetBookmark
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 4edcdfe7ddefadd993ef9c96e6dcc1416080b413
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104524793"
---
# <a name="apigetbookmark-method"></a><span data-ttu-id="13027-103">API. GetBookmark, metodo</span><span class="sxs-lookup"><span data-stu-id="13027-103">Api.GetBookmark method</span></span>

<span data-ttu-id="13027-104">Recupera il segnalibro per il record associato alla voce di indice in corrispondenza della posizione corrente di un cursore.</span><span class="sxs-lookup"><span data-stu-id="13027-104">Retrieves the bookmark for the record that is associated with the index entry at the current position of a cursor.</span></span> <span data-ttu-id="13027-105">Questo segnalibro può quindi essere utilizzato per riposizionare il cursore sullo stesso record utilizzando JetGotoBookmark.</span><span class="sxs-lookup"><span data-stu-id="13027-105">This bookmark can then be used to reposition that cursor back to the same record using JetGotoBookmark.</span></span>

<span data-ttu-id="13027-106">**Spazio dei nomi:**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="13027-106">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="13027-107">**Assembly:**  Microsoft. ISAM. esent. Interop (in Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="13027-107">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="13027-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="13027-108">Syntax</span></span>

``` vb
'Declaration
Public Shared Function GetBookmark ( _
    sesid As JET_SESID, _
    tableid As JET_TABLEID _
) As Byte()
'Usage
Dim sesid As JET_SESID
Dim tableid As JET_TABLEID
Dim returnValue As Byte()

returnValue = Api.GetBookmark(sesid, _
    tableid)
```

``` csharp
public static byte[] GetBookmark(
    JET_SESID sesid,
    JET_TABLEID tableid
)
```

#### <a name="parameters"></a><span data-ttu-id="13027-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="13027-109">Parameters</span></span>

  - <span data-ttu-id="13027-110">sesid</span><span class="sxs-lookup"><span data-stu-id="13027-110">sesid</span></span>  
    <span data-ttu-id="13027-111">Tipo: [Microsoft.ISAM.esent.Interop.JET_SESID](./jet-sesid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="13027-111">Type: [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)</span></span>  
    
    <span data-ttu-id="13027-112">Sessione da utilizzare.</span><span class="sxs-lookup"><span data-stu-id="13027-112">The session to use.</span></span>

<!-- end list -->

  - <span data-ttu-id="13027-113">TableID</span><span class="sxs-lookup"><span data-stu-id="13027-113">tableid</span></span>  
    <span data-ttu-id="13027-114">Tipo: [Microsoft.ISAM.esent.Interop.JET_TABLEID](./jet-tableid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="13027-114">Type: [Microsoft.Isam.Esent.Interop.JET_TABLEID](./jet-tableid-structure.md)</span></span>  
    
    <span data-ttu-id="13027-115">Cursore da cui recuperare il segnalibro.</span><span class="sxs-lookup"><span data-stu-id="13027-115">The cursor to retrieve the bookmark from.</span></span>

#### <a name="return-value"></a><span data-ttu-id="13027-116">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="13027-116">Return value</span></span>

<span data-ttu-id="13027-117">Tipo \[\]</span><span class="sxs-lookup"><span data-stu-id="13027-117">Type: \[\]</span></span>  
<span data-ttu-id="13027-118">Segnalibro del record.</span><span class="sxs-lookup"><span data-stu-id="13027-118">The bookmark of the record.</span></span>  

## <a name="see-also"></a><span data-ttu-id="13027-119">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="13027-119">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="13027-120">Riferimento</span><span class="sxs-lookup"><span data-stu-id="13027-120">Reference</span></span>

[<span data-ttu-id="13027-121">Classe API</span><span class="sxs-lookup"><span data-stu-id="13027-121">Api class</span></span>](./api-class.md)

[<span data-ttu-id="13027-122">Membri API</span><span class="sxs-lookup"><span data-stu-id="13027-122">Api members</span></span>](./api-members.md)

[<span data-ttu-id="13027-123">Spazio dei nomi Microsoft. ISAM. esent. Interop</span><span class="sxs-lookup"><span data-stu-id="13027-123">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
