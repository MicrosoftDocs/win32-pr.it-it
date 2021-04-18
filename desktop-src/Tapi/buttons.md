---
description: La telefonia Microsoft modella i pulsanti e le lampade del telefono come coppie pulsante-lampada.
ms.assetid: 6ac912bb-8d2b-4aa3-a6e8-af86fbaabd58
title: Pulsanti (API di telefonia)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ddd1fc18e02331f98f4dbb98cfea7d9df2ca7f33
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106309974"
---
# <a name="buttons-telephony-api"></a><span data-ttu-id="bb030-103">Pulsanti (API di telefonia)</span><span class="sxs-lookup"><span data-stu-id="bb030-103">Buttons (Telephony API)</span></span>

<span data-ttu-id="bb030-104">La telefonia Microsoft modella i pulsanti e le lampade di un telefono come coppie di pulsanti.</span><span class="sxs-lookup"><span data-stu-id="bb030-104">Microsoft Telephony models a phone's buttons and lamps as button-lamp pairs.</span></span> <span data-ttu-id="bb030-105">Un pulsante senza lampada accanto o una lampada senza pulsante viene specificato usando un indicatore fittizio per la lampada o il pulsante mancante.</span><span class="sxs-lookup"><span data-stu-id="bb030-105">A button with no lamp next to it, or a lamp with no button is specified using a dummy indicator for the missing lamp or button.</span></span> <span data-ttu-id="bb030-106">Un pulsante con più lampade viene modellato usando più coppie di pulsanti.</span><span class="sxs-lookup"><span data-stu-id="bb030-106">A button with multiple lamps is modeled by using multiple button-lamp pairs.</span></span>

<span data-ttu-id="bb030-107">È possibile impostare e recuperare le informazioni associate a un pulsante del telefono.</span><span class="sxs-lookup"><span data-stu-id="bb030-107">Information associated with a phone button can be set and retrieved.</span></span> <span data-ttu-id="bb030-108">Quando si preme un pulsante, il provider di servizi invia un messaggio di un [**\_ pulsante telefonico**](/previous-versions/windows/desktop/legacy/ms725254(v=vs.85)) alla funzione di callback TAPI.</span><span class="sxs-lookup"><span data-stu-id="bb030-108">When a button is pressed, the service provider sends a [**PHONE\_BUTTON**](/previous-versions/windows/desktop/legacy/ms725254(v=vs.85)) message to the TAPI callback function.</span></span> <span data-ttu-id="bb030-109">I parametri di questo messaggio sono un handle per il dispositivo telefonico e l'identificatore pulsante/lampada del pulsante premuto.</span><span class="sxs-lookup"><span data-stu-id="bb030-109">Parameters of this message are a handle to the phone device and the button/lamp identifier of the button that was pressed.</span></span> <span data-ttu-id="bb030-110">Al pulsante del tastierino da' 0' a' 9',' \* ' è \# ' vengono assegnati gli identificatori di pulsante/lampo fissi da 0 a 11.</span><span class="sxs-lookup"><span data-stu-id="bb030-110">The keypad button '0' through '9', '\*', and '\#' are assigned fixed button/lamp identifiers 0 through 11.</span></span>

<span data-ttu-id="bb030-111">La funzione [**TSPI \_ phoneSetButtonInfo**](/windows/win32/api/tspi/nf-tspi-tspi_phonesetbuttoninfo) imposta le informazioni associate a un pulsante in un dispositivo telefonico.</span><span class="sxs-lookup"><span data-stu-id="bb030-111">The function [**TSPI\_phoneSetButtonInfo**](/windows/win32/api/tspi/nf-tspi-tspi_phonesetbuttoninfo) sets the information associated with a button on a phone device.</span></span> <span data-ttu-id="bb030-112">[**TSPI \_ phoneGetButtonInfo**](/windows/win32/api/tspi/nf-tspi-tspi_phonegetbuttoninfo) restituisce le informazioni associate a un pulsante in un dispositivo telefonico.</span><span class="sxs-lookup"><span data-stu-id="bb030-112">[**TSPI\_phoneGetButtonInfo**](/windows/win32/api/tspi/nf-tspi-tspi_phonegetbuttoninfo) returns information associated with a button on a phone device.</span></span> <span data-ttu-id="bb030-113">Il provider di servizi invia un \_ messaggio di pulsante telefonico alla funzione di callback TAPI quando viene premuto un pulsante sul telefono.</span><span class="sxs-lookup"><span data-stu-id="bb030-113">The service provider sends a PHONE\_BUTTON message to the TAPI callback function when a button on the phone is pressed.</span></span>

<span data-ttu-id="bb030-114">Le informazioni associate a un pulsante non contengono alcun significato semantico per quanto concerne TSPI.</span><span class="sxs-lookup"><span data-stu-id="bb030-114">The information associated with a button does not carry any semantic meaning as far as TSPI is concerned.</span></span> <span data-ttu-id="bb030-115">È utile per le applicazioni specifiche del dispositivo che interpretano queste informazioni per un determinato dispositivo telefonico o per la visualizzazione all'utente, ad esempio nel sistema della Guida di un'applicazione.</span><span class="sxs-lookup"><span data-stu-id="bb030-115">It is useful for device-specific applications that interpret this information for a given phone device, or for display to the user, such as in an application's help system.</span></span>

 

 
