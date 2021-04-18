---
title: Impostazione del registro di sistema acquisizione invisibile all'utente
description: Impostazione del registro di sistema acquisizione invisibile all'utente
ms.assetid: 50e0b27e-ddf8-441f-adcd-d88d36f3edaf
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1a00bbb6d930cb137ed12ffbcb05af31cee3c99c
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "106298586"
---
# <a name="silent-acquisition-registry-setting"></a><span data-ttu-id="68bc7-103">Impostazione del registro di sistema acquisizione invisibile all'utente</span><span class="sxs-lookup"><span data-stu-id="68bc7-103">Silent Acquisition Registry Setting</span></span>

<span data-ttu-id="68bc7-104">Microsoft Windows Media Player utilizza il seguente valore del registro di sistema per determinare se abilitare l'acquisizione invisibile all'utente, uno stato in cui il lettore scarica automaticamente i diritti di utilizzo quando l'utente riproduce o Sincronizza il contenuto protetto.</span><span class="sxs-lookup"><span data-stu-id="68bc7-104">Microsoft Windows Media Player uses the following registry value to determine whether to enable silent acquisition, a state in which the player downloads usage rights automatically when the user plays or syncs protected content.</span></span>

<span data-ttu-id="68bc7-105">**HKEY \_ \_Computer locale** \\ **software** \\ **Microsoft** \\ **MediaPlayer** \\ **Preferences** \\ **SilentAcquisition**</span><span class="sxs-lookup"><span data-stu-id="68bc7-105">**HKEY\_LOCAL\_MACHINE**\\**SOFTWARE**\\**Microsoft**\\**MediaPlayer**\\**Preferences**\\**SilentAcquisition**</span></span>

<span data-ttu-id="68bc7-106">Il valore di SilentAcquisition ha il formato seguente:</span><span class="sxs-lookup"><span data-stu-id="68bc7-106">The SilentAcquisition value has the following form:</span></span>



| <span data-ttu-id="68bc7-107">Nome</span><span class="sxs-lookup"><span data-stu-id="68bc7-107">Name</span></span>              | <span data-ttu-id="68bc7-108">Tipo</span><span class="sxs-lookup"><span data-stu-id="68bc7-108">Type</span></span>           | <span data-ttu-id="68bc7-109">Descrizione</span><span class="sxs-lookup"><span data-stu-id="68bc7-109">Description</span></span>                                                                                                       |
|-------------------|----------------|-------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="68bc7-110">SilentAcquisition</span><span class="sxs-lookup"><span data-stu-id="68bc7-110">SilentAcquisition</span></span> | <span data-ttu-id="68bc7-111">**REG \_ DWORD**</span><span class="sxs-lookup"><span data-stu-id="68bc7-111">**REG\_DWORD**</span></span> | <span data-ttu-id="68bc7-112">Impostare questo valore su 1 per abilitare l'acquisizione invisibile all'utente o impostarlo su 0 per disabilitare l'acquisizione invisibile all'utente.</span><span class="sxs-lookup"><span data-stu-id="68bc7-112">Set this value to 1 to enable silent acquisition, or set it to 0 to disable silent acquisition.</span></span> <span data-ttu-id="68bc7-113">Il valore predefinito è 1.</span><span class="sxs-lookup"><span data-stu-id="68bc7-113">The default is 1.</span></span> |



 

<span data-ttu-id="68bc7-114">Per specificare un valore, l'utente può avviare Media Player di Windows, aprire la finestra di dialogo **Opzioni** , fare clic sulla scheda **privacy** , quindi selezionare o deselezionare la casella di controllo **Scarica automaticamente i diritti di utilizzo quando si riproduce o si sincronizza un file** .</span><span class="sxs-lookup"><span data-stu-id="68bc7-114">To specify a value, the user can start Windows Media Player, open the **Options** dialog box, click the **Privacy** tab, and then select or clear the **Download usage rights automatically when I play or sync a file** check box.</span></span> <span data-ttu-id="68bc7-115">Selezionando questa casella di controllo, si imposta SilentAcquisition su 1; Se si deseleziona la casella di controllo, questo viene impostato su 0.</span><span class="sxs-lookup"><span data-stu-id="68bc7-115">Selecting this check box sets SilentAcquisition to 1; clearing the check box sets it to 0.</span></span>

## <a name="related-topics"></a><span data-ttu-id="68bc7-116">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="68bc7-116">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="68bc7-117">**Impostazioni del registro di sistema**</span><span class="sxs-lookup"><span data-stu-id="68bc7-117">**Registry Settings**</span></span>](registry-settings.md)
</dt> </dl>

 

 




