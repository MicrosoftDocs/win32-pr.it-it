---
description: 'Altre informazioni su: Metodo CimMofDeserializer. DeserializeClasses (byte [], UInt32)'
title: Metodo CimMofDeserializer. DeserializeClasses (byte [], UInt32) (Microsoft. Management. Infrastructure. Serialization)
TOCTitle: CimMofDeserializer.DeserializeClasses method (Byte[], UInt32) (Microsoft.Management.Infrastructure.Serialization)
ms:assetid: M:Microsoft.Management.Infrastructure.Serialization.CimMofDeserializer.DeserializeClasses(System.Byte[],System.UInt32@)
ms.date: 11/13/2019
mtps_version: v=VS.85
dev_langs:
- csharp
- c++
- fsharp
- vb
api_location:
- Microsoft.Management.Infrastructure.dll
api_name:
- Microsoft.Management.Infrastructure.Serialization.CimMofDeserializer.DeserializeClasses
api_type:
- Assembly
topic_type:
- apiref
product_family_name: VS
ms.topic: reference
ms.openlocfilehash: 983fa9e8fe36b872d05c3140c74f572b7d1ebf50
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104524816"
---
# <a name="cimmofdeserializerdeserializeclasses-method-byteuint32"></a><span data-ttu-id="08574-103">Metodo CimMofDeserializer. DeserializeClasses (byte \[ \] , UInt32)</span><span class="sxs-lookup"><span data-stu-id="08574-103">CimMofDeserializer.DeserializeClasses method (Byte\[\], UInt32)</span></span>

<span data-ttu-id="08574-104">Deserializza le classi CIM in base ai dati serializzati.</span><span class="sxs-lookup"><span data-stu-id="08574-104">Deserializes CIM classes based on serialized data.</span></span>

<span data-ttu-id="08574-105">**Spazio dei nomi:**   [Microsoft. Management. Infrastructure. Serialization](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832966(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="08574-105">**Namespace:**   [Microsoft.Management.Infrastructure.Serialization](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832966(v=vs.85))</span></span>  
<span data-ttu-id="08574-106">**Assembly:**  Microsoft. Management. Infrastructure (in Microsoft.Management.Infrastructure.dll)</span><span class="sxs-lookup"><span data-stu-id="08574-106">**Assembly:**  Microsoft.Management.Infrastructure (in Microsoft.Management.Infrastructure.dll)</span></span>  

## <a name="syntax"></a><span data-ttu-id="08574-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="08574-107">Syntax</span></span>

``` csharp
public IEnumerable<CimClass> DeserializeClasses(
    byte[] serializedData,
    ref uint offset
)
```

``` c++
public:
IEnumerable<CimClass^>^ DeserializeClasses(
    array<unsigned char>^ serializedData,
    unsigned int% offset
)
```

``` fsharp
member DeserializeClasses : 
        serializedData:byte[] *
        offset:uint32 byref -> IEnumerable<CimClass>
```

``` vb
Public Function DeserializeClasses (
    serializedData As Byte(),
    ByRef offset As UInteger
) As IEnumerable(CimClass)
```

#### <a name="parameters"></a><span data-ttu-id="08574-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="08574-108">Parameters</span></span>

  - <span data-ttu-id="08574-109">serializedData</span><span class="sxs-lookup"><span data-stu-id="08574-109">serializedData</span></span>  
    <span data-ttu-id="08574-110">Tipo: [System. byte](/dotnet/api/system.byte?view=netframework-4.8)\[\]</span><span class="sxs-lookup"><span data-stu-id="08574-110">Type: [System.Byte](/dotnet/api/system.byte?view=netframework-4.8)\[\]</span></span>
    
    <span data-ttu-id="08574-111">Buffer che contiene i dati serializzati.</span><span class="sxs-lookup"><span data-stu-id="08574-111">A buffer that contains the serialized data.</span></span>

<!-- end list -->

  - <span data-ttu-id="08574-112">offset</span><span class="sxs-lookup"><span data-stu-id="08574-112">offset</span></span>  
    <span data-ttu-id="08574-113">Tipo: [System. UInt32](/dotnet/api/system.uint32?view=netframework-4.8)</span><span class="sxs-lookup"><span data-stu-id="08574-113">Type: [System.UInt32](/dotnet/api/system.uint32?view=netframework-4.8)</span></span>
    
    <span data-ttu-id="08574-114">Offset dei byte nella posizione da cui iniziare la lettura dei dati.</span><span class="sxs-lookup"><span data-stu-id="08574-114">The byte offset to the location at which to begin reading the data.</span></span> <span data-ttu-id="08574-115">Quando il metodo restituisce un risultato, l'offset verrà puntato al byte successivo dopo le classi deserializzate.</span><span class="sxs-lookup"><span data-stu-id="08574-115">When the method returns, the offset will be pointing to the next byte after the deserialized classes.</span></span>

#### <a name="return-value"></a><span data-ttu-id="08574-116">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="08574-116">Return value</span></span>

<span data-ttu-id="08574-117">Tipo: [System. Collections. Generic. IEnumerable](/dotnet/api/system.collections.generic.ienumerable-1?view=netframework-4.8)\<[CimClass](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832269(v=vs.85))\></span><span class="sxs-lookup"><span data-stu-id="08574-117">Type: [System.Collections.Generic.IEnumerable](/dotnet/api/system.collections.generic.ienumerable-1?view=netframework-4.8)\<[CimClass](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832269(v=vs.85))\></span></span>

<span data-ttu-id="08574-118">Interfaccia [IEnumerable \<T\> ](/dotnet/api/system.collections.generic.ienumerable-1?view=netframework-4.8) che può essere utilizzata per enumerare le classi CIM.</span><span class="sxs-lookup"><span data-stu-id="08574-118">An [IEnumerable\<T\>](/dotnet/api/system.collections.generic.ienumerable-1?view=netframework-4.8) interface that can be used to enumerate the CIM classes.</span></span>

## <a name="see-also"></a><span data-ttu-id="08574-119">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="08574-119">See also</span></span>

<span data-ttu-id="08574-120">[Classe CimClass](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832269(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="08574-120">[CimClass class](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832269(v=vs.85))</span></span>  
<span data-ttu-id="08574-121">[Spazio dei nomi Microsoft. Management. Infrastructure. Serialization](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832966(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="08574-121">[Microsoft.Management.Infrastructure.Serialization namespace](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832966(v=vs.85))</span></span>
