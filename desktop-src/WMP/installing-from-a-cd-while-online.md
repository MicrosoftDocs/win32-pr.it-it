---
title: Installazione da un CD mentre è in linea
description: Installazione da un CD mentre è in linea
ms.assetid: 4cf34f0e-caa0-42d1-b99a-51bbb7f0a7df
keywords:
- Windows Media Player Online Stores, installazione da CD mentre è online
- negozi online, installazione da CD mentre è online
- digitare 1 negozi online, installazione da CD mentre è in linea
- digitare 2 archivi online, installazione da CD mentre è in linea
- Windows Media Player Online Stores, installazioni online da CD
- negozi online, installazioni online da CD
- digitare 1 negozi online, installazioni online da CD
- digitare 2 archivi online, installazioni online da CD
- Windows Media Player Online Stores, installazione CD in linea
- negozi online, installazioni CD in linea
- digitare 1 negozi online, installazione CD mentre è in linea
- digitare 2 negozi online, installazioni CD mentre è online
- installazione di archivi online da CD in linea
- Installazioni CD di negozi online in linea
- installazioni online di archivi online
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dd57015e64dece444b1a91afebe3144bee117caa
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "106298430"
---
# <a name="installing-from-a-cd-while-online"></a><span data-ttu-id="4ae00-118">Installazione da un CD mentre è in linea</span><span class="sxs-lookup"><span data-stu-id="4ae00-118">Installing from a CD While Online</span></span>

<span data-ttu-id="4ae00-119">Gli utenti possono installare Windows Media Player da un CD mentre si è connessi a Internet.</span><span class="sxs-lookup"><span data-stu-id="4ae00-119">Users can install Windows Media Player from a CD while connected to the Internet.</span></span> <span data-ttu-id="4ae00-120">In questo caso, il programma di installazione di Windows Media Player individua il documento ServiceInfo specificato dal parametro della riga di comando *ServiceInfo* .</span><span class="sxs-lookup"><span data-stu-id="4ae00-120">When this happens, Windows Media Player setup locates the ServiceInfo document specified by the *ServiceInfo* command line parameter.</span></span> <span data-ttu-id="4ae00-121">Se l'attributo **chiave** corrisponde al parametro della riga di comando *DefaultService* , il programma di installazione controlla l'elemento install per personalizzare il processo di installazione.</span><span class="sxs-lookup"><span data-stu-id="4ae00-121">If the **Key** attribute matches the *DefaultService* command line parameter, setup inspects the Install element to customize the setup process.</span></span> <span data-ttu-id="4ae00-122">Utilizzando i valori di attributo, il programma di installazione Visualizza il contratto di licenza con l'utente finale (EULA) e l'informativa sulla privacy, nonché recupera e installa il file CAB nel computer dell'utente.</span><span class="sxs-lookup"><span data-stu-id="4ae00-122">Using the attribute values, setup displays your End User License Agreement (EULA) and your privacy statement, and also retrieves and installs your .cab file to the user's computer.</span></span> <span data-ttu-id="4ae00-123">Ad esempio, è possibile usare questa funzionalità per installare la versione più recente di un oggetto COM richiesto dal negozio online.</span><span class="sxs-lookup"><span data-stu-id="4ae00-123">For example, you can use this feature to install the latest version of a COM object that your online store requires.</span></span>

<span data-ttu-id="4ae00-124">Una volta installato, Windows Media Player imposta l'archivio online iniziale usando il nome della chiave specificato per il parametro della riga di comando *DefaultService* .</span><span class="sxs-lookup"><span data-stu-id="4ae00-124">After it is installed, Windows Media Player sets the initial online store using the key name you specified for the *DefaultService* command line parameter.</span></span>

## <a name="related-topics"></a><span data-ttu-id="4ae00-125">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="4ae00-125">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="4ae00-126">**Informazioni comuni ai negozi online di tipo 1 e di tipo 2**</span><span class="sxs-lookup"><span data-stu-id="4ae00-126">**Information Common to Type 1 and Type 2 Online Stores**</span></span>](information-common-to-type-1-and-type-2-online-stores.md)
</dt> <dt>

[<span data-ttu-id="4ae00-127">**Elemento install**</span><span class="sxs-lookup"><span data-stu-id="4ae00-127">**Install Element**</span></span>](install-element.md)
</dt> <dt>

[<span data-ttu-id="4ae00-128">**Documento ServiceInfo**</span><span class="sxs-lookup"><span data-stu-id="4ae00-128">**ServiceInfo Document**</span></span>](serviceinfo-document.md)
</dt> <dt>

[<span data-ttu-id="4ae00-129">**Impostazione dell'archivio online iniziale**</span><span class="sxs-lookup"><span data-stu-id="4ae00-129">**Setting the Initial Online Store**</span></span>](setting-the-initial-online-store.md)
</dt> <dt>

[<span data-ttu-id="4ae00-130">**Configurare i parametri della riga di comando per i negozi online**</span><span class="sxs-lookup"><span data-stu-id="4ae00-130">**Setup Command-line Parameters for Online Stores**</span></span>](setup-command-line-parameters-for-online-stores.md)
</dt> </dl>

 

 




