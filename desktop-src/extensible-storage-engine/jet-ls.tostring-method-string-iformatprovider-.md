---
description: 'Altre informazioni su: JET_LS. Metodo ToString (String, IFormatProvider)'
title: JET_LS. Metodo ToString (String, IFormatProvider)
TOCTitle: ToString method (String, IFormatProvider)
ms:assetid: M:Microsoft.Isam.Esent.Interop.JET_LS.ToString(System.String,System.IFormatProvider)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.jet_ls.tostring(v=EXCHG.10)
ms:contentKeyID: 39512228
ms.date: 07/30/2014
ms.topic: reference
dev_langs:
- vb
- csharp
api_name:
- Microsoft.Isam.Esent.Interop.JET_LS.ToString
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: e9979a10ea3afe41a995661f1af8eac8cba80cbd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104232568"
---
# <a name="jet_lstostring-method-string-iformatprovider"></a><span data-ttu-id="92ec1-103">JET_LS. Metodo ToString (String, IFormatProvider)</span><span class="sxs-lookup"><span data-stu-id="92ec1-103">JET_LS.ToString method (String, IFormatProvider)</span></span>

<span data-ttu-id="92ec1-104">Formatta il valore dell'istanza corrente usando il formato specificato.</span><span class="sxs-lookup"><span data-stu-id="92ec1-104">Formats the value of the current instance using the specified format.</span></span>

<span data-ttu-id="92ec1-105">**Spazio dei nomi:**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="92ec1-105">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="92ec1-106">**Assembly:**  Microsoft. ISAM. esent. Interop (in Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="92ec1-106">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="92ec1-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="92ec1-107">Syntax</span></span>

``` vb
'Declaration
Public Function ToString ( _
    format As String, _
    formatProvider As IFormatProvider _
) As String
'Usage
Dim instance As JET_LS
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

#### <a name="parameters"></a><span data-ttu-id="92ec1-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="92ec1-108">Parameters</span></span>

  - <span data-ttu-id="92ec1-109">format</span><span class="sxs-lookup"><span data-stu-id="92ec1-109">format</span></span>  
    <span data-ttu-id="92ec1-110">Tipo: [System. String](/dotnet/api/system.string)</span><span class="sxs-lookup"><span data-stu-id="92ec1-110">Type: [System.String](/dotnet/api/system.string)</span></span>  
    
    <span data-ttu-id="92ec1-111">[Stringa](/dotnet/api/system.string) che specifica il formato da utilizzare.</span><span class="sxs-lookup"><span data-stu-id="92ec1-111">The [String](/dotnet/api/system.string) specifying the format to use.</span></span> <span data-ttu-id="92ec1-112">-oppure-null per usare il formato predefinito definito per il tipo dell'implementazione di [IFormattable](/dotnet/api/system.iformattable) .</span><span class="sxs-lookup"><span data-stu-id="92ec1-112">-or- null to use the default format defined for the type of the [IFormattable](/dotnet/api/system.iformattable) implementation.</span></span>

<!-- end list -->

  - <span data-ttu-id="92ec1-113">formatProvider</span><span class="sxs-lookup"><span data-stu-id="92ec1-113">formatProvider</span></span>  
    <span data-ttu-id="92ec1-114">Tipo: [System. IFormatProvider](/dotnet/api/system.iformatprovider)</span><span class="sxs-lookup"><span data-stu-id="92ec1-114">Type: [System.IFormatProvider](/dotnet/api/system.iformatprovider)</span></span>  
    
    <span data-ttu-id="92ec1-115">[IFormatProvider](/dotnet/api/system.iformatprovider) da utilizzare per formattare il valore.</span><span class="sxs-lookup"><span data-stu-id="92ec1-115">The [IFormatProvider](/dotnet/api/system.iformatprovider) to use to format the value.</span></span> <span data-ttu-id="92ec1-116">-oppure-null per ottenere le informazioni sul formato numerico dalle impostazioni locali correnti del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="92ec1-116">-or- null to obtain the numeric format information from the current locale setting of the operating system.</span></span>

#### <a name="return-value"></a><span data-ttu-id="92ec1-117">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="92ec1-117">Return value</span></span>

<span data-ttu-id="92ec1-118">Tipo: [System. String](/dotnet/api/system.string)</span><span class="sxs-lookup"><span data-stu-id="92ec1-118">Type: [System.String](/dotnet/api/system.string)</span></span>  
<span data-ttu-id="92ec1-119">[Stringa](/dotnet/api/system.string) contenente il valore dell'istanza corrente nel formato specificato.</span><span class="sxs-lookup"><span data-stu-id="92ec1-119">A [String](/dotnet/api/system.string) containing the value of the current instance in the specified format.</span></span>  

#### <a name="implements"></a><span data-ttu-id="92ec1-120">Implementazioni</span><span class="sxs-lookup"><span data-stu-id="92ec1-120">Implements</span></span>

[<span data-ttu-id="92ec1-121">IFormattable. ToString (String, IFormatProvider)</span><span class="sxs-lookup"><span data-stu-id="92ec1-121">IFormattable.ToString(String, IFormatProvider)</span></span>](/dotnet/api/system.iformattable.tostring#System_IFormattable_ToString_System_String_System_IFormatProvider_)  

## <a name="see-also"></a><span data-ttu-id="92ec1-122">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="92ec1-122">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="92ec1-123">Riferimento</span><span class="sxs-lookup"><span data-stu-id="92ec1-123">Reference</span></span>

[<span data-ttu-id="92ec1-124">Struttura JET_LS</span><span class="sxs-lookup"><span data-stu-id="92ec1-124">JET_LS structure</span></span>](./jet-ls-structure.md)

[<span data-ttu-id="92ec1-125">Membri JET_LS</span><span class="sxs-lookup"><span data-stu-id="92ec1-125">JET_LS members</span></span>](./jet-ls-members.md)

[<span data-ttu-id="92ec1-126">Overload ToString</span><span class="sxs-lookup"><span data-stu-id="92ec1-126">ToString overload</span></span>](./jet-ls.tostring-method2.md)

[<span data-ttu-id="92ec1-127">Spazio dei nomi Microsoft. ISAM. esent. Interop</span><span class="sxs-lookup"><span data-stu-id="92ec1-127">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
