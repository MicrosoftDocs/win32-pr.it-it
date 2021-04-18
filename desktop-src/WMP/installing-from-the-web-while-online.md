---
title: Installazione dal Web in linea
description: Installazione dal Web in linea
ms.assetid: 891483b0-6ba4-4ed4-b043-c6c109dc696b
keywords:
- Windows Media Player Online Stores, installazione dal Web in linea
- negozi online, installazione dal Web in linea
- digitare 1 negozi online, installazione dal Web in linea
- digitare 2 archivi online, installazione dal Web in linea
- Windows Media Player Online Stores, installazioni online dal Web
- negozi online, installazioni online dal Web
- digitare 1 negozi online, installazioni online dal Web
- digitare 2 archivi online, installazioni online dal Web
- installazione di archivi online dal Web in linea
- installazioni online di archivi online
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dd342d3fc79cf3012d5bc290561a9b63167e044f
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "106298429"
---
# <a name="installing-from-the-web-while-online"></a><span data-ttu-id="4ff33-113">Installazione dal Web in linea</span><span class="sxs-lookup"><span data-stu-id="4ff33-113">Installing from the Web While Online</span></span>

<span data-ttu-id="4ff33-114">Gli utenti possono installare Windows Media Player come download Web mentre si è connessi a Internet.</span><span class="sxs-lookup"><span data-stu-id="4ff33-114">Users can install Windows Media Player as a Web download while connected to the Internet.</span></span> <span data-ttu-id="4ff33-115">In questo caso, Microsoft può configurare l'archivio online iniziale specificato.</span><span class="sxs-lookup"><span data-stu-id="4ff33-115">In this case, Microsoft can configure the initial online store that you specify.</span></span>

<span data-ttu-id="4ff33-116">Per ridistribuire Windows Media Player in questo modo, usare l'URL seguente:</span><span class="sxs-lookup"><span data-stu-id="4ff33-116">To redistribute Windows Media Player in this manner, use the following URL:</span></span>

<span data-ttu-id="4ff33-117"> https://go.microsoft.com/fwlink/p/?linkid=32981&SV=*version*&UserLocale =*localizzated*&Service =*Key*</span><span class="sxs-lookup"><span data-stu-id="4ff33-117">https://go.microsoft.com/fwlink/p/?linkid=32981&SV=*version*&UserLocale=*localID*&Service=*key*</span></span>

<span data-ttu-id="4ff33-118">Nell'URL precedente impostare *chiave* sul nome della chiave per l'archivio online e impostare *LocaleID* sull'identificatore delle impostazioni locali in cui l'archivio fornisce il servizio.</span><span class="sxs-lookup"><span data-stu-id="4ff33-118">In the preceding URL, set *key* to the key name for your online store, and set *localeID* to the identifier of the locale where your store provides service.</span></span> <span data-ttu-id="4ff33-119">Impostare la *versione* su 2 per Windows Media Player 11 in Windows XP o 1 per Windows Media Player 10.</span><span class="sxs-lookup"><span data-stu-id="4ff33-119">Set *version* to 2 for Windows Media Player 11 on Windows XP or 1 for Windows Media Player 10.</span></span> <span data-ttu-id="4ff33-120">L'URL installa Windows Media Player e imposta l'archivio attivo iniziale su quello specificato dalla *chiave*.</span><span class="sxs-lookup"><span data-stu-id="4ff33-120">The URL installs Windows Media Player and sets the initial active store to the one specified by *key*.</span></span>

<span data-ttu-id="4ff33-121">Nell'esempio seguente viene illustrato un URL che installa Windows Media Player 11 e imposta Proseware come archivio attivo iniziale.</span><span class="sxs-lookup"><span data-stu-id="4ff33-121">The following example shows a URL that installs Windows Media Player 11 and sets Proseware as the initial active store.</span></span> <span data-ttu-id="4ff33-122">Il valore di 409 per *LocaleID* indica che Proseware fornisce il servizio nel Stati Uniti.</span><span class="sxs-lookup"><span data-stu-id="4ff33-122">The value of 409 for *localeID* indicates that Proseware provides service in the United States.</span></span>

https://go.microsoft.com/fwlink/p/?linkid=32981&SV=2&UserLocale=409&Service=Proseware

<span data-ttu-id="4ff33-123">Se il documento ServiceInfo per l'archivio online include un elemento di installazione, il programma di installazione di Windows Media Player Personalizza il processo di installazione.</span><span class="sxs-lookup"><span data-stu-id="4ff33-123">If the ServiceInfo document for the online store includes an Install element, Windows Media Player setup will customize the setup process.</span></span> <span data-ttu-id="4ff33-124">Utilizzando i valori di attributo, il programma di installazione Visualizza il contratto di licenza con l'utente finale (EULA) e l'informativa sulla privacy, nonché recupera e installa il file CAB nel computer dell'utente.</span><span class="sxs-lookup"><span data-stu-id="4ff33-124">Using the attribute values, setup displays your End User License Agreement (EULA) and your privacy statement, and also retrieves and installs your .cab file to the user's computer.</span></span> <span data-ttu-id="4ff33-125">Ad esempio, è possibile usare questa funzionalità per installare la versione più recente di un oggetto COM richiesto dal negozio online.</span><span class="sxs-lookup"><span data-stu-id="4ff33-125">For example, you can use this feature to install the latest version of a COM object that your online store requires.</span></span>

## <a name="related-topics"></a><span data-ttu-id="4ff33-126">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="4ff33-126">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="4ff33-127">**Informazioni comuni ai negozi online di tipo 1 e di tipo 2**</span><span class="sxs-lookup"><span data-stu-id="4ff33-127">**Information Common to Type 1 and Type 2 Online Stores**</span></span>](information-common-to-type-1-and-type-2-online-stores.md)
</dt> <dt>

[<span data-ttu-id="4ff33-128">**Elemento install**</span><span class="sxs-lookup"><span data-stu-id="4ff33-128">**Install Element**</span></span>](install-element.md)
</dt> <dt>

[<span data-ttu-id="4ff33-129">**Documento ServiceInfo**</span><span class="sxs-lookup"><span data-stu-id="4ff33-129">**ServiceInfo Document**</span></span>](serviceinfo-document.md)
</dt> <dt>

[<span data-ttu-id="4ff33-130">**Impostazione dell'archivio online iniziale**</span><span class="sxs-lookup"><span data-stu-id="4ff33-130">**Setting the Initial Online Store**</span></span>](setting-the-initial-online-store.md)
</dt> </dl>

 

 




