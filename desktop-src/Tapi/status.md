---
description: La maggior parte delle operazioni get e set occupano solo un componente di informazioni. La funzione phoneGetStatus restituisce informazioni complete sullo stato di un dispositivo telefonico a un'applicazione.
ms.assetid: ca38396c-6f97-4c1c-99fb-2bd64c74c626
title: Stato (API di telefonia)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 44a9a93fdd97d32b477545ba0fb9f73f10b45021
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103881642"
---
# <a name="status-telephony-api"></a><span data-ttu-id="a9253-104">Stato (API di telefonia)</span><span class="sxs-lookup"><span data-stu-id="a9253-104">Status (Telephony API)</span></span>

<span data-ttu-id="a9253-105">La maggior parte delle operazioni get e set occupano solo un componente di informazioni.</span><span class="sxs-lookup"><span data-stu-id="a9253-105">Most of the get and set operations deal with one component of information only.</span></span> <span data-ttu-id="a9253-106">La funzione [**phoneGetStatus**](/windows/desktop/api/Tapi/nf-tapi-phonegetstatus) restituisce informazioni complete sullo stato di un dispositivo telefonico a un'applicazione.</span><span class="sxs-lookup"><span data-stu-id="a9253-106">The [**phoneGetStatus**](/windows/desktop/api/Tapi/nf-tapi-phonegetstatus) function returns complete status information about a phone device to an application.</span></span>

<span data-ttu-id="a9253-107">Come indicato in precedenza, ogni volta che un elemento di stato viene modificato sul dispositivo telefonico, viene inviato un messaggio di [**\_ stato telefonico**](phone-state.md) alla funzione dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="a9253-107">As mentioned earlier, whenever a status item changes on the phone device, a [**PHONE\_STATE**](phone-state.md) message is sent to the application function.</span></span> <span data-ttu-id="a9253-108">I parametri di questo messaggio includono un handle per il dispositivo telefonico e un'indicazione dell'elemento di stato modificato.</span><span class="sxs-lookup"><span data-stu-id="a9253-108">This message's parameters include a handle to the phone device and an indication of the status item that changed.</span></span>

<span data-ttu-id="a9253-109">Un'applicazione può usare [**phoneSetStatusMessages**](/windows/desktop/api/Tapi/nf-tapi-phonesetstatusmessages) per selezionare le modifiche di stato specifiche per le quali si vuole ricevere una notifica.</span><span class="sxs-lookup"><span data-stu-id="a9253-109">An application can use [**phoneSetStatusMessages**](/windows/desktop/api/Tapi/nf-tapi-phonesetstatusmessages) to select the specific status changes for which it wants to be notified.</span></span> <span data-ttu-id="a9253-110">In modo corrispondente, [**phoneGetStatusMessages**](/windows/desktop/api/Tapi/nf-tapi-phonegetstatusmessages) restituisce le modifiche dello stato per le quali l'applicazione vuole ricevere una notifica.</span><span class="sxs-lookup"><span data-stu-id="a9253-110">Correspondingly, [**phoneGetStatusMessages**](/windows/desktop/api/Tapi/nf-tapi-phonegetstatusmessages) returns the status changes for which the application wants to be notified.</span></span>

 

 



