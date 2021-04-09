---
description: Utilizzando il sottosistema Smart Card, è possibile comunicare con schede che potrebbero non essere conformi alle specifiche ISO 7816.
ms.assetid: ea6cfa5a-2abf-4b7f-b3f4-99655266f030
title: Funzioni di accesso diretto alle schede
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ad360974210114a1069db3226ee814d08008cc98
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103878629"
---
# <a name="direct-card-access-functions"></a><span data-ttu-id="0919d-103">Funzioni di accesso diretto alle schede</span><span class="sxs-lookup"><span data-stu-id="0919d-103">Direct Card Access Functions</span></span>

<span data-ttu-id="0919d-104">Utilizzando il sottosistema [*Smart Card*](/windows/desktop/SecGloss/s-gly) , è possibile comunicare con schede che potrebbero non essere conformi alle specifiche ISO 7816.</span><span class="sxs-lookup"><span data-stu-id="0919d-104">By using the [*smart card*](/windows/desktop/SecGloss/s-gly) subsystem, you can communicate with cards that may not conform to the ISO 7816 specifications.</span></span> <span data-ttu-id="0919d-105">A tale scopo, le funzioni seguenti consentono di controllare gli attributi delle comunicazioni tra l'applicazione e la scheda fornendo una manipolazione diretta di basso livello del [*lettore*](/windows/desktop/SecGloss/r-gly).</span><span class="sxs-lookup"><span data-stu-id="0919d-105">To do this, the following functions let you control the attributes of the communications between the application and the card by giving you direct, low-level manipulation of the [*reader*](/windows/desktop/SecGloss/r-gly).</span></span>

<span data-ttu-id="0919d-106">Per usare queste funzioni, è necessario specificare un identificatore per l'attributo in questione.</span><span class="sxs-lookup"><span data-stu-id="0919d-106">To use these functions, you have to supply an identifier for the attribute in question.</span></span> <span data-ttu-id="0919d-107">Per gli identificatori e i valori validi per gli attributi, vedere la tabella 3-1 in *requisiti per i dispositivi di interfaccia PC-Connected*.</span><span class="sxs-lookup"><span data-stu-id="0919d-107">For valid attribute identifiers and values, refer to Table 3-1 in *Requirements for PC-Connected Interface Devices*.</span></span>



| <span data-ttu-id="0919d-108">Argomento</span><span class="sxs-lookup"><span data-stu-id="0919d-108">Topic</span></span>                                    | <span data-ttu-id="0919d-109">Descrizione</span><span class="sxs-lookup"><span data-stu-id="0919d-109">Description</span></span>                           |
|------------------------------------------|---------------------------------------|
| [<span data-ttu-id="0919d-110">**SCardControl**</span><span class="sxs-lookup"><span data-stu-id="0919d-110">**SCardControl**</span></span>](/windows/desktop/api/Winscard/nf-winscard-scardcontrol)     | <span data-ttu-id="0919d-111">Fornire il controllo diretto del lettore.</span><span class="sxs-lookup"><span data-stu-id="0919d-111">Provide direct control of the reader.</span></span> |
| [<span data-ttu-id="0919d-112">**SCardGetAttrib**</span><span class="sxs-lookup"><span data-stu-id="0919d-112">**SCardGetAttrib**</span></span>](/windows/desktop/api/Winscard/nf-winscard-scardgetattrib) | <span data-ttu-id="0919d-113">Ottiene gli attributi del lettore.</span><span class="sxs-lookup"><span data-stu-id="0919d-113">Get reader attributes.</span></span>                |
| [<span data-ttu-id="0919d-114">**SCardSetAttrib**</span><span class="sxs-lookup"><span data-stu-id="0919d-114">**SCardSetAttrib**</span></span>](/windows/desktop/api/Winscard/nf-winscard-scardsetattrib) | <span data-ttu-id="0919d-115">Imposta attributo Reader.</span><span class="sxs-lookup"><span data-stu-id="0919d-115">Set reader attribute.</span></span>                 |



 

 

 
