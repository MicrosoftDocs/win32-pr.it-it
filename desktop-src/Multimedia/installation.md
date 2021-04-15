---
title: Installazione (Windows Multimedia)
description: Installazione
ms.assetid: 1f0e23ad-4db7-4f32-98d9-e672370db559
keywords:
- driver installabili, installazione
- driver installabili, messaggio DRV_INSTALL
- driver installabili, messaggio DRV_REMOVE
- Messaggio DRV_INSTALL
- Messaggio DRV_REMOVE
- Messaggio DRVCONFIGINFO
- installazione dei driver
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c4ebebd090c7499698c59c325d1ac0d487902454
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/10/2020
ms.locfileid: "104400111"
---
# <a name="installation-windows-multimedia"></a><span data-ttu-id="8535c-110">Installazione (Windows Multimedia)</span><span class="sxs-lookup"><span data-stu-id="8535c-110">Installation (Windows Multimedia)</span></span>

<span data-ttu-id="8535c-111">Un driver installabile può eseguire attività di installazione specifiche del driver quando si elaborano i messaggi [**drv \_ Install**](drv-install.md) e [**drv \_ Remove**](drv-remove.md) .</span><span class="sxs-lookup"><span data-stu-id="8535c-111">An installable driver can carry out driver-specific installation tasks when processing the [**DRV\_INSTALL**](drv-install.md) and [**DRV\_REMOVE**](drv-remove.md) messages.</span></span> <span data-ttu-id="8535c-112">Un'applicazione di installazione, ad esempio un'applicazione del pannello di controllo, invia i messaggi al driver rispettivamente durante l'installazione o la rimozione del driver.</span><span class="sxs-lookup"><span data-stu-id="8535c-112">An installation application, such as a Control Panel application, sends the messages to the driver when installing or removing the driver, respectively.</span></span>

<span data-ttu-id="8535c-113">Quando si elabora il \_ messaggio di installazione di DRV, il driver verifica in genere che l'hardware necessario sia presente e quindi Visualizza la finestra di dialogo di configurazione per consentire all'utente di scegliere le impostazioni di configurazione iniziali per il driver e l'hardware associato.</span><span class="sxs-lookup"><span data-stu-id="8535c-113">When processing the DRV\_INSTALL message, the driver typically verifies that the required hardware is present and then displays the configuration dialog box to let the user choose the initial configuration settings for the driver and associated hardware.</span></span> <span data-ttu-id="8535c-114">Il messaggio include l'indirizzo di una struttura [**DRVCONFIGINFO**](/windows/win32/api/mmiscapi/ns-mmiscapi-drvconfiginfo) che contiene i nomi della chiave del registro di sistema e il valore associato al driver; il driver controlla il valore del registro di sistema per le informazioni di configurazione predefinite.</span><span class="sxs-lookup"><span data-stu-id="8535c-114">The message includes the address of a [**DRVCONFIGINFO**](/windows/win32/api/mmiscapi/ns-mmiscapi-drvconfiginfo) structure that contains the names of the registry key and value associated with the driver; the driver checks the registry value for default configuration information.</span></span> <span data-ttu-id="8535c-115">Infine, il driver crea anche le chiavi del registro di sistema e i valori aggiuntivi necessari per l'operazione riuscita.</span><span class="sxs-lookup"><span data-stu-id="8535c-115">Finally, the driver also creates any additional registry keys and values needed for successful operation.</span></span>

<span data-ttu-id="8535c-116">Quando si elabora il \_ messaggio di rimozione di DRV, il driver rimuove le chiavi del registro di sistema e i valori che potrebbero essere stati creati.</span><span class="sxs-lookup"><span data-stu-id="8535c-116">When processing the DRV\_REMOVE message, the driver removes any registry keys and values it may have created.</span></span>

 

 
