---
title: Interfaccia IWMDRMLicense
description: L'interfaccia IWMDRMLicense rappresenta un elenco di una o più licenze.
ms.assetid: afef7f9a-6621-4de7-bd40-3211c5c7ba09
keywords:
- Formato Windows Media Interface IWMDRMLicense
- Interfaccia IWMDRMLicense-formato Windows Media, descritto
topic_type:
- apiref
api_name:
- IWMDRMLicense
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 918154b180ed95dce51224e6340a3ab18f432d18
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104473579"
---
# <a name="iwmdrmlicense-interface"></a><span data-ttu-id="fe187-105">Interfaccia IWMDRMLicense</span><span class="sxs-lookup"><span data-stu-id="fe187-105">IWMDRMLicense interface</span></span>

<span data-ttu-id="fe187-106">L'interfaccia **IWMDRMLicense** rappresenta un elenco di una o più licenze.</span><span class="sxs-lookup"><span data-stu-id="fe187-106">The **IWMDRMLicense** interface represents a list of one or more licenses.</span></span>

## <a name="members"></a><span data-ttu-id="fe187-107">Membri</span><span class="sxs-lookup"><span data-stu-id="fe187-107">Members</span></span>

<span data-ttu-id="fe187-108">L'interfaccia **IWMDRMLicense** eredita dall'interfaccia [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="fe187-108">The **IWMDRMLicense** interface inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="fe187-109">**IWMDRMLicense** dispone anche di questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="fe187-109">**IWMDRMLicense** also has these types of members:</span></span>

-   [<span data-ttu-id="fe187-110">Metodi</span><span class="sxs-lookup"><span data-stu-id="fe187-110">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="fe187-111">Metodi</span><span class="sxs-lookup"><span data-stu-id="fe187-111">Methods</span></span>

<span data-ttu-id="fe187-112">L'interfaccia **IWMDRMLicense** dispone di questi metodi.</span><span class="sxs-lookup"><span data-stu-id="fe187-112">The **IWMDRMLicense** interface has these methods.</span></span>



| <span data-ttu-id="fe187-113">Metodo</span><span class="sxs-lookup"><span data-stu-id="fe187-113">Method</span></span>                                                                                   | <span data-ttu-id="fe187-114">Descrizione</span><span class="sxs-lookup"><span data-stu-id="fe187-114">Description</span></span>                                                                                                                                                                                                                        |
|:-----------------------------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="fe187-115">**CanPersist**</span><span class="sxs-lookup"><span data-stu-id="fe187-115">**CanPersist**</span></span>](iwmdrmlicense-canpersist.md)                                           | <span data-ttu-id="fe187-116">Esegue una query per determinare se la licenza può essere mantenute in un archivio licenze locale.</span><span class="sxs-lookup"><span data-stu-id="fe187-116">Queries whether the license can be persisted on in a local license store.</span></span><br/>                                                                                                                                               |
| [<span data-ttu-id="fe187-117">**CreateDecryptor**</span><span class="sxs-lookup"><span data-stu-id="fe187-117">**CreateDecryptor**</span></span>](iwmdrmlicense-createdecryptor.md)                                 | <span data-ttu-id="fe187-118">Crea un oggetto di decrittografia utilizzando le impostazioni della licenza corrente.</span><span class="sxs-lookup"><span data-stu-id="fe187-118">Creates a decryptor object using the settings of the current license.</span></span><br/>                                                                                                                                                   |
| [<span data-ttu-id="fe187-119">**Al CreateDecryptor**</span><span class="sxs-lookup"><span data-stu-id="fe187-119">**CreateEncryptor**</span></span>](iwmdrmlicense-createencryptor.md)                                 | <span data-ttu-id="fe187-120">Crea un oggetto di crittografia utilizzando le impostazioni della licenza corrente.</span><span class="sxs-lookup"><span data-stu-id="fe187-120">Creates an encryptor object using the settings of the current license.</span></span><br/>                                                                                                                                                  |
| [<span data-ttu-id="fe187-121">**CreateSecureDecryptor**</span><span class="sxs-lookup"><span data-stu-id="fe187-121">**CreateSecureDecryptor**</span></span>](iwmdrmlicense-createsecuredecryptor.md)                     | <span data-ttu-id="fe187-122">Crea un oggetto di decrittografia protetto.</span><span class="sxs-lookup"><span data-stu-id="fe187-122">Creates a secure decryptor object.</span></span> <span data-ttu-id="fe187-123">Il decrittografia sicuro è diverso da quello normale in quanto decrittografa il contenuto e quindi lo crittografa nuovamente in base alle impostazioni specificate nei parametri di questo metodo.</span><span class="sxs-lookup"><span data-stu-id="fe187-123">The secure decryptor differs from the normal decryptor in that it decrypts the content and then re-encrypts it according to the settings specified in the parameters of this method.</span></span><br/> |
| [<span data-ttu-id="fe187-124">**GetAnalogVideoRestrictionLevels**</span><span class="sxs-lookup"><span data-stu-id="fe187-124">**GetAnalogVideoRestrictionLevels**</span></span>](iwmdrmlicense-getanalogvideorestrictionlevels.md) | <span data-ttu-id="fe187-125">Recupera tutte le restrizioni video analogiche impostate per la licenza corrente.</span><span class="sxs-lookup"><span data-stu-id="fe187-125">Retrieves all analog video restrictions set on the current license.</span></span><br/>                                                                                                                                                     |
| [<span data-ttu-id="fe187-126">**Getinclusiving**</span><span class="sxs-lookup"><span data-stu-id="fe187-126">**GetInclusionList**</span></span>](iwmdrmlicense-getinclusionlist.md)                               | <span data-ttu-id="fe187-127">Recupera l'intero elenco di inclusione per la licenza o la catena di licenze corrente.</span><span class="sxs-lookup"><span data-stu-id="fe187-127">Retrieves the entire inclusion list for the current license or license chain.</span></span><br/>                                                                                                                                           |
| [<span data-ttu-id="fe187-128">**GetLicense**</span><span class="sxs-lookup"><span data-stu-id="fe187-128">**GetLicense**</span></span>](iwmdrmlicense-getlicense.md)                                           | <span data-ttu-id="fe187-129">Recupera la licenza come dati Extensible Markup Language (XML) o XMR (Extensible Media Rights).</span><span class="sxs-lookup"><span data-stu-id="fe187-129">Retrieves the license as Extensible Markup Language (XML) or Extensible Media Rights (XMR) data.</span></span><br/>                                                                                                                        |
| [<span data-ttu-id="fe187-130">**GetLicenseProperty**</span><span class="sxs-lookup"><span data-stu-id="fe187-130">**GetLicenseProperty**</span></span>](iwmdrmlicense-getlicenseproperty.md)                           | <span data-ttu-id="fe187-131">Recupera una proprietà dalla licenza corrente.</span><span class="sxs-lookup"><span data-stu-id="fe187-131">Retrieves a property from the current license.</span></span><br/>                                                                                                                                                                          |
| [<span data-ttu-id="fe187-132">**GetNext**</span><span class="sxs-lookup"><span data-stu-id="fe187-132">**GetNext**</span></span>](iwmdrmlicense-getnext.md)                                                 | <span data-ttu-id="fe187-133">Carica le informazioni relative alla licenza successiva nell'elenco.</span><span class="sxs-lookup"><span data-stu-id="fe187-133">Loads the information about the next license in the list.</span></span><br/>                                                                                                                                                               |
| [<span data-ttu-id="fe187-134">**GetOutputProtectionLevels**</span><span class="sxs-lookup"><span data-stu-id="fe187-134">**GetOutputProtectionLevels**</span></span>](iwmdrmlicense-getoutputprotectionlevels.md)             | <span data-ttu-id="fe187-135">Recupera informazioni su tutti i livelli di protezione dell'output (OPLs) assegnati alla licenza.</span><span class="sxs-lookup"><span data-stu-id="fe187-135">Retrieves information about all output protection levels (OPLs) assigned to the license.</span></span><br/>                                                                                                                                |
| [<span data-ttu-id="fe187-136">**PersistLicense**</span><span class="sxs-lookup"><span data-stu-id="fe187-136">**PersistLicense**</span></span>](iwmdrmlicense-persistlicense.md)                                   | <span data-ttu-id="fe187-137">Salva la licenza corrente dall'archivio temporaneo nell'archivio licenze locale permanente.</span><span class="sxs-lookup"><span data-stu-id="fe187-137">Saves the current license from the temporary store into the permanent local license store.</span></span><br/>                                                                                                                              |
| [<span data-ttu-id="fe187-138">**ResetEnumeration**</span><span class="sxs-lookup"><span data-stu-id="fe187-138">**ResetEnumeration**</span></span>](iwmdrmlicense-resetenumeration.md)                               | <span data-ttu-id="fe187-139">Reimposta l'elenco di licenze sullo stato originale.</span><span class="sxs-lookup"><span data-stu-id="fe187-139">Resets the license list to its original state.</span></span><br/>                                                                                                                                                                          |



 

## <a name="see-also"></a><span data-ttu-id="fe187-140">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="fe187-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fe187-141">**Interfacce**</span><span class="sxs-lookup"><span data-stu-id="fe187-141">**Interfaces**</span></span>](drm-interfaces.md)
</dt> </dl>

 

