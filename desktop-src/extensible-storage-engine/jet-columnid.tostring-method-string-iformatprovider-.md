---
description: 'Altre informazioni su: JET_COLUMNID. Metodo ToString (String, IFormatProvider)'
title: JET_COLUMNID. Metodo ToString (String, IFormatProvider)
TOCTitle: ToString method (String, IFormatProvider)
ms:assetid: M:Microsoft.Isam.Esent.Interop.JET_COLUMNID.ToString(System.String,System.IFormatProvider)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.jet_columnid.tostring(v=EXCHG.10)
ms:contentKeyID: 39513695
ms.date: 07/30/2014
ms.topic: reference
dev_langs:
- vb
- csharp
api_name:
- Microsoft.Isam.Esent.Interop.JET_COLUMNID.ToString
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 163fcd773224e183b5c83d764c8dac508b269592
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104527468"
---
# <a name="jet_columnidtostring-method-string-iformatprovider"></a><span data-ttu-id="6bb56-103">JET_COLUMNID. Metodo ToString (String, IFormatProvider)</span><span class="sxs-lookup"><span data-stu-id="6bb56-103">JET_COLUMNID.ToString method (String, IFormatProvider)</span></span>

<span data-ttu-id="6bb56-104">Formatta il valore dell'istanza corrente usando il formato specificato.</span><span class="sxs-lookup"><span data-stu-id="6bb56-104">Formats the value of the current instance using the specified format.</span></span>

<span data-ttu-id="6bb56-105">**Spazio dei nomi:**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="6bb56-105">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="6bb56-106">**Assembly:**  Microsoft. ISAM. esent. Interop (in Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="6bb56-106">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="6bb56-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="6bb56-107">Syntax</span></span>

``` vb
'Declaration
Public Function ToString ( _
    format As String, _
    formatProvider As IFormatProvider _
) As String
'Usage
Dim instance As JET_COLUMNID
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

#### <a name="parameters"></a><span data-ttu-id="6bb56-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="6bb56-108">Parameters</span></span>

  - <span data-ttu-id="6bb56-109">format</span><span class="sxs-lookup"><span data-stu-id="6bb56-109">format</span></span>  
    <span data-ttu-id="6bb56-110">Tipo: [System. String](/dotnet/api/system.string)</span><span class="sxs-lookup"><span data-stu-id="6bb56-110">Type: [System.String](/dotnet/api/system.string)</span></span>  
    
    <span data-ttu-id="6bb56-111">[Stringa](/dotnet/api/system.string) che specifica il formato da utilizzare.</span><span class="sxs-lookup"><span data-stu-id="6bb56-111">The [String](/dotnet/api/system.string) specifying the format to use.</span></span> <span data-ttu-id="6bb56-112">-oppure-null per usare il formato predefinito definito per il tipo dell'implementazione di [IFormattable](/dotnet/api/system.iformattable) .</span><span class="sxs-lookup"><span data-stu-id="6bb56-112">-or- null to use the default format defined for the type of the [IFormattable](/dotnet/api/system.iformattable) implementation.</span></span>

<!-- end list -->

  - <span data-ttu-id="6bb56-113">formatProvider</span><span class="sxs-lookup"><span data-stu-id="6bb56-113">formatProvider</span></span>  
    <span data-ttu-id="6bb56-114">Tipo: [System. IFormatProvider](/dotnet/api/system.iformatprovider)</span><span class="sxs-lookup"><span data-stu-id="6bb56-114">Type: [System.IFormatProvider](/dotnet/api/system.iformatprovider)</span></span>  
    
    <span data-ttu-id="6bb56-115">[IFormatProvider](/dotnet/api/system.iformatprovider) da utilizzare per formattare il valore.</span><span class="sxs-lookup"><span data-stu-id="6bb56-115">The [IFormatProvider](/dotnet/api/system.iformatprovider) to use to format the value.</span></span> <span data-ttu-id="6bb56-116">-oppure-null per ottenere le informazioni sul formato numerico dalle impostazioni locali correnti del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="6bb56-116">-or- null to obtain the numeric format information from the current locale setting of the operating system.</span></span>

#### <a name="return-value"></a><span data-ttu-id="6bb56-117">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="6bb56-117">Return value</span></span>

<span data-ttu-id="6bb56-118">Tipo: [System. String](/dotnet/api/system.string)</span><span class="sxs-lookup"><span data-stu-id="6bb56-118">Type: [System.String](/dotnet/api/system.string)</span></span>  
<span data-ttu-id="6bb56-119">[Stringa](/dotnet/api/system.string) contenente il valore dell'istanza corrente nel formato specificato.</span><span class="sxs-lookup"><span data-stu-id="6bb56-119">A [String](/dotnet/api/system.string) containing the value of the current instance in the specified format.</span></span>  

#### <a name="implements"></a><span data-ttu-id="6bb56-120">Implementazioni</span><span class="sxs-lookup"><span data-stu-id="6bb56-120">Implements</span></span>

[<span data-ttu-id="6bb56-121">IFormattable. ToString (String, IFormatProvider)</span><span class="sxs-lookup"><span data-stu-id="6bb56-121">IFormattable.ToString(String, IFormatProvider)</span></span>](/dotnet/api/system.iformattable.tostring#System_IFormattable_ToString_System_String_System_IFormatProvider_)  

## <a name="see-also"></a><span data-ttu-id="6bb56-122">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="6bb56-122">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="6bb56-123">Riferimento</span><span class="sxs-lookup"><span data-stu-id="6bb56-123">Reference</span></span>

[<span data-ttu-id="6bb56-124">Struttura JET_COLUMNID</span><span class="sxs-lookup"><span data-stu-id="6bb56-124">JET_COLUMNID structure</span></span>](./jet-columnid-structure.md)

[<span data-ttu-id="6bb56-125">Membri JET_COLUMNID</span><span class="sxs-lookup"><span data-stu-id="6bb56-125">JET_COLUMNID members</span></span>](./jet-columnid-members.md)

[<span data-ttu-id="6bb56-126">Overload ToString</span><span class="sxs-lookup"><span data-stu-id="6bb56-126">ToString overload</span></span>](./jet-columnid.tostring-method2.md)

[<span data-ttu-id="6bb56-127">Spazio dei nomi Microsoft. ISAM. esent. Interop</span><span class="sxs-lookup"><span data-stu-id="6bb56-127">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
