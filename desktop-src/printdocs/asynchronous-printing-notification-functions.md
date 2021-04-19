---
description: Le interfacce seguenti vengono utilizzate nella comunicazione asincrona tra le applicazioni e i componenti ospitati dallo spooler di stampa, ad esempio i driver della stampante e i monitoraggi delle porte.
ms.assetid: 7e98e63f-616c-4cd1-a8aa-482d27529b8c
title: Funzioni di notifica di stampa asincrone
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 72fa7b0b61de15af9f7117e7c36104eb51abbb7c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106318037"
---
# <a name="asynchronous-printing-notification-functions"></a><span data-ttu-id="ab5bd-103">Funzioni di notifica di stampa asincrone</span><span class="sxs-lookup"><span data-stu-id="ab5bd-103">Asynchronous Printing Notification Functions</span></span>

<span data-ttu-id="ab5bd-104">Le interfacce seguenti vengono utilizzate nella comunicazione asincrona tra le applicazioni e i componenti ospitati dallo spooler di stampa, ad esempio i driver della stampante e i monitoraggi delle porte.</span><span class="sxs-lookup"><span data-stu-id="ab5bd-104">The following interfaces are used in asynchronous communication between applications and components that are hosted by the print spooler, such as printer drivers and port monitors.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="ab5bd-105">Contenuto della sezione</span><span class="sxs-lookup"><span data-stu-id="ab5bd-105">In this section</span></span>



| <span data-ttu-id="ab5bd-106">Funzione</span><span class="sxs-lookup"><span data-stu-id="ab5bd-106">Function</span></span>                                                                                        | <span data-ttu-id="ab5bd-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="ab5bd-107">Description</span></span>                                                                                                                                                                                              |
|-------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="ab5bd-108">**CreatePrintAsyncNotifyChannel**</span><span class="sxs-lookup"><span data-stu-id="ab5bd-108">**CreatePrintAsyncNotifyChannel**</span></span>](/windows/desktop/api/prnasnot/nf-prnasnot-createprintasyncnotifychannel)<br/>               | <span data-ttu-id="ab5bd-109">Consente di creare un canale di comunicazione tra un componente di stampa ospitato da spooler di stampa, ad esempio un driver di stampa o un monitor di porta, e un'applicazione che riceve le notifiche dal componente.</span><span class="sxs-lookup"><span data-stu-id="ab5bd-109">Creates a communication channel between a Print Spooler-hosted printing component, such as a print driver or port monitor, and an application that receives notifications from the component.</span></span><br/> |
| [<span data-ttu-id="ab5bd-110">**RegisterForPrintAsyncNotifications**</span><span class="sxs-lookup"><span data-stu-id="ab5bd-110">**RegisterForPrintAsyncNotifications**</span></span>](/windows/desktop/api/prnasnot/nf-prnasnot-registerforprintasyncnotifications)<br/>     | <span data-ttu-id="ab5bd-111">Consente a un'applicazione di registrarsi per le notifiche dai componenti di stampa ospitati dallo spooler di stampa, ad esempio driver della stampante, processori di stampa e monitoraggi delle porte.</span><span class="sxs-lookup"><span data-stu-id="ab5bd-111">Enables an application to register for notifications from Print Spooler-hosted printing components such as printer drivers, print processors, and port monitors.</span></span><br/>                              |
| [<span data-ttu-id="ab5bd-112">**UnRegisterForPrintAsyncNotifications**</span><span class="sxs-lookup"><span data-stu-id="ab5bd-112">**UnRegisterForPrintAsyncNotifications**</span></span>](/windows/desktop/api/prnasnot/nf-prnasnot-unregisterforprintasyncnotifications)<br/> | <span data-ttu-id="ab5bd-113">Consente a un'applicazione che ha effettuato la registrazione di ricevere notifiche da componenti di stampa ospitati da spooler di stampa per annullare la registrazione.</span><span class="sxs-lookup"><span data-stu-id="ab5bd-113">Enables an application that has registered to receive notifications from Print Spooler-hosted printing components to unregister.</span></span><br/>                                                              |



 

 

 




