---
description: Informazioni sulle funzioni usate nella comunicazione asincrona tra applicazioni e componenti ospitati dallo spooler di stampa.
ms.assetid: 7e98e63f-616c-4cd1-a8aa-482d27529b8c
title: Funzioni di notifica per la stampa asincrona
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fdc9a404d1675c8ee87be31c7c57dd14a370697c
ms.sourcegitcommit: 91530c19d26ba4c57a6af1f37b57f211f580464e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/19/2021
ms.locfileid: "112394856"
---
# <a name="asynchronous-printing-notification-functions"></a><span data-ttu-id="be0eb-103">Funzioni di notifica per la stampa asincrona</span><span class="sxs-lookup"><span data-stu-id="be0eb-103">Asynchronous Printing Notification Functions</span></span>

<span data-ttu-id="be0eb-104">Le funzioni seguenti vengono utilizzate nella comunicazione asincrona tra applicazioni e componenti ospitati dallo spooler di stampa, ad esempio i driver della stampante e i monitor di porta.</span><span class="sxs-lookup"><span data-stu-id="be0eb-104">The following functions are used in asynchronous communication between applications and components that are hosted by the print spooler, such as printer drivers and port monitors.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="be0eb-105">Contenuto della sezione</span><span class="sxs-lookup"><span data-stu-id="be0eb-105">In this section</span></span>



| <span data-ttu-id="be0eb-106">Funzione</span><span class="sxs-lookup"><span data-stu-id="be0eb-106">Function</span></span>                                                                                        | <span data-ttu-id="be0eb-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="be0eb-107">Description</span></span>                                                                                                                                                                                              |
|-------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="be0eb-108">**CreatePrintAsyncNotifyChannel**</span><span class="sxs-lookup"><span data-stu-id="be0eb-108">**CreatePrintAsyncNotifyChannel**</span></span>](/windows/desktop/api/prnasnot/nf-prnasnot-createprintasyncnotifychannel)<br/>               | <span data-ttu-id="be0eb-109">Crea un canale di comunicazione tra un componente di stampa ospitato da Spooler di stampa, ad esempio un driver di stampa o un monitor di porta, e un'applicazione che riceve notifiche dal componente.</span><span class="sxs-lookup"><span data-stu-id="be0eb-109">Creates a communication channel between a Print Spooler-hosted printing component, such as a print driver or port monitor, and an application that receives notifications from the component.</span></span><br/> |
| [<span data-ttu-id="be0eb-110">**RegisterForPrintAsyncNotifications**</span><span class="sxs-lookup"><span data-stu-id="be0eb-110">**RegisterForPrintAsyncNotifications**</span></span>](/windows/desktop/api/prnasnot/nf-prnasnot-registerforprintasyncnotifications)<br/>     | <span data-ttu-id="be0eb-111">Consente a un'applicazione di registrarsi per le notifiche dai componenti di stampa ospitati da Spooler di stampa, ad esempio driver della stampante, processori di stampa e monitor di porta.</span><span class="sxs-lookup"><span data-stu-id="be0eb-111">Enables an application to register for notifications from Print Spooler-hosted printing components such as printer drivers, print processors, and port monitors.</span></span><br/>                              |
| [<span data-ttu-id="be0eb-112">**UnRegisterForPrintAsyncNotifications**</span><span class="sxs-lookup"><span data-stu-id="be0eb-112">**UnRegisterForPrintAsyncNotifications**</span></span>](/windows/desktop/api/prnasnot/nf-prnasnot-unregisterforprintasyncnotifications)<br/> | <span data-ttu-id="be0eb-113">Consente a un'applicazione registrata di ricevere notifiche dai componenti di stampa ospitati da Spooler di stampa per annullare la registrazione.</span><span class="sxs-lookup"><span data-stu-id="be0eb-113">Enables an application that has registered to receive notifications from Print Spooler-hosted printing components to unregister.</span></span><br/>                                                              |



 

 

 




