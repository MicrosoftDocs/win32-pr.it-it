---
description: 'Altre informazioni su: JET_OSSNAPID. Metodo ToString (String, IFormatProvider)'
title: JET_OSSNAPID. Metodo ToString (String, IFormatProvider)
TOCTitle: ToString method (String, IFormatProvider)
ms:assetid: M:Microsoft.Isam.Esent.Interop.JET_OSSNAPID.ToString(System.String,System.IFormatProvider)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.jet_ossnapid.tostring(v=EXCHG.10)
ms:contentKeyID: 39512151
ms.date: 07/30/2014
ms.topic: reference
dev_langs:
- vb
- csharp
api_name:
- Microsoft.Isam.Esent.Interop.JET_OSSNAPID.ToString
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 95e93fd3a6bbf7f2fa3505fcb9480367b780ecc4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106318116"
---
# <a name="jet_ossnapidtostring-method-string-iformatprovider"></a><span data-ttu-id="a3357-103">JET_OSSNAPID. Metodo ToString (String, IFormatProvider)</span><span class="sxs-lookup"><span data-stu-id="a3357-103">JET_OSSNAPID.ToString method (String, IFormatProvider)</span></span>

<span data-ttu-id="a3357-104">Formatta il valore dell'istanza corrente usando il formato specificato.</span><span class="sxs-lookup"><span data-stu-id="a3357-104">Formats the value of the current instance using the specified format.</span></span>

<span data-ttu-id="a3357-105">**Spazio dei nomi:**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="a3357-105">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="a3357-106">**Assembly:**  Microsoft. ISAM. esent. Interop (in Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="a3357-106">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="a3357-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="a3357-107">Syntax</span></span>

``` vb
'Declaration
Public Function ToString ( _
    format As String, _
    formatProvider As IFormatProvider _
) As String
'Usage
Dim instance As JET_OSSNAPID
Dim format As String
Dim formatProvider As IFormatProvider
Dim returnValue As String

returnValue = instance.ToString(format, _
    formatProvider)
```

``` csharp
public string ToString(
    string format,
    IFormatProvider formatProvider
)
```

#### <a name="parameters"></a><span data-ttu-id="a3357-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="a3357-108">Parameters</span></span>

  - <span data-ttu-id="a3357-109">format</span><span class="sxs-lookup"><span data-stu-id="a3357-109">format</span></span>  
    <span data-ttu-id="a3357-110">Tipo: [System. String](/dotnet/api/system.string)</span><span class="sxs-lookup"><span data-stu-id="a3357-110">Type: [System.String](/dotnet/api/system.string)</span></span>  
    
    <span data-ttu-id="a3357-111">[Stringa](/dotnet/api/system.string) che specifica il formato da utilizzare.</span><span class="sxs-lookup"><span data-stu-id="a3357-111">The [String](/dotnet/api/system.string) specifying the format to use.</span></span> <span data-ttu-id="a3357-112">-oppure-null per usare il formato predefinito definito per il tipo dell'implementazione di [IFormattable](/dotnet/api/system.iformattable) .</span><span class="sxs-lookup"><span data-stu-id="a3357-112">-or- null to use the default format defined for the type of the [IFormattable](/dotnet/api/system.iformattable) implementation.</span></span>

<!-- end list -->

  - <span data-ttu-id="a3357-113">formatProvider</span><span class="sxs-lookup"><span data-stu-id="a3357-113">formatProvider</span></span>  
    <span data-ttu-id="a3357-114">Tipo: [System. IFormatProvider](/dotnet/api/system.iformatprovider)</span><span class="sxs-lookup"><span data-stu-id="a3357-114">Type: [System.IFormatProvider](/dotnet/api/system.iformatprovider)</span></span>  
    
    <span data-ttu-id="a3357-115">[IFormatProvider](/dotnet/api/system.iformatprovider) da utilizzare per formattare il valore.</span><span class="sxs-lookup"><span data-stu-id="a3357-115">The [IFormatProvider](/dotnet/api/system.iformatprovider) to use to format the value.</span></span> <span data-ttu-id="a3357-116">-oppure-null per ottenere le informazioni sul formato numerico dalle impostazioni locali correnti del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="a3357-116">-or- null to obtain the numeric format information from the current locale setting of the operating system.</span></span>

#### <a name="return-value"></a><span data-ttu-id="a3357-117">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="a3357-117">Return value</span></span>

<span data-ttu-id="a3357-118">Tipo: [System. String](/dotnet/api/system.string)</span><span class="sxs-lookup"><span data-stu-id="a3357-118">Type: [System.String](/dotnet/api/system.string)</span></span>  
<span data-ttu-id="a3357-119">[Stringa](/dotnet/api/system.string) contenente il valore dell'istanza corrente nel formato specificato.</span><span class="sxs-lookup"><span data-stu-id="a3357-119">A [String](/dotnet/api/system.string) containing the value of the current instance in the specified format.</span></span>  

#### <a name="implements"></a><span data-ttu-id="a3357-120">Implementazioni</span><span class="sxs-lookup"><span data-stu-id="a3357-120">Implements</span></span>

[<span data-ttu-id="a3357-121">IFormattable. ToString (String, IFormatProvider)</span><span class="sxs-lookup"><span data-stu-id="a3357-121">IFormattable.ToString(String, IFormatProvider)</span></span>](/dotnet/api/system.iformattable.tostring#System_IFormattable_ToString_System_String_System_IFormatProvider_)  

## <a name="see-also"></a><span data-ttu-id="a3357-122">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="a3357-122">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="a3357-123">Riferimento</span><span class="sxs-lookup"><span data-stu-id="a3357-123">Reference</span></span>

[<span data-ttu-id="a3357-124">Struttura JET_OSSNAPID</span><span class="sxs-lookup"><span data-stu-id="a3357-124">JET_OSSNAPID structure</span></span>](./jet-ossnapid-structure.md)

[<span data-ttu-id="a3357-125">Membri JET_OSSNAPID</span><span class="sxs-lookup"><span data-stu-id="a3357-125">JET_OSSNAPID members</span></span>](./jet-ossnapid-members.md)

[<span data-ttu-id="a3357-126">Overload ToString</span><span class="sxs-lookup"><span data-stu-id="a3357-126">ToString overload</span></span>](./jet-ossnapid.tostring-method.md)

[<span data-ttu-id="a3357-127">Spazio dei nomi Microsoft. ISAM. esent. Interop</span><span class="sxs-lookup"><span data-stu-id="a3357-127">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
