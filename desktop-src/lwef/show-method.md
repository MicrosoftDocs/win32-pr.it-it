---
title: Mostra metodo
description: Mostra metodo
ms.assetid: 58adbb55-f4cb-4356-abc4-b85fa3af744d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a05a1adaa46c85f34e02128960330c68d9a86db1
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2020
ms.locfileid: "106299595"
---
# <a name="show-method"></a><span data-ttu-id="63549-103">Mostra metodo</span><span class="sxs-lookup"><span data-stu-id="63549-103">Show Method</span></span>

<span data-ttu-id="63549-104">\[Microsoft Agent è stato deprecato a partire da Windows 7 e potrebbe non essere disponibile nelle versioni successive di Windows.\]</span><span class="sxs-lookup"><span data-stu-id="63549-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

<dl> <dt>

<span data-ttu-id="63549-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Descrizione**</span><span class="sxs-lookup"><span data-stu-id="63549-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Description**</span></span>
</dt> <dd>

<span data-ttu-id="63549-106">Rende visibile il carattere specificato e riproduce l'animazione di **visualizzazione** associata.</span><span class="sxs-lookup"><span data-stu-id="63549-106">Makes the specified character visible and plays its associated **Showing** animation.</span></span>

</dd> <dt>

<span data-ttu-id="63549-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Sintassi**</span><span class="sxs-lookup"><span data-stu-id="63549-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Syntax**</span></span>
</dt> <dd>

<span data-ttu-id="63549-108">\*agente ***. Caratteri ("*** CharacterID \* \* *"). Mostra* \*  \[ *veloce*\]</span><span class="sxs-lookup"><span data-stu-id="63549-108">*agent ***.Characters ("*** CharacterID\*\*\*").Show*\* \[*Fast*\]</span></span>



| <span data-ttu-id="63549-109">Parte</span><span class="sxs-lookup"><span data-stu-id="63549-109">Part</span></span>   | <span data-ttu-id="63549-110">Descrizione</span><span class="sxs-lookup"><span data-stu-id="63549-110">Description</span></span>                                                                                                                                                                                                                              |
|--------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="63549-111">*Veloce*</span><span class="sxs-lookup"><span data-stu-id="63549-111">*Fast*</span></span> | <span data-ttu-id="63549-112">facoltativo.</span><span class="sxs-lookup"><span data-stu-id="63549-112">Optional.</span></span> <span data-ttu-id="63549-113">Espressione booleana che specifica se il server riproduce l'animazione di **visualizzazione** .</span><span class="sxs-lookup"><span data-stu-id="63549-113">A Boolean expression specifying whether the server plays the **Showing** animation.</span></span> <span data-ttu-id="63549-114">Valore **true** Ignora l'animazione dello stato di **visualizzazione** .</span><span class="sxs-lookup"><span data-stu-id="63549-114">**True** Skips the **Showing** state animation.</span></span> <br/> <span data-ttu-id="63549-115">**False** (impostazione predefinita) non ignora l'animazione dello stato di **visualizzazione** .</span><span class="sxs-lookup"><span data-stu-id="63549-115">**False** (Default) Does not skip the **Showing** state animation.</span></span> <br/> |



 

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="63549-116">Commenti</span><span class="sxs-lookup"><span data-stu-id="63549-116">Remarks</span></span>

<span data-ttu-id="63549-117">Se si dichiara un riferimento a un oggetto e lo si imposta su questo metodo, viene restituito un oggetto [**Request**](/windows/desktop/lwef/the-request-object) .</span><span class="sxs-lookup"><span data-stu-id="63549-117">If you declare an object reference and set it to this method, it returns a [**Request**](/windows/desktop/lwef/the-request-object) object.</span></span> <span data-ttu-id="63549-118">Inoltre, se non è stata caricata la **visualizzazione** dell'animazione associata e il parametro **Fast** non è stato specificato come **true**, il server imposta la proprietà [**status**](status-property.md) dell'oggetto **richiesta** su "failed" con un numero di errore appropriato.</span><span class="sxs-lookup"><span data-stu-id="63549-118">In addition, if the associated **Showing** animation has not been loaded and you have not specified the **Fast** parameter as **True**, the server sets the **Request** object's [**Status**](status-property.md) property to "failed" with an appropriate error number.</span></span> <span data-ttu-id="63549-119">Se pertanto si utilizza il protocollo HTTP per accedere ai dati di animazione dei caratteri, utilizzare il metodo [**Get**](get-method.md) per caricare l'animazione **di visualizzazione dello stato prima** di chiamare il metodo **show** .</span><span class="sxs-lookup"><span data-stu-id="63549-119">Therefore, if you are using the HTTP protocol to access character animation data, use the [**Get**](get-method.md) method to load the **Showing** state animation before calling the **Show** method.</span></span>

<span data-ttu-id="63549-120">Evitare di impostare il parametro **Fast** su **true** senza prima riprodurre prima un'animazione. in caso contrario, il frame di caratteri può essere visualizzato senza immagine.</span><span class="sxs-lookup"><span data-stu-id="63549-120">Avoid setting the **Fast** parameter to **True** without first playing an animation beforehand; otherwise, the character frame may display with no image.</span></span> <span data-ttu-id="63549-121">In particolare, si noti che se si chiama [**MoveTo**](moveto-method.md) quando il carattere non è visibile, non viene eseguita alcuna animazione.</span><span class="sxs-lookup"><span data-stu-id="63549-121">In particular, note that if you call [**MoveTo**](moveto-method.md) when the character is not visible, it does not play any animation.</span></span> <span data-ttu-id="63549-122">Se pertanto si chiama il metodo **show** con **Fast** impostato su **true**, non viene visualizzata alcuna immagine.</span><span class="sxs-lookup"><span data-stu-id="63549-122">Therefore, if you call the **Show** method with **Fast** set to **True**, no image will display.</span></span> <span data-ttu-id="63549-123">Analogamente, se si chiama [**Nascondi**](hide-method.md) e **Mostra** con **Fast** impostato su **true**, non sarà presente alcuna immagine visibile.</span><span class="sxs-lookup"><span data-stu-id="63549-123">Similarly, if you call [**Hide**](hide-method.md) then **Show** with **Fast** set to **True**, there will be no visible image.</span></span>

## <a name="see-also"></a><span data-ttu-id="63549-124">Vedere anche</span><span class="sxs-lookup"><span data-stu-id="63549-124">See Also</span></span>

[<span data-ttu-id="63549-125">**Hide (metodo)**</span><span class="sxs-lookup"><span data-stu-id="63549-125">**Hide method**</span></span>](hide-method.md)


 

