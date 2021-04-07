---
description: Le interfacce seguenti vengono utilizzate nella comunicazione asincrona tra le applicazioni e i componenti ospitati dallo spooler di stampa, ad esempio i driver della stampante e i monitoraggi delle porte.
ms.assetid: e96c957f-3972-4afc-9d76-a4725b8688f8
title: Interfacce di notifica di stampa asincrone
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c7da8d320b33224e81852542e39f435b45b6dab5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103759557"
---
# <a name="asynchronous-printing-notification-interfaces"></a><span data-ttu-id="a768b-103">Interfacce di notifica di stampa asincrone</span><span class="sxs-lookup"><span data-stu-id="a768b-103">Asynchronous Printing Notification Interfaces</span></span>

<span data-ttu-id="a768b-104">Le interfacce seguenti vengono utilizzate nella comunicazione asincrona tra le applicazioni e i componenti ospitati dallo spooler di stampa, ad esempio i driver della stampante e i monitoraggi delle porte.</span><span class="sxs-lookup"><span data-stu-id="a768b-104">The following interfaces are used in asynchronous communication between applications and components that are hosted by the print spooler, such as printer drivers and port monitors.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="a768b-105">Contenuto della sezione</span><span class="sxs-lookup"><span data-stu-id="a768b-105">In this section</span></span>



| <span data-ttu-id="a768b-106">Interfaccia</span><span class="sxs-lookup"><span data-stu-id="a768b-106">Interface</span></span>                                                                     | <span data-ttu-id="a768b-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="a768b-107">Description</span></span>                                                                                                                                                                                                                                                   |
|-------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="a768b-108">**IPrintAsyncNotifyCallback**</span><span class="sxs-lookup"><span data-stu-id="a768b-108">**IPrintAsyncNotifyCallback**</span></span>](/windows/desktop/api/prnasnot/nn-prnasnot-iprintasyncnotifycallback)<br/>     | <span data-ttu-id="a768b-109">Crea e gestisce un canale di comunicazione utilizzato dalle applicazioni e dai componenti ospitati dallo spooler di stampa.</span><span class="sxs-lookup"><span data-stu-id="a768b-109">Creates and manages a communication channel used by applications and components that are hosted by the print spooler.</span></span><br/>                                                                                                                              |
| [<span data-ttu-id="a768b-110">**IPrintAsyncNotifyChannel**</span><span class="sxs-lookup"><span data-stu-id="a768b-110">**IPrintAsyncNotifyChannel**</span></span>](/windows/desktop/api/prnasnot/nn-prnasnot-iprintasyncnotifychannel)<br/>       | <span data-ttu-id="a768b-111">Rappresenta un canale di comunicazione utilizzato dai componenti ospitati dallo spooler di stampa per inviare notifiche alle applicazioni.</span><span class="sxs-lookup"><span data-stu-id="a768b-111">Represents a communication channel that components that are hosted by the print spooler use to send notifications to applications.</span></span> <span data-ttu-id="a768b-112">Se il canale è bidirezionale, le applicazioni possono utilizzare lo stesso canale per restituire risposte al componente.</span><span class="sxs-lookup"><span data-stu-id="a768b-112">If the channel is bidirectional, applications can use the same channel to send responses back to the component.</span></span><br/> |
| [<span data-ttu-id="a768b-113">**IPrintAsyncNotifyDataObject**</span><span class="sxs-lookup"><span data-stu-id="a768b-113">**IPrintAsyncNotifyDataObject**</span></span>](/windows/desktop/api/prnasnot/nn-prnasnot-iprintasyncnotifydataobject)<br/> | <span data-ttu-id="a768b-114">Incapsula i dati inviati in un canale di notifica.</span><span class="sxs-lookup"><span data-stu-id="a768b-114">Encapsulates the data sent in a notification channel.</span></span> <br/>                                                                                                                                                                                             |



 

 

 




