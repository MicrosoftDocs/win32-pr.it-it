---
description: Compatibilità DEP/NX
ms.assetid: 18F74BA7-2729-4EB3-8E6F-4E5A8C17C317
title: Compatibilità DEP/NX
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cb8b46c9143ee96b8599c10d4c70276d36e20a08
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108116429"
---
# <a name="depnx-compatibility"></a><span data-ttu-id="3874b-103">Compatibilità DEP/NX</span><span class="sxs-lookup"><span data-stu-id="3874b-103">DEP/NX compatibility</span></span>

<span data-ttu-id="3874b-104">Per impostazione predefinita, in Windows Internet Explorer 7 DEP/NX è disabilitato per motivi di compatibilità.</span><span class="sxs-lookup"><span data-stu-id="3874b-104">By default, in Windows Internet Explorer 7, DEP/NX is disabled for compatibility reasons.</span></span> <span data-ttu-id="3874b-105">Diversi componenti aggiuntivi più diffusi non sono compatibili con DEP/NX e hanno esito negativo quando Windows Internet Explorer li carica con DEP/NX abilitato.</span><span class="sxs-lookup"><span data-stu-id="3874b-105">Several popular add-ons are not compatible with DEP/NX and fail when Windows Internet Explorer loads them with DEP/NX enabled.</span></span>

<span data-ttu-id="3874b-106">In genere, questi componenti aggiuntivi vengono compilati usando una versione precedente del framework ATL.</span><span class="sxs-lookup"><span data-stu-id="3874b-106">Typically, these add-ons are built by using an older version of the ATL framework.</span></span> <span data-ttu-id="3874b-107">ATL 7.1 e versioni precedenti non sono progettati con la funzionalità di sicurezza DEP.</span><span class="sxs-lookup"><span data-stu-id="3874b-107">ATL 7.1 and earlier versions are not designed with the DEP security feature.</span></span> <span data-ttu-id="3874b-108">Fortunatamente, le nuove versioni dei Service Pack di Microsoft Windows hanno nuove API DEP/NX che consentono di usare DEP/NX e di mantenere la compatibilità con le versioni precedenti di ATL.</span><span class="sxs-lookup"><span data-stu-id="3874b-108">Fortunately, new versions of Microsoft Windows service packs have new DEP/NX APIs that enable you to use DEP/NX and retain compatibility with older ATL versions.</span></span> <span data-ttu-id="3874b-109">Queste nuove API consentono Internet Explorer di acconsentire esplicitamente a DEP/NX senza causare errori nei componenti aggiuntivi compilati con versioni precedenti di ATL.</span><span class="sxs-lookup"><span data-stu-id="3874b-109">These new APIs enable Internet Explorer to opt into DEP/NX without causing add-ons that are built by using older versions of ATL to fail.</span></span>

<span data-ttu-id="3874b-110">Quando un componente aggiuntivo non è compatibile con DEP/NX e non usa un atl obsoleto, è possibile usare un'opzione Criteri di gruppo per rifiutare esplicitamente DEP/NX per Internet Explorer fino a quando non viene distribuita una versione aggiornata del controllo interrotto.</span><span class="sxs-lookup"><span data-stu-id="3874b-110">When an add-on is not DEP/NX-compatible and it does not use an outdated ATL, you can use a Group Policy option to opt out of DEP/NX for Internet Explorer until an updated version of the broken control is deployed.</span></span> <span data-ttu-id="3874b-111">Gli amministratori locali possono controllare DEP/NX eseguendo Internet Explorer come amministratore  e deselezionando  l'opzione Abilita protezione memoria nel riquadro Avanzate di **Opzioni Internet**.</span><span class="sxs-lookup"><span data-stu-id="3874b-111">Local administrators can control DEP/NX by running Internet Explorer as an administrator and by clearing the **Enable memory protection** option in the **Advanced** pane of **Internet Options**.</span></span>

## <a name="related-topics"></a><span data-ttu-id="3874b-112">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="3874b-112">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="3874b-113">Risoluzione dei problemi di compatibilità nelle applicazioni Web tramite Visualizzazione Compatibilità</span><span class="sxs-lookup"><span data-stu-id="3874b-113">Fixing Compatibility Issues in Web Applications by Using Compatibility View</span></span>](remediating-web-applications-and-add-ons.md)
</dt> </dl>

 

 
