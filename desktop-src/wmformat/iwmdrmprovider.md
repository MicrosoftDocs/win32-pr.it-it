---
title: Interfaccia IWMDRMProvider
description: L'interfaccia IWMDRMProvider fornisce un metodo per la creazione degli altri oggetti delle API estese del client DRM di Microsoft Windows Media. è possibile ottenere un puntatore a un'istanza di questa interfaccia chiamando la funzione WMDRMCreateProvider.
ms.assetid: bcd346e3-a79f-49a8-b5f9-b9ae8b54527a
keywords:
- Formato Windows Media Interface IWMDRMProvider
- Interfaccia IWMDRMProvider-formato Windows Media, descritto
topic_type:
- apiref
api_name:
- IWMDRMProvider
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 9653bc612cdbc865d8e77cb7916b0b8f54d0fd0e
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "103729215"
---
# <a name="iwmdrmprovider-interface"></a><span data-ttu-id="c0601-105">Interfaccia IWMDRMProvider</span><span class="sxs-lookup"><span data-stu-id="c0601-105">IWMDRMProvider interface</span></span>

<span data-ttu-id="c0601-106">L'interfaccia **IWMDRMProvider** fornisce un metodo per la creazione degli altri oggetti delle API estese del client DRM di Microsoft Windows Media.</span><span class="sxs-lookup"><span data-stu-id="c0601-106">The **IWMDRMProvider** interface provides a method that creates the other objects of the Microsoft Windows Media DRM Client Extended APIs.</span></span>

<span data-ttu-id="c0601-107">È possibile ottenere un puntatore a un'istanza di questa interfaccia chiamando la funzione [**WMDRMCreateProvider**](wmdrmcreateprovider.md) .</span><span class="sxs-lookup"><span data-stu-id="c0601-107">You can obtain a pointer to an instance of this interface by calling the [**WMDRMCreateProvider**](wmdrmcreateprovider.md) function.</span></span> <span data-ttu-id="c0601-108">Per ottenere un puntatore a un'istanza di questa interfaccia in grado di creare oggetti protetti, è necessario chiamare la funzione [**WMDRMCreateProtectedProvider**](wmdrmcreateprotectedprovider.md) .</span><span class="sxs-lookup"><span data-stu-id="c0601-108">To obtain a pointer to an instance of this interface that can create secure objects, you must call the [**WMDRMCreateProtectedProvider**](wmdrmcreateprotectedprovider.md) function.</span></span>

## <a name="members"></a><span data-ttu-id="c0601-109">Membri</span><span class="sxs-lookup"><span data-stu-id="c0601-109">Members</span></span>

<span data-ttu-id="c0601-110">L'interfaccia **IWMDRMProvider** eredita dall'interfaccia [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="c0601-110">The **IWMDRMProvider** interface inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="c0601-111">**IWMDRMProvider** dispone anche di questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="c0601-111">**IWMDRMProvider** also has these types of members:</span></span>

-   [<span data-ttu-id="c0601-112">Metodi</span><span class="sxs-lookup"><span data-stu-id="c0601-112">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="c0601-113">Metodi</span><span class="sxs-lookup"><span data-stu-id="c0601-113">Methods</span></span>

<span data-ttu-id="c0601-114">L'interfaccia **IWMDRMProvider** dispone di questi metodi.</span><span class="sxs-lookup"><span data-stu-id="c0601-114">The **IWMDRMProvider** interface has these methods.</span></span>



| <span data-ttu-id="c0601-115">Metodo</span><span class="sxs-lookup"><span data-stu-id="c0601-115">Method</span></span>                                              | <span data-ttu-id="c0601-116">Descrizione</span><span class="sxs-lookup"><span data-stu-id="c0601-116">Description</span></span>                                                                                          |
|:----------------------------------------------------|:-----------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="c0601-117">**CreateObject**</span><span class="sxs-lookup"><span data-stu-id="c0601-117">**CreateObject**</span></span>](iwmdrmprovider-createobject.md) | <span data-ttu-id="c0601-118">Recupera un puntatore a un'interfaccia specificata, creando l'oggetto di implementazione, se necessario.</span><span class="sxs-lookup"><span data-stu-id="c0601-118">Retrieves a pointer to a specified interface, creating the implementing object if needed.</span></span><br/> |



 

## <a name="see-also"></a><span data-ttu-id="c0601-119">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="c0601-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c0601-120">**Interfacce**</span><span class="sxs-lookup"><span data-stu-id="c0601-120">**Interfaces**</span></span>](drm-interfaces.md)
</dt> </dl>

 

