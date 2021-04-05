---
title: Interfaccia IWMDRMNonSilentLicenseAquisition
description: L'interfaccia IWMDRMNonSilentLicenseAquisition fornisce metodi che consentono l'acquisizione di licenze che richiedono l'intervento dell'utente. Questa interfaccia può essere ottenuta eseguendo l'acquisizione di una licenza non invisibile all'utente.
ms.assetid: 57dc3daa-d457-49b0-b589-a72ba180e75e
keywords:
- Formato Windows Media Interface IWMDRMNonSilentLicenseAquisition
- Interfaccia IWMDRMNonSilentLicenseAquisition-formato Windows Media, descritto
topic_type:
- apiref
api_name:
- IWMDRMNonSilentLicenseAquisition
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 89fce7764b755231812c761778131c159ddd860b
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "103728711"
---
# <a name="iwmdrmnonsilentlicenseaquisition-interface"></a><span data-ttu-id="f8005-105">Interfaccia IWMDRMNonSilentLicenseAquisition</span><span class="sxs-lookup"><span data-stu-id="f8005-105">IWMDRMNonSilentLicenseAquisition interface</span></span>

<span data-ttu-id="f8005-106">L'interfaccia **IWMDRMNonSilentLicenseAquisition** fornisce metodi che consentono l'acquisizione di licenze che richiedono l'intervento dell'utente.</span><span class="sxs-lookup"><span data-stu-id="f8005-106">The **IWMDRMNonSilentLicenseAquisition** interface provides methods that enable license acquisition requiring user intervention.</span></span>

<span data-ttu-id="f8005-107">Questa interfaccia può essere ottenuta eseguendo l'acquisizione di una licenza non invisibile all'utente.</span><span class="sxs-lookup"><span data-stu-id="f8005-107">This interface can be obtained by performing non-silent license acquisition.</span></span> <span data-ttu-id="f8005-108">Dopo la chiamata a [**IWMDRMLicenseManagement:: AcquireLicense**](iwmdrmlicensemanagement-acquirelicense.md) , verrà generato un evento **MEWMDRMLicenseAcquisitionCompleted** .</span><span class="sxs-lookup"><span data-stu-id="f8005-108">After you call [**IWMDRMLicenseManagement::AcquireLicense**](iwmdrmlicensemanagement-acquirelicense.md) an **MEWMDRMLicenseAcquisitionCompleted** event will be generated.</span></span> <span data-ttu-id="f8005-109">Chiamare il metodo **IMFMediaEvent:: GetValue** dell'evento per ottenere un puntatore a un'interfaccia **IUnknown** su cui è possibile eseguire una query per un puntatore a un'istanza di questa interfaccia.</span><span class="sxs-lookup"><span data-stu-id="f8005-109">Call the **IMFMediaEvent::GetValue** method of the event to get a pointer to an **IUnknown** interface that can be queried for a pointer to an instance of this interface.</span></span>

## <a name="members"></a><span data-ttu-id="f8005-110">Membri</span><span class="sxs-lookup"><span data-stu-id="f8005-110">Members</span></span>

<span data-ttu-id="f8005-111">L'interfaccia **IWMDRMNonSilentLicenseAquisition** eredita dall'interfaccia [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="f8005-111">The **IWMDRMNonSilentLicenseAquisition** interface inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="f8005-112">**IWMDRMNonSilentLicenseAquisition** dispone anche di questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="f8005-112">**IWMDRMNonSilentLicenseAquisition** also has these types of members:</span></span>

-   [<span data-ttu-id="f8005-113">Metodi</span><span class="sxs-lookup"><span data-stu-id="f8005-113">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="f8005-114">Metodi</span><span class="sxs-lookup"><span data-stu-id="f8005-114">Methods</span></span>

<span data-ttu-id="f8005-115">L'interfaccia **IWMDRMNonSilentLicenseAquisition** dispone di questi metodi.</span><span class="sxs-lookup"><span data-stu-id="f8005-115">The **IWMDRMNonSilentLicenseAquisition** interface has these methods.</span></span>



| <span data-ttu-id="f8005-116">Metodo</span><span class="sxs-lookup"><span data-stu-id="f8005-116">Method</span></span>                                                                | <span data-ttu-id="f8005-117">Descrizione</span><span class="sxs-lookup"><span data-stu-id="f8005-117">Description</span></span>                                                                             |
|:----------------------------------------------------------------------|:----------------------------------------------------------------------------------------|
| [<span data-ttu-id="f8005-118">**Getchallenge**</span><span class="sxs-lookup"><span data-stu-id="f8005-118">**GetChallenge**</span></span>](iwmdrmnonsilentlicenseaquisition-getchallenge.md) | <span data-ttu-id="f8005-119">Recupera la richiesta di licenza che deve essere inviata al server licenze.</span><span class="sxs-lookup"><span data-stu-id="f8005-119">Retrieves the license challenge that should be posted to the license server.</span></span><br/> |
| [<span data-ttu-id="f8005-120">**GetURL**</span><span class="sxs-lookup"><span data-stu-id="f8005-120">**GetURL**</span></span>](iwmdrmnonsilentlicenseaquisition-geturl.md)             | <span data-ttu-id="f8005-121">Recupera l'URL a cui deve essere inviata la richiesta di licenza.</span><span class="sxs-lookup"><span data-stu-id="f8005-121">Retrieves the URL to which the license challenge should be posted.</span></span><br/>           |



 

## <a name="see-also"></a><span data-ttu-id="f8005-122">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="f8005-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f8005-123">**Interfacce**</span><span class="sxs-lookup"><span data-stu-id="f8005-123">**Interfaces**</span></span>](drm-interfaces.md)
</dt> <dt>

[<span data-ttu-id="f8005-124">**Acquisizione di licenza non invisibile all'utente**</span><span class="sxs-lookup"><span data-stu-id="f8005-124">**Non-Silent License Acquisition**</span></span>](non-silent-license-acquisition.md)
</dt> </dl>

 

