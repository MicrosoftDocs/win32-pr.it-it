---
description: È necessario arrestare correttamente le sessioni di comunicazione e un'intera applicazione per evitare che le risorse rimangano vincolate nelle chiamate o nelle applicazioni che non sono più necessarie.
ms.assetid: 40694b7f-474b-41aa-be3f-48e4ca517a6f
title: Arresto TAPI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 661273a3d72559d965fa1ea6066f1090f8e6b6e6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106317635"
---
# <a name="tapi-shutdown"></a><span data-ttu-id="bfe42-103">Arresto TAPI</span><span class="sxs-lookup"><span data-stu-id="bfe42-103">TAPI Shutdown</span></span>

<span data-ttu-id="bfe42-104">È necessario arrestare correttamente le sessioni di comunicazione e un'intera applicazione per evitare che le risorse rimangano vincolate nelle chiamate o nelle applicazioni che non sono più necessarie.</span><span class="sxs-lookup"><span data-stu-id="bfe42-104">Proper shutdown of communications sessions and of an entire application is required to prevent resources from remaining tied up in calls or applications that no longer need them.</span></span>

<span data-ttu-id="bfe42-105">TAPI fornisce una serie di funzioni e metodi che consentono di semplificare il processo.</span><span class="sxs-lookup"><span data-stu-id="bfe42-105">TAPI provides a series of functions and methods to assist in the process.</span></span> <span data-ttu-id="bfe42-106">Ovviamente, l'applicazione deve anche essere responsabile del rilascio corretto della memoria allocata, sia sotto forma di strutture di dati che di riferimenti COM.</span><span class="sxs-lookup"><span data-stu-id="bfe42-106">Obviously, the application must also take responsibility for properly releasing allocated memory, whether in the form of data structures or COM references.</span></span>



| <span data-ttu-id="bfe42-107">Funzioni di TAPI 2. x</span><span class="sxs-lookup"><span data-stu-id="bfe42-107">TAPI 2.x functions</span></span>                                                            | <span data-ttu-id="bfe42-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="bfe42-108">Description</span></span>                                                            |
|-------------------------------------------------------------------------------|------------------------------------------------------------------------|
| [<span data-ttu-id="bfe42-109">**lineRegisterRequestRecipient**</span><span class="sxs-lookup"><span data-stu-id="bfe42-109">**lineRegisterRequestRecipient**</span></span>](/windows/win32/api/tapi/nf-tapi-lineregisterrequestrecipient) | <span data-ttu-id="bfe42-110">Annulla la registrazione dell'applicazione come gestore per le chiamate di telefonia assistita.</span><span class="sxs-lookup"><span data-stu-id="bfe42-110">Unregisters the application as a handler for assisted telephony calls.</span></span> |
| [<span data-ttu-id="bfe42-111">**lineClose**</span><span class="sxs-lookup"><span data-stu-id="bfe42-111">**lineClose**</span></span>](/windows/win32/api/tapi/nf-tapi-lineclose)                                       | <span data-ttu-id="bfe42-112">Disconnette l'applicazione come responsabile per le chiamate sulla riga specificata.</span><span class="sxs-lookup"><span data-stu-id="bfe42-112">Disconnects the application as a manager for calls on the given line.</span></span>  |
| [<span data-ttu-id="bfe42-113">**lineShutdown**</span><span class="sxs-lookup"><span data-stu-id="bfe42-113">**lineShutdown**</span></span>](/windows/win32/api/tapi/nf-tapi-lineshutdown)                                 | <span data-ttu-id="bfe42-114">Arresta l'utilizzo dell'applicazione dell'astrazione di riga.</span><span class="sxs-lookup"><span data-stu-id="bfe42-114">Shuts down the application's usage of the line abstraction.</span></span>            |



 



| <span data-ttu-id="bfe42-115">Interfacce o metodi di TAPI 3. x</span><span class="sxs-lookup"><span data-stu-id="bfe42-115">TAPI 3.x interfaces or methods</span></span>                                            | <span data-ttu-id="bfe42-116">Descrizione</span><span class="sxs-lookup"><span data-stu-id="bfe42-116">Description</span></span>                                                                |
|---------------------------------------------------------------------------|----------------------------------------------------------------------------|
| [<span data-ttu-id="bfe42-117">**ITTAPI::UnregisterNotifications**</span><span class="sxs-lookup"><span data-stu-id="bfe42-117">**ITTAPI::UnregisterNotifications**</span></span>](/windows/desktop/api/tapi3if/nf-tapi3if-ittapi-unregisternotifications) | <span data-ttu-id="bfe42-118">Rimuove tutte le registrazioni di notifiche degli eventi eseguite dall'applicazione.</span><span class="sxs-lookup"><span data-stu-id="bfe42-118">Removes any event notification registrations performed by the application.</span></span> |
| [<span data-ttu-id="bfe42-119">**ITTAPI:: Shutdown**</span><span class="sxs-lookup"><span data-stu-id="bfe42-119">**ITTAPI::Shutdown**</span></span>](/windows/desktop/api/tapi3if/nf-tapi3if-ittapi-shutdown)                               | <span data-ttu-id="bfe42-120">Disconnette l'applicazione come gestione chiamate.</span><span class="sxs-lookup"><span data-stu-id="bfe42-120">Disconnects the application as a call manager.</span></span>                             |



 

 

 
