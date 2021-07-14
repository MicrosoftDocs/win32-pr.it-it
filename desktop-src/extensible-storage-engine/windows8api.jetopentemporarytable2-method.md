---
description: 'Altre informazioni su: Metodo Windows8Api.JetOpenTemporaryTable2'
title: Metodo Windows8Api.JetOpenTemporaryTable2 (Microsoft.Isam.Esent.Interop.Windows8)
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
- DllExport
api_location:
- Microsoft.Isam.Esent.Interop.dll
- esent.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: eb01792608ec542918f4bd8ff6ec06ef27091bb1
ms.sourcegitcommit: 63c93e0ad0b48d60b11008767196718feb475cb0
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 07/13/2021
ms.locfileid: "113691730"
---
# <a name="windows8apijetopentemporarytable2-method"></a><span data-ttu-id="f8e34-103">Metodo Windows8Api.JetOpenTemporaryTable2</span><span class="sxs-lookup"><span data-stu-id="f8e34-103">Windows8Api.JetOpenTemporaryTable2 method</span></span>

<span data-ttu-id="f8e34-104">Crea una tabella temporanea con un singolo indice.</span><span class="sxs-lookup"><span data-stu-id="f8e34-104">Creates a temporary table with a single index.</span></span> <span data-ttu-id="f8e34-105">Una tabella temporanea archivia e recupera i record esattamente come una normale tabella creata usando JetCreateTableColumnIndex.</span><span class="sxs-lookup"><span data-stu-id="f8e34-105">A temporary table stores and retrieves records just like an ordinary table created using JetCreateTableColumnIndex.</span></span> <span data-ttu-id="f8e34-106">Tuttavia, le tabelle temporanee sono molto più veloci delle tabelle normali a causa della loro natura volatile.</span><span class="sxs-lookup"><span data-stu-id="f8e34-106">However, temporary tables are much faster than ordinary tables due to their volatile nature.</span></span> <span data-ttu-id="f8e34-107">Possono anche essere usati per ordinare ed eseguire molto rapidamente la rimozione dei duplicati nei set di record quando vi si accede in modo puramente sequenziale.</span><span class="sxs-lookup"><span data-stu-id="f8e34-107">They can also be used to very quickly sort and perform duplicate removal on record sets when accessed in a purely sequential manner.</span></span> <span data-ttu-id="f8e34-108">Vedere anche [JetOpenTempTable(JET_SESID, \[ \] , Int32, TempTableGrbit, JET_TABLEID, \[ \] )](./api.jetopentemptable-method.md), "Api.JetOpenTempTable2", [JetOpenTempTable3(JET_SESID, \[ \] , Int32, JET_UNICODEINDEX, TempTableGrbit, JET_TABLEID, \[ \] )](./api.jetopentemptable3-method.md).</span><span class="sxs-lookup"><span data-stu-id="f8e34-108">Also see [JetOpenTempTable(JET_SESID, \[\], Int32, TempTableGrbit, JET_TABLEID, \[\])](./api.jetopentemptable-method.md), "Api.JetOpenTempTable2", [JetOpenTempTable3(JET_SESID, \[\], Int32, JET_UNICODEINDEX, TempTableGrbit, JET_TABLEID, \[\])](./api.jetopentemptable3-method.md).</span></span> <span data-ttu-id="f8e34-109">[JetOpenTemporaryTable(JET_SESID, JET_OPENTEMPORARYTABLE)](./vistaapi.jetopentemporarytable-method.md).</span><span class="sxs-lookup"><span data-stu-id="f8e34-109">[JetOpenTemporaryTable(JET_SESID, JET_OPENTEMPORARYTABLE)](./vistaapi.jetopentemporarytable-method.md).</span></span>

<span data-ttu-id="f8e34-110">**Spazio dei**  [nomi: Microsoft.Isam.Esent.Interop.Windows8](./microsoft.isam.esent.interop.windows8-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="f8e34-110">**Namespace:**  [Microsoft.Isam.Esent.Interop.Windows8](./microsoft.isam.esent.interop.windows8-namespace.md)</span></span>  
<span data-ttu-id="f8e34-111">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="f8e34-111">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="f8e34-112">Sintassi</span><span class="sxs-lookup"><span data-stu-id="f8e34-112">Syntax</span></span>

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

#### <a name="parameters"></a><span data-ttu-id="f8e34-113">Parametri</span><span class="sxs-lookup"><span data-stu-id="f8e34-113">Parameters</span></span>

  - <span data-ttu-id="f8e34-114">sesid</span><span class="sxs-lookup"><span data-stu-id="f8e34-114">sesid</span></span>  
    <span data-ttu-id="f8e34-115">Tipo: [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="f8e34-115">Type: [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)</span></span>  
    
    <span data-ttu-id="f8e34-116">Sessione da utilizzare.</span><span class="sxs-lookup"><span data-stu-id="f8e34-116">The session to use.</span></span>

<!-- end list -->

  - <span data-ttu-id="f8e34-117">tabella temporanea</span><span class="sxs-lookup"><span data-stu-id="f8e34-117">temporarytable</span></span>  
    <span data-ttu-id="f8e34-118">Tipo: [Microsoft.Isam.Esent.Interop.Vista.JET_OPENTEMPORARYTABLE](./jet-opentemporarytable-class.md)</span><span class="sxs-lookup"><span data-stu-id="f8e34-118">Type: [Microsoft.Isam.Esent.Interop.Vista.JET_OPENTEMPORARYTABLE](./jet-opentemporarytable-class.md)</span></span>  
    
    <span data-ttu-id="f8e34-119">Descrizione della tabella temporanea da creare in base all'input.</span><span class="sxs-lookup"><span data-stu-id="f8e34-119">Description of the temporary table to create on input.</span></span> <span data-ttu-id="f8e34-120">Dopo una chiamata riuscita, la struttura contiene l'handle per le identificazioni di tabella e colonna temporanee.</span><span class="sxs-lookup"><span data-stu-id="f8e34-120">After a successful call, the structure contains the handle to the temporary table and column identifications.</span></span> <span data-ttu-id="f8e34-121">Usare [JetCloseTable(JET_SESID, JET_TABLEID)](./api.jetclosetable-method.md) per liberare la tabella temporanea al termine.</span><span class="sxs-lookup"><span data-stu-id="f8e34-121">Use [JetCloseTable(JET_SESID, JET_TABLEID)](./api.jetclosetable-method.md) to free the temporary table when finished.</span></span>

## <a name="remarks"></a><span data-ttu-id="f8e34-122">Commenti</span><span class="sxs-lookup"><span data-stu-id="f8e34-122">Remarks</span></span>

<span data-ttu-id="f8e34-123">Usare [JetOpenTemporaryTable(JET_SESID, JET_OPENTEMPORARYTABLE)](./vistaapi.jetopentemporarytable-method.md) per le versioni precedenti di Esent.</span><span class="sxs-lookup"><span data-stu-id="f8e34-123">Use [JetOpenTemporaryTable(JET_SESID, JET_OPENTEMPORARYTABLE)](./vistaapi.jetopentemporarytable-method.md) for earlier versions of Esent.</span></span>

## <a name="see-also"></a><span data-ttu-id="f8e34-124">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="f8e34-124">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="f8e34-125">Riferimento</span><span class="sxs-lookup"><span data-stu-id="f8e34-125">Reference</span></span>

[<span data-ttu-id="f8e34-126">Classe Windows8Api</span><span class="sxs-lookup"><span data-stu-id="f8e34-126">Windows8Api class</span></span>](./windows8api-class.md)

[<span data-ttu-id="f8e34-127">Membri windows8Api</span><span class="sxs-lookup"><span data-stu-id="f8e34-127">Windows8Api members</span></span>](./windows8api-members.md)

[<span data-ttu-id="f8e34-128">Spazio dei nomi Microsoft.Isam.Esent.Interop.Windows8</span><span class="sxs-lookup"><span data-stu-id="f8e34-128">Microsoft.Isam.Esent.Interop.Windows8 namespace</span></span>](./microsoft.isam.esent.interop.windows8-namespace.md)
