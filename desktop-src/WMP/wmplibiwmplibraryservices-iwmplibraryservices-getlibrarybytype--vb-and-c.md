---
title: Metodo IWMPLibraryServices getLibraryByType
description: Il metodo getLibraryByType restituisce un'interfaccia IWMPLibrary che rappresenta la libreria con il tipo e l'indice specificati.
ms.assetid: 2507c764-a2cf-42f9-ad44-eaf040b78891
keywords:
- Metodo getLibraryByType Windows Media Player
- Metodo getLibraryByType Windows Media Player, interfaccia IWMPLibraryServices
- Interfaccia IWMPLibraryServices Windows Media Player, metodo getLibraryByType
topic_type:
- apiref
api_name:
- IWMPLibraryServices.getLibraryByType
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4d57fcc71f912fe1ee896ec893ea8f556eeb2277
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106332411"
---
# <a name="iwmplibraryservicesgetlibrarybytype-method"></a><span data-ttu-id="e2572-106">Metodo IWMPLibraryServices:: getLibraryByType</span><span class="sxs-lookup"><span data-stu-id="e2572-106">IWMPLibraryServices::getLibraryByType method</span></span>

<span data-ttu-id="e2572-107">Il metodo **getLibraryByType** restituisce un'interfaccia **IWMPLibrary** che rappresenta la libreria con il tipo e l'indice specificati.</span><span class="sxs-lookup"><span data-stu-id="e2572-107">The **getLibraryByType** method returns an **IWMPLibrary** interface that represents the library that has the specified type and index.</span></span>

## <a name="syntax"></a><span data-ttu-id="e2572-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="e2572-108">Syntax</span></span>


```CSharp
public IWMPLibrary getLibraryByType(
  WMPLibraryType wmplt,
  System.Int32 lIndex
);
```


```VB

Public Function getLibraryByType( _
  ByVal wmplt As WMPLibraryType, _
  ByVal lIndex As System.Int32 _
) As IWMPLibrary
Implements IWMPLibraryServices.getLibraryByType
```





## <a name="parameters"></a><span data-ttu-id="e2572-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="e2572-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e2572-110">*wmplt* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="e2572-110">*wmplt* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e2572-111">Valore dell'enumerazione **wmplib. WMPLibraryType** che specifica il tipo di libreria da recuperare.</span><span class="sxs-lookup"><span data-stu-id="e2572-111">A value from the **WMPLib.WMPLibraryType** enumeration that specifies the type of library to retrieve.</span></span>

</dd> <dt>

<span data-ttu-id="e2572-112">*lIndex* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="e2572-112">*lIndex* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e2572-113">**System. Int32** che rappresenta l'indice della libreria da recuperare.</span><span class="sxs-lookup"><span data-stu-id="e2572-113">A **System.Int32** that is the index of the library to retrieve.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e2572-114">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="e2572-114">Return value</span></span>

<span data-ttu-id="e2572-115">Interfaccia **wmplib. IWMPLibrary** per la libreria restituita.</span><span class="sxs-lookup"><span data-stu-id="e2572-115">A **WMPLib.IWMPLibrary** interface for the library that is returned.</span></span>

## <a name="remarks"></a><span data-ttu-id="e2572-116">Commenti</span><span class="sxs-lookup"><span data-stu-id="e2572-116">Remarks</span></span>

<span data-ttu-id="e2572-117">Esiste una sola libreria locale e le librerie di dischi sono disponibili solo sui CD di dati e i DVD che contengono contenuto multimediale.</span><span class="sxs-lookup"><span data-stu-id="e2572-117">There is only one local library, and disc libraries are available only on data CDs and DVDs that contain media content.</span></span>

## <a name="requirements"></a><span data-ttu-id="e2572-118">Requisiti</span><span class="sxs-lookup"><span data-stu-id="e2572-118">Requirements</span></span>



| <span data-ttu-id="e2572-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="e2572-119">Requirement</span></span> | <span data-ttu-id="e2572-120">Valore</span><span class="sxs-lookup"><span data-stu-id="e2572-120">Value</span></span> |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e2572-121">Versione</span><span class="sxs-lookup"><span data-stu-id="e2572-121">Version</span></span><br/>   | <span data-ttu-id="e2572-122">Windows Media Player 11.</span><span class="sxs-lookup"><span data-stu-id="e2572-122">Windows Media Player 11.</span></span><br/>                                                                                    |
| <span data-ttu-id="e2572-123">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="e2572-123">Namespace</span></span><br/> | <span data-ttu-id="e2572-124">**WMPLib**</span><span class="sxs-lookup"><span data-stu-id="e2572-124">**WMPLib**</span></span><br/>                                                                                                  |
| <span data-ttu-id="e2572-125">Assembly</span><span class="sxs-lookup"><span data-stu-id="e2572-125">Assembly</span></span><br/>  | <dl> <span data-ttu-id="e2572-126"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="e2572-126"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e2572-127">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="e2572-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e2572-128">**Interfaccia IWMPLibrary (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="e2572-128">**IWMPLibrary Interface (VB and C#)**</span></span>](iwmplibrary--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="e2572-129">**Interfaccia IWMPLibraryServices (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="e2572-129">**IWMPLibraryServices Interface (VB and C#)**</span></span>](iwmplibraryservices--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="e2572-130">**WMPLibraryType**</span><span class="sxs-lookup"><span data-stu-id="e2572-130">**WMPLibraryType**</span></span>](/previous-versions/windows/desktop/api/wmp/ne-wmp-wmplibrarytype)
</dt> </dl>

 

 





