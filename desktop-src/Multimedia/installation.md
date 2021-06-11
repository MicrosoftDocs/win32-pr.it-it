---
title: Installazione (Windows Multimedia)
description: Informazioni sull'installazione di Windows Multimedia, inclusa l'elaborazione DRV_INSTALL e DRV_REMOVE messaggi.
ms.assetid: 1f0e23ad-4db7-4f32-98d9-e672370db559
keywords:
- driver installabili, installazione
- driver installabili, DRV_INSTALL messaggio
- driver installabili, DRV_REMOVE messaggio
- DRV_INSTALL messaggio
- DRV_REMOVE messaggio
- Messaggio DRVCONFIGINFO
- installazione di driver
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 29f82a23a781e62553d6488331b2c832104fd770
ms.sourcegitcommit: 6fc8a7419bd01787cf6a1c52c355a4a2d1aec471
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/10/2021
ms.locfileid: "111989036"
---
# <a name="installation-windows-multimedia"></a><span data-ttu-id="95a6d-110">Installazione (Windows Multimedia)</span><span class="sxs-lookup"><span data-stu-id="95a6d-110">Installation (Windows Multimedia)</span></span>

<span data-ttu-id="95a6d-111">Un driver installabile può eseguire attività di installazione specifiche del driver durante l'elaborazione dei messaggi [**\_ DRV INSTALL**](drv-install.md) [**e DRV \_ REMOVE.**](drv-remove.md)</span><span class="sxs-lookup"><span data-stu-id="95a6d-111">An installable driver can carry out driver-specific installation tasks when processing the [**DRV\_INSTALL**](drv-install.md) and [**DRV\_REMOVE**](drv-remove.md) messages.</span></span> <span data-ttu-id="95a6d-112">Un'applicazione di installazione, ad esempio Pannello di controllo, invia i messaggi al driver rispettivamente durante l'installazione o la rimozione del driver.</span><span class="sxs-lookup"><span data-stu-id="95a6d-112">An installation application, such as a Control Panel application, sends the messages to the driver when installing or removing the driver, respectively.</span></span>

<span data-ttu-id="95a6d-113">Durante l'elaborazione del messaggio DRV INSTALL, il driver verifica in genere che l'hardware necessario sia presente e quindi visualizza la finestra di dialogo di configurazione per consentire all'utente di scegliere le impostazioni di configurazione iniziali per il driver e \_ l'hardware associato.</span><span class="sxs-lookup"><span data-stu-id="95a6d-113">When processing the DRV\_INSTALL message, the driver typically verifies that the required hardware is present and then displays the configuration dialog box to let the user choose the initial configuration settings for the driver and associated hardware.</span></span> <span data-ttu-id="95a6d-114">Il messaggio include l'indirizzo di una [**struttura DRVCONFIGINFO**](/windows/win32/api/mmiscapi/ns-mmiscapi-drvconfiginfo) che contiene i nomi della chiave e del valore del Registro di sistema associati al driver. Il driver controlla il valore del Registro di sistema per le informazioni di configurazione predefinite.</span><span class="sxs-lookup"><span data-stu-id="95a6d-114">The message includes the address of a [**DRVCONFIGINFO**](/windows/win32/api/mmiscapi/ns-mmiscapi-drvconfiginfo) structure that contains the names of the registry key and value associated with the driver; the driver checks the registry value for default configuration information.</span></span> <span data-ttu-id="95a6d-115">Infine, il driver crea anche eventuali chiavi e valori del Registro di sistema aggiuntivi necessari per il corretto funzionamento.</span><span class="sxs-lookup"><span data-stu-id="95a6d-115">Finally, the driver also creates any additional registry keys and values needed for successful operation.</span></span>

<span data-ttu-id="95a6d-116">Durante l'elaborazione del messaggio DRV REMOVE, il driver rimuove le chiavi e i valori \_ del Registro di sistema che potrebbero essere stati creati.</span><span class="sxs-lookup"><span data-stu-id="95a6d-116">When processing the DRV\_REMOVE message, the driver removes any registry keys and values it may have created.</span></span>

 

 
