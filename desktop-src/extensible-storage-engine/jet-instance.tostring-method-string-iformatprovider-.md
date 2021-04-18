---
description: 'Altre informazioni su: JET_INSTANCE. Metodo ToString (String, IFormatProvider)'
title: JET_INSTANCE. Metodo ToString (String, IFormatProvider)
TOCTitle: ToString method (String, IFormatProvider)
ms:assetid: M:Microsoft.Isam.Esent.Interop.JET_INSTANCE.ToString(System.String,System.IFormatProvider)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.jet_instance.tostring(v=EXCHG.10)
ms:contentKeyID: 39511283
ms.date: 07/30/2014
ms.topic: reference
dev_langs:
- vb
- csharp
api_name:
- Microsoft.Isam.Esent.Interop.JET_INSTANCE.ToString
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 4030a86ed867a2463346dca549acb35809264c34
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106315129"
---
# <a name="jet_instancetostring-method-string-iformatprovider"></a><span data-ttu-id="2e4c5-103">JET_INSTANCE. Metodo ToString (String, IFormatProvider)</span><span class="sxs-lookup"><span data-stu-id="2e4c5-103">JET_INSTANCE.ToString method (String, IFormatProvider)</span></span>

<span data-ttu-id="2e4c5-104">Formatta il valore dell'istanza corrente usando il formato specificato.</span><span class="sxs-lookup"><span data-stu-id="2e4c5-104">Formats the value of the current instance using the specified format.</span></span>

<span data-ttu-id="2e4c5-105">**Spazio dei nomi:**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="2e4c5-105">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="2e4c5-106">**Assembly:**  Microsoft. ISAM. esent. Interop (in Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="2e4c5-106">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="2e4c5-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="2e4c5-107">Syntax</span></span>

``` vb
'Declaration
Public Function ToString ( _
    format As String, _
    formatProvider As IFormatProvider _
) As String
'Usage
Dim instance As JET_INSTANCE
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

#### <a name="parameters"></a><span data-ttu-id="2e4c5-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="2e4c5-108">Parameters</span></span>

  - <span data-ttu-id="2e4c5-109">format</span><span class="sxs-lookup"><span data-stu-id="2e4c5-109">format</span></span>  
    <span data-ttu-id="2e4c5-110">Tipo: [System. String](/dotnet/api/system.string)</span><span class="sxs-lookup"><span data-stu-id="2e4c5-110">Type: [System.String](/dotnet/api/system.string)</span></span>  
    
    <span data-ttu-id="2e4c5-111">[Stringa](/dotnet/api/system.string) che specifica il formato da utilizzare. oppure null per usare il formato predefinito definito per il tipo dell'implementazione di [IFormattable](/dotnet/api/system.iformattable) .</span><span class="sxs-lookup"><span data-stu-id="2e4c5-111">The [String](/dotnet/api/system.string) specifying the format to use; or, null to use the default format defined for the type of the [IFormattable](/dotnet/api/system.iformattable) implementation.</span></span>

<!-- end list -->

  - <span data-ttu-id="2e4c5-112">formatProvider</span><span class="sxs-lookup"><span data-stu-id="2e4c5-112">formatProvider</span></span>  
    <span data-ttu-id="2e4c5-113">Tipo: [System. IFormatProvider](/dotnet/api/system.iformatprovider)</span><span class="sxs-lookup"><span data-stu-id="2e4c5-113">Type: [System.IFormatProvider](/dotnet/api/system.iformatprovider)</span></span>  
    
    <span data-ttu-id="2e4c5-114">[IFormatProvider](/dotnet/api/system.iformatprovider) da utilizzare per formattare il valore. oppure, null per ottenere le informazioni sul formato numerico dalle impostazioni locali correnti del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="2e4c5-114">The [IFormatProvider](/dotnet/api/system.iformatprovider) to use to format the value; or, null to obtain the numeric format information from the current locale setting of the operating system.</span></span>

#### <a name="return-value"></a><span data-ttu-id="2e4c5-115">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="2e4c5-115">Return value</span></span>

<span data-ttu-id="2e4c5-116">Tipo: [System. String](/dotnet/api/system.string)</span><span class="sxs-lookup"><span data-stu-id="2e4c5-116">Type: [System.String](/dotnet/api/system.string)</span></span>  
<span data-ttu-id="2e4c5-117">[Stringa](/dotnet/api/system.string) contenente il valore dell'istanza corrente nel formato specificato.</span><span class="sxs-lookup"><span data-stu-id="2e4c5-117">A [String](/dotnet/api/system.string) containing the value of the current instance in the specified format.</span></span>  

#### <a name="implements"></a><span data-ttu-id="2e4c5-118">Implementazioni</span><span class="sxs-lookup"><span data-stu-id="2e4c5-118">Implements</span></span>

[<span data-ttu-id="2e4c5-119">IFormattable. ToString (String, IFormatProvider)</span><span class="sxs-lookup"><span data-stu-id="2e4c5-119">IFormattable.ToString(String, IFormatProvider)</span></span>](/dotnet/api/system.iformattable.tostring#System_IFormattable_ToString_System_String_System_IFormatProvider_)  

## <a name="see-also"></a><span data-ttu-id="2e4c5-120">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="2e4c5-120">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="2e4c5-121">Riferimento</span><span class="sxs-lookup"><span data-stu-id="2e4c5-121">Reference</span></span>

[<span data-ttu-id="2e4c5-122">Struttura JET_INSTANCE</span><span class="sxs-lookup"><span data-stu-id="2e4c5-122">JET_INSTANCE structure</span></span>](./jet-instance-structure.md)

[<span data-ttu-id="2e4c5-123">Membri JET_INSTANCE</span><span class="sxs-lookup"><span data-stu-id="2e4c5-123">JET_INSTANCE members</span></span>](./jet-instance-members.md)

[<span data-ttu-id="2e4c5-124">Overload ToString</span><span class="sxs-lookup"><span data-stu-id="2e4c5-124">ToString overload</span></span>](./jet-instance.tostring-method2.md)

[<span data-ttu-id="2e4c5-125">Spazio dei nomi Microsoft. ISAM. esent. Interop</span><span class="sxs-lookup"><span data-stu-id="2e4c5-125">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
