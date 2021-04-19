---
description: Dispositivi portatili Windows (WPD) supporta le seguenti proprietà dei parametri del comando.
ms.assetid: 03eff101-5c36-48ea-9dcd-2c4ee29a2ac6
title: Parametri del comando (PortableDevice. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Command
api_type:
- HeaderDef
api_location:
- PortableDevice.h
ms.openlocfilehash: 7687488c38f95fd6d7e7b69d64ad6ae32631700d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106330248"
---
# <a name="command-parameters"></a><span data-ttu-id="9ca69-103">Parametri dei comandi</span><span class="sxs-lookup"><span data-stu-id="9ca69-103">Command Parameters</span></span>

<span data-ttu-id="9ca69-104">Dispositivi portatili Windows (WPD) supporta le seguenti proprietà dei parametri del comando.</span><span class="sxs-lookup"><span data-stu-id="9ca69-104">Windows Portable Devices (WPD) supports the following properties of command parameters.</span></span>




| <span data-ttu-id="9ca69-105">**Proprietà**</span><span class="sxs-lookup"><span data-stu-id="9ca69-105">**Property**</span></span>                                            | <span data-ttu-id="9ca69-106">**VarType**</span><span class="sxs-lookup"><span data-stu-id="9ca69-106">**VarType**</span></span>     | <span data-ttu-id="9ca69-107">**Descrizione**</span><span class="sxs-lookup"><span data-stu-id="9ca69-107">**Description**</span></span>                                                                                                                                                              |
|---------------------------------------------------------|-----------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9ca69-108">**\_Proprietà WPD \_ \_ informazioni client \_ comuni**</span><span class="sxs-lookup"><span data-stu-id="9ca69-108">**WPD\_PROPERTY\_COMMON\_CLIENT\_INFORMATION**</span></span>          | <span data-ttu-id="9ca69-109">**VT \_ sconosciuto**</span><span class="sxs-lookup"><span data-stu-id="9ca69-109">**VT\_UNKNOWN**</span></span> | <span data-ttu-id="9ca69-110">Interfaccia [**IPortableDeviceValues**](iportabledevicevalues.md) utilizzata dal driver per identificare il client.</span><span class="sxs-lookup"><span data-stu-id="9ca69-110">An [**IPortableDeviceValues**](iportabledevicevalues.md) interface that the driver uses to identify the client.</span></span>                                                             |
| <span data-ttu-id="9ca69-111">**\_Proprietà WPD \_ \_ \_ contesto delle informazioni client comuni \_**</span><span class="sxs-lookup"><span data-stu-id="9ca69-111">**WPD\_PROPERTY\_COMMON\_CLIENT\_INFORMATION\_CONTEXT**</span></span> | <span data-ttu-id="9ca69-112">**\_LPWSTR VT**</span><span class="sxs-lookup"><span data-stu-id="9ca69-112">**VT\_LPWSTR**</span></span>  | <span data-ttu-id="9ca69-113">Contesto specificato dal driver che identifica un client per tutte le operazioni successive.</span><span class="sxs-lookup"><span data-stu-id="9ca69-113">A driver-specified context which identifies a client for all subsequent operations.</span></span>                                                                                          |
| <span data-ttu-id="9ca69-114">**\_categoria di \_ \_ comandi comune della proprietà \_ WPD**</span><span class="sxs-lookup"><span data-stu-id="9ca69-114">**WPD\_PROPERTY\_COMMON\_COMMAND\_CATEGORY**</span></span>            | <span data-ttu-id="9ca69-115">**\_CLSID VT**</span><span class="sxs-lookup"><span data-stu-id="9ca69-115">**VT\_CLSID**</span></span>   | <span data-ttu-id="9ca69-116">Parte del **GUID** del valore **PropertyKey** del comando.</span><span class="sxs-lookup"><span data-stu-id="9ca69-116">The **GUID** portion of the **PROPERTYKEY** value of the command.</span></span>                                                                                                            |
| <span data-ttu-id="9ca69-117">**\_ \_ \_ ID comando comune della proprietà WPD \_**</span><span class="sxs-lookup"><span data-stu-id="9ca69-117">**WPD\_PROPERTY\_COMMON\_COMMAND\_ID**</span></span>                  | <span data-ttu-id="9ca69-118">**\_UI4 VT**</span><span class="sxs-lookup"><span data-stu-id="9ca69-118">**VT\_UI4**</span></span>     | <span data-ttu-id="9ca69-119">Porzione di ID univoco permanente (PID) del valore **PropertyKey** del comando.</span><span class="sxs-lookup"><span data-stu-id="9ca69-119">The Persistent Unique ID (PID) portion of the **PROPERTYKEY** value of the command.</span></span>                                                                                          |
| <span data-ttu-id="9ca69-120">**\_ \_ \_ destinazione comando comune della proprietà WPD \_**</span><span class="sxs-lookup"><span data-stu-id="9ca69-120">**WPD\_PROPERTY\_COMMON\_COMMAND\_TARGET**</span></span>              | <span data-ttu-id="9ca69-121">**\_LPWSTR VT**</span><span class="sxs-lookup"><span data-stu-id="9ca69-121">**VT\_LPWSTR**</span></span>  | <span data-ttu-id="9ca69-122">Identificatore dell'oggetto di destinazione.</span><span class="sxs-lookup"><span data-stu-id="9ca69-122">The target-object identifier.</span></span>                                                                                                                                                |
| <span data-ttu-id="9ca69-123">**\_codice di \_ \_ errore del driver comune della proprietà \_ WPD \_**</span><span class="sxs-lookup"><span data-stu-id="9ca69-123">**WPD\_PROPERTY\_COMMON\_DRIVER\_ERROR\_CODE**</span></span>          | <span data-ttu-id="9ca69-124">**\_UI4 VT**</span><span class="sxs-lookup"><span data-stu-id="9ca69-124">**VT\_UI4**</span></span>     | <span data-ttu-id="9ca69-125">Codice di errore specifico del driver restituito da un driver WPD.</span><span class="sxs-lookup"><span data-stu-id="9ca69-125">A driver-specific error code returned by a WPD driver.</span></span>                                                                                                                       |
| <span data-ttu-id="9ca69-126">**\_ \_ HRESULT comune della proprietà WPD \_**</span><span class="sxs-lookup"><span data-stu-id="9ca69-126">**WPD\_PROPERTY\_COMMON\_HRESULT**</span></span>                      | <span data-ttu-id="9ca69-127">**\_errore VT**</span><span class="sxs-lookup"><span data-stu-id="9ca69-127">**VT\_ERROR**</span></span>   | <span data-ttu-id="9ca69-128">Valore **HRESULT** restituito da un driver WPD per un'operazione specifica.</span><span class="sxs-lookup"><span data-stu-id="9ca69-128">The **HRESULT** value returned by a WPD driver for a particular operation.</span></span>                                                                                                   |
| <span data-ttu-id="9ca69-129">**\_ \_ \_ ID oggetto comuni della proprietà WPD \_**</span><span class="sxs-lookup"><span data-stu-id="9ca69-129">**WPD\_PROPERTY\_COMMON\_OBJECT\_IDS**</span></span>                  | <span data-ttu-id="9ca69-130">**VT \_ sconosciuto**</span><span class="sxs-lookup"><span data-stu-id="9ca69-130">**VT\_UNKNOWN**</span></span> | <span data-ttu-id="9ca69-131">Interfaccia [**IPortableDevicePropVariantCollection**](iportabledevicepropvariantcollection.md) di tipo Variant **VT \_ LPWSTR** che contiene un elenco di identificatori di oggetto.</span><span class="sxs-lookup"><span data-stu-id="9ca69-131">An [**IPortableDevicePropVariantCollection**](iportabledevicepropvariantcollection.md) interface of variant type **VT\_LPWSTR** that contains a list of object identifiers.</span></span> |
| <span data-ttu-id="9ca69-132">**\_Proprietà WPD \_ gli \_ \_ ID univoci permanenti comuni \_**</span><span class="sxs-lookup"><span data-stu-id="9ca69-132">**WPD\_PROPERTY\_COMMON\_PERSISTENT\_UNIQUE\_IDS**</span></span>      | <span data-ttu-id="9ca69-133">**VT \_ sconosciuto**</span><span class="sxs-lookup"><span data-stu-id="9ca69-133">**VT\_UNKNOWN**</span></span> | <span data-ttu-id="9ca69-134">Interfaccia [**IPortableDevicePropVariantCollection**](iportabledevicepropvariantcollection.md) di tipo Variant **VT \_ LPWSTR** che contiene un elenco di PID.</span><span class="sxs-lookup"><span data-stu-id="9ca69-134">An [**IPortableDevicePropVariantCollection**](iportabledevicepropvariantcollection.md) interface of variant type **VT\_LPWSTR** that contains a list of PIDs.</span></span>               |



 

## <a name="requirements"></a><span data-ttu-id="9ca69-135">Requisiti</span><span class="sxs-lookup"><span data-stu-id="9ca69-135">Requirements</span></span>



| <span data-ttu-id="9ca69-136">Requisito</span><span class="sxs-lookup"><span data-stu-id="9ca69-136">Requirement</span></span> | <span data-ttu-id="9ca69-137">Valore</span><span class="sxs-lookup"><span data-stu-id="9ca69-137">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="9ca69-138">Intestazione</span><span class="sxs-lookup"><span data-stu-id="9ca69-138">Header</span></span><br/> | <dl> <span data-ttu-id="9ca69-139"><dt>PortableDevice. h</dt></span><span class="sxs-lookup"><span data-stu-id="9ca69-139"><dt>PortableDevice.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9ca69-140">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="9ca69-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9ca69-141">**Proprietà e attributi**</span><span class="sxs-lookup"><span data-stu-id="9ca69-141">**Properties and Attributes**</span></span>](properties-and-attributes.md)
</dt> </dl>

 

 




