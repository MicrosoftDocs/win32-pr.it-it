---
description: Informazioni sulle interfacce usate nella comunicazione asincrona tra applicazioni e componenti ospitati dallo spooler di stampa.
ms.assetid: e96c957f-3972-4afc-9d76-a4725b8688f8
title: Interfacce di notifica per la stampa asincrona
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ecfe0de2cf8510b1bb039907067b62fce08a4145
ms.sourcegitcommit: 91530c19d26ba4c57a6af1f37b57f211f580464e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/19/2021
ms.locfileid: "112396096"
---
# <a name="asynchronous-printing-notification-interfaces"></a><span data-ttu-id="284e2-103">Interfacce di notifica per la stampa asincrona</span><span class="sxs-lookup"><span data-stu-id="284e2-103">Asynchronous Printing Notification Interfaces</span></span>

<span data-ttu-id="284e2-104">Le interfacce seguenti vengono usate nella comunicazione asincrona tra applicazioni e componenti ospitati dallo spooler di stampa, ad esempio i driver della stampante e i monitoraggi delle porte.</span><span class="sxs-lookup"><span data-stu-id="284e2-104">The following interfaces are used in asynchronous communication between applications and components that are hosted by the print spooler, such as printer drivers and port monitors.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="284e2-105">Contenuto della sezione</span><span class="sxs-lookup"><span data-stu-id="284e2-105">In this section</span></span>



| <span data-ttu-id="284e2-106">Interfaccia</span><span class="sxs-lookup"><span data-stu-id="284e2-106">Interface</span></span>                                                                     | <span data-ttu-id="284e2-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="284e2-107">Description</span></span>                                                                                                                                                                                                                                                   |
|-------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="284e2-108">**IPrintAsyncNotifyCallback**</span><span class="sxs-lookup"><span data-stu-id="284e2-108">**IPrintAsyncNotifyCallback**</span></span>](/windows/desktop/api/prnasnot/nn-prnasnot-iprintasyncnotifycallback)<br/>     | <span data-ttu-id="284e2-109">Crea e gestisce un canale di comunicazione utilizzato dalle applicazioni e dai componenti ospitati dallo spooler di stampa.</span><span class="sxs-lookup"><span data-stu-id="284e2-109">Creates and manages a communication channel used by applications and components that are hosted by the print spooler.</span></span><br/>                                                                                                                              |
| [<span data-ttu-id="284e2-110">**IPrintAsyncNotifyChannel**</span><span class="sxs-lookup"><span data-stu-id="284e2-110">**IPrintAsyncNotifyChannel**</span></span>](/windows/desktop/api/prnasnot/nn-prnasnot-iprintasyncnotifychannel)<br/>       | <span data-ttu-id="284e2-111">Rappresenta un canale di comunicazione utilizzato dai componenti ospitati dallo spooler di stampa per inviare notifiche alle applicazioni.</span><span class="sxs-lookup"><span data-stu-id="284e2-111">Represents a communication channel that components that are hosted by the print spooler use to send notifications to applications.</span></span> <span data-ttu-id="284e2-112">Se il canale è bidirezionale, le applicazioni possono usare lo stesso canale per inviare le risposte al componente.</span><span class="sxs-lookup"><span data-stu-id="284e2-112">If the channel is bidirectional, applications can use the same channel to send responses back to the component.</span></span><br/> |
| [<span data-ttu-id="284e2-113">**IPrintAsyncNotifyDataObject**</span><span class="sxs-lookup"><span data-stu-id="284e2-113">**IPrintAsyncNotifyDataObject**</span></span>](/windows/desktop/api/prnasnot/nn-prnasnot-iprintasyncnotifydataobject)<br/> | <span data-ttu-id="284e2-114">Incapsula i dati inviati in un canale di notifica.</span><span class="sxs-lookup"><span data-stu-id="284e2-114">Encapsulates the data sent in a notification channel.</span></span> <br/>                                                                                                                                                                                             |



 

 

 




