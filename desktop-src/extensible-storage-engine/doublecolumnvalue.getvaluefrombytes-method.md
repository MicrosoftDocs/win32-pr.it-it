---
description: 'Altre informazioni su: DoubleColumnValue. GetValueFromBytes, metodo'
title: DoubleColumnValue. GetValueFromBytes, metodo
TOCTitle: 'GetValueFromBytes method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.DoubleColumnValue.GetValueFromBytes(System.Byte[],System.Int32,System.Int32,System.Int32)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.doublecolumnvalue.getvaluefrombytes(v=EXCHG.10)
ms:contentKeyID: 55107244
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.DoubleColumnValue.GetValueFromBytes
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.DoubleColumnValue.GetValueFromBytes
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 209f573862a257e587a26c1957e80e46f3190616
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106309180"
---
# <a name="doublecolumnvaluegetvaluefrombytes-method"></a><span data-ttu-id="3f662-103">DoubleColumnValue. GetValueFromBytes, metodo</span><span class="sxs-lookup"><span data-stu-id="3f662-103">DoubleColumnValue.GetValueFromBytes method</span></span>

<span data-ttu-id="3f662-104">Dato che i dati sono stati recuperati da ESENT, decodificano i dati e impostano il valore nell'oggetto ColumnValue.</span><span class="sxs-lookup"><span data-stu-id="3f662-104">Given data retrieved from ESENT, decode the data and set the value in the ColumnValue object.</span></span>

<span data-ttu-id="3f662-105">**Spazio dei nomi:**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="3f662-105">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="3f662-106">**Assembly:**  Microsoft. ISAM. esent. Interop (in Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="3f662-106">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="3f662-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="3f662-107">Syntax</span></span>

``` vb
'Declaration
Protected Overrides Sub GetValueFromBytes ( _
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
protected override void GetValueFromBytes(
    byte[] value,
    int startIndex,
    int count,
    int err
)
```

#### <a name="parameters"></a><span data-ttu-id="3f662-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="3f662-108">Parameters</span></span>

  - <span data-ttu-id="3f662-109">Valore</span><span class="sxs-lookup"><span data-stu-id="3f662-109">value</span></span>  
    <span data-ttu-id="3f662-110">Tipo \[\]</span><span class="sxs-lookup"><span data-stu-id="3f662-110">Type: \[\]</span></span>  
    
    <span data-ttu-id="3f662-111">Matrice di byte.</span><span class="sxs-lookup"><span data-stu-id="3f662-111">An array of bytes.</span></span>

<!-- end list -->

  - <span data-ttu-id="3f662-112">startIndex</span><span class="sxs-lookup"><span data-stu-id="3f662-112">startIndex</span></span>  
    <span data-ttu-id="3f662-113">Tipo: [System. Int32](/dotnet/api/system.int32)</span><span class="sxs-lookup"><span data-stu-id="3f662-113">Type: [System.Int32](/dotnet/api/system.int32)</span></span>  
    
    <span data-ttu-id="3f662-114">Posizione iniziale all'interno dei byte.</span><span class="sxs-lookup"><span data-stu-id="3f662-114">The starting position within the bytes.</span></span>

<!-- end list -->

  - <span data-ttu-id="3f662-115">count</span><span class="sxs-lookup"><span data-stu-id="3f662-115">count</span></span>  
    <span data-ttu-id="3f662-116">Tipo: [System. Int32](/dotnet/api/system.int32)</span><span class="sxs-lookup"><span data-stu-id="3f662-116">Type: [System.Int32](/dotnet/api/system.int32)</span></span>  
    
    <span data-ttu-id="3f662-117">Numero di byte da decodificare.</span><span class="sxs-lookup"><span data-stu-id="3f662-117">The number of bytes to decode.</span></span>

<!-- end list -->

  - <span data-ttu-id="3f662-118">Err</span><span class="sxs-lookup"><span data-stu-id="3f662-118">err</span></span>  
    <span data-ttu-id="3f662-119">Tipo: [System. Int32](/dotnet/api/system.int32)</span><span class="sxs-lookup"><span data-stu-id="3f662-119">Type: [System.Int32](/dotnet/api/system.int32)</span></span>  
    
    <span data-ttu-id="3f662-120">Errore restituito da ESENT.</span><span class="sxs-lookup"><span data-stu-id="3f662-120">The error returned from ESENT.</span></span>

## <a name="see-also"></a><span data-ttu-id="3f662-121">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="3f662-121">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="3f662-122">Riferimento</span><span class="sxs-lookup"><span data-stu-id="3f662-122">Reference</span></span>

[<span data-ttu-id="3f662-123">Classe DoubleColumnValue</span><span class="sxs-lookup"><span data-stu-id="3f662-123">DoubleColumnValue class</span></span>](./doublecolumnvalue-class.md)

[<span data-ttu-id="3f662-124">Membri di DoubleColumnValue</span><span class="sxs-lookup"><span data-stu-id="3f662-124">DoubleColumnValue members</span></span>](./doublecolumnvalue-members.md)

[<span data-ttu-id="3f662-125">Spazio dei nomi Microsoft. ISAM. esent. Interop</span><span class="sxs-lookup"><span data-stu-id="3f662-125">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
