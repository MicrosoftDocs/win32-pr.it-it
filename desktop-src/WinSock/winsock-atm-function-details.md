---
description: In base alla tassonomia definita per gli schemi multipoint/multicast indipendenti dal protocollo di Windows Sockets 2, l'ATM rientra nella categoria dei dati radice e dei piani di controllo rooted.
ms.assetid: 309afa65-2cc4-4b7b-9968-4c4efb2d10a3
title: Dettagli della funzione ATM di Winsock
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5e82ca0531272490c2d3189467186535a63d6ba2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104130406"
---
# <a name="winsock-atm-function-details"></a><span data-ttu-id="ec40e-103">Dettagli della funzione ATM di Winsock</span><span class="sxs-lookup"><span data-stu-id="ec40e-103">Winsock ATM Function Details</span></span>

<span data-ttu-id="ec40e-104">In base alla tassonomia definita per gli schemi multipoint/multicast indipendenti dal protocollo di Windows Sockets 2, l'ATM rientra nella categoria dei dati radice e dei piani di controllo rooted.</span><span class="sxs-lookup"><span data-stu-id="ec40e-104">Based on the taxonomy defined for Windows Sockets 2 protocol-independent multipoint/multicast schemes, ATM falls into the category of rooted data and rooted control planes.</span></span> <span data-ttu-id="ec40e-105">(Per altre informazioni, vedere la specifica dell'API di Windows Sockets 2, Appendice D). Un'applicazione che funge da radice creerebbe i \_ socket radice c e le controparti in esecuzione nei nodi foglia utilizzeranno i \_ socket foglia c.</span><span class="sxs-lookup"><span data-stu-id="ec40e-105">(See the Windows Sockets 2 API Specification, Appendix D for more information.) An application acting as the root would create c\_root sockets, and counterparts running on leaf nodes would utilize c\_leaf sockets.</span></span> <span data-ttu-id="ec40e-106">Per aggiungere nuovi nodi foglia, l'applicazione radice utilizzerà [**WSAJoinLeaf**](/windows/desktop/api/Winsock2/nf-winsock2-wsajoinleaf) .</span><span class="sxs-lookup"><span data-stu-id="ec40e-106">The root application will use [**WSAJoinLeaf**](/windows/desktop/api/Winsock2/nf-winsock2-wsajoinleaf) to add new leaf nodes.</span></span> <span data-ttu-id="ec40e-107">Le applicazioni corrispondenti nei nodi foglia avranno impostato i \_ socket foglia c nella modalità di ascolto.</span><span class="sxs-lookup"><span data-stu-id="ec40e-107">The corresponding applications on the leaf nodes will have set their c\_leaf sockets into the listening mode.</span></span> <span data-ttu-id="ec40e-108">**WSAJoinLeaf** con un \_ socket radice c specificato verrà mappato al messaggio di installazione Q. 2931 (per la prima foglia) o al messaggio di aggiunta entità (per qualsiasi foglia successiva).</span><span class="sxs-lookup"><span data-stu-id="ec40e-108">**WSAJoinLeaf** with a c\_root socket specified will be mapped to the Q.2931 SETUP message (for the first leaf) or ADD PARTY message (for any subsequent leaves).</span></span>

> [!Note]  
> <span data-ttu-id="ec40e-109">I parametri QoS specificati in **WSAJoinLeaf** per le foglie successive devono essere ignorati in base alla specifica UNI del forum ATM.</span><span class="sxs-lookup"><span data-stu-id="ec40e-109">The QoS parameters specified in **WSAJoinLeaf** for any subsequent leaves should be ignored per the ATM Forum UNI specification.</span></span>

 

<span data-ttu-id="ec40e-110">Il join avviato da foglia non fa parte del bancomat UNI 3,1, ma è supportato in ATM UNI 4,0.</span><span class="sxs-lookup"><span data-stu-id="ec40e-110">The leaf-initiated join is not part of the ATM UNI 3.1, but is supported in the ATM UNI 4.0.</span></span> <span data-ttu-id="ec40e-111">Pertanto [](/windows/desktop/api/Winsock2/nf-winsock2-wsajoinleaf) \_ , è possibile eseguire il mapping di WSAJoinLeaf con un socket foglia c al messaggio ATM UNI 4,0 appropriato.</span><span class="sxs-lookup"><span data-stu-id="ec40e-111">Thus [**WSAJoinLeaf**](/windows/desktop/api/Winsock2/nf-winsock2-wsajoinleaf) with a c\_leaf socket specified can be mapped to the appropriate ATM UNI 4.0 message.</span></span>

<span data-ttu-id="ec40e-112">Il parametro AAL e la negoziazione B-LLI sono supportati tramite la modifica delle IEs corrispondenti nel parametro *lpSQOS* alla chiamata della funzione Condition specificata in [**WSAAccept**](/windows/desktop/api/Winsock2/nf-winsock2-wsaaccept).</span><span class="sxs-lookup"><span data-stu-id="ec40e-112">The AAL Parameter and B-LLI negotiation is supported through the modification of the corresponding IEs in the *lpSQOS* parameter upon the invocation of the condition function specified in [**WSAAccept**](/windows/desktop/api/Winsock2/nf-winsock2-wsaaccept).</span></span>

> [!Note]  
> <span data-ttu-id="ec40e-113">È possibile modificare solo determinati campi in queste due IEs.</span><span class="sxs-lookup"><span data-stu-id="ec40e-113">Only certain fields in those two IEs can be modified.</span></span> <span data-ttu-id="ec40e-114">Per informazioni dettagliate, vedere la specifica UNI del forum ATM Appendice C e Appendice F.</span><span class="sxs-lookup"><span data-stu-id="ec40e-114">See the ATM Forum UNI specification Appendix C and Appendix F for details.</span></span>

 

 

 



