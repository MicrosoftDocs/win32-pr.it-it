---
description: L'interfaccia utente della smart card è una singola finestra di dialogo comune che consente all'utente di specificare o cercare una smart card da aprire, ovvero connettersi e utilizzare in un'applicazione.
ms.assetid: a64a617a-b2ae-471f-a88f-a73f0fc3a791
title: Interfaccia utente della smart card
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fc558446516149529e9a98d28aa9fe94f80b2777
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106316221"
---
# <a name="smart-card-user-interface"></a><span data-ttu-id="84be3-103">Interfaccia utente della smart card</span><span class="sxs-lookup"><span data-stu-id="84be3-103">Smart Card User Interface</span></span>

<span data-ttu-id="84be3-104">L' [*interfaccia utente*](../secgloss/u-gly.md) della smart card è una singola finestra di [*dialogo comune*](../secgloss/s-gly.md) che consente all'utente di specificare o cercare una smart card da aprire, ovvero connettersi e utilizzare in un'applicazione.</span><span class="sxs-lookup"><span data-stu-id="84be3-104">The smart card [*user interface*](../secgloss/u-gly.md) (UI) is a single [*common dialog box*](../secgloss/s-gly.md) that lets the user specify or search for a smart card to open (that is, connect to and use in an application).</span></span>

<span data-ttu-id="84be3-105">Di seguito sono illustrati due modi per utilizzare la finestra di dialogo comune.</span><span class="sxs-lookup"><span data-stu-id="84be3-105">Following are two ways you can use the common dialog box.</span></span> <span data-ttu-id="84be3-106">Entrambi presuppongono che venga visualizzata l'interfaccia utente della finestra di dialogo.</span><span class="sxs-lookup"><span data-stu-id="84be3-106">Both assume that the dialog box UI will be displayed.</span></span> <span data-ttu-id="84be3-107">Per ulteriori informazioni, vedere [**OPENCARDNAME**](/windows/desktop/api/Winscard/ns-winscard-opencardnamea).</span><span class="sxs-lookup"><span data-stu-id="84be3-107">For more information, see [**OPENCARDNAME**](/windows/desktop/api/Winscard/ns-winscard-opencardnamea).</span></span>

<span data-ttu-id="84be3-108">**Per selezionare una smart card da aprire**</span><span class="sxs-lookup"><span data-stu-id="84be3-108">**To select a smart card to open**</span></span>

1.  <span data-ttu-id="84be3-109">Dichiarare una variabile di tipo **OPENCARDNAME**.</span><span class="sxs-lookup"><span data-stu-id="84be3-109">Declare a variable of type **OPENCARDNAME**.</span></span>
2.  <span data-ttu-id="84be3-110">Fornire informazioni sufficienti nella finestra di dialogo comune per limitare la ricerca di una smart card che l'applicazione chiamante sta cercando.</span><span class="sxs-lookup"><span data-stu-id="84be3-110">Provide enough information in the common dialog box to narrow the search for a smart card that the calling application is looking for.</span></span> <span data-ttu-id="84be3-111">Ciò include la specifica di **lpstrGroupNames**, **lpstrCardNames** e **rgguidInterfaces**.</span><span class="sxs-lookup"><span data-stu-id="84be3-111">This includes specifying **lpstrGroupNames**, **lpstrCardNames**, and **rgguidInterfaces**.</span></span> <span data-ttu-id="84be3-112">Questo include anche la definizione di una modalità di condivisione preferita e di un protocollo da usare quando la finestra di dialogo comune si connette alla scheda usando i membri **dwShareMode** e **DwPreferredProtocols** della struttura [**OPENCARDNAME**](/windows/desktop/api/Winscard/ns-winscard-opencardnamea) .</span><span class="sxs-lookup"><span data-stu-id="84be3-112">This also includes specifying a preferred share mode and protocol to use when the common dialog box connects to the card by using the **dwShareMode** and **dwPreferredProtocols** members of the [**OPENCARDNAME**](/windows/desktop/api/Winscard/ns-winscard-opencardnamea) structure.</span></span>
3.  <span data-ttu-id="84be3-113">Chiamare la funzione [**GetOpenCardName**](/windows/desktop/api/Winscard/nf-winscard-getopencardnamea) per visualizzare la finestra di dialogo comune all'utente.</span><span class="sxs-lookup"><span data-stu-id="84be3-113">Call the [**GetOpenCardName**](/windows/desktop/api/Winscard/nf-winscard-getopencardnamea) function to display the common dialog box to the user.</span></span> <span data-ttu-id="84be3-114">Verrà visualizzata una semplice riga di informazioni della guida e, se viene trovata una delle schede richieste, la scheda verrà evidenziata nella visualizzazione.</span><span class="sxs-lookup"><span data-stu-id="84be3-114">A simple help information line will be displayed, and if one of the cards being requested is found, the card will be highlighted in the display.</span></span> <span data-ttu-id="84be3-115">Per le ricerche con più nomi di carta, verrà evidenziato il primo lettore che contiene una delle schede preferite.</span><span class="sxs-lookup"><span data-stu-id="84be3-115">For multiple card name searches, the first reader that contains one of the preferred cards will be highlighted.</span></span>
4.  <span data-ttu-id="84be3-116">L'utente seleziona quindi una scheda, fa clic su **OK** e si connette alla smart card.</span><span class="sxs-lookup"><span data-stu-id="84be3-116">The user then selects a card, clicks **OK**, and connects to the smart card.</span></span>

<span data-ttu-id="84be3-117">**Per cercare una scheda specifica**</span><span class="sxs-lookup"><span data-stu-id="84be3-117">**To search for a specific card**</span></span>

1.  <span data-ttu-id="84be3-118">Dichiarare una variabile di tipo **OPENCARDNAME**.</span><span class="sxs-lookup"><span data-stu-id="84be3-118">Declare a variable of type **OPENCARDNAME**.</span></span>
2.  <span data-ttu-id="84be3-119">Fornire informazioni sufficienti nella finestra di dialogo comune per limitare la ricerca di una smart card che l'applicazione chiamante sta cercando.</span><span class="sxs-lookup"><span data-stu-id="84be3-119">Provide enough information in the common dialog box to narrow the search for a smart card that the calling application is looking for.</span></span> <span data-ttu-id="84be3-120">Ciò include la specifica di **lpstrGroupNames**, **lpstrCardNames** e **rgguidInterfaces**.</span><span class="sxs-lookup"><span data-stu-id="84be3-120">This includes specifying **lpstrGroupNames**, **lpstrCardNames**, and **rgguidInterfaces**.</span></span>
3.  <span data-ttu-id="84be3-121">Creare le funzioni di callback **Connect**, **Check** e **Disconnect** e impostare i membri dati **lpfnConnect**, **lpfnCheck** e **lpfnDisconnect** in modo appropriato.</span><span class="sxs-lookup"><span data-stu-id="84be3-121">Create the **Connect**, **Check**, and **Disconnect** callback functions, and set the **lpfnConnect**, **lpfnCheck**, and **lpfnDisconnect** data members appropriately.</span></span>
    > [!Note]  
    > <span data-ttu-id="84be3-122">Tutte e tre le funzioni e i membri devono essere disponibili quando si utilizza la finestra di dialogo comune in questo modo.</span><span class="sxs-lookup"><span data-stu-id="84be3-122">All three functions and members must be available when using the common dialog box in this way.</span></span>

     

4.  <span data-ttu-id="84be3-123">Chiamare la funzione della finestra di dialogo comune [**GetOpenCardName**](/windows/desktop/api/Winscard/nf-winscard-getopencardnamea) .</span><span class="sxs-lookup"><span data-stu-id="84be3-123">Call the [**GetOpenCardName**](/windows/desktop/api/Winscard/nf-winscard-getopencardnamea) common dialog box function.</span></span>
5.  <span data-ttu-id="84be3-124">Nella finestra di dialogo comune sarà quindi possibile cercare le schede richieste.</span><span class="sxs-lookup"><span data-stu-id="84be3-124">The common dialog box will then search for the requested cards.</span></span> <span data-ttu-id="84be3-125">Se viene trovato un nome di scheda o una [*stringa ATR*](../secgloss/a-gly.md) corrispondente, le funzioni di callback **Connect**, **Check** e **Disconnect** verranno chiamate in sequenza.</span><span class="sxs-lookup"><span data-stu-id="84be3-125">If a matching card name or [*ATR string*](../secgloss/a-gly.md) is found, the **Connect**, **Check**, and **Disconnect** callback functions will be called in sequence.</span></span> <span data-ttu-id="84be3-126">Se una scheda supera la routine di **controllo** , ovvero il callback di **controllo** restituisce **true**, questa scheda viene evidenziata nella visualizzazione dell'utente.</span><span class="sxs-lookup"><span data-stu-id="84be3-126">If a card passes the **Check** routine (that is, the **Check** callback returns **TRUE**), this card is highlighted in the display to the user.</span></span>
    > [!Note]  
    > <span data-ttu-id="84be3-127">Se vengono specificati più nomi di schede, il primo lettore che contiene una delle schede richieste e passa la routine di **controllo** sarà la scheda selezionata.</span><span class="sxs-lookup"><span data-stu-id="84be3-127">If multiple card names are given, the first reader that contains one of the requested cards and passes the **Check** routine will be the selected card.</span></span>

     

6.  <span data-ttu-id="84be3-128">Se non viene trovata alcuna corrispondenza, viene visualizzata una finestra di dialogo comune.</span><span class="sxs-lookup"><span data-stu-id="84be3-128">If no matches are found, a common dialog box will appear.</span></span>

 

 
