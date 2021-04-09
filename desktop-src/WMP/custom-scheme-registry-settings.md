---
title: Impostazioni del registro di sistema personalizzato
description: Impostazioni del registro di sistema personalizzato
ms.assetid: ded2b492-7755-4ba5-87cf-720a79ec79de
keywords:
- Windows Media Player, impostazioni del registro di sistema personalizzato
- Windows Media Player, schemi
- Windows Media Player, registro di sistema
- Registro di sistema, Impostazioni schema personalizzate
- Registro di sistema, schemi
- Registro di sistema, impostazioni per Windows Media Player
- schemi
- impostazioni del registro di sistema personalizzato
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6a02649d9536140fff0ff0d3188a5b25feb49688
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104044304"
---
# <a name="custom-scheme-registry-settings"></a><span data-ttu-id="89f15-111">Impostazioni del registro di sistema personalizzato</span><span class="sxs-lookup"><span data-stu-id="89f15-111">Custom Scheme Registry Settings</span></span>

<span data-ttu-id="89f15-112">Gli schemi sono protocolli personalizzati.</span><span class="sxs-lookup"><span data-stu-id="89f15-112">Schemes are custom protocols.</span></span> <span data-ttu-id="89f15-113">Windows Media Player gestisce un elenco di schemi nel registro di sistema nel computer dell'utente.</span><span class="sxs-lookup"><span data-stu-id="89f15-113">Windows Media Player maintains a list of schemes in the registry on the user's computer.</span></span> <span data-ttu-id="89f15-114">Quando l'utente tenta di riprodurre un file multimediale digitale, il giocatore verifica prima di tutto se Windows Media Format SDK supporta lo schema.</span><span class="sxs-lookup"><span data-stu-id="89f15-114">When the user attempts to play a digital media file, the Player first checks whether the Windows Media Format SDK supports the scheme.</span></span> <span data-ttu-id="89f15-115">In caso contrario, il lettore controlla lo schema rispetto all'elenco nel registro di sistema.</span><span class="sxs-lookup"><span data-stu-id="89f15-115">If it doesn't, the Player checks the scheme against the list in the registry.</span></span> <span data-ttu-id="89f15-116">Se viene trovata una corrispondenza, il lettore controlla un valore che indica quale tecnologia o *Runtime* sottostante (ad esempio Microsoft DirectShow o Windows Media Format SDK) può essere usato per riprodurre il file.</span><span class="sxs-lookup"><span data-stu-id="89f15-116">If a match is found, the Player then checks a value that indicates which underlying technology, or *runtime* (such as Microsoft DirectShow or the Windows Media Format SDK), can be used to play the file.</span></span> <span data-ttu-id="89f15-117">Se non viene trovata alcuna corrispondenza, il lettore Visualizza all'utente una finestra di dialogo di avviso che richiede all'utente l'autorizzazione per tentare di riprodurre il file.</span><span class="sxs-lookup"><span data-stu-id="89f15-117">If no match is found, the Player presents the user with a warning dialog box that prompts the user for permission to attempt to play the file.</span></span> <span data-ttu-id="89f15-118">Se si esegue lo streaming di file multimediali digitali utilizzando uno schema di protocollo personalizzato, è possibile impedire che questo avviso venga visualizzato nel computer dell'utente registrando lo schema e fornendo un valore per il Runtime.</span><span class="sxs-lookup"><span data-stu-id="89f15-118">If you stream digital media files using a custom protocol scheme, you can prevent this warning from appearing on the user's computer by registering the scheme and providing a value for the runtime.</span></span>

<span data-ttu-id="89f15-119">L'elenco di schemi viene mantenuto come un set di chiavi del registro di sistema che corrispondono agli schemi registrati, senza i due punti e le due barre (://).</span><span class="sxs-lookup"><span data-stu-id="89f15-119">The list of schemes is maintained as a set of registry keys that match the registered schemes, without the colon and the two slashes (://).</span></span> <span data-ttu-id="89f15-120">Ad esempio, la chiave per lo schema wmhtml://, usata per lo streaming di file multimediali avanzati, è denominata "wmhtml".</span><span class="sxs-lookup"><span data-stu-id="89f15-120">For example, the key for the wmhtml:// scheme, which is used to stream rich media, is named "wmhtml".</span></span> <span data-ttu-id="89f15-121">Viene mantenuto un elenco separato per il computer locale e per ogni utente.</span><span class="sxs-lookup"><span data-stu-id="89f15-121">A separate list is maintained for the local machine and for each user.</span></span> <span data-ttu-id="89f15-122">Per il computer locale, le chiavi dello schema sono sottochiavi della chiave del registro di sistema seguente:</span><span class="sxs-lookup"><span data-stu-id="89f15-122">For the local machine, the scheme keys are subkeys of the following registry key:</span></span>

<span data-ttu-id="89f15-123">**HKEY \_ \_ computer locale \\ software \\ Microsoft \\ Multimedia \\ wmplayer \\ Scheme\\**</span><span class="sxs-lookup"><span data-stu-id="89f15-123">**HKEY\_LOCAL\_MACHINE\\Software\\Microsoft\\Multimedia\\WMPlayer\\Schemes\\**</span></span>

<span data-ttu-id="89f15-124">Ad esempio, la chiave per lo schema wmhtml://per il computer locale è:</span><span class="sxs-lookup"><span data-stu-id="89f15-124">For example, the key for the wmhtml:// scheme for the local machine is:</span></span>

<span data-ttu-id="89f15-125">**HKEY \_ Local \_ Machine \\ software \\ Microsoft \\ Multimedia \\ wmplayer \\ schemes \\ wmhtml**</span><span class="sxs-lookup"><span data-stu-id="89f15-125">**HKEY\_LOCAL\_MACHINE\\Software\\Microsoft\\Multimedia\\WMPlayer\\Schemes\\wmhtml**</span></span>

<span data-ttu-id="89f15-126">Per modificare i valori in questa chiave o creare una nuova sottochiave, l'utente corrente deve essere un amministratore del computer.</span><span class="sxs-lookup"><span data-stu-id="89f15-126">To change values in this key or to create a new subkey, the current user must be an administrator for the computer.</span></span>

<span data-ttu-id="89f15-127">Per i singoli utenti, le chiavi dello schema sono sottochiavi della chiave del registro di sistema seguente:</span><span class="sxs-lookup"><span data-stu-id="89f15-127">For individual users, the scheme keys are subkeys of the following registry key:</span></span>

<span data-ttu-id="89f15-128">**HKEY \_ \_ software utente \\ corrente \\ \\ schemi Microsoft MediaPlayer \\ Player \\\\**</span><span class="sxs-lookup"><span data-stu-id="89f15-128">**HKEY\_CURRENT\_USER\\Software\\Microsoft\\MediaPlayer\\Player\\Schemes\\**</span></span>

<span data-ttu-id="89f15-129">Ad esempio, la chiave per lo schema wmhtml://per l'utente corrente è:</span><span class="sxs-lookup"><span data-stu-id="89f15-129">For example, the key for the wmhtml:// scheme for the current user is:</span></span>

<span data-ttu-id="89f15-130">**HKEY \_ \_ software utente \\ corrente \\ Microsoft \\ MediaPlayer \\ Player \\ schemes \\ wmhtml**</span><span class="sxs-lookup"><span data-stu-id="89f15-130">**HKEY\_CURRENT\_USER\\Software\\Microsoft\\MediaPlayer\\Player\\Schemes\\wmhtml**</span></span>

<span data-ttu-id="89f15-131">Quando si verificano gli schemi registrati, il lettore controlla prima i valori presenti nel **\_ \_ computer locale HKEY**.</span><span class="sxs-lookup"><span data-stu-id="89f15-131">When checking for registered schemes, the Player first checks the values located in **HKEY\_LOCAL\_MACHINE**.</span></span> <span data-ttu-id="89f15-132">Se non ne viene trovato nessuno per lo schema corrente, il lettore controlla i valori **nell' \_ \_ utente corrente di HKEY**.</span><span class="sxs-lookup"><span data-stu-id="89f15-132">If none are found for the current scheme, the Player next checks the values in **HKEY\_CURRENT\_USER**.</span></span> <span data-ttu-id="89f15-133">Se non viene trovato alcuno per lo schema corrente, il lettore Visualizza l'avviso per l'utente.</span><span class="sxs-lookup"><span data-stu-id="89f15-133">If none are found for the current scheme, the Player displays the warning to the user.</span></span>

<span data-ttu-id="89f15-134">Ogni sottochiave dello schema può contenere uno dei seguenti valori possibili per il *Runtime*.</span><span class="sxs-lookup"><span data-stu-id="89f15-134">Each scheme subkey may contain one of the following possible values for *Runtime*.</span></span>



| <span data-ttu-id="89f15-135">Valore</span><span class="sxs-lookup"><span data-stu-id="89f15-135">Value</span></span> | <span data-ttu-id="89f15-136">Descrizione</span><span class="sxs-lookup"><span data-stu-id="89f15-136">Description</span></span>                                |
|-------|--------------------------------------------|
| <span data-ttu-id="89f15-137">6</span><span class="sxs-lookup"><span data-stu-id="89f15-137">6</span></span>     | <span data-ttu-id="89f15-138">Eseguire il rendering usando Windows Media Format SDK.</span><span class="sxs-lookup"><span data-stu-id="89f15-138">Render using the Windows Media Format SDK.</span></span> |
| <span data-ttu-id="89f15-139">7</span><span class="sxs-lookup"><span data-stu-id="89f15-139">7</span></span>     | <span data-ttu-id="89f15-140">Eseguire il rendering con Microsoft DirectShow.</span><span class="sxs-lookup"><span data-stu-id="89f15-140">Render using Microsoft DirectShow.</span></span>         |



 

<span data-ttu-id="89f15-141">La modifica del valore di *Runtime* per uno schema supportato da Windows Media Format SDK non avrà alcun effetto.</span><span class="sxs-lookup"><span data-stu-id="89f15-141">Changing the *Runtime* value for a scheme that the Windows Media Format SDK supports will have no effect.</span></span> <span data-ttu-id="89f15-142">Il lettore utilizzerà sempre Windows Media Format SDK come runtime per gli schemi supportati da Windows Media Format SDK.</span><span class="sxs-lookup"><span data-stu-id="89f15-142">The Player will always use the Windows Media Format SDK as the runtime for schemes that the Windows Media Format SDK supports.</span></span> <span data-ttu-id="89f15-143">Questo valore del registro di sistema è progettato per consentire la configurazione di runtime per gli schemi personalizzati.</span><span class="sxs-lookup"><span data-stu-id="89f15-143">This registry value is designed to allow runtime configuration for custom schemes.</span></span>

## <a name="related-topics"></a><span data-ttu-id="89f15-144">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="89f15-144">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="89f15-145">**Impostazioni del registro di sistema**</span><span class="sxs-lookup"><span data-stu-id="89f15-145">**Registry Settings**</span></span>](registry-settings.md)
</dt> </dl>

 

 




