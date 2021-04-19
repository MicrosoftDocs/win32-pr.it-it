---
description: 'Altre informazioni su: Metodo CimMofDeserializer. DeserializeInstances (byte [], UInt32, IEnumerable <CimClass> , OnClassNeeded, GetIncludedFileContent)'
title: Metodo CimMofDeserializer. DeserializeInstances (byte [], UInt32, IEnumerable (CimClass), OnClassNeeded, GetIncludedFileContent) (Microsoft. Management. Infrastructure. Serialization)
TOCTitle: CimMofDeserializer.DeserializeInstances method (Byte[], UInt32, IEnumerable(CimClass), OnClassNeeded, GetIncludedFileContent) (Microsoft.Management.Infrastructure.Serialization)
ms:assetid: M:Microsoft.Management.Infrastructure.Serialization.CimMofDeserializer.DeserializeInstances(System.Byte[],System.UInt32@,System.Collections.Generic.IEnumerable{Microsoft.Management.Infrastructure.CimClass},Microsoft.Management.Infrastructure.Serialization.CimMofDeserializer.OnClassNeeded,Microsoft.Management.Infrastructure.Serialization.CimMofDeserializer.GetIncludedFileContent)
ms.date: 11/14/2019
mtps_version: v=VS.85
dev_langs:
- csharp
- c++
- fsharp
- vb
api_location:
- Microsoft.Management.Infrastructure.dll
api_name:
- Microsoft.Management.Infrastructure.Serialization.CimMofDeserializer.DeserializeInstances
api_type:
- Assembly
topic_type:
- apiref
product_family_name: VS
ms.topic: reference
ms.openlocfilehash: 081c6d028abdb341d75ff57758c703458fd0b62c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106305580"
---
# <a name="cimmofdeserializerdeserializeinstances-method-byteuint32ienumerablecimclass-onclassneeded-getincludedfilecontent"></a><span data-ttu-id="eb07f-103">Metodo CimMofDeserializer. DeserializeInstances (byte \[ \] , UInt32, IEnumerable \<CimClass\> , OnClassNeeded, GetIncludedFileContent)</span><span class="sxs-lookup"><span data-stu-id="eb07f-103">CimMofDeserializer.DeserializeInstances method (Byte\[\], UInt32, IEnumerable\<CimClass\>, OnClassNeeded, GetIncludedFileContent)</span></span>

<span data-ttu-id="eb07f-104">Deserializza le istanze CIM in base ai dati serializzati, una raccolta di classi CIM padre e callback.</span><span class="sxs-lookup"><span data-stu-id="eb07f-104">Deserializes CIM instances based on serialized data, a collection of parent CIM classes, and callbacks.</span></span>

<span data-ttu-id="eb07f-105">**Spazio dei nomi:**   [Microsoft. Management. Infrastructure. Serialization](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832966(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="eb07f-105">**Namespace:**   [Microsoft.Management.Infrastructure.Serialization](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832966(v=vs.85))</span></span>  
<span data-ttu-id="eb07f-106">**Assembly:**  Microsoft. Management. Infrastructure (in Microsoft.Management.Infrastructure.dll)</span><span class="sxs-lookup"><span data-stu-id="eb07f-106">**Assembly:**  Microsoft.Management.Infrastructure (in Microsoft.Management.Infrastructure.dll)</span></span>  

## <a name="syntax"></a><span data-ttu-id="eb07f-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="eb07f-107">Syntax</span></span>

``` csharp
public IEnumerable<CimInstance> DeserializeInstances(
    byte[] serializedData,
    ref uint offset,
    IEnumerable<CimClass> cimClasses,
    OnClassNeeded onClassNeededCallback,
    GetIncludedFileContent getIncludedFileCallback
)
```

``` c++
public:
IEnumerable<CimInstance^>^ DeserializeInstances(
    array<unsigned char>^ serializedData,
    unsigned int% offset,
    IEnumerable<CimClass^>^ cimClasses,
    OnClassNeeded^ onClassNeededCallback,
    GetIncludedFileContent^ getIncludedFileCallback
)
```

``` fsharp
member DeserializeInstances : 
        serializedData:byte[] *
        offset:uint32 byref *
        cimClasses:IEnumerable<CimClass> *
        onClassNeededCallback:OnClassNeeded *
        getIncludedFileCallback:GetIncludedFileContent -> IEnumerable<CimInstance>
```

``` vb
Public Function DeserializeInstances (
    serializedData As Byte(),
    ByRef offset As UInteger,
    cimClasses As IEnumerable(Of CimClass),
    onClassNeededCallback As OnClassNeeded,
    getIncludedFileCallback As GetIncludedFileContent
) As IEnumerable(CimInstance)
```

#### <a name="parameters"></a><span data-ttu-id="eb07f-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="eb07f-108">Parameters</span></span>

  - <span data-ttu-id="eb07f-109">serializedData</span><span class="sxs-lookup"><span data-stu-id="eb07f-109">serializedData</span></span>  
    <span data-ttu-id="eb07f-110">Tipo: [System. byte](/dotnet/api/system.byte?view=netframework-4.8)\[\]</span><span class="sxs-lookup"><span data-stu-id="eb07f-110">Type: [System.Byte](/dotnet/api/system.byte?view=netframework-4.8)\[\]</span></span>
    
    <span data-ttu-id="eb07f-111">Buffer che contiene i dati serializzati.</span><span class="sxs-lookup"><span data-stu-id="eb07f-111">A buffer that contains the serialized data.</span></span>

<!-- end list -->

  - <span data-ttu-id="eb07f-112">offset</span><span class="sxs-lookup"><span data-stu-id="eb07f-112">offset</span></span>  
    <span data-ttu-id="eb07f-113">Tipo: [System. UInt32](/dotnet/api/system.uint32?view=netframework-4.8)</span><span class="sxs-lookup"><span data-stu-id="eb07f-113">Type: [System.UInt32](/dotnet/api/system.uint32?view=netframework-4.8)</span></span>
    
    <span data-ttu-id="eb07f-114">Offset dei byte nella posizione da cui iniziare la lettura dei dati.</span><span class="sxs-lookup"><span data-stu-id="eb07f-114">The byte offset to the location at which to begin reading the data.</span></span> <span data-ttu-id="eb07f-115">Quando il metodo restituisce un risultato, l'offset verrà puntato al byte successivo dopo le istanze deserializzate.</span><span class="sxs-lookup"><span data-stu-id="eb07f-115">When the method returns, the offset will be pointing to the next byte after the deserialized instances.</span></span>

<!-- end list -->

  - <span data-ttu-id="eb07f-116">cimClasses</span><span class="sxs-lookup"><span data-stu-id="eb07f-116">cimClasses</span></span>  
    <span data-ttu-id="eb07f-117">Tipo: [System. Collections. Generic. IEnumerable](/dotnet/api/system.collections.generic.ienumerable-1?view=netframework-4.8)\<[CimClass](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832269(v=vs.85))\></span><span class="sxs-lookup"><span data-stu-id="eb07f-117">Type: [System.Collections.Generic.IEnumerable](/dotnet/api/system.collections.generic.ienumerable-1?view=netframework-4.8)\<[CimClass](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832269(v=vs.85))\></span></span>
    
    <span data-ttu-id="eb07f-118">Cache facoltativa delle classi CIM padre.</span><span class="sxs-lookup"><span data-stu-id="eb07f-118">An optional cache of parent CIM classes.</span></span>

<!-- end list -->

  - <span data-ttu-id="eb07f-119">onClassNeededCallback</span><span class="sxs-lookup"><span data-stu-id="eb07f-119">onClassNeededCallback</span></span>  
    <span data-ttu-id="eb07f-120">Tipo: [OnClassNeeded](microsoft.management.infrastructure.serialization.cimmofdeserializer.onclassneeded.md)</span><span class="sxs-lookup"><span data-stu-id="eb07f-120">Type: [OnClassNeeded](microsoft.management.infrastructure.serialization.cimmofdeserializer.onclassneeded.md)</span></span>
    
    <span data-ttu-id="eb07f-121">Funzione di callback utilizzata per fornire un oggetto classe richiesto durante la deserializzazione.</span><span class="sxs-lookup"><span data-stu-id="eb07f-121">A callback function used to provide a requested class object during deserialization.</span></span>

<!-- end list -->

  - <span data-ttu-id="eb07f-122">getIncludedFileCallback</span><span class="sxs-lookup"><span data-stu-id="eb07f-122">getIncludedFileCallback</span></span>  
    <span data-ttu-id="eb07f-123">Tipo: [GetIncludedFileContent](microsoft.management.infrastructure.serialization.cimmofdeserializer.getincludedfilecontent.md)</span><span class="sxs-lookup"><span data-stu-id="eb07f-123">Type: [GetIncludedFileContent](microsoft.management.infrastructure.serialization.cimmofdeserializer.getincludedfilecontent.md)</span></span>
    
    <span data-ttu-id="eb07f-124">Funzione di callback utilizzata per fornire il contenuto del buffer di file di un file specificato.</span><span class="sxs-lookup"><span data-stu-id="eb07f-124">A callback function used to provide the file buffer contents of a specified file.</span></span>

#### <a name="return-value"></a><span data-ttu-id="eb07f-125">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="eb07f-125">Return value</span></span>

<span data-ttu-id="eb07f-126">Tipo: [System. Collections. Generic. IEnumerable](/dotnet/api/system.collections.generic.ienumerable-1?view=netframework-4.8)\<[CimInstance](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832336(v=vs.85))\></span><span class="sxs-lookup"><span data-stu-id="eb07f-126">Type: [System.Collections.Generic.IEnumerable](/dotnet/api/system.collections.generic.ienumerable-1?view=netframework-4.8)\<[CimInstance](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832336(v=vs.85))\></span></span>

<span data-ttu-id="eb07f-127">Interfaccia [IEnumerable \<T\> ](/dotnet/api/system.collections.generic.ienumerable-1?view=netframework-4.8) che può essere utilizzata per enumerare le classi CIM.</span><span class="sxs-lookup"><span data-stu-id="eb07f-127">An [IEnumerable\<T\>](/dotnet/api/system.collections.generic.ienumerable-1?view=netframework-4.8) interface that can be used to enumerate the CIM classes.</span></span>

## <a name="see-also"></a><span data-ttu-id="eb07f-128">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="eb07f-128">See also</span></span>

<span data-ttu-id="eb07f-129">[Classe CimInstance](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832336(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="eb07f-129">[CimInstance class](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832336(v=vs.85))</span></span>  
<span data-ttu-id="eb07f-130">[Spazio dei nomi Microsoft. Management. Infrastructure. Serialization](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832966(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="eb07f-130">[Microsoft.Management.Infrastructure.Serialization namespace](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832966(v=vs.85))</span></span>
