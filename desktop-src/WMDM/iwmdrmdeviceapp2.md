---
title: Interfaccia IWMDRMDeviceApp2
description: L'interfaccia IWMDRMDeviceApp2 estende IWMDRMDeviceApp fornendo una nuova versione del metodo QueryDeviceStatus.
ms.assetid: a7e28d5a-041f-4102-97db-0c77ca146e26
keywords:
- Interfaccia IWMDRMDeviceApp2 Windows Media Gestione dispositivi
- Interfaccia IWMDRMDeviceApp2 Windows Media Gestione dispositivi, descritta
topic_type:
- apiref
api_name:
- IWMDRMDeviceApp2
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: df4bfdb023198631b16ffa0e511488fa52423c5e
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/25/2019
ms.locfileid: "104334807"
---
# <a name="iwmdrmdeviceapp2-interface"></a><span data-ttu-id="90b57-105">Interfaccia IWMDRMDeviceApp2</span><span class="sxs-lookup"><span data-stu-id="90b57-105">IWMDRMDeviceApp2 interface</span></span>

<span data-ttu-id="90b57-106">L'interfaccia **IWMDRMDeviceApp2** estende [**IWMDRMDeviceApp**](iwmdrmdeviceapp.md) fornendo una nuova versione del metodo [**QueryDeviceStatus**](iwmdrmdeviceapp-querydevicestatus.md) .</span><span class="sxs-lookup"><span data-stu-id="90b57-106">The **IWMDRMDeviceApp2** interface extends [**IWMDRMDeviceApp**](iwmdrmdeviceapp.md) by providing a new version of the [**QueryDeviceStatus**](iwmdrmdeviceapp-querydevicestatus.md) method.</span></span> <span data-ttu-id="90b57-107">**QueryDeviceStatus2** consente al chiamante di eseguire una query per un requisito DRM specifico.</span><span class="sxs-lookup"><span data-stu-id="90b57-107">**QueryDeviceStatus2** enables the caller to query for a specific DRM requirement.</span></span>

<span data-ttu-id="90b57-108">Per ottenere questa interfaccia, chiamare **CoCreateInstance** e passare il CLSID \_ WMDRMDeviceApp.</span><span class="sxs-lookup"><span data-stu-id="90b57-108">To get this interface, call **CoCreateInstance** and pass in CLSID\_WMDRMDeviceApp.</span></span>

> [!Note]  
> <span data-ttu-id="90b57-109">Questa interfaccia viene definita nel file di intestazione compilato da WMDRMDeviceApp. idl.</span><span class="sxs-lookup"><span data-stu-id="90b57-109">This interface is defined in the header file built from WMDRMDeviceApp.idl.</span></span> <span data-ttu-id="90b57-110">Questa intestazione **\# include** "WMDM. h".</span><span class="sxs-lookup"><span data-stu-id="90b57-110">This header **\#includes** "wmdm.h".</span></span> <span data-ttu-id="90b57-111">Potrebbe essere necessario modificare il nome del file in modo che corrisponda all'intestazione compilata da WMDM. idl.</span><span class="sxs-lookup"><span data-stu-id="90b57-111">You might need to change this file name to match the header built from WMDM.idl.</span></span>

 

## <a name="members"></a><span data-ttu-id="90b57-112">Membri</span><span class="sxs-lookup"><span data-stu-id="90b57-112">Members</span></span>

<span data-ttu-id="90b57-113">L'interfaccia **IWMDRMDeviceApp2** eredita da [**IWMDRMDeviceApp**](iwmdrmdeviceapp.md).</span><span class="sxs-lookup"><span data-stu-id="90b57-113">The **IWMDRMDeviceApp2** interface inherits from [**IWMDRMDeviceApp**](iwmdrmdeviceapp.md).</span></span> <span data-ttu-id="90b57-114">**IWMDRMDeviceApp2** dispone anche di questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="90b57-114">**IWMDRMDeviceApp2** also has these types of members:</span></span>

-   [<span data-ttu-id="90b57-115">Metodi</span><span class="sxs-lookup"><span data-stu-id="90b57-115">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="90b57-116">Metodi</span><span class="sxs-lookup"><span data-stu-id="90b57-116">Methods</span></span>

<span data-ttu-id="90b57-117">L'interfaccia **IWMDRMDeviceApp2** dispone di questi metodi.</span><span class="sxs-lookup"><span data-stu-id="90b57-117">The **IWMDRMDeviceApp2** interface has these methods.</span></span>



| <span data-ttu-id="90b57-118">Metodo</span><span class="sxs-lookup"><span data-stu-id="90b57-118">Method</span></span>                                                            | <span data-ttu-id="90b57-119">Descrizione</span><span class="sxs-lookup"><span data-stu-id="90b57-119">Description</span></span>                                                          |
|:------------------------------------------------------------------|:---------------------------------------------------------------------|
| [<span data-ttu-id="90b57-120">**QueryDeviceStatus2**</span><span class="sxs-lookup"><span data-stu-id="90b57-120">**QueryDeviceStatus2**</span></span>](iwmdrmdeviceapp2-querydevicestatus2.md) | <span data-ttu-id="90b57-121">Esegue una query su un dispositivo per uno stato o una funzionalità DRM specifica.</span><span class="sxs-lookup"><span data-stu-id="90b57-121">Queries a device for a specific DRM status or capability.</span></span><br/> |



 

## <a name="see-also"></a><span data-ttu-id="90b57-122">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="90b57-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="90b57-123">**IWMDRMDeviceApp**</span><span class="sxs-lookup"><span data-stu-id="90b57-123">**IWMDRMDeviceApp**</span></span>](iwmdrmdeviceapp.md)
</dt> <dt>

[<span data-ttu-id="90b57-124">**Gestione del contenuto protetto nell'applicazione**</span><span class="sxs-lookup"><span data-stu-id="90b57-124">**Handling Protected Content in the Application**</span></span>](handling-protected-content-in-the-application.md)
</dt> <dt>

[<span data-ttu-id="90b57-125">**Interfacce per le applicazioni**</span><span class="sxs-lookup"><span data-stu-id="90b57-125">**Interfaces for Applications**</span></span>](interfaces-for-applications.md)
</dt> <dt>

[<span data-ttu-id="90b57-126">**Misurazione dell'utilizzo del contenuto**</span><span class="sxs-lookup"><span data-stu-id="90b57-126">**Metering Content Usage**</span></span>](metering-content-usage.md)
</dt> </dl>

 

 





