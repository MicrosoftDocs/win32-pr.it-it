---
description: Il percorso di un oggetto spazio dei nomi descrive la posizione di un determinato spazio dei nomi in un server. Il percorso di un oggetto spazio dei nomi contiene elementi server e spazio dei nomi e viene formattato con le barre avanti o indietro.
ms.assetid: 6d8da19e-0914-4267-870e-c203176b895e
ms.tgt_platform: multiple
title: Descrizione del percorso di un oggetto dello spazio dei nomi WMI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 586104a1c193f1c229b0fbb27437d22e3686585b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104049814"
---
# <a name="describing-a-wmi-namespace-object-path"></a><span data-ttu-id="7ba34-104">Descrizione del percorso di un oggetto dello spazio dei nomi WMI</span><span class="sxs-lookup"><span data-stu-id="7ba34-104">Describing a WMI Namespace Object Path</span></span>

<span data-ttu-id="7ba34-105">Il percorso di un oggetto spazio dei nomi descrive la posizione di un determinato spazio dei nomi in un server.</span><span class="sxs-lookup"><span data-stu-id="7ba34-105">A namespace object path describes the location of a particular namespace on a server.</span></span> <span data-ttu-id="7ba34-106">Il percorso di un oggetto spazio dei nomi contiene elementi server e spazio dei nomi e viene formattato con le barre avanti o indietro.</span><span class="sxs-lookup"><span data-stu-id="7ba34-106">A namespace object path contains server and namespace elements, and is formatted using either forward or backward slashes.</span></span>

<span data-ttu-id="7ba34-107">L'elemento server specifica il nome di rete del computer che ospita lo spazio dei nomi, come illustrato nell'esempio seguente.</span><span class="sxs-lookup"><span data-stu-id="7ba34-107">The server element specifies the network name of the computer that is hosting the namespace, as shown in the following example.</span></span>

``` syntax
\\Server\Namespace
```

<span data-ttu-id="7ba34-108">\- - oppure -</span><span class="sxs-lookup"><span data-stu-id="7ba34-108">\- or -</span></span>

``` syntax
//Server/Namespace
```

<span data-ttu-id="7ba34-109">Se il server è il computer locale, usare un singolo punto anziché il nome del server, come illustrato nell'esempio seguente.</span><span class="sxs-lookup"><span data-stu-id="7ba34-109">If the server is the local computer, use a single dot instead of the server name, as shown in the following example.</span></span>

``` syntax
\\.\Namespace
```

<span data-ttu-id="7ba34-110">L'elemento Namespace specifica qualsiasi spazio dei nomi valido.</span><span class="sxs-lookup"><span data-stu-id="7ba34-110">The namespace element specifies any valid namespace.</span></span> <span data-ttu-id="7ba34-111">Uno spazio dei nomi è rappresentato da una stringa gerarchica contenente elementi delimitati da singole barre rovesciate, ad esempio \\ CIMV2 radice.</span><span class="sxs-lookup"><span data-stu-id="7ba34-111">A namespace is represented with a hierarchical string containing elements delimited by single backslashes, such as root\\cimv2.</span></span> <span data-ttu-id="7ba34-112">Non è possibile utilizzare le barre nei nomi degli spazi dei nomi.</span><span class="sxs-lookup"><span data-stu-id="7ba34-112">You cannot use forward slashes within namespace names.</span></span>

 

 



