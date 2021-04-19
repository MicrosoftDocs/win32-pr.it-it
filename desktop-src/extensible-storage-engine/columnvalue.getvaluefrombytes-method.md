---
description: 'Altre informazioni su: ColumnValue. GetValueFromBytes, metodo'
title: ColumnValue. GetValueFromBytes, metodo
TOCTitle: 'GetValueFromBytes method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.ColumnValue.GetValueFromBytes(System.Byte[],System.Int32,System.Int32,System.Int32)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.columnvalue.getvaluefrombytes(v=EXCHG.10)
ms:contentKeyID: 55101191
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.ColumnValue.GetValueFromBytes
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.ColumnValue.GetValueFromBytes
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 448c0626c0e4cf91b266a6894a021789d52955b3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106319272"
---
# <a name="columnvaluegetvaluefrombytes-method"></a><span data-ttu-id="13ae6-103">ColumnValue. GetValueFromBytes, metodo</span><span class="sxs-lookup"><span data-stu-id="13ae6-103">ColumnValue.GetValueFromBytes method</span></span>

<span data-ttu-id="13ae6-104">Dato che i dati sono stati recuperati da ESENT, decodificano i dati e impostano il valore nell'oggetto ColumnValue.</span><span class="sxs-lookup"><span data-stu-id="13ae6-104">Given data retrieved from ESENT, decode the data and set the value in the ColumnValue object.</span></span>

<span data-ttu-id="13ae6-105">**Spazio dei nomi:**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="13ae6-105">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="13ae6-106">**Assembly:**  Microsoft. ISAM. esent. Interop (in Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="13ae6-106">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="13ae6-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="13ae6-107">Syntax</span></span>

``` vb
'Declaration
Protected MustOverride Sub GetValueFromBytes ( _
    value As Byte(), _
    startIndex As Integer, _
    count As Integer, _
    err As Integer _
)
'Usage
Dim value As Byte()
Dim startIndex As Integer
Dim count As Integer
Dim err As Integer

Me.GetValueFromBytes(value, startIndex, _
    count, err)
```

``` csharp
protected abstract void GetValueFromBytes(
    byte[] value,
    int startIndex,
    int count,
    int err
)
```

#### <a name="parameters"></a><span data-ttu-id="13ae6-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="13ae6-108">Parameters</span></span>

  - <span data-ttu-id="13ae6-109">Valore</span><span class="sxs-lookup"><span data-stu-id="13ae6-109">value</span></span>  
    <span data-ttu-id="13ae6-110">Tipo \[\]</span><span class="sxs-lookup"><span data-stu-id="13ae6-110">Type: \[\]</span></span>  
    
    <span data-ttu-id="13ae6-111">Matrice di byte.</span><span class="sxs-lookup"><span data-stu-id="13ae6-111">An array of bytes.</span></span>

<!-- end list -->

  - <span data-ttu-id="13ae6-112">startIndex</span><span class="sxs-lookup"><span data-stu-id="13ae6-112">startIndex</span></span>  
    <span data-ttu-id="13ae6-113">Tipo: [System. Int32](/dotnet/api/system.int32)</span><span class="sxs-lookup"><span data-stu-id="13ae6-113">Type: [System.Int32](/dotnet/api/system.int32)</span></span>  
    
    <span data-ttu-id="13ae6-114">Posizione iniziale all'interno dei byte.</span><span class="sxs-lookup"><span data-stu-id="13ae6-114">The starting position within the bytes.</span></span>

<!-- end list -->

  - <span data-ttu-id="13ae6-115">count</span><span class="sxs-lookup"><span data-stu-id="13ae6-115">count</span></span>  
    <span data-ttu-id="13ae6-116">Tipo: [System. Int32](/dotnet/api/system.int32)</span><span class="sxs-lookup"><span data-stu-id="13ae6-116">Type: [System.Int32](/dotnet/api/system.int32)</span></span>  
    
    <span data-ttu-id="13ae6-117">Numero di byte da decodificare.</span><span class="sxs-lookup"><span data-stu-id="13ae6-117">The number of bytes to decode.</span></span>

<!-- end list -->

  - <span data-ttu-id="13ae6-118">Err</span><span class="sxs-lookup"><span data-stu-id="13ae6-118">err</span></span>  
    <span data-ttu-id="13ae6-119">Tipo: [System. Int32](/dotnet/api/system.int32)</span><span class="sxs-lookup"><span data-stu-id="13ae6-119">Type: [System.Int32](/dotnet/api/system.int32)</span></span>  
    
    <span data-ttu-id="13ae6-120">Errore restituito da ESENT.</span><span class="sxs-lookup"><span data-stu-id="13ae6-120">The error returned from ESENT.</span></span>

## <a name="see-also"></a><span data-ttu-id="13ae6-121">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="13ae6-121">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="13ae6-122">Riferimento</span><span class="sxs-lookup"><span data-stu-id="13ae6-122">Reference</span></span>

[<span data-ttu-id="13ae6-123">Classe ColumnValue</span><span class="sxs-lookup"><span data-stu-id="13ae6-123">ColumnValue class</span></span>](./columnvalue-class.md)

[<span data-ttu-id="13ae6-124">Membri di ColumnValue</span><span class="sxs-lookup"><span data-stu-id="13ae6-124">ColumnValue members</span></span>](./columnvalue-members.md)

[<span data-ttu-id="13ae6-125">Spazio dei nomi Microsoft. ISAM. esent. Interop</span><span class="sxs-lookup"><span data-stu-id="13ae6-125">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
