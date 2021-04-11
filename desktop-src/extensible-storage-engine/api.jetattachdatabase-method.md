---
description: 'Altre informazioni su: metodo API. JetAttachDatabase'
title: API. JetAttachDatabase, metodo
TOCTitle: 'JetAttachDatabase method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.JetAttachDatabase(Microsoft.Isam.Esent.Interop.JET_SESID,System.String,Microsoft.Isam.Esent.Interop.AttachDatabaseGrbit)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.jetattachdatabase(v=EXCHG.10)
ms:contentKeyID: 55100652
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Api.JetAttachDatabase
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Api.JetAttachDatabase
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 0447d4e6c5e8474c4d82340e35a23692096305bf
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104128059"
---
# <a name="apijetattachdatabase-method"></a><span data-ttu-id="40068-103">API. JetAttachDatabase, metodo</span><span class="sxs-lookup"><span data-stu-id="40068-103">Api.JetAttachDatabase method</span></span>

<span data-ttu-id="40068-104">Associa un file di database per l'utilizzo con un'istanza di database.</span><span class="sxs-lookup"><span data-stu-id="40068-104">Attaches a database file for use with a database instance.</span></span> <span data-ttu-id="40068-105">Per utilizzare il database, sarà necessario aprirlo successivamente con [JetOpenDatabase (JET_SESID, String, String, JET_DBID, OpenDatabaseGrbit)](./api.jetopendatabase-method.md).</span><span class="sxs-lookup"><span data-stu-id="40068-105">In order to use the database, it will need to be subsequently opened with [JetOpenDatabase(JET_SESID, String, String, JET_DBID, OpenDatabaseGrbit)](./api.jetopendatabase-method.md).</span></span>

<span data-ttu-id="40068-106">**Spazio dei nomi:**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="40068-106">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="40068-107">**Assembly:**  Microsoft. ISAM. esent. Interop (in Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="40068-107">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="40068-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="40068-108">Syntax</span></span>

``` vb
'Declaration
Public Shared Function JetAttachDatabase ( _
    sesid As JET_SESID, _
    database As String, _
    grbit As AttachDatabaseGrbit _
) As JET_wrn
'Usage
Dim sesid As JET_SESID
Dim database As String
Dim grbit As AttachDatabaseGrbit
Dim returnValue As JET_wrn

returnValue = Api.JetAttachDatabase(sesid, _
    database, grbit)
```

``` csharp
public static JET_wrn JetAttachDatabase(
    JET_SESID sesid,
    string database,
    AttachDatabaseGrbit grbit
)
```

#### <a name="parameters"></a><span data-ttu-id="40068-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="40068-109">Parameters</span></span>

  - <span data-ttu-id="40068-110">sesid</span><span class="sxs-lookup"><span data-stu-id="40068-110">sesid</span></span>  
    <span data-ttu-id="40068-111">Tipo: [Microsoft.ISAM.esent.Interop.JET_SESID](./jet-sesid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="40068-111">Type: [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)</span></span>  
    
    <span data-ttu-id="40068-112">Sessione da utilizzare.</span><span class="sxs-lookup"><span data-stu-id="40068-112">The session to use.</span></span>

<!-- end list -->

  - <span data-ttu-id="40068-113">database</span><span class="sxs-lookup"><span data-stu-id="40068-113">database</span></span>  
    <span data-ttu-id="40068-114">Tipo: [System. String](/dotnet/api/system.string)</span><span class="sxs-lookup"><span data-stu-id="40068-114">Type: [System.String](/dotnet/api/system.string)</span></span>  
    
    <span data-ttu-id="40068-115">Database da aggiungere.</span><span class="sxs-lookup"><span data-stu-id="40068-115">The database to attach.</span></span>

<!-- end list -->

  - <span data-ttu-id="40068-116">grbit</span><span class="sxs-lookup"><span data-stu-id="40068-116">grbit</span></span>  
    <span data-ttu-id="40068-117">Tipo: [Microsoft. ISAM. esent. Interop. AttachDatabaseGrbit](./attachdatabasegrbit-enumeration.md)</span><span class="sxs-lookup"><span data-stu-id="40068-117">Type: [Microsoft.Isam.Esent.Interop.AttachDatabaseGrbit](./attachdatabasegrbit-enumeration.md)</span></span>  
    
    <span data-ttu-id="40068-118">Opzioni di connessione.</span><span class="sxs-lookup"><span data-stu-id="40068-118">Attach options.</span></span>

#### <a name="return-value"></a><span data-ttu-id="40068-119">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="40068-119">Return value</span></span>

<span data-ttu-id="40068-120">Tipo: [Microsoft.ISAM.esent.Interop.JET_wrn](./jet-wrn-enumeration.md)</span><span class="sxs-lookup"><span data-stu-id="40068-120">Type: [Microsoft.Isam.Esent.Interop.JET_wrn](./jet-wrn-enumeration.md)</span></span>  
<span data-ttu-id="40068-121">Codice di avviso ESENT.</span><span class="sxs-lookup"><span data-stu-id="40068-121">An ESENT warning code.</span></span>  

## <a name="see-also"></a><span data-ttu-id="40068-122">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="40068-122">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="40068-123">Riferimento</span><span class="sxs-lookup"><span data-stu-id="40068-123">Reference</span></span>

[<span data-ttu-id="40068-124">Classe API</span><span class="sxs-lookup"><span data-stu-id="40068-124">Api class</span></span>](./api-class.md)

[<span data-ttu-id="40068-125">Membri API</span><span class="sxs-lookup"><span data-stu-id="40068-125">Api members</span></span>](./api-members.md)

[<span data-ttu-id="40068-126">Spazio dei nomi Microsoft. ISAM. esent. Interop</span><span class="sxs-lookup"><span data-stu-id="40068-126">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
