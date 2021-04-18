---
description: Le funzioni della finestra di dialogo specifiche del provider consentono a un provider di visualizzare e gestire informazioni specifiche della rete mediante la modifica delle finestre di dialogo di sistema o la visualizzazione di finestre di dialogo personalizzate.
ms.assetid: c9a52867-0a0b-40d8-a09d-2b7bed517e13
title: Funzioni della finestra di dialogo Provider-Specific
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 567c4dcb9f1fd6c2e289d678cf09b3d0d66e4207
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106316735"
---
# <a name="provider-specific-dialog-box-functions"></a><span data-ttu-id="d657d-103">Funzioni della finestra di dialogo Provider-Specific</span><span class="sxs-lookup"><span data-stu-id="d657d-103">Provider-Specific Dialog Box Functions</span></span>

<span data-ttu-id="d657d-104">Le funzioni della finestra di dialogo specifiche del provider consentono a un provider di visualizzare e gestire informazioni specifiche della rete mediante la modifica delle finestre di dialogo di sistema o la visualizzazione di finestre di dialogo personalizzate.</span><span class="sxs-lookup"><span data-stu-id="d657d-104">Provider-specific dialog box functions enable a provider to display and handle network-specific information by altering system dialog boxes or displaying custom dialog boxes.</span></span>

<span data-ttu-id="d657d-105">Le funzioni della finestra di dialogo seguenti aggiungono pulsanti alla finestra di dialogo **Proprietà** di file Manager.</span><span class="sxs-lookup"><span data-stu-id="d657d-105">The following dialog box functions add buttons to the File Manager **Properties** dialog box.</span></span> <span data-ttu-id="d657d-106">Il provider può quindi gestire gli eventi di questi pulsanti per eseguire attività specifiche della rete.</span><span class="sxs-lookup"><span data-stu-id="d657d-106">The provider can then handle the events of those buttons to perform network-specific tasks.</span></span> <span data-ttu-id="d657d-107">Si noti che esiste un limite al numero di pulsanti che è possibile aggiungere.</span><span class="sxs-lookup"><span data-stu-id="d657d-107">Note that there is a limit to the number of buttons that can be added.</span></span> <span data-ttu-id="d657d-108">Per questo motivo, i provider devono usare questa funzionalità con moderazione.</span><span class="sxs-lookup"><span data-stu-id="d657d-108">Because of this, providers should use this capability sparingly.</span></span> <span data-ttu-id="d657d-109">Inoltre, un provider potrebbe non essere in grado di aggiungere un pulsante perché lo spazio disponibile è già stato utilizzato da altri provider.</span><span class="sxs-lookup"><span data-stu-id="d657d-109">Also, a provider may find itself unable to add a button because the available space has been used already by other providers.</span></span> <span data-ttu-id="d657d-110">Questa situazione deve essere gestita da un provider di rete.</span><span class="sxs-lookup"><span data-stu-id="d657d-110">A network provider should handle this situation.</span></span>



| <span data-ttu-id="d657d-111">Funzione</span><span class="sxs-lookup"><span data-stu-id="d657d-111">Function</span></span>                                           | <span data-ttu-id="d657d-112">Descrizione</span><span class="sxs-lookup"><span data-stu-id="d657d-112">Description</span></span>                                                                                                                             |
|----------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="d657d-113">**NPGetPropertyText**</span><span class="sxs-lookup"><span data-stu-id="d657d-113">**NPGetPropertyText**</span></span>](/windows/desktop/api/Npapi/nf-npapi-npgetpropertytext)     | <span data-ttu-id="d657d-114">Determina i nomi dei pulsanti aggiunti a una finestra di dialogo delle proprietà per una risorsa specifica.</span><span class="sxs-lookup"><span data-stu-id="d657d-114">Determines the names of buttons added to a property dialog box for a specific resource.</span></span><br/>                                      |
| [<span data-ttu-id="d657d-115">**NPPropertyDialog**</span><span class="sxs-lookup"><span data-stu-id="d657d-115">**NPPropertyDialog**</span></span>](/windows/desktop/api/Npapi/nf-npapi-nppropertydialog)       | <span data-ttu-id="d657d-116">Chiamato quando un utente fa clic su un pulsante aggiunto tramite la funzione [**NPGetPropertyText**](/windows/desktop/api/Npapi/nf-npapi-npgetpropertytext) .</span><span class="sxs-lookup"><span data-stu-id="d657d-116">Called when a user clicks a button added by using the [**NPGetPropertyText**](/windows/desktop/api/Npapi/nf-npapi-npgetpropertytext) function.</span></span><br/>               |
| [<span data-ttu-id="d657d-117">**NPSearchDialog**</span><span class="sxs-lookup"><span data-stu-id="d657d-117">**NPSearchDialog**</span></span>](/windows/desktop/api/Npapi/nf-npapi-npsearchdialog)           | <span data-ttu-id="d657d-118">Consente ai provider di rete di implementare una propria funzionalità di ricerca oltre a quella specificata nella finestra di dialogo di **connessione** .</span><span class="sxs-lookup"><span data-stu-id="d657d-118">Enables network providers to implement their own search functionality beyond that provided in the **Connection** dialog box.</span></span><br/> |
| [<span data-ttu-id="d657d-119">**NPFormatNetworkName**</span><span class="sxs-lookup"><span data-stu-id="d657d-119">**NPFormatNetworkName**</span></span>](/windows/desktop/api/Npapi/nf-npapi-npformatnetworkname) | <span data-ttu-id="d657d-120">Consente ai provider di rete di formattare o modificare in altro modo i nomi di rete prima di essere presentati all'utente.</span><span class="sxs-lookup"><span data-stu-id="d657d-120">Enables network providers to format or otherwise modify network names before they are presented to the user.</span></span><br/>                 |



 

 

 




