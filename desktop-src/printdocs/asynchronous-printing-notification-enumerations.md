---
description: Le enumerazioni seguenti vengono utilizzate nella comunicazione asincrona tra le applicazioni e i componenti ospitati dallo spooler di stampa, ad esempio i driver della stampante e i monitoraggi delle porte.
ms.assetid: 732a552b-caf9-45da-9a9e-a325c4f6341b
title: Enumerazioni di notifiche di stampa asincrone
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6e2baf2a4476ac858a883dda55b2864a79d78cf6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106311563"
---
# <a name="asynchronous-printing-notification-enumerations"></a><span data-ttu-id="7a285-103">Enumerazioni di notifiche di stampa asincrone</span><span class="sxs-lookup"><span data-stu-id="7a285-103">Asynchronous Printing Notification Enumerations</span></span>

<span data-ttu-id="7a285-104">Le enumerazioni seguenti vengono utilizzate nella comunicazione asincrona tra le applicazioni e i componenti ospitati dallo spooler di stampa, ad esempio i driver della stampante e i monitoraggi delle porte.</span><span class="sxs-lookup"><span data-stu-id="7a285-104">The following enumerations are used in asynchronous communication between applications and components that are hosted by the print spooler, such as printer drivers and port monitors.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="7a285-105">Contenuto della sezione</span><span class="sxs-lookup"><span data-stu-id="7a285-105">In this section</span></span>



| <span data-ttu-id="7a285-106">Enumerazione</span><span class="sxs-lookup"><span data-stu-id="7a285-106">Enumeration</span></span>                                                                               | <span data-ttu-id="7a285-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="7a285-107">Description</span></span>                                                                                                                                                                                                    |
|-------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="7a285-108">**PrintAsyncNotifyConversationStyle**</span><span class="sxs-lookup"><span data-stu-id="7a285-108">**PrintAsyncNotifyConversationStyle**</span></span>](/windows/desktop/api/prnasnot/ne-prnasnot-printasyncnotifyconversationstyle)<br/> | <span data-ttu-id="7a285-109">Specifica se la comunicazione è bidirezionale o unidirezionale tra le applicazioni e i componenti ospitati dallo spooler di stampa, ad esempio i driver della stampante, i processori di stampa e i monitoraggi delle porte.</span><span class="sxs-lookup"><span data-stu-id="7a285-109">Specifies whether communication is bidirectional or unidirectional between applications and Print Spooler-hosted components such as printer drivers, print processors, and port monitors.</span></span><br/>           |
| [<span data-ttu-id="7a285-110">**PrintAsyncNotifyError**</span><span class="sxs-lookup"><span data-stu-id="7a285-110">**PrintAsyncNotifyError**</span></span>](/windows/desktop/api/prnasnot/ne-prnasnot-printasyncnotifyerror)<br/>                         | <span data-ttu-id="7a285-111">Specifica la parte del codice di errore del valore **HRESULT** restituito dopo un errore di notifica asincrono.</span><span class="sxs-lookup"><span data-stu-id="7a285-111">Specifies the error code portion of the **HRESULT** returned after an asynchronous notification failure.</span></span><br/>                                                                                            |
| [<span data-ttu-id="7a285-112">**PrintAsyncNotifyUserFilter**</span><span class="sxs-lookup"><span data-stu-id="7a285-112">**PrintAsyncNotifyUserFilter**</span></span>](/windows/desktop/api/prnasnot/ne-prnasnot-printasyncnotifyuserfilter)<br/>               | <span data-ttu-id="7a285-113">Specifica se le notifiche passeranno solo alle applicazioni in ascolto associate allo stesso utente del mittente ospitato dallo spooler di stampa o a un set più ampio di applicazioni in ascolto.</span><span class="sxs-lookup"><span data-stu-id="7a285-113">Specifies whether notifications will go only to listening applications that are associated with the same user as the Print Spooler-hosted sender, or go to a broader set of listening applications.</span></span><br/> |



 

 

 




