---
title: Messaggi driver
description: Messaggi driver
ms.assetid: ed3748ac-08e6-418e-b345-30c796fa38f3
keywords:
- driver installabili, messaggi
- driver installabili, messaggi personalizzati
- messaggi driver
- messaggi di driver personalizzati
- driver installabili, funzione DriverProc
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 25e03f9d68254752655be8abe9040a17d44dc0ff
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2020
ms.locfileid: "104046608"
---
# <a name="driver-messages"></a><span data-ttu-id="69186-108">Messaggi driver</span><span class="sxs-lookup"><span data-stu-id="69186-108">Driver Messages</span></span>

<span data-ttu-id="69186-109">Ogni messaggio di driver è costituito da un identificatore di messaggio e da parametri a 2 32 bit.</span><span class="sxs-lookup"><span data-stu-id="69186-109">Each driver message consists of a message identifier and two 32-bit parameters.</span></span> <span data-ttu-id="69186-110">L'identificatore del messaggio è un valore univoco che la funzione [DriverProc](/windows/win32/api/mmiscapi/nc-mmiscapi-driverproc) controlla per determinare l'azione da eseguire. Il significato dei parametri del messaggio dipende dal messaggio.</span><span class="sxs-lookup"><span data-stu-id="69186-110">The message identifier is a unique value that the [DriverProc](/windows/win32/api/mmiscapi/nc-mmiscapi-driverproc) function checks to determine which action to carry out. The meaning of the message parameters depends on the message.</span></span> <span data-ttu-id="69186-111">I parametri possono rappresentare valori o indirizzi.</span><span class="sxs-lookup"><span data-stu-id="69186-111">The parameters may represent values or addresses.</span></span> <span data-ttu-id="69186-112">In molti casi, i parametri non vengono usati e sono impostati su zero.</span><span class="sxs-lookup"><span data-stu-id="69186-112">In many cases, the parameters are not used and are set to zero.</span></span>

<span data-ttu-id="69186-113">I messaggi del driver possono essere standard o personalizzati.</span><span class="sxs-lookup"><span data-stu-id="69186-113">Driver messages can be standard or custom.</span></span> <span data-ttu-id="69186-114">Windows invia messaggi di driver standard, ad esempio [**drv \_ Open**](drv-open.md), [**drv \_ Close**](drv-close.md)e [**drv \_ Configure**](drv-configure.md), a un driver installabile in risposta a una richiesta di apertura, chiusura o configurazione del driver.</span><span class="sxs-lookup"><span data-stu-id="69186-114">Windows sends standard driver messages, such as [**DRV\_OPEN**](drv-open.md), [**DRV\_CLOSE**](drv-close.md), and [**DRV\_CONFIGURE**](drv-configure.md), to an installable driver in response to a request to open, close, or configure the driver.</span></span> <span data-ttu-id="69186-115">I messaggi standard indirizzano il driver installabile per caricare o scaricare le risorse, abilitare o disabilitare l'operazione, aprire o chiudere un'istanza del driver e visualizzare una finestra di dialogo di configurazione.</span><span class="sxs-lookup"><span data-stu-id="69186-115">The standard messages direct the installable driver to load or unload its resources, enable or disable its operation, open or close a driver instance, and display a configuration dialog box.</span></span> <span data-ttu-id="69186-116">Alcuni messaggi standard, ad esempio [**drv \_ Power**](drv-power.md) e [**drv \_ EXITSESSION**](drv-exitsession.md), notificano al driver gli eventi a livello di sistema che influiscono sul funzionamento del driver o di qualsiasi hardware correlato.</span><span class="sxs-lookup"><span data-stu-id="69186-116">Some standard messages, such as [**DRV\_POWER**](drv-power.md) and [**DRV\_EXITSESSION**](drv-exitsession.md), notify the driver of system-wide events that affect the operation of the driver or any related hardware.</span></span>

<span data-ttu-id="69186-117">Le applicazioni e le dll inviano messaggi di driver personalizzati per indirizzare un driver installabile per eseguire azioni specifiche del driver.</span><span class="sxs-lookup"><span data-stu-id="69186-117">Applications and DLLs send custom driver messages to direct an installable driver to carry out driver-specific actions.</span></span> <span data-ttu-id="69186-118">I driver installabili che supportano messaggi personalizzati devono includere l'elaborazione appropriata nella funzione **DriverProc** .</span><span class="sxs-lookup"><span data-stu-id="69186-118">Installable drivers that support custom messages must include appropriate processing in the **DriverProc** function.</span></span> <span data-ttu-id="69186-119">Per evitare conflitti tra i messaggi di driver personalizzati e standard, gli identificatori di messaggio personalizzati devono avere valori compresi tra DRV \_ riservato all' \_ utente DRV.</span><span class="sxs-lookup"><span data-stu-id="69186-119">To prevent conflict between custom and standard driver messages, custom message identifiers must have values ranging from DRV\_RESERVED to DRV\_USER.</span></span> <span data-ttu-id="69186-120">I messaggi personalizzati passati alla funzione [DefDriverProc](/windows/win32/api/mmiscapi/nf-mmiscapi-defdriverproc) vengono ignorati.</span><span class="sxs-lookup"><span data-stu-id="69186-120">Custom messages passed to the [DefDriverProc](/windows/win32/api/mmiscapi/nf-mmiscapi-defdriverproc) function are ignored.</span></span>

 

 