---
description: L'interfaccia ITAttributeList fornisce i metodi per ottenere e impostare gli attributi non interpretati.
ms.assetid: 12806c2e-615c-4d78-a4bb-5cc35ea21175
title: Interfaccia ITAttributeList (sdpblb. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a2afbc7ab447188943c0f02e6c5a664bbcc4c6d0
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106332729"
---
# <a name="itattributelist-interface"></a><span data-ttu-id="a04eb-103">Interfaccia ITAttributeList</span><span class="sxs-lookup"><span data-stu-id="a04eb-103">ITAttributeList interface</span></span>

<span data-ttu-id="a04eb-104">\[ I controlli e le interfacce per la comunicazione di telefonia IP Rendezvous non sono disponibili per l'uso in Windows Vista, Windows Server 2008 e nelle versioni successive del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="a04eb-104">\[ Rendezvous IP Telephony Conferencing controls and interfaces are not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="a04eb-105">L'API del client RTC fornisce funzionalità simili.\]</span><span class="sxs-lookup"><span data-stu-id="a04eb-105">The RTC Client API provides similar functionality.\]</span></span>

<span data-ttu-id="a04eb-106">L'interfaccia **ITAttributeList** fornisce i metodi per ottenere e impostare gli attributi non interpretati.</span><span class="sxs-lookup"><span data-stu-id="a04eb-106">The **ITAttributeList** interface supplies methods for getting and setting of uninterpreted attributes.</span></span> <span data-ttu-id="a04eb-107">Per quanto riguarda la posizione delle stringhe degli attributi in un pacchetto del protocollo di descrizione della sessione (SDP, see RFC 2327), i metodi presuppongono che tutte le stringhe di attributo esistano immediatamente prima che siano specificati gli attributi multimediali e dopo tutti gli attributi comuni.</span><span class="sxs-lookup"><span data-stu-id="a04eb-107">Regarding the position of the attribute strings in a Session Descriptor Protocol (SDP, see RFC 2327) packet, the methods assume that all attribute strings exist just before the media attributes are specified and after all the common attributes.</span></span> <span data-ttu-id="a04eb-108">L'interfaccia **ITAttributeList** viene creata chiamando **QueryInterface** in [**ITDirectoryObject**](/windows/desktop/api/Rend/nn-rend-itdirectoryobject).</span><span class="sxs-lookup"><span data-stu-id="a04eb-108">The **ITAttributeList** interface is created by calling **QueryInterface** on [**ITDirectoryObject**](/windows/desktop/api/Rend/nn-rend-itdirectoryobject).</span></span>

## <a name="members"></a><span data-ttu-id="a04eb-109">Membri</span><span class="sxs-lookup"><span data-stu-id="a04eb-109">Members</span></span>

<span data-ttu-id="a04eb-110">L'interfaccia **ITAttributeList** eredita dall'interfaccia [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) .</span><span class="sxs-lookup"><span data-stu-id="a04eb-110">The **ITAttributeList** interface inherits from the [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) interface.</span></span> <span data-ttu-id="a04eb-111">**ITAttributeList** dispone anche di questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="a04eb-111">**ITAttributeList** also has these types of members:</span></span>

-   [<span data-ttu-id="a04eb-112">Metodi</span><span class="sxs-lookup"><span data-stu-id="a04eb-112">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="a04eb-113">Metodi</span><span class="sxs-lookup"><span data-stu-id="a04eb-113">Methods</span></span>

<span data-ttu-id="a04eb-114">L'interfaccia **ITAttributeList** dispone di questi metodi.</span><span class="sxs-lookup"><span data-stu-id="a04eb-114">The **ITAttributeList** interface has these methods.</span></span>



| <span data-ttu-id="a04eb-115">Metodo</span><span class="sxs-lookup"><span data-stu-id="a04eb-115">Method</span></span>                                                          | <span data-ttu-id="a04eb-116">Descrizione</span><span class="sxs-lookup"><span data-stu-id="a04eb-116">Description</span></span>                                             |
|:----------------------------------------------------------------|:--------------------------------------------------------|
| [<span data-ttu-id="a04eb-117">**Aggiungere**</span><span class="sxs-lookup"><span data-stu-id="a04eb-117">**Add**</span></span>](itattributelist-add.md)                              | <span data-ttu-id="a04eb-118">Aggiunge l'attributo in corrispondenza dell'indice specificato.</span><span class="sxs-lookup"><span data-stu-id="a04eb-118">Adds the attribute at the specified index.</span></span><br/>   |
| [<span data-ttu-id="a04eb-119">**Delete**</span><span class="sxs-lookup"><span data-stu-id="a04eb-119">**Delete**</span></span>](itattributelist-delete.md)                        | <span data-ttu-id="a04eb-120">Elimina l'attributo in corrispondenza dell'indice specificato.</span><span class="sxs-lookup"><span data-stu-id="a04eb-120">Deletes the attribute at the specified index</span></span><br/> |
| [<span data-ttu-id="a04eb-121">**Ottieni \_ attributo**</span><span class="sxs-lookup"><span data-stu-id="a04eb-121">**get\_AttributeList**</span></span>](itattributelist-get-attributelist.md) | <span data-ttu-id="a04eb-122">Ottiene l'elenco di attributi.</span><span class="sxs-lookup"><span data-stu-id="a04eb-122">Gets the list of attributes.</span></span><br/>                 |
| [<span data-ttu-id="a04eb-123">**Ottieni \_ conteggio**</span><span class="sxs-lookup"><span data-stu-id="a04eb-123">**get\_Count**</span></span>](itattributelist-get-count.md)                 | <span data-ttu-id="a04eb-124">Ottiene il numero di attributi.</span><span class="sxs-lookup"><span data-stu-id="a04eb-124">Gets the number of attributes.</span></span><br/>               |
| [<span data-ttu-id="a04eb-125">**Ottieni \_ elemento**</span><span class="sxs-lookup"><span data-stu-id="a04eb-125">**get\_Item**</span></span>](itattributelist-get-item.md)                   | <span data-ttu-id="a04eb-126">Ottiene l'attributo specificato dall'indice.</span><span class="sxs-lookup"><span data-stu-id="a04eb-126">Gets the attribute specified by the index.</span></span><br/>   |
| [<span data-ttu-id="a04eb-127">**Inserisci \_ attributo**</span><span class="sxs-lookup"><span data-stu-id="a04eb-127">**put\_AttributeList**</span></span>](itattributelist-put-attributelist.md) | <span data-ttu-id="a04eb-128">Imposta l'elenco di attributi.</span><span class="sxs-lookup"><span data-stu-id="a04eb-128">Sets the list of attributes.</span></span><br/>                 |



 

## <a name="requirements"></a><span data-ttu-id="a04eb-129">Requisiti</span><span class="sxs-lookup"><span data-stu-id="a04eb-129">Requirements</span></span>



| <span data-ttu-id="a04eb-130">Requisito</span><span class="sxs-lookup"><span data-stu-id="a04eb-130">Requirement</span></span> | <span data-ttu-id="a04eb-131">Valore</span><span class="sxs-lookup"><span data-stu-id="a04eb-131">Value</span></span> |
|-------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="a04eb-132">Versione TAPI</span><span class="sxs-lookup"><span data-stu-id="a04eb-132">TAPI version</span></span><br/> | <span data-ttu-id="a04eb-133">Richiede TAPI 3,0 o versione successiva</span><span class="sxs-lookup"><span data-stu-id="a04eb-133">Requires TAPI 3.0 or later</span></span><br/>                                                 |
| <span data-ttu-id="a04eb-134">Intestazione</span><span class="sxs-lookup"><span data-stu-id="a04eb-134">Header</span></span><br/>       | <dl> <span data-ttu-id="a04eb-135"><dt>Sdpblb. h</dt></span><span class="sxs-lookup"><span data-stu-id="a04eb-135"><dt>Sdpblb.h</dt></span></span> </dl>   |
| <span data-ttu-id="a04eb-136">Libreria</span><span class="sxs-lookup"><span data-stu-id="a04eb-136">Library</span></span><br/>      | <dl> <span data-ttu-id="a04eb-137"><dt>UUID. lib</dt></span><span class="sxs-lookup"><span data-stu-id="a04eb-137"><dt>Uuid.lib</dt></span></span> </dl>   |
| <span data-ttu-id="a04eb-138">DLL</span><span class="sxs-lookup"><span data-stu-id="a04eb-138">DLL</span></span><br/>          | <dl> <span data-ttu-id="a04eb-139"><dt>Sdpblb.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a04eb-139"><dt>Sdpblb.dll</dt></span></span> </dl> |



 

