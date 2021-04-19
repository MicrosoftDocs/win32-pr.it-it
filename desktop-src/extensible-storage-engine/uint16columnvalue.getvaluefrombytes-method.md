---
description: 'Altre informazioni su: UInt16ColumnValue. GetValueFromBytes, metodo'
title: UInt16ColumnValue. GetValueFromBytes, metodo
TOCTitle: 'GetValueFromBytes method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.UInt16ColumnValue.GetValueFromBytes(System.Byte[],System.Int32,System.Int32,System.Int32)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.uint16columnvalue.getvaluefrombytes(v=EXCHG.10)
ms:contentKeyID: 55104191
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.UInt16ColumnValue.GetValueFromBytes
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.UInt16ColumnValue.GetValueFromBytes
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 5df0a21587dfa30c01d04879db0c5370b8371287
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106317336"
---
# <a name="uint16columnvaluegetvaluefrombytes-method"></a><span data-ttu-id="55a0a-103">UInt16ColumnValue. GetValueFromBytes, metodo</span><span class="sxs-lookup"><span data-stu-id="55a0a-103">UInt16ColumnValue.GetValueFromBytes method</span></span>

<span data-ttu-id="55a0a-104">Dato che i dati sono stati recuperati da ESENT, decodificano i dati e impostano il valore nell'oggetto ColumnValue.</span><span class="sxs-lookup"><span data-stu-id="55a0a-104">Given data retrieved from ESENT, decode the data and set the value in the ColumnValue object.</span></span>

<span data-ttu-id="55a0a-105">**Spazio dei nomi:**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="55a0a-105">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="55a0a-106">**Assembly:**  Microsoft. ISAM. esent. Interop (in Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="55a0a-106">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="55a0a-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="55a0a-107">Syntax</span></span>

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

#### <a name="parameters"></a><span data-ttu-id="55a0a-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="55a0a-108">Parameters</span></span>

  - <span data-ttu-id="55a0a-109">Valore</span><span class="sxs-lookup"><span data-stu-id="55a0a-109">value</span></span>  
    <span data-ttu-id="55a0a-110">Tipo \[\]</span><span class="sxs-lookup"><span data-stu-id="55a0a-110">Type: \[\]</span></span>  
    
    <span data-ttu-id="55a0a-111">Matrice di byte.</span><span class="sxs-lookup"><span data-stu-id="55a0a-111">An array of bytes.</span></span>

<!-- end list -->

  - <span data-ttu-id="55a0a-112">startIndex</span><span class="sxs-lookup"><span data-stu-id="55a0a-112">startIndex</span></span>  
    <span data-ttu-id="55a0a-113">Tipo: [System. Int32](/dotnet/api/system.int32)</span><span class="sxs-lookup"><span data-stu-id="55a0a-113">Type: [System.Int32](/dotnet/api/system.int32)</span></span>  
    
    <span data-ttu-id="55a0a-114">Posizione iniziale all'interno dei byte.</span><span class="sxs-lookup"><span data-stu-id="55a0a-114">The starting position within the bytes.</span></span>

<!-- end list -->

  - <span data-ttu-id="55a0a-115">count</span><span class="sxs-lookup"><span data-stu-id="55a0a-115">count</span></span>  
    <span data-ttu-id="55a0a-116">Tipo: [System. Int32](/dotnet/api/system.int32)</span><span class="sxs-lookup"><span data-stu-id="55a0a-116">Type: [System.Int32](/dotnet/api/system.int32)</span></span>  
    
    <span data-ttu-id="55a0a-117">Numero di byte da decodificare.</span><span class="sxs-lookup"><span data-stu-id="55a0a-117">The number of bytes to decode.</span></span>

<!-- end list -->

  - <span data-ttu-id="55a0a-118">Err</span><span class="sxs-lookup"><span data-stu-id="55a0a-118">err</span></span>  
    <span data-ttu-id="55a0a-119">Tipo: [System. Int32](/dotnet/api/system.int32)</span><span class="sxs-lookup"><span data-stu-id="55a0a-119">Type: [System.Int32](/dotnet/api/system.int32)</span></span>  
    
    <span data-ttu-id="55a0a-120">Errore restituito da ESENT.</span><span class="sxs-lookup"><span data-stu-id="55a0a-120">The error returned from ESENT.</span></span>

## <a name="see-also"></a><span data-ttu-id="55a0a-121">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="55a0a-121">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="55a0a-122">Riferimento</span><span class="sxs-lookup"><span data-stu-id="55a0a-122">Reference</span></span>

[<span data-ttu-id="55a0a-123">Classe UInt16ColumnValue</span><span class="sxs-lookup"><span data-stu-id="55a0a-123">UInt16ColumnValue class</span></span>](./uint16columnvalue-class.md)

[<span data-ttu-id="55a0a-124">Membri di UInt16ColumnValue</span><span class="sxs-lookup"><span data-stu-id="55a0a-124">UInt16ColumnValue members</span></span>](./uint16columnvalue-members.md)

[<span data-ttu-id="55a0a-125">Spazio dei nomi Microsoft. ISAM. esent. Interop</span><span class="sxs-lookup"><span data-stu-id="55a0a-125">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
