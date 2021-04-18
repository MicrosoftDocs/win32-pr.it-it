---
description: 'Altre informazioni su: Conversions. ConvertDoubleToDateTime, metodo'
title: Conversions. ConvertDoubleToDateTime, metodo
TOCTitle: 'ConvertDoubleToDateTime method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Conversions.ConvertDoubleToDateTime(System.Double)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.conversions.convertdoubletodatetime(v=EXCHG.10)
ms:contentKeyID: 55101133
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Conversions.ConvertDoubleToDateTime
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Conversions.ConvertDoubleToDateTime
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: a1d066780ade3da95f4d4d5500143700f7a7d5bf
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106315707"
---
# <a name="conversionsconvertdoubletodatetime-method"></a><span data-ttu-id="5a048-103">Conversions. ConvertDoubleToDateTime, metodo</span><span class="sxs-lookup"><span data-stu-id="5a048-103">Conversions.ConvertDoubleToDateTime method</span></span>

<span data-ttu-id="5a048-104">Converte un valore Double (formato di data e ora di OA) in DateTime.</span><span class="sxs-lookup"><span data-stu-id="5a048-104">Convert a double (OA date time format) to a DateTime.</span></span> <span data-ttu-id="5a048-105">Diversamente da DateTime. FromOADate, questa operazione non genera eccezioni.</span><span class="sxs-lookup"><span data-stu-id="5a048-105">Unlike DateTime.FromOADate this doesn't throw exceptions.</span></span>

<span data-ttu-id="5a048-106">**Spazio dei nomi:**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="5a048-106">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="5a048-107">**Assembly:**  Microsoft. ISAM. esent. Interop (in Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="5a048-107">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="5a048-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="5a048-108">Syntax</span></span>

``` vb
'Declaration
Public Shared Function ConvertDoubleToDateTime ( _
    d As Double _
) As DateTime
'Usage
Dim d As Double
Dim returnValue As DateTime

returnValue = Conversions.ConvertDoubleToDateTime(d)
```

``` csharp
public static DateTime ConvertDoubleToDateTime(
    double d
)
```

#### <a name="parameters"></a><span data-ttu-id="5a048-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="5a048-109">Parameters</span></span>

  - <span data-ttu-id="5a048-110">d</span><span class="sxs-lookup"><span data-stu-id="5a048-110">d</span></span>  
    <span data-ttu-id="5a048-111">Tipo: [System. Double](/dotnet/api/system.double)</span><span class="sxs-lookup"><span data-stu-id="5a048-111">Type: [System.Double](/dotnet/api/system.double)</span></span>  
    
    <span data-ttu-id="5a048-112">Valore Double.</span><span class="sxs-lookup"><span data-stu-id="5a048-112">The double value.</span></span>

#### <a name="return-value"></a><span data-ttu-id="5a048-113">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="5a048-113">Return value</span></span>

<span data-ttu-id="5a048-114">Tipo: [System. DateTime](/dotnet/api/system.datetime)</span><span class="sxs-lookup"><span data-stu-id="5a048-114">Type: [System.DateTime](/dotnet/api/system.datetime)</span></span>  
<span data-ttu-id="5a048-115">Valore DateTime.</span><span class="sxs-lookup"><span data-stu-id="5a048-115">A DateTime.</span></span>  

## <a name="see-also"></a><span data-ttu-id="5a048-116">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="5a048-116">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="5a048-117">Riferimento</span><span class="sxs-lookup"><span data-stu-id="5a048-117">Reference</span></span>

[<span data-ttu-id="5a048-118">Classe Conversions</span><span class="sxs-lookup"><span data-stu-id="5a048-118">Conversions class</span></span>](./conversions-class.md)

[<span data-ttu-id="5a048-119">Membri delle conversioni</span><span class="sxs-lookup"><span data-stu-id="5a048-119">Conversions members</span></span>](./conversions-members.md)

[<span data-ttu-id="5a048-120">Spazio dei nomi Microsoft. ISAM. esent. Interop</span><span class="sxs-lookup"><span data-stu-id="5a048-120">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
