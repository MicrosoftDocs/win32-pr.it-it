---
description: TAPI modella i pulsanti e le lampade del telefono come coppie pulsante-lampada.
ms.assetid: e4c50bd6-a256-407f-af3b-b24383a30ea0
title: Pulsanti telefono
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ee3e65c34096c0cf043b85d80c9c726c6bef982d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103755111"
---
# <a name="phone-buttons"></a><span data-ttu-id="f94fe-103">Pulsanti telefono</span><span class="sxs-lookup"><span data-stu-id="f94fe-103">Phone Buttons</span></span>

<span data-ttu-id="f94fe-104">TAPI modella i pulsanti e le lampade di un telefono come coppie pulsante-lampada.</span><span class="sxs-lookup"><span data-stu-id="f94fe-104">TAPI models a phone's buttons and lamps as button-lamp pairs.</span></span> <span data-ttu-id="f94fe-105">Un pulsante senza lampada accanto o una lampada senza pulsante viene specificato usando un indicatore "fittizio" per la lampada o il pulsante mancante.</span><span class="sxs-lookup"><span data-stu-id="f94fe-105">A button with no lamp next to it or a lamp with no button is specified using a "dummy" indicator for the missing lamp or button.</span></span> <span data-ttu-id="f94fe-106">Un pulsante con più lampade viene modellato usando più coppie di pulsanti.</span><span class="sxs-lookup"><span data-stu-id="f94fe-106">A button with multiple lamps is modeled by using multiple button-lamp pairs.</span></span>

<span data-ttu-id="f94fe-107">È possibile impostare e recuperare le informazioni associate a un pulsante del telefono.</span><span class="sxs-lookup"><span data-stu-id="f94fe-107">Information associated with a phone button can be set and retrieved.</span></span> <span data-ttu-id="f94fe-108">Quando si preme un pulsante, alla funzione dell'applicazione viene inviato un messaggio di un [**\_ pulsante telefonico**](phone-button.md) .</span><span class="sxs-lookup"><span data-stu-id="f94fe-108">When a button is pressed, a [**PHONE\_BUTTON**](phone-button.md) message is sent to the application function.</span></span> <span data-ttu-id="f94fe-109">I parametri di questo messaggio sono un handle per il dispositivo telefonico e l'identificatore della lampada pulsante del pulsante premuto.</span><span class="sxs-lookup"><span data-stu-id="f94fe-109">The parameters of this message are a handle to the phone device and the button-lamp identifier of the button that was pressed.</span></span> <span data-ttu-id="f94fe-110">Ai pulsanti di tastiera da' 0' a' 9',' \* ' è \# ' vengono assegnati gli identificatori di pulsanti fissi da 0 a 11.</span><span class="sxs-lookup"><span data-stu-id="f94fe-110">The keypad buttons '0' through '9', '\*', and '\#' are assigned the fixed button-lamp identifiers 0 through 11.</span></span>

<span data-ttu-id="f94fe-111">Le funzioni associate ai pulsanti sono [**phoneSetButtonInfo**](/windows/desktop/api/Tapi/nf-tapi-phonesetbuttoninfo), che consente di impostare le informazioni associate a un pulsante in un dispositivo telefonico e [**phoneGetButtonInfo**](/windows/desktop/api/Tapi/nf-tapi-phonegetbuttoninfo), che restituisce informazioni associate a un pulsante in un dispositivo telefonico.</span><span class="sxs-lookup"><span data-stu-id="f94fe-111">The functions associated with buttons are [**phoneSetButtonInfo**](/windows/desktop/api/Tapi/nf-tapi-phonesetbuttoninfo), which sets the information associated with a button on a phone device, and [**phoneGetButtonInfo**](/windows/desktop/api/Tapi/nf-tapi-phonegetbuttoninfo), which returns information associated with a button on a phone device.</span></span> <span data-ttu-id="f94fe-112">Il \_ messaggio del pulsante telefonico viene inviato a un'applicazione quando viene premuto un pulsante sul telefono.</span><span class="sxs-lookup"><span data-stu-id="f94fe-112">The PHONE\_BUTTON message is sent to an application when a button on the phone is pressed.</span></span>

<span data-ttu-id="f94fe-113">Le informazioni associate a un pulsante non contengono alcun significato semantico per quanto riguarda TAPI.</span><span class="sxs-lookup"><span data-stu-id="f94fe-113">The information associated with a button does not carry any semantic meaning as far as TAPI is concerned.</span></span> <span data-ttu-id="f94fe-114">È utile per le applicazioni specifiche del dispositivo che comprendono il significato di queste informazioni per un determinato dispositivo telefonico o per la visualizzazione all'utente, ad esempio la Guida in linea.</span><span class="sxs-lookup"><span data-stu-id="f94fe-114">It is useful for device-specific applications that understand the meaning of this information for a given phone device, or for display to the user, such as online help.</span></span>

 

 



