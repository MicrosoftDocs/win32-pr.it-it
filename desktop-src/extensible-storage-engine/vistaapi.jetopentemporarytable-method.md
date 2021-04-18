---
description: 'Altre informazioni su: VistaApi. JetOpenTemporaryTable, metodo'
title: Metodo VistaApi. JetOpenTemporaryTable (Microsoft. ISAM. esent. Interop. vista)
TOCTitle: 'JetOpenTemporaryTable method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Vista.VistaApi.JetOpenTemporaryTable(Microsoft.Isam.Esent.Interop.JET_SESID,Microsoft.Isam.Esent.Interop.Vista.JET_OPENTEMPORARYTABLE)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.vista.vistaapi.jetopentemporarytable(v=EXCHG.10)
ms:contentKeyID: 55104291
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Vista.VistaApi.JetOpenTemporaryTable
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Vista.VistaApi.JetOpenTemporaryTable
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 0a261494cf8b12039371c445a4cf2124f3ec1c52
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106309651"
---
# <a name="vistaapijetopentemporarytable-method"></a><span data-ttu-id="9f9b4-103">VistaApi. JetOpenTemporaryTable, metodo</span><span class="sxs-lookup"><span data-stu-id="9f9b4-103">VistaApi.JetOpenTemporaryTable method</span></span>

<span data-ttu-id="9f9b4-104">Crea una tabella temporanea con un solo indice.</span><span class="sxs-lookup"><span data-stu-id="9f9b4-104">Creates a temporary table with a single index.</span></span> <span data-ttu-id="9f9b4-105">Una tabella temporanea archivia e recupera i record esattamente come una tabella ordinaria creata con JetCreateTableColumnIndex.</span><span class="sxs-lookup"><span data-stu-id="9f9b4-105">A temporary table stores and retrieves records just like an ordinary table created using JetCreateTableColumnIndex.</span></span> <span data-ttu-id="9f9b4-106">Tuttavia, le tabelle temporanee sono molto più veloci delle tabelle ordinarie a causa della loro natura volatile.</span><span class="sxs-lookup"><span data-stu-id="9f9b4-106">However, temporary tables are much faster than ordinary tables due to their volatile nature.</span></span> <span data-ttu-id="9f9b4-107">Possono anche essere usati per ordinare ed eseguire molto rapidamente la rimozione dei duplicati nei set di record quando si accede in modo puramente sequenziale.</span><span class="sxs-lookup"><span data-stu-id="9f9b4-107">They can also be used to very quickly sort and perform duplicate removal on record sets when accessed in a purely sequential manner.</span></span> <span data-ttu-id="9f9b4-108">Vedere anche [JetOpenTempTable (JET_SESID, \[ \] , Int32, TempTableGrbit, JET_TABLEID, \[ \] )](./api.jetopentemptable-method.md), [JetOpenTempTable3 (JET_SESID, \[ \] , Int32, JET_UNICODEINDEX, TempTableGrbit, JET_TABLEID, \[ \] )](./api.jetopentemptable3-method.md).</span><span class="sxs-lookup"><span data-stu-id="9f9b4-108">Also see [JetOpenTempTable(JET_SESID, \[\], Int32, TempTableGrbit, JET_TABLEID, \[\])](./api.jetopentemptable-method.md), [JetOpenTempTable3(JET_SESID, \[\], Int32, JET_UNICODEINDEX, TempTableGrbit, JET_TABLEID, \[\])](./api.jetopentemptable3-method.md).</span></span>

<span data-ttu-id="9f9b4-109">**Spazio dei nomi:**  [Microsoft. ISAM. esent. Interop. vista](./microsoft.isam.esent.interop.vista-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="9f9b4-109">**Namespace:**  [Microsoft.Isam.Esent.Interop.Vista](./microsoft.isam.esent.interop.vista-namespace.md)</span></span>  
<span data-ttu-id="9f9b4-110">**Assembly:**  Microsoft. ISAM. esent. Interop (in Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="9f9b4-110">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="9f9b4-111">Sintassi</span><span class="sxs-lookup"><span data-stu-id="9f9b4-111">Syntax</span></span>

``` vb
'Declaration
Public Shared Sub JetOpenTemporaryTable ( _
    sesid As JET_SESID, _
    temporarytable As JET_OPENTEMPORARYTABLE _
)
'Usage
Dim sesid As JET_SESID
Dim temporarytable As JET_OPENTEMPORARYTABLEVistaApi.JetOpenTemporaryTable(sesid, _
    temporarytable)
```

``` csharp
public static void JetOpenTemporaryTable(
    JET_SESID sesid,
    JET_OPENTEMPORARYTABLE temporarytable
)
```

#### <a name="parameters"></a><span data-ttu-id="9f9b4-112">Parametri</span><span class="sxs-lookup"><span data-stu-id="9f9b4-112">Parameters</span></span>

  - <span data-ttu-id="9f9b4-113">sesid</span><span class="sxs-lookup"><span data-stu-id="9f9b4-113">sesid</span></span>  
    <span data-ttu-id="9f9b4-114">Tipo: [Microsoft.ISAM.esent.Interop.JET_SESID](./jet-sesid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="9f9b4-114">Type: [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)</span></span>  
    
    <span data-ttu-id="9f9b4-115">Sessione da utilizzare.</span><span class="sxs-lookup"><span data-stu-id="9f9b4-115">The session to use.</span></span>

<!-- end list -->

  - <span data-ttu-id="9f9b4-116">temporarytable</span><span class="sxs-lookup"><span data-stu-id="9f9b4-116">temporarytable</span></span>  
    <span data-ttu-id="9f9b4-117">Tipo: [Microsoft.ISAM.esent.Interop.vista.JET_OPENTEMPORARYTABLE](./jet-opentemporarytable-class.md)</span><span class="sxs-lookup"><span data-stu-id="9f9b4-117">Type: [Microsoft.Isam.Esent.Interop.Vista.JET_OPENTEMPORARYTABLE](./jet-opentemporarytable-class.md)</span></span>  
    
    <span data-ttu-id="9f9b4-118">Descrizione della tabella temporanea da creare in input.</span><span class="sxs-lookup"><span data-stu-id="9f9b4-118">Description of the temporary table to create on input.</span></span> <span data-ttu-id="9f9b4-119">Dopo una chiamata con esito positivo, la struttura contiene l'handle per gli identificatori di tabella e colonna temporanei.</span><span class="sxs-lookup"><span data-stu-id="9f9b4-119">After a successful call, the structure contains the handle to the temporary table and column identifications.</span></span> <span data-ttu-id="9f9b4-120">Al termine [, usare JetCloseTable (JET_SESID, JET_TABLEID)](./api.jetclosetable-method.md) per liberare la tabella temporanea.</span><span class="sxs-lookup"><span data-stu-id="9f9b4-120">Use [JetCloseTable(JET_SESID, JET_TABLEID)](./api.jetclosetable-method.md) to free the temporary table when finished.</span></span>

## <a name="remarks"></a><span data-ttu-id="9f9b4-121">Commenti</span><span class="sxs-lookup"><span data-stu-id="9f9b4-121">Remarks</span></span>

<span data-ttu-id="9f9b4-122">Introdotta in Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="9f9b4-122">Introduced in Windows Vista.</span></span> <span data-ttu-id="9f9b4-123">Usare [JetOpenTempTable3 (JET_SESID, \[ \] , Int32, JET_UNICODEINDEX, TempTableGrbit, JET_TABLEID, \[ \] )](./api.jetopentemptable3-method.md) per le versioni precedenti di esent.</span><span class="sxs-lookup"><span data-stu-id="9f9b4-123">Use [JetOpenTempTable3(JET_SESID, \[\], Int32, JET_UNICODEINDEX, TempTableGrbit, JET_TABLEID, \[\])](./api.jetopentemptable3-method.md) for earlier versions of Esent.</span></span>

## <a name="see-also"></a><span data-ttu-id="9f9b4-124">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="9f9b4-124">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="9f9b4-125">Riferimento</span><span class="sxs-lookup"><span data-stu-id="9f9b4-125">Reference</span></span>

[<span data-ttu-id="9f9b4-126">Classe VistaApi</span><span class="sxs-lookup"><span data-stu-id="9f9b4-126">VistaApi class</span></span>](./vistaapi-class.md)

[<span data-ttu-id="9f9b4-127">Membri di VistaApi</span><span class="sxs-lookup"><span data-stu-id="9f9b4-127">VistaApi members</span></span>](./vistaapi-members.md)

[<span data-ttu-id="9f9b4-128">Spazio dei nomi Microsoft. ISAM. esent. Interop. vista</span><span class="sxs-lookup"><span data-stu-id="9f9b4-128">Microsoft.Isam.Esent.Interop.Vista namespace</span></span>](./microsoft.isam.esent.interop.vista-namespace.md)
