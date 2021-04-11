---
title: Configurazione del provider di servizi Microsoft Locator Name
description: È possibile modificare il provider di servizi dei nomi specificato modificando il file di configurazione Rpcreg. dat, che contiene i parametri NSP e le impostazioni del protocollo RPC. Usare un editor di testo per modificare le voci NSP.
ms.assetid: b499e40e-d38f-4e51-bbce-41af3ff12a7e
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 14a5334436ce307030048a862f1375a91000b41e
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104330751"
---
# <a name="configuring-the-microsoft-locator-name-service-provider"></a><span data-ttu-id="14ffa-104">Configurazione del provider di servizi Microsoft Locator Name</span><span class="sxs-lookup"><span data-stu-id="14ffa-104">Configuring the Microsoft Locator Name Service Provider</span></span>

<span data-ttu-id="14ffa-105">È possibile modificare il provider di servizi dei nomi specificato modificando il file di configurazione Rpcreg. dat, che contiene i parametri NSP e le impostazioni del protocollo RPC.</span><span class="sxs-lookup"><span data-stu-id="14ffa-105">You can change the name service provider you specified by editing the Rpcreg.dat configuration file, which contains the NSP parameters and RPC protocol settings.</span></span> <span data-ttu-id="14ffa-106">Usare un editor di testo per modificare le voci NSP.</span><span class="sxs-lookup"><span data-stu-id="14ffa-106">Use a text editor to change NSP entries.</span></span>

<span data-ttu-id="14ffa-107">**Per riconfigurare il provider di servizi Microsoft Locator Name**</span><span class="sxs-lookup"><span data-stu-id="14ffa-107">**To reconfigure the Microsoft Locator name service provider**</span></span>

1.  <span data-ttu-id="14ffa-108">Aprire il file RPCREG. dat usando un editor di testo.</span><span class="sxs-lookup"><span data-stu-id="14ffa-108">Open the Rpcreg.dat file using a text editor.</span></span>

    <span data-ttu-id="14ffa-109">Rpcreg. dat si trova nella directory radice, a meno che non sia stato specificato un percorso diverso durante l'installazione.</span><span class="sxs-lookup"><span data-stu-id="14ffa-109">Rpcreg.dat is in the root directory unless you specified a different path during setup.</span></span>

2.  <span data-ttu-id="14ffa-110">Impostare i valori seguenti per le voci del registro di sistema.</span><span class="sxs-lookup"><span data-stu-id="14ffa-110">Set the following values for the registry entries.</span></span> 

    | <span data-ttu-id="14ffa-111">Voce del Registro di sistema</span><span class="sxs-lookup"><span data-stu-id="14ffa-111">Registry entry</span></span>                                         | <span data-ttu-id="14ffa-112">Valore</span><span class="sxs-lookup"><span data-stu-id="14ffa-112">Value</span></span>                                                                                                                                                 |
    |--------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------|
    | <span data-ttu-id="14ffa-113">Software \\ Microsoft \\ RPC \\ NameService \\ Protocol</span><span class="sxs-lookup"><span data-stu-id="14ffa-113">Software\\Microsoft\\RPC \\NameService\\Protocol</span></span>       | <span data-ttu-id="14ffa-114">Sequenza di protocollo per il protocollo utilizzato.</span><span class="sxs-lookup"><span data-stu-id="14ffa-114">The protocol sequence for the protocol you are using.</span></span> <span data-ttu-id="14ffa-115">Il valore predefinito è **ncacn \_ NP**.</span><span class="sxs-lookup"><span data-stu-id="14ffa-115">The default is **ncacn\_np**.</span></span>                                                                   |
    | <span data-ttu-id="14ffa-116">Software \\ Microsoft \\ RPC \\ NameService \\ networkaddress</span><span class="sxs-lookup"><span data-stu-id="14ffa-116">Software\\Microsoft\\RPC\\ NameService\\NetworkAddress</span></span> | <span data-ttu-id="14ffa-117">Nome del computer che esegue il localizzatore usato dai client durante le operazioni di ricerca del nome del servizio.</span><span class="sxs-lookup"><span data-stu-id="14ffa-117">The name of the computer running Locator that is used by clients during name service lookup operations.</span></span> <span data-ttu-id="14ffa-118">Il valore predefinito è il controller di dominio primario.</span><span class="sxs-lookup"><span data-stu-id="14ffa-118">The default is the primary domain controller.</span></span> |
    | <span data-ttu-id="14ffa-119">Software \\ Microsoft \\ RPC \\ NameService \\ endpoint</span><span class="sxs-lookup"><span data-stu-id="14ffa-119">Software\\Microsoft\\RPC\\ NameService\\Endpoint</span></span>       | <span data-ttu-id="14ffa-120">Nome dell'endpoint utilizzato dal servizio del nome.</span><span class="sxs-lookup"><span data-stu-id="14ffa-120">The name of the endpoint used by the name service.</span></span> <span data-ttu-id="14ffa-121">Il valore predefinito \\ è \\ Locator pipe.</span><span class="sxs-lookup"><span data-stu-id="14ffa-121">The default is \\pipe\\locator.</span></span>                                                                    |

    

     

3.  <span data-ttu-id="14ffa-122">Salvare e chiudere il file.</span><span class="sxs-lookup"><span data-stu-id="14ffa-122">Save and close the file.</span></span>

 

 




