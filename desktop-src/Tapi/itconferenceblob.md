---
description: Modifica una descrizione della conferenza testuale.
ms.assetid: b9ce61d1-3fc5-4963-8d2f-586a4b6a159d
title: Interfaccia ITConferenceBlob (sdpblb. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c961b8fb006f1e172f82827216292cb9d12a158f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106328226"
---
# <a name="itconferenceblob-interface"></a><span data-ttu-id="4e98f-103">Interfaccia ITConferenceBlob</span><span class="sxs-lookup"><span data-stu-id="4e98f-103">ITConferenceBlob interface</span></span>

<span data-ttu-id="4e98f-104">\[ I controlli e le interfacce per la comunicazione di telefonia IP Rendezvous non sono disponibili per l'uso in Windows Vista, Windows Server 2008 e nelle versioni successive del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="4e98f-104">\[ Rendezvous IP Telephony Conferencing controls and interfaces are not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="4e98f-105">L'API del client RTC fornisce funzionalità simili.\]</span><span class="sxs-lookup"><span data-stu-id="4e98f-105">The RTC Client API provides similar functionality.\]</span></span>

<span data-ttu-id="4e98f-106">L'interfaccia **ITConferenceBlob** manipola una descrizione della conferenza testuale.</span><span class="sxs-lookup"><span data-stu-id="4e98f-106">The **ITConferenceBlob** interface manipulates a textual conference description.</span></span> <span data-ttu-id="4e98f-107">L'interfaccia è progettata per essere indipendente dal formato e dalla sintassi della descrizione della conferenza.</span><span class="sxs-lookup"><span data-stu-id="4e98f-107">The interface is intended to be independent of the format and syntax of the conference description.</span></span> <span data-ttu-id="4e98f-108">Per modificare aspetti specifici della descrizione della conferenza, l'applicazione deve eseguire una query per un'altra interfaccia.</span><span class="sxs-lookup"><span data-stu-id="4e98f-108">To manipulate specific aspects of the conference description, the application must query for another interface.</span></span> <span data-ttu-id="4e98f-109">Attualmente sono supportate solo le descrizioni delle conferenze SDP; l'applicazione deve usare **QueryInterface** per [**ITSdp**](itsdp.md) per accedere ai diversi campi della descrizione della conferenza SDP.</span><span class="sxs-lookup"><span data-stu-id="4e98f-109">Currently, only SDP conference descriptions are supported; the application must use **QueryInterface** for [**ITSdp**](itsdp.md) to access the various fields of the SDP conference description.</span></span> <span data-ttu-id="4e98f-110">L'interfaccia **ITConferenceBlob** viene creata chiamando **QueryInterface** in [**ITDirectoryObject**](/windows/desktop/api/Rend/nn-rend-itdirectoryobject).</span><span class="sxs-lookup"><span data-stu-id="4e98f-110">The **ITConferenceBlob** interface is created by calling **QueryInterface** on [**ITDirectoryObject**](/windows/desktop/api/Rend/nn-rend-itdirectoryobject).</span></span>

## <a name="members"></a><span data-ttu-id="4e98f-111">Membri</span><span class="sxs-lookup"><span data-stu-id="4e98f-111">Members</span></span>

<span data-ttu-id="4e98f-112">L'interfaccia **ITConferenceBlob** eredita dall'interfaccia [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) .</span><span class="sxs-lookup"><span data-stu-id="4e98f-112">The **ITConferenceBlob** interface inherits from the [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) interface.</span></span> <span data-ttu-id="4e98f-113">**ITConferenceBlob** dispone anche di questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="4e98f-113">**ITConferenceBlob** also has these types of members:</span></span>

-   [<span data-ttu-id="4e98f-114">Metodi</span><span class="sxs-lookup"><span data-stu-id="4e98f-114">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="4e98f-115">Metodi</span><span class="sxs-lookup"><span data-stu-id="4e98f-115">Methods</span></span>

<span data-ttu-id="4e98f-116">L'interfaccia **ITConferenceBlob** dispone di questi metodi.</span><span class="sxs-lookup"><span data-stu-id="4e98f-116">The **ITConferenceBlob** interface has these methods.</span></span>



| <span data-ttu-id="4e98f-117">Metodo</span><span class="sxs-lookup"><span data-stu-id="4e98f-117">Method</span></span>                                                             | <span data-ttu-id="4e98f-118">Descrizione</span><span class="sxs-lookup"><span data-stu-id="4e98f-118">Description</span></span>                                                                                                                                   |
|:-------------------------------------------------------------------|:----------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="4e98f-119">**Ottieni \_ caratteri**</span><span class="sxs-lookup"><span data-stu-id="4e98f-119">**get\_CharacterSet**</span></span>](itconferenceblob-get-characterset.md)     | <span data-ttu-id="4e98f-120">Ottiene l'indicatore del [**\_ \_ set di caratteri BLOB**](blob-character-set.md) che indica se i caratteri BLOB sono ASCII, Unicode e così via.</span><span class="sxs-lookup"><span data-stu-id="4e98f-120">Gets the [**BLOB\_CHARACTER\_SET**](blob-character-set.md) indicator of whether blob characters are in ASCII, Unicode, and so on.</span></span><br/> |
| [<span data-ttu-id="4e98f-121">**ottenere \_ ConferenceBlob**</span><span class="sxs-lookup"><span data-stu-id="4e98f-121">**get\_ConferenceBlob**</span></span>](itconferenceblob-get-conferenceblob.md) | <span data-ttu-id="4e98f-122">Ottiene un puntatore al BLOB della conferenza.</span><span class="sxs-lookup"><span data-stu-id="4e98f-122">Gets a pointer to the conference blob.</span></span><br/>                                                                                             |
| [<span data-ttu-id="4e98f-123">**Init**</span><span class="sxs-lookup"><span data-stu-id="4e98f-123">**Init**</span></span>](itconferenceblob-init.md)                              | <span data-ttu-id="4e98f-124">Inizializza il BLOB della conferenza.</span><span class="sxs-lookup"><span data-stu-id="4e98f-124">Initializes the conference blob.</span></span><br/>                                                                                                   |
| [<span data-ttu-id="4e98f-125">**SetConferenceBlob**</span><span class="sxs-lookup"><span data-stu-id="4e98f-125">**SetConferenceBlob**</span></span>](itconferenceblob-setconferenceblob.md)    | <span data-ttu-id="4e98f-126">Salva le modifiche apportate al BLOB della conferenza.</span><span class="sxs-lookup"><span data-stu-id="4e98f-126">Commits changes to the conference blob.</span></span><br/>                                                                                            |



 

## <a name="requirements"></a><span data-ttu-id="4e98f-127">Requisiti</span><span class="sxs-lookup"><span data-stu-id="4e98f-127">Requirements</span></span>



| <span data-ttu-id="4e98f-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="4e98f-128">Requirement</span></span> | <span data-ttu-id="4e98f-129">Valore</span><span class="sxs-lookup"><span data-stu-id="4e98f-129">Value</span></span> |
|-------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="4e98f-130">Versione TAPI</span><span class="sxs-lookup"><span data-stu-id="4e98f-130">TAPI version</span></span><br/> | <span data-ttu-id="4e98f-131">Richiede TAPI 3,0 o versione successiva</span><span class="sxs-lookup"><span data-stu-id="4e98f-131">Requires TAPI 3.0 or later</span></span><br/>                                                 |
| <span data-ttu-id="4e98f-132">Intestazione</span><span class="sxs-lookup"><span data-stu-id="4e98f-132">Header</span></span><br/>       | <dl> <span data-ttu-id="4e98f-133"><dt>Sdpblb. h</dt></span><span class="sxs-lookup"><span data-stu-id="4e98f-133"><dt>Sdpblb.h</dt></span></span> </dl>   |
| <span data-ttu-id="4e98f-134">Libreria</span><span class="sxs-lookup"><span data-stu-id="4e98f-134">Library</span></span><br/>      | <dl> <span data-ttu-id="4e98f-135"><dt>UUID. lib</dt></span><span class="sxs-lookup"><span data-stu-id="4e98f-135"><dt>Uuid.lib</dt></span></span> </dl>   |
| <span data-ttu-id="4e98f-136">DLL</span><span class="sxs-lookup"><span data-stu-id="4e98f-136">DLL</span></span><br/>          | <dl> <span data-ttu-id="4e98f-137"><dt>Sdpblb.dll</dt></span><span class="sxs-lookup"><span data-stu-id="4e98f-137"><dt>Sdpblb.dll</dt></span></span> </dl> |



 

