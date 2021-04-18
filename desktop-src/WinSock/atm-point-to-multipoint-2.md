---
description: ATM rientra nella categoria dei dati con radice e dei piani di controllo rooted.
ms.assetid: 8e355efe-2903-49c1-a9b3-792b07bd2995
title: Da punto ATM a MultiPoint
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ba17616feadfe1c8bf87ee8468dd967af73452c6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106307052"
---
# <a name="atm-point-to-multipoint"></a><span data-ttu-id="adade-103">Da punto ATM a MultiPoint</span><span class="sxs-lookup"><span data-stu-id="adade-103">ATM Point to Multipoint</span></span>

<span data-ttu-id="adade-104">ATM rientra nella categoria dei dati con radice e dei piani di controllo rooted.</span><span class="sxs-lookup"><span data-stu-id="adade-104">ATM falls into the category of rooted data and rooted control planes.</span></span> <span data-ttu-id="adade-105">Un'applicazione che funge da radice creerebbe i \_ socket radice c e le controparti in esecuzione nei nodi foglia utilizzeranno i \_ socket foglia c.</span><span class="sxs-lookup"><span data-stu-id="adade-105">An application acting as the root would create c\_root sockets and counterparts running on leaf nodes would utilize c\_leaf sockets.</span></span> <span data-ttu-id="adade-106">L'applicazione radice USA [**WSAJoinLeaf**](/windows/desktop/api/Winsock2/nf-winsock2-wsajoinleaf) per aggiungere nuovi nodi foglia.</span><span class="sxs-lookup"><span data-stu-id="adade-106">The root application uses [**WSAJoinLeaf**](/windows/desktop/api/Winsock2/nf-winsock2-wsajoinleaf) to add new leaf nodes.</span></span> <span data-ttu-id="adade-107">Le applicazioni corrispondenti nei nodi foglia avranno impostato i \_ socket foglia c in modalità di ascolto.</span><span class="sxs-lookup"><span data-stu-id="adade-107">The corresponding applications on the leaf nodes will have set their c\_leaf sockets into listen mode.</span></span> <span data-ttu-id="adade-108">**WSAJoinLeaf** con un \_ socket radice c specificato viene mappato al messaggio Q. 2931 ADDPARTY.</span><span class="sxs-lookup"><span data-stu-id="adade-108">**WSAJoinLeaf** with a c\_root socket specified is mapped to the Q.2931 ADDPARTY message.</span></span> <span data-ttu-id="adade-109">Il join avviato da foglia non è supportato in ATM UNI 3,1, ma è supportato in ATM UNI 4,0.</span><span class="sxs-lookup"><span data-stu-id="adade-109">The leaf-initiated join is not supported in ATM UNI 3.1, but is supported in ATM UNI 4.0.</span></span> <span data-ttu-id="adade-110">Di conseguenza, **WSAJoinLeaf** con un \_ socket foglia c specificato viene mappato al messaggio ATM UNI 4,0 appropriato.</span><span class="sxs-lookup"><span data-stu-id="adade-110">Thus **WSAJoinLeaf** with a c\_leaf socket specified is mapped to the appropriate ATM UNI 4.0 message.</span></span>

<span data-ttu-id="adade-111">Ci sono considerazioni aggiuntive da tenere presenti per l'ATM da punto a multipoint:</span><span class="sxs-lookup"><span data-stu-id="adade-111">There are additional considerations to bear in mind for ATM point-to-multipoint:</span></span>

-   <span data-ttu-id="adade-112">L'aggiunta di nuove foglie alla sessione ATM da punto a MultiPoint è solo basata su invito.</span><span class="sxs-lookup"><span data-stu-id="adade-112">The addition of new leaves to the ATM point-to-multipoint session is invitation-based only.</span></span> <span data-ttu-id="adade-113">La radice invita le foglie, che hanno già la chiamata di funzione [**Accept**](/windows/desktop/api/Winsock2/nf-winsock2-accept) , chiamando la funzione [**WSAJoinLeaf**](/windows/desktop/api/Winsock2/nf-winsock2-wsajoinleaf) .</span><span class="sxs-lookup"><span data-stu-id="adade-113">The root invites leaves — which have already their [**accept**](/windows/desktop/api/Winsock2/nf-winsock2-accept) function call — by calling the [**WSAJoinLeaf**](/windows/desktop/api/Winsock2/nf-winsock2-wsajoinleaf) function.</span></span>
-   <span data-ttu-id="adade-114">Il flusso di dati in una sessione ATM da punto a MultiPoint è da solo da radice a foglia; leaves non può usare la stessa sessione per inviare informazioni alla radice.</span><span class="sxs-lookup"><span data-stu-id="adade-114">The flow of data in an ATM point-to-multipoint session is from root-to-leaves only; leaves cannot use the same session to send information to the root.</span></span>
-   <span data-ttu-id="adade-115">È consentita una sola foglia per ogni adapter ATM.</span><span class="sxs-lookup"><span data-stu-id="adade-115">Only one leaf per ATM adapter is allowed.</span></span>

 

 



