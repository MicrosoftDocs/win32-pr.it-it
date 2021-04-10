---
description: L'operazione di attesa consente a un singolo indirizzo di gestire più sessioni di comunicazione.
ms.assetid: 65e22e4e-e346-41c2-929a-ba0d1f7f1732
title: Contenere
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2df54b246c5bde5914a14b53dd56b71688d92a5e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103879874"
---
# <a name="hold"></a><span data-ttu-id="95076-103">Contenere</span><span class="sxs-lookup"><span data-stu-id="95076-103">Hold</span></span>

<span data-ttu-id="95076-104">L'operazione di attesa consente a un singolo indirizzo di gestire più sessioni di comunicazione.</span><span class="sxs-lookup"><span data-stu-id="95076-104">The hold operation allows a single address to handle multiple communications sessions.</span></span> <span data-ttu-id="95076-105">L'inserimento di una sessione in un disco rigido libera la riga o l'indirizzo dell'utente per effettuare altre chiamate.</span><span class="sxs-lookup"><span data-stu-id="95076-105">Placing a session on a hard hold frees the user's line/address to make other calls.</span></span> <span data-ttu-id="95076-106">Non è in genere possibile trasferire o includere una chiamata su un disco rigido in una chiamata di conferenza, ma è possibile eseguire una chiamata di consultazione.</span><span class="sxs-lookup"><span data-stu-id="95076-106">A call on hard hold typically cannot be transferred or included in a conference call, but a consultation call can.</span></span> <span data-ttu-id="95076-107">Le chiamate di consultazione vengono avviate mediante operazioni di [conferenza](conference-ovr.md) o di [trasferimento](transfer-ovr.md) .</span><span class="sxs-lookup"><span data-stu-id="95076-107">Consultation calls are initiated using [conference](conference-ovr.md) or [transfer](transfer-ovr.md) operations.</span></span>

<span data-ttu-id="95076-108">Dopo che una chiamata è stata posizionata correttamente in attesa, lo stato della chiamata passa in genere allo stato onHolding.</span><span class="sxs-lookup"><span data-stu-id="95076-108">After a call has been successfully placed on hold, the call state typically transitions to the onhold state.</span></span> <span data-ttu-id="95076-109">Mentre è in attesa una chiamata, l'applicazione può ricevere messaggi sulle modifiche di stato della chiamata mantenuta.</span><span class="sxs-lookup"><span data-stu-id="95076-109">While a call is on hold, the application can receive messages about state changes of the held call.</span></span> <span data-ttu-id="95076-110">Se, ad esempio, l'entità tenuta si blocca, lo stato della chiamata può passare a disconnected.</span><span class="sxs-lookup"><span data-stu-id="95076-110">For example, if the held party hangs up, the call state can transition to disconnected.</span></span>

<span data-ttu-id="95076-111">In una situazione con Bridge, è possibile che l'operazione di attesa non inserisca effettivamente la chiamata in attesa.</span><span class="sxs-lookup"><span data-stu-id="95076-111">In a bridged situation, the hold operation may not actually place the call on hold.</span></span> <span data-ttu-id="95076-112">Lo stato di altre stazioni della chiamata può governare, ad esempio il tentativo di "mantenere" una chiamata quando non è possibile partecipare ad altre stazioni. al contrario, la chiamata può essere semplicemente modificata nello stato inattivo mentre rimane connessa in altre stazioni.</span><span class="sxs-lookup"><span data-stu-id="95076-112">The status of other stations on the call can govern (for example, attempting to "hold" a call when other stations are participating is not possible); instead, the call can simply be changed to the inactive state while it remains connected at other stations.</span></span>

<span data-ttu-id="95076-113">Non tutti i provider di servizi supportano l'utilizzo di questa operazione.</span><span class="sxs-lookup"><span data-stu-id="95076-113">Not all service providers support use of this operation.</span></span>

<span data-ttu-id="95076-114">**TAPI 2. x:** Vedere [**lineHold**](/windows/win32/api/tapi/nf-tapi-linehold), [**lineUnhold**](/windows/win32/api/tapi/nf-tapi-lineunhold).</span><span class="sxs-lookup"><span data-stu-id="95076-114">**TAPI 2.x:** See [**lineHold**](/windows/win32/api/tapi/nf-tapi-linehold), [**lineUnhold**](/windows/win32/api/tapi/nf-tapi-lineunhold).</span></span>

<span data-ttu-id="95076-115">**TAPI 3. x:** Vedere [**ITBasicCallControl:: Holding**](/windows/desktop/api/tapi3if/nf-tapi3if-itbasiccallcontrol-hold).</span><span class="sxs-lookup"><span data-stu-id="95076-115">**TAPI 3.x:** See [**ITBasicCallControl::Hold**](/windows/desktop/api/tapi3if/nf-tapi3if-itbasiccallcontrol-hold).</span></span>

 

 
