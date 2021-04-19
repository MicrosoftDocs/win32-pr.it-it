---
description: 'Altre informazioni su: Metodo CimMofDeserializer. DeserializeClasses (byte [], UInt32, IEnumerable <CimClass> )'
title: Metodo CimMofDeserializer. DeserializeClasses (byte [], UInt32, IEnumerable (CimClass)) (Microsoft. Management. Infrastructure. Serialization)
TOCTitle: CimMofDeserializer.DeserializeClasses method (Byte[], UInt32, IEnumerable(CimClass)) (Microsoft.Management.Infrastructure.Serialization)
ms:assetid: M:Microsoft.Management.Infrastructure.Serialization.CimMofDeserializer.DeserializeClasses(System.Byte[],System.UInt32@,System.Collections.Generic.IEnumerable{Microsoft.Management.Infrastructure.CimClass})
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
ms.openlocfilehash: edcdb84e9c3a3fe7a070263385c9ee6551341152
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106317547"
---
# <a name="cimmofdeserializerdeserializeclasses-method-byteuint32ienumerablecimclass"></a><span data-ttu-id="2310e-103">Metodo CimMofDeserializer. DeserializeClasses (byte \[ \] , UInt32, IEnumerable \<CimClass\> )</span><span class="sxs-lookup"><span data-stu-id="2310e-103">CimMofDeserializer.DeserializeClasses method (Byte\[\], UInt32, IEnumerable\<CimClass\>)</span></span>

<span data-ttu-id="2310e-104">Deserializza le classi CIM basate sui dati serializzati e una raccolta di classi CIM padre.</span><span class="sxs-lookup"><span data-stu-id="2310e-104">Deserializes CIM classes based on serialized data, and a collection of parent CIM classes.</span></span>

<span data-ttu-id="2310e-105">**Spazio dei nomi:**   [Microsoft. Management. Infrastructure. Serialization](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832966(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="2310e-105">**Namespace:**   [Microsoft.Management.Infrastructure.Serialization](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832966(v=vs.85))</span></span>  
<span data-ttu-id="2310e-106">**Assembly:**  Microsoft. Management. Infrastructure (in Microsoft.Management.Infrastructure.dll)</span><span class="sxs-lookup"><span data-stu-id="2310e-106">**Assembly:**  Microsoft.Management.Infrastructure (in Microsoft.Management.Infrastructure.dll)</span></span>  

## <a name="syntax"></a><span data-ttu-id="2310e-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="2310e-107">Syntax</span></span>

``` csharp
public IEnumerable<CimClass> DeserializeClasses(
    byte[] serializedData,
    ref uint offset,
    IEnumerable<CimClass> classes
)
```

``` c++
public:
IEnumerable<CimClass^>^ DeserializeClasses(
    array<unsigned char>^ serializedData,
    unsigned int% offset,
    IEnumerable<CimClass^>^ classes
)
```

``` fsharp
member DeserializeClasses : 
        serializedData:byte[] *
        offset:uint32 byref *
        classes:IEnumerable<CimClass> -> IEnumerable<CimClass>
```

``` vb
Public Function DeserializeClasses (
    serializedData As Byte(),
    ByRef offset As UInteger,
    classes As IEnumerable(Of CimClass)
) As IEnumerable(CimClass)
```

#### <a name="parameters"></a><span data-ttu-id="2310e-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="2310e-108">Parameters</span></span>

  - <span data-ttu-id="2310e-109">serializedData</span><span class="sxs-lookup"><span data-stu-id="2310e-109">serializedData</span></span>  
    <span data-ttu-id="2310e-110">Tipo: [System. byte](/dotnet/api/system.byte?view=netframework-4.8)\[\]</span><span class="sxs-lookup"><span data-stu-id="2310e-110">Type: [System.Byte](/dotnet/api/system.byte?view=netframework-4.8)\[\]</span></span>
    
    <span data-ttu-id="2310e-111">Buffer che contiene i dati serializzati.</span><span class="sxs-lookup"><span data-stu-id="2310e-111">A buffer that contains the serialized data.</span></span>

<!-- end list -->

  - <span data-ttu-id="2310e-112">offset</span><span class="sxs-lookup"><span data-stu-id="2310e-112">offset</span></span>  
    <span data-ttu-id="2310e-113">Tipo: [System. UInt32](/dotnet/api/system.uint32?view=netframework-4.8)</span><span class="sxs-lookup"><span data-stu-id="2310e-113">Type: [System.UInt32](/dotnet/api/system.uint32?view=netframework-4.8)</span></span>
    
    <span data-ttu-id="2310e-114">Offset dei byte nella posizione da cui iniziare la lettura dei dati.</span><span class="sxs-lookup"><span data-stu-id="2310e-114">The byte offset to the location at which to begin reading the data.</span></span> <span data-ttu-id="2310e-115">Quando il metodo restituisce un risultato, l'offset verrà puntato al byte successivo dopo le classi deserializzate.</span><span class="sxs-lookup"><span data-stu-id="2310e-115">When the method returns, the offset will be pointing to the next byte after the deserialized classes.</span></span>

<!-- end list -->

  - <span data-ttu-id="2310e-116">classi</span><span class="sxs-lookup"><span data-stu-id="2310e-116">classes</span></span>  
    <span data-ttu-id="2310e-117">Tipo: [System. Collections. Generic. IEnumerable](/dotnet/api/system.collections.generic.ienumerable-1?view=netframework-4.8)\<[CimClass](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832269(v=vs.85))\></span><span class="sxs-lookup"><span data-stu-id="2310e-117">Type: [System.Collections.Generic.IEnumerable](/dotnet/api/system.collections.generic.ienumerable-1?view=netframework-4.8)\<[CimClass](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832269(v=vs.85))\></span></span>
    
    <span data-ttu-id="2310e-118">Cache facoltativa delle classi CIM padre.</span><span class="sxs-lookup"><span data-stu-id="2310e-118">An optional cache of parent CIM classes.</span></span>

#### <a name="return-value"></a><span data-ttu-id="2310e-119">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="2310e-119">Return value</span></span>

<span data-ttu-id="2310e-120">Tipo: [System. Collections. Generic. IEnumerable](/dotnet/api/system.collections.generic.ienumerable-1?view=netframework-4.8)\<[CimClass](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832269(v=vs.85))\></span><span class="sxs-lookup"><span data-stu-id="2310e-120">Type: [System.Collections.Generic.IEnumerable](/dotnet/api/system.collections.generic.ienumerable-1?view=netframework-4.8)\<[CimClass](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832269(v=vs.85))\></span></span>

<span data-ttu-id="2310e-121">Interfaccia [IEnumerable \<T\> ](/dotnet/api/system.collections.generic.ienumerable-1?view=netframework-4.8) che può essere utilizzata per enumerare le classi CIM.</span><span class="sxs-lookup"><span data-stu-id="2310e-121">An [IEnumerable\<T\>](/dotnet/api/system.collections.generic.ienumerable-1?view=netframework-4.8) interface that can be used to enumerate the CIM classes.</span></span>

## <a name="see-also"></a><span data-ttu-id="2310e-122">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="2310e-122">See also</span></span>

<span data-ttu-id="2310e-123">[Classe CimClass](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832269(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="2310e-123">[CimClass class](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832269(v=vs.85))</span></span>  
<span data-ttu-id="2310e-124">[Spazio dei nomi Microsoft. Management. Infrastructure. Serialization](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832966(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="2310e-124">[Microsoft.Management.Infrastructure.Serialization namespace](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832966(v=vs.85))</span></span>
