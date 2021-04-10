---
description: La struttura COMMCONFIG definisce la configurazione di una risorsa di comunicazione, seriale o in altro modo.
ms.assetid: 05094b98-4694-42dd-883c-b3c90735b3bc
title: Configurazione delle risorse di comunicazione
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4c6d19bb8478590c85c9f0c1d60ce91cbd1b802a
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104126801"
---
# <a name="communications-resource-configuration"></a><span data-ttu-id="0ba3d-103">Configurazione delle risorse di comunicazione</span><span class="sxs-lookup"><span data-stu-id="0ba3d-103">Communications Resource Configuration</span></span>

<span data-ttu-id="0ba3d-104">La struttura [**COMMCONFIG**](/windows/desktop/api/Winbase/ns-winbase-commconfig) definisce la configurazione di una risorsa di comunicazione, seriale o in altro modo.</span><span class="sxs-lookup"><span data-stu-id="0ba3d-104">The [**COMMCONFIG**](/windows/desktop/api/Winbase/ns-winbase-commconfig) structure defines the configuration of a communications resource, serial or otherwise.</span></span> <span data-ttu-id="0ba3d-105">Il formato della struttura varia a seconda del tipo di risorsa di comunicazione (il sottotipo del provider).</span><span class="sxs-lookup"><span data-stu-id="0ba3d-105">The format of the structure varies depending on the type of communications resource (the provider subtype).</span></span> <span data-ttu-id="0ba3d-106">I primi membri della struttura sono comuni a tutte le risorse di comunicazione; sono definiti membri aggiuntivi per sottotipi di provider specifici.</span><span class="sxs-lookup"><span data-stu-id="0ba3d-106">The first few structure members are common to all communications resources; additional members are defined for specific provider subtypes.</span></span> <span data-ttu-id="0ba3d-107">I provider di servizi specifici possono estendere anche la struttura **COMMCONFIG** .</span><span class="sxs-lookup"><span data-stu-id="0ba3d-107">Specific service providers may extend the **COMMCONFIG** structure as well.</span></span>

<span data-ttu-id="0ba3d-108">Un'applicazione può ottenere e impostare la configurazione di una risorsa di comunicazione usando le funzioni [**GetCommConfig**](/windows/desktop/api/Winbase/nf-winbase-getcommconfig) e [**SetCommConfig**](/windows/desktop/api/Winbase/nf-winbase-setcommconfig) .</span><span class="sxs-lookup"><span data-stu-id="0ba3d-108">An application can get and set the configuration of a communications resource by using the [**GetCommConfig**](/windows/desktop/api/Winbase/nf-winbase-getcommconfig) and [**SetCommConfig**](/windows/desktop/api/Winbase/nf-winbase-setcommconfig) functions.</span></span> <span data-ttu-id="0ba3d-109">Quando viene aperto, una risorsa di comunicazione viene inizializzata usando la configurazione predefinita per il relativo sottotipo di provider.</span><span class="sxs-lookup"><span data-stu-id="0ba3d-109">When opened, a communications resource is initialized using the default configuration for its provider subtype.</span></span> <span data-ttu-id="0ba3d-110">Per ottenere e impostare la configurazione predefinita per un sottotipo di provider, usare le funzioni [**GetDefaultCommConfig**](/windows/desktop/api/Winbase/nf-winbase-getdefaultcommconfiga) e [**SetDefaultCommConfig**](/windows/desktop/api/Winbase/nf-winbase-setdefaultcommconfiga) .</span><span class="sxs-lookup"><span data-stu-id="0ba3d-110">To get and set the default configuration for a provider subtype, use the [**GetDefaultCommConfig**](/windows/desktop/api/Winbase/nf-winbase-getdefaultcommconfiga) and [**SetDefaultCommConfig**](/windows/desktop/api/Winbase/nf-winbase-setdefaultcommconfiga) functions.</span></span>

<span data-ttu-id="0ba3d-111">Per richiedere all'utente le informazioni di configurazione, usare la funzione [**CommConfigDialog**](/windows/desktop/api/Winbase/nf-winbase-commconfigdialoga) .</span><span class="sxs-lookup"><span data-stu-id="0ba3d-111">To prompt the user for configuration information, use the [**CommConfigDialog**](/windows/desktop/api/Winbase/nf-winbase-commconfigdialoga) function.</span></span> <span data-ttu-id="0ba3d-112">Questa funzione Visualizza una finestra di dialogo definita dal provider di servizi e compila una struttura [**COMMCONFIG**](/windows/desktop/api/Winbase/ns-winbase-commconfig) in base all'input dell'utente.</span><span class="sxs-lookup"><span data-stu-id="0ba3d-112">This function displays a dialog box defined by the service provider and fills in a [**COMMCONFIG**](/windows/desktop/api/Winbase/ns-winbase-commconfig) structure based on user input.</span></span>

 

 



