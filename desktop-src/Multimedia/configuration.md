---
title: Configurazione (Windows Multimedia)
description: Informazioni su come un driver multimediale Windows può consentire agli utenti di scegliere le impostazioni di configurazione visualizzando una finestra di dialogo di configurazione.
ms.assetid: d61d6c8b-8dba-45c2-ba99-0b2111a2d624
keywords:
- driver installabili, configurazione
- driver installabili, DRV_CONFIGURE messaggio
- DRV_CONFIGURE messaggio
- DRV_QUERYCONFIGURE messaggio
- Messaggio DRVCONFIGINFO
- configurazione di driver installabili
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7804e4d92d30d666d4d28c253a1a44572a707daa
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/19/2021
ms.locfileid: "112403924"
---
# <a name="configuration-windows-multimedia"></a><span data-ttu-id="da3fd-109">Configurazione (Windows Multimedia)</span><span class="sxs-lookup"><span data-stu-id="da3fd-109">Configuration (Windows Multimedia)</span></span>

<span data-ttu-id="da3fd-110">Un driver installabile può consentire agli utenti di scegliere le impostazioni di configurazione per il driver e l'hardware associato visualizzando una finestra di dialogo di configurazione durante l'elaborazione [**del messaggio DRV \_ CONFIGURE.**](drv-configure.md)</span><span class="sxs-lookup"><span data-stu-id="da3fd-110">An installable driver can let users choose configuration settings for the driver and associated hardware by displaying a configuration dialog box when processing the [**DRV\_CONFIGURE**](drv-configure.md) message.</span></span> <span data-ttu-id="da3fd-111">Il driver è responsabile della creazione e della gestione della finestra di dialogo, dell'elaborazione di qualsiasi input utente dalla finestra di dialogo e della modifica della configurazione del driver o dell'hardware come richiesto dall'utente.</span><span class="sxs-lookup"><span data-stu-id="da3fd-111">The driver is responsible for creating and managing the dialog box, processing any user input from the dialog box, and changing the configuration of the driver or hardware as requested by the user.</span></span> <span data-ttu-id="da3fd-112">Il driver deve fornire una procedura di finestra di dialogo separata per elaborare i messaggi della finestra di dialogo e un modello di finestra di dialogo per definire l'aspetto e il contenuto della finestra di dialogo.</span><span class="sxs-lookup"><span data-stu-id="da3fd-112">The driver must provide a separate dialog box procedure to process window messages for the dialog box and a dialog box template to define the appearance and content of the dialog box.</span></span>

<span data-ttu-id="da3fd-113">Prima di ricevere il messaggio DRV \_ CONFIGURE, un driver riceve il [**messaggio DRV \_ QUERYCONFIGURE.**](drv-queryconfigure.md)</span><span class="sxs-lookup"><span data-stu-id="da3fd-113">Before receiving the DRV\_CONFIGURE message, a driver receives the [**DRV\_QUERYCONFIGURE**](drv-queryconfigure.md) message.</span></span> <span data-ttu-id="da3fd-114">Il driver deve restituire un valore diverso da zero alla query per garantire la ricezione del messaggio DRV \_ CONFIGURE successivo.</span><span class="sxs-lookup"><span data-stu-id="da3fd-114">The driver must return a nonzero value to the query to ensure receipt of the subsequent DRV\_CONFIGURE message.</span></span>

<span data-ttu-id="da3fd-115">Quando si inizializza la finestra di dialogo di configurazione, il driver recupera in genere le informazioni di configurazione dal Registro di sistema.</span><span class="sxs-lookup"><span data-stu-id="da3fd-115">When initializing the configuration dialog box, the driver typically retrieves configuration information from the registry.</span></span> <span data-ttu-id="da3fd-116">Per facilitare l'individuazione di queste informazioni, il messaggio DRV CONFIGURE include in genere l'indirizzo di una struttura \_ [**DRVCONFIGINFO**](/windows/win32/api/mmiscapi/ns-mmiscapi-drvconfiginfo) che contiene i nomi della chiave del Registro di sistema e del valore associati al driver.</span><span class="sxs-lookup"><span data-stu-id="da3fd-116">To help locate this information, the DRV\_CONFIGURE message usually includes the address of a [**DRVCONFIGINFO**](/windows/win32/api/mmiscapi/ns-mmiscapi-drvconfiginfo) structure that contains the names of the registry key and value associated with the driver.</span></span> <span data-ttu-id="da3fd-117">Se l'utente richiede modifiche alla configurazione, il driver deve aggiornare le informazioni di configurazione nel Registro di sistema.</span><span class="sxs-lookup"><span data-stu-id="da3fd-117">If the user requests changes to the configuration, the driver should update the configuration information in the registry.</span></span>

 

 
