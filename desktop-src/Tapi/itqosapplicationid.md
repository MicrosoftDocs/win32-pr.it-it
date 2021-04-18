---
description: L'interfaccia ITQOSApplicationID espone un metodo che consente a un'applicazione di ottenere l'identificatore QOS per la chiamata corrente.
ms.assetid: 1df50b3a-bd16-4e9b-afca-b025bfe537a4
title: Interfaccia ITQOSApplicationID (Ipmsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 23df8da80798cc52ecd73b4f29288812f3774d9f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106333658"
---
# <a name="itqosapplicationid-interface"></a><span data-ttu-id="02525-103">Interfaccia ITQOSApplicationID</span><span class="sxs-lookup"><span data-stu-id="02525-103">ITQOSApplicationID interface</span></span>

<span data-ttu-id="02525-104">\[ Questa interfaccia non è disponibile per l'utilizzo in Windows Vista, Windows Server 2008 e nelle versioni successive del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="02525-104">\[ This interface is not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="02525-105">L'API del client RTC fornisce funzionalità simili.\]</span><span class="sxs-lookup"><span data-stu-id="02525-105">The RTC Client API provides similar functionality.\]</span></span>

<span data-ttu-id="02525-106">L'interfaccia **ITQOSApplicationID** espone un metodo che consente a un'applicazione di ottenere l'identificatore QoS per la chiamata corrente.</span><span class="sxs-lookup"><span data-stu-id="02525-106">The **ITQOSApplicationID** interface exposes a method that allows an application to get the QOS identifier for the current call.</span></span>

<span data-ttu-id="02525-107">Questa interfaccia viene implementata da [IPConf msp](ipconf-msp.md) ed è esposta solo quando una chiamata utilizza la conferenza IP.</span><span class="sxs-lookup"><span data-stu-id="02525-107">This interface is implemented by the [IPConf MSP](ipconf-msp.md) and is exposed only when a call uses IP Conferencing.</span></span>

## <a name="members"></a><span data-ttu-id="02525-108">Membri</span><span class="sxs-lookup"><span data-stu-id="02525-108">Members</span></span>

<span data-ttu-id="02525-109">L'interfaccia **ITQOSApplicationID** eredita dall'interfaccia [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) .</span><span class="sxs-lookup"><span data-stu-id="02525-109">The **ITQOSApplicationID** interface inherits from the [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) interface.</span></span> <span data-ttu-id="02525-110">**ITQOSApplicationID** dispone anche di questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="02525-110">**ITQOSApplicationID** also has these types of members:</span></span>

-   [<span data-ttu-id="02525-111">Metodi</span><span class="sxs-lookup"><span data-stu-id="02525-111">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="02525-112">Metodi</span><span class="sxs-lookup"><span data-stu-id="02525-112">Methods</span></span>

<span data-ttu-id="02525-113">L'interfaccia **ITQOSApplicationID** dispone di questi metodi.</span><span class="sxs-lookup"><span data-stu-id="02525-113">The **ITQOSApplicationID** interface has these methods.</span></span>



| <span data-ttu-id="02525-114">Metodo</span><span class="sxs-lookup"><span data-stu-id="02525-114">Method</span></span>                                                                | <span data-ttu-id="02525-115">Descrizione</span><span class="sxs-lookup"><span data-stu-id="02525-115">Description</span></span>                         |
|:----------------------------------------------------------------------|:------------------------------------|
| [<span data-ttu-id="02525-116">**SetQOSApplicationID**</span><span class="sxs-lookup"><span data-stu-id="02525-116">**SetQOSApplicationID**</span></span>](itqosapplicationid-setqosapplicationid.md) | <span data-ttu-id="02525-117">Imposta l'identificatore QOS.</span><span class="sxs-lookup"><span data-stu-id="02525-117">Sets the QOS identifier.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="02525-118">Requisiti</span><span class="sxs-lookup"><span data-stu-id="02525-118">Requirements</span></span>



| <span data-ttu-id="02525-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="02525-119">Requirement</span></span> | <span data-ttu-id="02525-120">Valore</span><span class="sxs-lookup"><span data-stu-id="02525-120">Value</span></span> |
|-------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="02525-121">Versione TAPI</span><span class="sxs-lookup"><span data-stu-id="02525-121">TAPI version</span></span><br/> | <span data-ttu-id="02525-122">Richiede TAPI 3,1</span><span class="sxs-lookup"><span data-stu-id="02525-122">Requires TAPI 3.1</span></span><br/>                                                         |
| <span data-ttu-id="02525-123">Intestazione</span><span class="sxs-lookup"><span data-stu-id="02525-123">Header</span></span><br/>       | <dl> <span data-ttu-id="02525-124"><dt>Ipmsp. h</dt></span><span class="sxs-lookup"><span data-stu-id="02525-124"><dt>Ipmsp.h</dt></span></span> </dl>   |
| <span data-ttu-id="02525-125">Libreria</span><span class="sxs-lookup"><span data-stu-id="02525-125">Library</span></span><br/>      | <dl> <span data-ttu-id="02525-126"><dt>UUID. lib</dt></span><span class="sxs-lookup"><span data-stu-id="02525-126"><dt>Uuid.lib</dt></span></span> </dl>  |
| <span data-ttu-id="02525-127">DLL</span><span class="sxs-lookup"><span data-stu-id="02525-127">DLL</span></span><br/>          | <dl> <span data-ttu-id="02525-128"><dt>Tapi3.dll</dt></span><span class="sxs-lookup"><span data-stu-id="02525-128"><dt>Tapi3.dll</dt></span></span> </dl> |



 

