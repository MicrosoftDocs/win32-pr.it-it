---
description: Uso dei menu DVD
ms.assetid: 8c5f8072-b74f-4e15-8991-73bcc4145fd2
title: Uso dei menu DVD
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 113647a37200762b5eaf0a9ac231dea74ad19925
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106320048"
---
# <a name="working-with-dvd-menus"></a><span data-ttu-id="dbac8-103">Uso dei menu DVD</span><span class="sxs-lookup"><span data-stu-id="dbac8-103">Working With DVD Menus</span></span>

<span data-ttu-id="dbac8-104">Il navigatore DVD potrebbe visualizzare un menu quando l'utente attiva un pulsante o quando lo strumento di navigazione entra nel primo dominio di riproduzione.</span><span class="sxs-lookup"><span data-stu-id="dbac8-104">The DVD Navigator might show a menu when the user activates a button, or when the Navigator enters the First Play domain.</span></span> <span data-ttu-id="dbac8-105">Per visualizzare un menu a livello di codice, chiamare il metodo [**IDVDControl2:: ShowMenu**](/windows/desktop/api/Strmif/nf-strmif-idvdcontrol2-showmenu) .</span><span class="sxs-lookup"><span data-stu-id="dbac8-105">To show a menu programmatically, call the [**IDvdControl2::ShowMenu**](/windows/desktop/api/Strmif/nf-strmif-idvdcontrol2-showmenu) method.</span></span>

<span data-ttu-id="dbac8-106">Sono disponibili diversi modi per selezionare i pulsanti di menu a livello di codice:</span><span class="sxs-lookup"><span data-stu-id="dbac8-106">There are several ways to select menu buttons programmatically:</span></span>

-   <span data-ttu-id="dbac8-107">Per selezionare un pulsante in base al numero, chiamare [**IDVDControl2:: SelectButton**](/windows/desktop/api/Strmif/nf-strmif-idvdcontrol2-selectbutton).</span><span class="sxs-lookup"><span data-stu-id="dbac8-107">To select a button by number, call [**IDvdControl2::SelectButton**](/windows/desktop/api/Strmif/nf-strmif-idvdcontrol2-selectbutton).</span></span> <span data-ttu-id="dbac8-108">I pulsanti sono numerati da 1 a 36.</span><span class="sxs-lookup"><span data-stu-id="dbac8-108">Buttons are numbered 1 to 36.</span></span> <span data-ttu-id="dbac8-109">Il metodo [**IDvdInfo2:: GetCurrentButton**](/windows/desktop/api/Strmif/nf-strmif-idvdinfo2-getcurrentbutton) restituisce il numero di pulsanti disponibili.</span><span class="sxs-lookup"><span data-stu-id="dbac8-109">The [**IDvdInfo2::GetCurrentButton**](/windows/desktop/api/Strmif/nf-strmif-idvdinfo2-getcurrentbutton) method returns the number of available buttons.</span></span>
-   <span data-ttu-id="dbac8-110">Per selezionare un pulsante relativo alla posizione del pulsante attualmente selezionato, chiamare [**IDVDControl2:: SelectRelativeButton**](/windows/desktop/api/Strmif/nf-strmif-idvdcontrol2-selectrelativebutton).</span><span class="sxs-lookup"><span data-stu-id="dbac8-110">To select a button relative to the position of the currently selected button, call [**IDvdControl2::SelectRelativeButton**](/windows/desktop/api/Strmif/nf-strmif-idvdcontrol2-selectrelativebutton).</span></span> <span data-ttu-id="dbac8-111">È possibile selezionare un pulsante nella direzione verso l'alto, verso il basso, verso sinistra o verso destra.</span><span class="sxs-lookup"><span data-stu-id="dbac8-111">You can select a button in the up, down, left, or right direction.</span></span>
-   <span data-ttu-id="dbac8-112">Per selezionare un pulsante in base alle coordinate all'interno della finestra, chiamare [**IDVDControl2:: SelectAtPosition**](/windows/desktop/api/Strmif/nf-strmif-idvdcontrol2-selectatposition).</span><span class="sxs-lookup"><span data-stu-id="dbac8-112">To select a button by its coordinates within the window, call [**IDvdControl2::SelectAtPosition**](/windows/desktop/api/Strmif/nf-strmif-idvdcontrol2-selectatposition).</span></span> <span data-ttu-id="dbac8-113">Questo metodo accetta le coordinate (x, y) relative all'area client della finestra del video.</span><span class="sxs-lookup"><span data-stu-id="dbac8-113">This method takes (x,y) coordinates relative to the client area of the video window.</span></span> <span data-ttu-id="dbac8-114">Per la modalità senza finestra, si tratta della finestra dell'applicazione. Se non è presente alcun pulsante in tale posizione, il metodo restituisce \_ il \_ pulsante VFW E DVD \_ No \_ .</span><span class="sxs-lookup"><span data-stu-id="dbac8-114">(For windowless mode, this is the application window.) If there is no button at that location, the method returns VFW\_E\_DVD\_NO\_BUTTON.</span></span>

<span data-ttu-id="dbac8-115">Sono inoltre disponibili diversi modi per attivare un pulsante:</span><span class="sxs-lookup"><span data-stu-id="dbac8-115">In addition, there are several ways to activate a button:</span></span>

-   <span data-ttu-id="dbac8-116">Per attivare un pulsante in base al numero, chiamare [**IDVDControl2:: SelectAndActivateButton**](/windows/desktop/api/Strmif/nf-strmif-idvdcontrol2-selectandactivatebutton).</span><span class="sxs-lookup"><span data-stu-id="dbac8-116">To activate a button by number, call [**IDvdControl2::SelectAndActivateButton**](/windows/desktop/api/Strmif/nf-strmif-idvdcontrol2-selectandactivatebutton).</span></span>
-   <span data-ttu-id="dbac8-117">Per attivare un pulsante in base alle coordinate, chiamare [**IDVDControl2:: ActivateAtPosition**](/windows/desktop/api/Strmif/nf-strmif-idvdcontrol2-activateatposition).</span><span class="sxs-lookup"><span data-stu-id="dbac8-117">To activate a button by its coordinates, call [**IDvdControl2::ActivateAtPosition**](/windows/desktop/api/Strmif/nf-strmif-idvdcontrol2-activateatposition).</span></span>
-   <span data-ttu-id="dbac8-118">Per attivare il pulsante attualmente selezionato, chiamare [**IDVDControl2:: ActivateButton**](/windows/desktop/api/Strmif/nf-strmif-idvdcontrol2-activatebutton).</span><span class="sxs-lookup"><span data-stu-id="dbac8-118">To activate the button that is currently selected, call [**IDvdControl2::ActivateButton**](/windows/desktop/api/Strmif/nf-strmif-idvdcontrol2-activatebutton).</span></span> <span data-ttu-id="dbac8-119">Se non è selezionato alcun pulsante, il metodo restituisce \_ il \_ pulsante VFW E DVD \_ No \_ .</span><span class="sxs-lookup"><span data-stu-id="dbac8-119">If no button is selected, the method returns VFW\_E\_DVD\_NO\_BUTTON.</span></span>

<span data-ttu-id="dbac8-120">Tenere presente che la selezione di un pulsante evidenzia semplicemente i bordi.</span><span class="sxs-lookup"><span data-stu-id="dbac8-120">Keep in mind that selecting a button merely highlights its borders.</span></span> <span data-ttu-id="dbac8-121">Per far sì che il comando associato venga attivato, è necessario attivare il pulsante.</span><span class="sxs-lookup"><span data-stu-id="dbac8-121">To cause the associated command to be fired, the button must be activated.</span></span> <span data-ttu-id="dbac8-122">L'attivazione di un pulsante a livello di codice può essere eseguita in vari modi, ma il pulsante deve sempre essere selezionato prima di poter essere attivato.</span><span class="sxs-lookup"><span data-stu-id="dbac8-122">Activating a button programmatically can be done in various ways, but the button must always be selected before it can be activated.</span></span>

## <a name="related-topics"></a><span data-ttu-id="dbac8-123">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="dbac8-123">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="dbac8-124">Applicazioni DVD</span><span class="sxs-lookup"><span data-stu-id="dbac8-124">DVD Applications</span></span>](dvd-applications.md)
</dt> </dl>

 

 



