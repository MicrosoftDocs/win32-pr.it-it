---
description: .
ms.assetid: 18F74BA7-2729-4EB3-8E6F-4E5A8C17C317
title: Compatibilità DEP/NX
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: beb542331d218ed4c493efde091be3e5efae6aee
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/03/2021
ms.locfileid: "106320643"
---
# <a name="depnx-compatibility"></a><span data-ttu-id="7e7ad-103">Compatibilità DEP/NX</span><span class="sxs-lookup"><span data-stu-id="7e7ad-103">DEP/NX compatibility</span></span>

<span data-ttu-id="7e7ad-104">Per impostazione predefinita, in Windows Internet Explorer 7, DEP/NX è disabilitato per motivi di compatibilità.</span><span class="sxs-lookup"><span data-stu-id="7e7ad-104">By default, in Windows Internet Explorer 7, DEP/NX is disabled for compatibility reasons.</span></span> <span data-ttu-id="7e7ad-105">Diversi componenti aggiuntivi diffusi non sono compatibili con DEP/NX e non riescono quando Windows Internet Explorer li carica con DEP/NX abilitato.</span><span class="sxs-lookup"><span data-stu-id="7e7ad-105">Several popular add-ons are not compatible with DEP/NX and fail when Windows Internet Explorer loads them with DEP/NX enabled.</span></span>

<span data-ttu-id="7e7ad-106">In genere, questi componenti aggiuntivi vengono compilati utilizzando una versione precedente di ATL Framework.</span><span class="sxs-lookup"><span data-stu-id="7e7ad-106">Typically, these add-ons are built by using an older version of the ATL framework.</span></span> <span data-ttu-id="7e7ad-107">ATL 7,1 e versioni precedenti non sono progettati con la funzionalità di protezione DEP.</span><span class="sxs-lookup"><span data-stu-id="7e7ad-107">ATL 7.1 and earlier versions are not designed with the DEP security feature.</span></span> <span data-ttu-id="7e7ad-108">Fortunatamente, le nuove versioni di Microsoft Windows Service Pack hanno nuove API DEP/NX che consentono di utilizzare DEP/NX e mantenere la compatibilità con le versioni precedenti di ATL.</span><span class="sxs-lookup"><span data-stu-id="7e7ad-108">Fortunately, new versions of Microsoft Windows service packs have new DEP/NX APIs that enable you to use DEP/NX and retain compatibility with older ATL versions.</span></span> <span data-ttu-id="7e7ad-109">Queste nuove API consentono a Internet Explorer di scegliere DEP/NX senza causare l'esito negativo dei componenti aggiuntivi compilati utilizzando versioni precedenti di ATL.</span><span class="sxs-lookup"><span data-stu-id="7e7ad-109">These new APIs enable Internet Explorer to opt into DEP/NX without causing add-ons that are built by using older versions of ATL to fail.</span></span>

<span data-ttu-id="7e7ad-110">Quando un componente aggiuntivo non è compatibile con DEP/NX e non utilizza un oggetto ATL obsoleto, è possibile utilizzare un'opzione di Criteri di gruppo per rifiutare esplicitamente DEP/NX per Internet Explorer fino a quando non viene distribuita una versione aggiornata del controllo non funzionante.</span><span class="sxs-lookup"><span data-stu-id="7e7ad-110">When an add-on is not DEP/NX-compatible and it does not use an outdated ATL, you can use a Group Policy option to opt out of DEP/NX for Internet Explorer until an updated version of the broken control is deployed.</span></span> <span data-ttu-id="7e7ad-111">Gli amministratori locali possono controllare DEP/NX eseguendo Internet Explorer come amministratore e deselezionando l'opzione **Abilita protezione della memoria** nel riquadro **Avanzate** di **Opzioni Internet**.</span><span class="sxs-lookup"><span data-stu-id="7e7ad-111">Local administrators can control DEP/NX by running Internet Explorer as an administrator and by clearing the **Enable memory protection** option in the **Advanced** pane of **Internet Options**.</span></span>

## <a name="related-topics"></a><span data-ttu-id="7e7ad-112">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="7e7ad-112">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="7e7ad-113">Correzione dei problemi di compatibilità nelle applicazioni Web utilizzando visualizzazione compatibilità</span><span class="sxs-lookup"><span data-stu-id="7e7ad-113">Fixing Compatibility Issues in Web Applications by Using Compatibility View</span></span>](remediating-web-applications-and-add-ons.md)
</dt> </dl>

 

 
