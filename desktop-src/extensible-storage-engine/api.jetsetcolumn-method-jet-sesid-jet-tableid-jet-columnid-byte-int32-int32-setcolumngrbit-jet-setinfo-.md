---
description: 'Altre informazioni su: metodo API. JetSetColumn (JET_SESID, JET_TABLEID, JET_COLUMNID, byte, Int32, Int32, SetColumnGrbit, JET_SETINFO)'
title: Metodo API. JetSetColumn (JET_SESID, JET_TABLEID, JET_COLUMNID, byte, Int32, Int32, SetColumnGrbit, JET_SETINFO)
TOCTitle: JetSetColumn method (JET_SESID, JET_TABLEID, JET_COLUMNID, Byte , Int32, Int32, SetColumnGrbit, JET_SETINFO)
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.JetSetColumn(Microsoft.Isam.Esent.Interop.JET_SESID,Microsoft.Isam.Esent.Interop.JET_TABLEID,Microsoft.Isam.Esent.Interop.JET_COLUMNID,System.Byte[],System.Int32,System.Int32,Microsoft.Isam.Esent.Interop.SetColumnGrbit,Microsoft.Isam.Esent.Interop.JET_SETINFO)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.jetsetcolumn(v=EXCHG.10)
ms:contentKeyID: 55100801
ms.date: 07/30/2014
ms.topic: reference
dev_langs:
- vb
- csharp
api_name:
- Microsoft.Isam.Esent.Interop.Api.JetSetColumn
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 8f52c900521d28c82245db53b98ab376dd82faec
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106306268"
---
# <a name="apijetsetcolumn-method-jet_sesid-jet_tableid-jet_columnid-byte--int32-int32-setcolumngrbit-jet_setinfo"></a><span data-ttu-id="54d34-103">Metodo API. JetSetColumn (JET_SESID, JET_TABLEID, JET_COLUMNID, byte, Int32, Int32, SetColumnGrbit, JET_SETINFO)</span><span class="sxs-lookup"><span data-stu-id="54d34-103">Api.JetSetColumn method (JET_SESID, JET_TABLEID, JET_COLUMNID, Byte , Int32, Int32, SetColumnGrbit, JET_SETINFO)</span></span>

<span data-ttu-id="54d34-104">La funzione JetSetColumn modifica un valore di colonna singolo in un record modificato da inserire o per aggiornare il record corrente.</span><span class="sxs-lookup"><span data-stu-id="54d34-104">The JetSetColumn function modifies a single column value in a modified record to be inserted or to update the current record.</span></span> <span data-ttu-id="54d34-105">Può sovrascrivere un valore esistente, aggiungere un nuovo valore a una sequenza di valori in una colonna multivalore, rimuovere un valore da una sequenza di valori in una colonna multivalore o aggiornare tutto o parte di un valore Long, ovvero una colonna di tipo [LONGTEXT](./jet-coltyp-enumeration.md) o [LongBinary](./jet-coltyp-enumeration.md).</span><span class="sxs-lookup"><span data-stu-id="54d34-105">It can overwrite an existing value, add a new value to a sequence of values in a multi-valued column, remove a value from a sequence of values in a multi-valued column, or update all or part of a long value (a column of type [LongText](./jet-coltyp-enumeration.md) or [LongBinary](./jet-coltyp-enumeration.md)).</span></span>

<span data-ttu-id="54d34-106">**Spazio dei nomi:**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="54d34-106">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="54d34-107">**Assembly:**  Microsoft. ISAM. esent. Interop (in Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="54d34-107">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="54d34-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="54d34-108">Syntax</span></span>

``` vb
'Declaration
Public Shared Function JetSetColumn ( _
    sesid As JET_SESID, _
    tableid As JET_TABLEID, _
    columnid As JET_COLUMNID, _
    data As Byte(), _
    dataSize As Integer, _
    dataOffset As Integer, _
    grbit As SetColumnGrbit, _
    setinfo As JET_SETINFO _
) As JET_wrn
'Usage
Dim sesid As JET_SESID
Dim tableid As JET_TABLEID
Dim columnid As JET_COLUMNID
Dim data As Byte()
Dim dataSize As Integer
Dim dataOffset As Integer
Dim grbit As SetColumnGrbit
Dim setinfo As JET_SETINFO
Dim returnValue As JET_wrn

returnValue = Api.JetSetColumn(sesid, _
    tableid, columnid, data, dataSize, _
    dataOffset, grbit, setinfo)
```

``` csharp
public static JET_wrn JetSetColumn(
    JET_SESID sesid,
    JET_TABLEID tableid,
    JET_COLUMNID columnid,
    byte[] data,
    int dataSize,
    int dataOffset,
    SetColumnGrbit grbit,
    JET_SETINFO setinfo
)
```

#### <a name="parameters"></a><span data-ttu-id="54d34-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="54d34-109">Parameters</span></span>

  - <span data-ttu-id="54d34-110">sesid</span><span class="sxs-lookup"><span data-stu-id="54d34-110">sesid</span></span>  
    <span data-ttu-id="54d34-111">Tipo: [Microsoft.ISAM.esent.Interop.JET_SESID](./jet-sesid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="54d34-111">Type: [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)</span></span>  
    
    <span data-ttu-id="54d34-112">Sessione che esegue l'aggiornamento.</span><span class="sxs-lookup"><span data-stu-id="54d34-112">The session which is performing the update.</span></span>

<!-- end list -->

  - <span data-ttu-id="54d34-113">TableID</span><span class="sxs-lookup"><span data-stu-id="54d34-113">tableid</span></span>  
    <span data-ttu-id="54d34-114">Tipo: [Microsoft.ISAM.esent.Interop.JET_TABLEID](./jet-tableid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="54d34-114">Type: [Microsoft.Isam.Esent.Interop.JET_TABLEID](./jet-tableid-structure.md)</span></span>  
    
    <span data-ttu-id="54d34-115">Cursore da aggiornare.</span><span class="sxs-lookup"><span data-stu-id="54d34-115">The cursor to update.</span></span> <span data-ttu-id="54d34-116">È necessario preparare un aggiornamento.</span><span class="sxs-lookup"><span data-stu-id="54d34-116">An update should be prepared.</span></span>

<!-- end list -->

  - <span data-ttu-id="54d34-117">columnid</span><span class="sxs-lookup"><span data-stu-id="54d34-117">columnid</span></span>  
    <span data-ttu-id="54d34-118">Tipo: [Microsoft.ISAM.esent.Interop.JET_COLUMNID](./jet-columnid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="54d34-118">Type: [Microsoft.Isam.Esent.Interop.JET_COLUMNID](./jet-columnid-structure.md)</span></span>  
    
    <span data-ttu-id="54d34-119">ColumnID da impostare.</span><span class="sxs-lookup"><span data-stu-id="54d34-119">The columnid to set.</span></span>

<!-- end list -->

  - <span data-ttu-id="54d34-120">data</span><span class="sxs-lookup"><span data-stu-id="54d34-120">data</span></span>  
    <span data-ttu-id="54d34-121">Tipo \[\]</span><span class="sxs-lookup"><span data-stu-id="54d34-121">Type: \[\]</span></span>  
    
    <span data-ttu-id="54d34-122">Dati da impostare.</span><span class="sxs-lookup"><span data-stu-id="54d34-122">The data to set.</span></span>

<!-- end list -->

  - <span data-ttu-id="54d34-123">dataSize</span><span class="sxs-lookup"><span data-stu-id="54d34-123">dataSize</span></span>  
    <span data-ttu-id="54d34-124">Tipo: [System. Int32](/dotnet/api/system.int32)</span><span class="sxs-lookup"><span data-stu-id="54d34-124">Type: [System.Int32](/dotnet/api/system.int32)</span></span>  
    
    <span data-ttu-id="54d34-125">Dimensione dei dati da impostare.</span><span class="sxs-lookup"><span data-stu-id="54d34-125">The size of data to set.</span></span>

<!-- end list -->

  - <span data-ttu-id="54d34-126">dataOffset</span><span class="sxs-lookup"><span data-stu-id="54d34-126">dataOffset</span></span>  
    <span data-ttu-id="54d34-127">Tipo: [System. Int32](/dotnet/api/system.int32)</span><span class="sxs-lookup"><span data-stu-id="54d34-127">Type: [System.Int32](/dotnet/api/system.int32)</span></span>  
    
    <span data-ttu-id="54d34-128">Offset nel buffer di dati da cui impostare i dati.</span><span class="sxs-lookup"><span data-stu-id="54d34-128">The offset in the data buffer to set data from.</span></span>

<!-- end list -->

  - <span data-ttu-id="54d34-129">grbit</span><span class="sxs-lookup"><span data-stu-id="54d34-129">grbit</span></span>  
    <span data-ttu-id="54d34-130">Tipo: [Microsoft. ISAM. esent. Interop. SetColumnGrbit](./setcolumngrbit-enumeration.md)</span><span class="sxs-lookup"><span data-stu-id="54d34-130">Type: [Microsoft.Isam.Esent.Interop.SetColumnGrbit](./setcolumngrbit-enumeration.md)</span></span>  
    
    <span data-ttu-id="54d34-131">Opzioni di colonna.</span><span class="sxs-lookup"><span data-stu-id="54d34-131">SetColumn options.</span></span>

<!-- end list -->

  - <span data-ttu-id="54d34-132">SetInfo</span><span class="sxs-lookup"><span data-stu-id="54d34-132">setinfo</span></span>  
    <span data-ttu-id="54d34-133">Tipo: [Microsoft.ISAM.esent.Interop.JET_SETINFO](./jet-setinfo-class.md)</span><span class="sxs-lookup"><span data-stu-id="54d34-133">Type: [Microsoft.Isam.Esent.Interop.JET_SETINFO](./jet-setinfo-class.md)</span></span>  
    
    <span data-ttu-id="54d34-134">Utilizzato per specificare l'offset ITag o long-value.</span><span class="sxs-lookup"><span data-stu-id="54d34-134">Used to specify itag or long-value offset.</span></span>

#### <a name="return-value"></a><span data-ttu-id="54d34-135">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="54d34-135">Return value</span></span>

<span data-ttu-id="54d34-136">Tipo: [Microsoft.ISAM.esent.Interop.JET_wrn](./jet-wrn-enumeration.md)</span><span class="sxs-lookup"><span data-stu-id="54d34-136">Type: [Microsoft.Isam.Esent.Interop.JET_wrn](./jet-wrn-enumeration.md)</span></span>  
<span data-ttu-id="54d34-137">Valore di avviso.</span><span class="sxs-lookup"><span data-stu-id="54d34-137">A warning value.</span></span>  

## <a name="remarks"></a><span data-ttu-id="54d34-138">Commenti</span><span class="sxs-lookup"><span data-stu-id="54d34-138">Remarks</span></span>

<span data-ttu-id="54d34-139">Si tratta di una versione solo interna dell'API che accetta un buffer di dati e un offset nel buffer.</span><span class="sxs-lookup"><span data-stu-id="54d34-139">This is an internal-only version of the API that takes a data buffer and an offset into the buffer.</span></span>

## <a name="see-also"></a><span data-ttu-id="54d34-140">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="54d34-140">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="54d34-141">Riferimento</span><span class="sxs-lookup"><span data-stu-id="54d34-141">Reference</span></span>

[<span data-ttu-id="54d34-142">Classe API</span><span class="sxs-lookup"><span data-stu-id="54d34-142">Api class</span></span>](./api-class.md)

[<span data-ttu-id="54d34-143">Membri API</span><span class="sxs-lookup"><span data-stu-id="54d34-143">Api members</span></span>](./api-members.md)

[<span data-ttu-id="54d34-144">Overload JetSetColumn</span><span class="sxs-lookup"><span data-stu-id="54d34-144">JetSetColumn overload</span></span>](./api.jetsetcolumn-method.md)

[<span data-ttu-id="54d34-145">Spazio dei nomi Microsoft. ISAM. esent. Interop</span><span class="sxs-lookup"><span data-stu-id="54d34-145">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
