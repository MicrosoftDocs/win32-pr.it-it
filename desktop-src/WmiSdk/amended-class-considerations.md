---
description: Non è possibile creare istanze delle classi modificate nello spazio dei nomi localizzato. Le classi modificate nello spazio dei nomi localizzato vengono considerate come se fossero astratte, sebbene non contengano il qualificatore astratto.
ms.assetid: a0583153-f5d2-4f4c-ab2e-6ec468e665c7
ms.tgt_platform: multiple
title: Considerazioni sulle classi modificate
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f77a2caa315ab4878fe619c13c69bd5d2e1a2610
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104234320"
---
# <a name="amended-class-considerations"></a><span data-ttu-id="ec280-104">Considerazioni sulle classi modificate</span><span class="sxs-lookup"><span data-stu-id="ec280-104">Amended Class Considerations</span></span>

<span data-ttu-id="ec280-105">Non è possibile creare istanze delle classi modificate nello spazio dei nomi localizzato.</span><span class="sxs-lookup"><span data-stu-id="ec280-105">You cannot create instances of the amended classes in the localized namespace.</span></span> <span data-ttu-id="ec280-106">Le classi modificate nello spazio dei nomi localizzato vengono considerate come se fossero astratte, sebbene non contengano il qualificatore [**astratto**](standard-qualifiers.md) .</span><span class="sxs-lookup"><span data-stu-id="ec280-106">Amended classes in the localized namespace are treated as if they are abstract although they do not contain the [**Abstract**](standard-qualifiers.md) qualifier.</span></span>

<span data-ttu-id="ec280-107">Se si recupera una classe modificata da uno spazio dei nomi localizzato usando il flag WBEM \_ \_ , usare il \_ flag dei \_ qualificatori modificati e generare un'istanza da essa, l'istanza contiene tutti i qualificatori modificati della classe modificata.</span><span class="sxs-lookup"><span data-stu-id="ec280-107">If you retrieve an amended class from a localized namespace using the WBEM\_FLAG\_USE\_AMENDED\_QUALIFIERS flag and spawn an instance from it, the instance contains all of the amended qualifiers of the amended class.</span></span> <span data-ttu-id="ec280-108">Non è possibile archiviare questa nuova classe nello spazio dei nomi che contiene la definizione di classe di base, a meno che non si esegua l'operazione **put** con il flag WBEM \_ usare il flag dei \_ \_ \_ qualificatori modificati.</span><span class="sxs-lookup"><span data-stu-id="ec280-108">You cannot store this new class in the namespace that contains the basic class definition unless you perform the **put** operation with the WBEM\_FLAG\_USE\_AMENDED\_QUALIFIERS flag.</span></span> <span data-ttu-id="ec280-109">Questo flag indica a WMI di eliminare tutti i qualificatori modificati prima di salvare l'oggetto.</span><span class="sxs-lookup"><span data-stu-id="ec280-109">This flag instructs WMI to strip away any amended qualifiers before saving the object.</span></span> <span data-ttu-id="ec280-110">Se non si specifica \_ il flag WBEM \_ usare \_ \_ i qualificatori modificati, l'operazione **put** ha esito negativo con un errore di \_ oggetto WBEM E \_ modificato \_ .</span><span class="sxs-lookup"><span data-stu-id="ec280-110">If you do not specify WBEM\_FLAG\_USE\_AMENDED\_QUALIFIERS, the **put** operation fails with a WBEM\_E\_AMENDED\_OBJECT error.</span></span>

 

 



