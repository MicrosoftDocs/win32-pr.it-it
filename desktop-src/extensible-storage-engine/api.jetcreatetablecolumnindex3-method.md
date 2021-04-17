---
description: 'Altre informazioni su: metodo API. JetCreateTableColumnIndex3'
title: API. JetCreateTableColumnIndex3, metodo
TOCTitle: 'JetCreateTableColumnIndex3 method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.JetCreateTableColumnIndex3(Microsoft.Isam.Esent.Interop.JET_SESID,Microsoft.Isam.Esent.Interop.JET_DBID,Microsoft.Isam.Esent.Interop.JET_TABLECREATE)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.jetcreatetablecolumnindex3(v=EXCHG.10)
ms:contentKeyID: 55100678
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Api.JetCreateTableColumnIndex3
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Api.JetCreateTableColumnIndex3
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: a967db8f6a322ac29ba8a1e9352972ff1f4f4b76
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104484541"
---
# <a name="apijetcreatetablecolumnindex3-method"></a><span data-ttu-id="24269-103">API. JetCreateTableColumnIndex3, metodo</span><span class="sxs-lookup"><span data-stu-id="24269-103">Api.JetCreateTableColumnIndex3 method</span></span>

<span data-ttu-id="24269-104">Crea una tabella, aggiunge colonne e indici in tale tabella.</span><span class="sxs-lookup"><span data-stu-id="24269-104">Creates a table, adds columns, and indices on that table.</span></span>

<span data-ttu-id="24269-105">**Spazio dei nomi:**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="24269-105">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="24269-106">**Assembly:**  Microsoft. ISAM. esent. Interop (in Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="24269-106">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="24269-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="24269-107">Syntax</span></span>

``` vb
'Declaration
Public Shared Sub JetCreateTableColumnIndex3 ( _
    sesid As JET_SESID, _
    dbid As JET_DBID, _
    tablecreate As JET_TABLECREATE _
)
'Usage
Dim sesid As JET_SESID
Dim dbid As JET_DBID
Dim tablecreate As JET_TABLECREATEApi.JetCreateTableColumnIndex3(sesid, _
    dbid, tablecreate)
```

``` csharp
public static void JetCreateTableColumnIndex3(
    JET_SESID sesid,
    JET_DBID dbid,
    JET_TABLECREATE tablecreate
)
```

#### <a name="parameters"></a><span data-ttu-id="24269-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="24269-108">Parameters</span></span>

  - <span data-ttu-id="24269-109">sesid</span><span class="sxs-lookup"><span data-stu-id="24269-109">sesid</span></span>  
    <span data-ttu-id="24269-110">Tipo: [Microsoft.ISAM.esent.Interop.JET_SESID](./jet-sesid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="24269-110">Type: [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)</span></span>  
    
    <span data-ttu-id="24269-111">Sessione da utilizzare.</span><span class="sxs-lookup"><span data-stu-id="24269-111">The session to use.</span></span>

<!-- end list -->

  - <span data-ttu-id="24269-112">dbid</span><span class="sxs-lookup"><span data-stu-id="24269-112">dbid</span></span>  
    <span data-ttu-id="24269-113">Tipo: [Microsoft.ISAM.esent.Interop.JET_DBID](./jet-dbid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="24269-113">Type: [Microsoft.Isam.Esent.Interop.JET_DBID](./jet-dbid-structure.md)</span></span>  
    
    <span data-ttu-id="24269-114">Database al quale aggiungere la nuova tabella.</span><span class="sxs-lookup"><span data-stu-id="24269-114">The database to which to add the new table.</span></span>

<!-- end list -->

  - <span data-ttu-id="24269-115">tablecreate</span><span class="sxs-lookup"><span data-stu-id="24269-115">tablecreate</span></span>  
    <span data-ttu-id="24269-116">Tipo: [Microsoft.ISAM.esent.Interop.JET_TABLECREATE](./jet-tablecreate-class.md)</span><span class="sxs-lookup"><span data-stu-id="24269-116">Type: [Microsoft.Isam.Esent.Interop.JET_TABLECREATE](./jet-tablecreate-class.md)</span></span>  
    
    <span data-ttu-id="24269-117">Oggetto che descrive la tabella da creare.</span><span class="sxs-lookup"><span data-stu-id="24269-117">Object describing the table to create.</span></span>

## <a name="see-also"></a><span data-ttu-id="24269-118">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="24269-118">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="24269-119">Riferimento</span><span class="sxs-lookup"><span data-stu-id="24269-119">Reference</span></span>

[<span data-ttu-id="24269-120">Classe API</span><span class="sxs-lookup"><span data-stu-id="24269-120">Api class</span></span>](./api-class.md)

[<span data-ttu-id="24269-121">Membri API</span><span class="sxs-lookup"><span data-stu-id="24269-121">Api members</span></span>](./api-members.md)

[<span data-ttu-id="24269-122">Spazio dei nomi Microsoft. ISAM. esent. Interop</span><span class="sxs-lookup"><span data-stu-id="24269-122">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
