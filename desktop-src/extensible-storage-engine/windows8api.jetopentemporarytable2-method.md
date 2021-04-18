---
description: 'Altre informazioni su: Windows8Api. JetOpenTemporaryTable2, metodo'
title: Metodo Windows8Api. JetOpenTemporaryTable2 (Microsoft. ISAM. esent. Interop. Windows8)
TOCTitle: 'JetOpenTemporaryTable2 method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Windows8.Windows8Api.JetOpenTemporaryTable2(Microsoft.Isam.Esent.Interop.JET_SESID,Microsoft.Isam.Esent.Interop.Vista.JET_OPENTEMPORARYTABLE)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.windows8.windows8api.jetopentemporarytable2(v=EXCHG.10)
ms:contentKeyID: 55107829
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Windows8.Windows8Api.JetOpenTemporaryTable2
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Windows8.Windows8Api.JetOpenTemporaryTable2
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 5ebb96af18e655c9f9304e2fe7a339663c0206fc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106308799"
---
# <a name="windows8apijetopentemporarytable2-method"></a><span data-ttu-id="c343e-103">Windows8Api. JetOpenTemporaryTable2, metodo</span><span class="sxs-lookup"><span data-stu-id="c343e-103">Windows8Api.JetOpenTemporaryTable2 method</span></span>

<span data-ttu-id="c343e-104">Crea una tabella temporanea con un solo indice.</span><span class="sxs-lookup"><span data-stu-id="c343e-104">Creates a temporary table with a single index.</span></span> <span data-ttu-id="c343e-105">Una tabella temporanea archivia e recupera i record esattamente come una tabella ordinaria creata con JetCreateTableColumnIndex.</span><span class="sxs-lookup"><span data-stu-id="c343e-105">A temporary table stores and retrieves records just like an ordinary table created using JetCreateTableColumnIndex.</span></span> <span data-ttu-id="c343e-106">Tuttavia, le tabelle temporanee sono molto più veloci delle tabelle ordinarie a causa della loro natura volatile.</span><span class="sxs-lookup"><span data-stu-id="c343e-106">However, temporary tables are much faster than ordinary tables due to their volatile nature.</span></span> <span data-ttu-id="c343e-107">Possono anche essere usati per ordinare ed eseguire molto rapidamente la rimozione dei duplicati nei set di record quando si accede in modo puramente sequenziale.</span><span class="sxs-lookup"><span data-stu-id="c343e-107">They can also be used to very quickly sort and perform duplicate removal on record sets when accessed in a purely sequential manner.</span></span> <span data-ttu-id="c343e-108">Vedere anche [JetOpenTempTable (JET_SESID, \[ \] , Int32, TempTableGrbit, JET_TABLEID, \[ \] )](./api.jetopentemptable-method.md), "API. JetOpenTempTable2", [JetOpenTempTable3 (JET_SESID, \[ \] , Int32, JET_UNICODEINDEX, TempTableGrbit, JET_TABLEID, \[ \] )](./api.jetopentemptable3-method.md).</span><span class="sxs-lookup"><span data-stu-id="c343e-108">Also see [JetOpenTempTable(JET_SESID, \[\], Int32, TempTableGrbit, JET_TABLEID, \[\])](./api.jetopentemptable-method.md), "Api.JetOpenTempTable2", [JetOpenTempTable3(JET_SESID, \[\], Int32, JET_UNICODEINDEX, TempTableGrbit, JET_TABLEID, \[\])](./api.jetopentemptable3-method.md).</span></span> <span data-ttu-id="c343e-109">[JetOpenTemporaryTable (JET_SESID, JET_OPENTEMPORARYTABLE)](./vistaapi.jetopentemporarytable-method.md).</span><span class="sxs-lookup"><span data-stu-id="c343e-109">[JetOpenTemporaryTable(JET_SESID, JET_OPENTEMPORARYTABLE)](./vistaapi.jetopentemporarytable-method.md).</span></span>

<span data-ttu-id="c343e-110">**Spazio dei nomi:**  [Microsoft. ISAM. esent. Interop. Windows8](./microsoft.isam.esent.interop.windows8-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="c343e-110">**Namespace:**  [Microsoft.Isam.Esent.Interop.Windows8](./microsoft.isam.esent.interop.windows8-namespace.md)</span></span>  
<span data-ttu-id="c343e-111">**Assembly:**  Microsoft. ISAM. esent. Interop (in Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="c343e-111">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="c343e-112">Sintassi</span><span class="sxs-lookup"><span data-stu-id="c343e-112">Syntax</span></span>

``` vb
'Declaration
Public Shared Sub JetOpenTemporaryTable2 ( _
    sesid As JET_SESID, _
    temporarytable As JET_OPENTEMPORARYTABLE _
)
'Usage
Dim sesid As JET_SESID
Dim temporarytable As JET_OPENTEMPORARYTABLEWindows8Api.JetOpenTemporaryTable2(sesid, _
    temporarytable)
```

``` csharp
public static void JetOpenTemporaryTable2(
    JET_SESID sesid,
    JET_OPENTEMPORARYTABLE temporarytable
)
```

#### <a name="parameters"></a><span data-ttu-id="c343e-113">Parametri</span><span class="sxs-lookup"><span data-stu-id="c343e-113">Parameters</span></span>

  - <span data-ttu-id="c343e-114">sesid</span><span class="sxs-lookup"><span data-stu-id="c343e-114">sesid</span></span>  
    <span data-ttu-id="c343e-115">Tipo: [Microsoft.ISAM.esent.Interop.JET_SESID](./jet-sesid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="c343e-115">Type: [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)</span></span>  
    
    <span data-ttu-id="c343e-116">Sessione da utilizzare.</span><span class="sxs-lookup"><span data-stu-id="c343e-116">The session to use.</span></span>

<!-- end list -->

  - <span data-ttu-id="c343e-117">temporarytable</span><span class="sxs-lookup"><span data-stu-id="c343e-117">temporarytable</span></span>  
    <span data-ttu-id="c343e-118">Tipo: [Microsoft.ISAM.esent.Interop.vista.JET_OPENTEMPORARYTABLE](./jet-opentemporarytable-class.md)</span><span class="sxs-lookup"><span data-stu-id="c343e-118">Type: [Microsoft.Isam.Esent.Interop.Vista.JET_OPENTEMPORARYTABLE](./jet-opentemporarytable-class.md)</span></span>  
    
    <span data-ttu-id="c343e-119">Descrizione della tabella temporanea da creare in input.</span><span class="sxs-lookup"><span data-stu-id="c343e-119">Description of the temporary table to create on input.</span></span> <span data-ttu-id="c343e-120">Dopo una chiamata con esito positivo, la struttura contiene l'handle per gli identificatori di tabella e colonna temporanei.</span><span class="sxs-lookup"><span data-stu-id="c343e-120">After a successful call, the structure contains the handle to the temporary table and column identifications.</span></span> <span data-ttu-id="c343e-121">Al termine [, usare JetCloseTable (JET_SESID, JET_TABLEID)](./api.jetclosetable-method.md) per liberare la tabella temporanea.</span><span class="sxs-lookup"><span data-stu-id="c343e-121">Use [JetCloseTable(JET_SESID, JET_TABLEID)](./api.jetclosetable-method.md) to free the temporary table when finished.</span></span>

## <a name="remarks"></a><span data-ttu-id="c343e-122">Commenti</span><span class="sxs-lookup"><span data-stu-id="c343e-122">Remarks</span></span>

<span data-ttu-id="c343e-123">Usare [JetOpenTemporaryTable (JET_SESID, JET_OPENTEMPORARYTABLE)](./vistaapi.jetopentemporarytable-method.md) per le versioni precedenti di esent.</span><span class="sxs-lookup"><span data-stu-id="c343e-123">Use [JetOpenTemporaryTable(JET_SESID, JET_OPENTEMPORARYTABLE)](./vistaapi.jetopentemporarytable-method.md) for earlier versions of Esent.</span></span>

## <a name="see-also"></a><span data-ttu-id="c343e-124">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="c343e-124">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="c343e-125">Riferimento</span><span class="sxs-lookup"><span data-stu-id="c343e-125">Reference</span></span>

[<span data-ttu-id="c343e-126">Classe Windows8Api</span><span class="sxs-lookup"><span data-stu-id="c343e-126">Windows8Api class</span></span>](./windows8api-class.md)

[<span data-ttu-id="c343e-127">Membri di Windows8Api</span><span class="sxs-lookup"><span data-stu-id="c343e-127">Windows8Api members</span></span>](./windows8api-members.md)

[<span data-ttu-id="c343e-128">Spazio dei nomi Microsoft. ISAM. esent. Interop. Windows8</span><span class="sxs-lookup"><span data-stu-id="c343e-128">Microsoft.Isam.Esent.Interop.Windows8 namespace</span></span>](./microsoft.isam.esent.interop.windows8-namespace.md)
