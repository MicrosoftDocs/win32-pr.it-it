---
title: Componenti di Windows installati su richiesta
description: Componenti di Windows installati su richiesta
ms.assetid: 14865DD7-167C-462C-B85A-BD07C929D7B8
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 09d2c3c3fee1cd12d7b12900e41dc006badcf53f
ms.sourcegitcommit: ea4baf9953a78d2d6bd530b680601e39f3884541
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/01/2020
ms.locfileid: "104047492"
---
# <a name="windows-components-installed-on-demand"></a><span data-ttu-id="8fe5b-103">Componenti di Windows installati su richiesta</span><span class="sxs-lookup"><span data-stu-id="8fe5b-103">Windows components installed on demand</span></span>

## <a name="platform"></a><span data-ttu-id="8fe5b-104">Piattaforma</span><span class="sxs-lookup"><span data-stu-id="8fe5b-104">Platform</span></span>

<span data-ttu-id="8fe5b-105">**Client-** Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="8fe5b-105">**Clients -** Windows 8.1</span></span>  







## <a name="description"></a><span data-ttu-id="8fe5b-106">Descrizione</span><span class="sxs-lookup"><span data-stu-id="8fe5b-106">Description</span></span>

<span data-ttu-id="8fe5b-107">Due componenti di Windows verranno installati su richiesta in Windows 8.1: DirectPlay e NTVDM.</span><span class="sxs-lookup"><span data-stu-id="8fe5b-107">Two Windows components will be installed on demand in Windows 8.1: DirectPlay and NTVDM.</span></span> <span data-ttu-id="8fe5b-108">Questi componenti sono elencati all'interno dei componenti facoltativi nel nodo "componenti legacy".</span><span class="sxs-lookup"><span data-stu-id="8fe5b-108">These components are listed within Optional Components under the “Legacy Components” node.</span></span> <span data-ttu-id="8fe5b-109">Questi componenti vengono installati localmente come parte del sistema operativo e compressi come componenti facoltativi.</span><span class="sxs-lookup"><span data-stu-id="8fe5b-109">These components are installed locally as part of the operating system, and compressed as optional components.</span></span> <span data-ttu-id="8fe5b-110">Quando un'app fa riferimento a o chiama uno di questi componenti (in genere al primo avvio dell'app), l'installazione viene attivata automaticamente.</span><span class="sxs-lookup"><span data-stu-id="8fe5b-110">When an app references or calls one of these components (usually at first launch of the app), installation is triggered automatically.</span></span> <span data-ttu-id="8fe5b-111">Gli utenti riceveranno una notifica che indica che il componente verrà installato e dovranno confermare l'azione per continuare.</span><span class="sxs-lookup"><span data-stu-id="8fe5b-111">Users will be notified that the component will be installed, and they must confirm the action in order to proceed.</span></span> <span data-ttu-id="8fe5b-112">Per avere esito positivo, l'elevazione è necessaria se l'utente non è un amministratore.</span><span class="sxs-lookup"><span data-stu-id="8fe5b-112">Elevation is required for this to succeed if the user is not an administrator.</span></span> <span data-ttu-id="8fe5b-113">Dopo l'installazione iniziale, l'utente non deve eseguire altre azioni per riutilizzare il componente.</span><span class="sxs-lookup"><span data-stu-id="8fe5b-113">After the initial installation, the user does not need to perform any other actions to use the component again.</span></span>

## <a name="manifestation"></a><span data-ttu-id="8fe5b-114">Manifestazione</span><span class="sxs-lookup"><span data-stu-id="8fe5b-114">Manifestation</span></span>

<span data-ttu-id="8fe5b-115">Quando un'app fa riferimento o chiama un componente legacy in componenti facoltativi (al primo avvio), l'app verrà sospesa e verrà visualizzata la finestra di dialogo funzionalità su richiesta, che richiede l'autorizzazione utente per installare il componente.</span><span class="sxs-lookup"><span data-stu-id="8fe5b-115">When an app references or calls a legacy component in optional components (at first launch), the app will be suspended and the Feature on Demand dialog will open, requesting user permission to install the component.</span></span> <span data-ttu-id="8fe5b-116">Se gli utenti fanno clic su OK, è possibile che venga visualizzata una richiesta di elevazione dei privilegi in cui devono immettere le proprie credenziali.</span><span class="sxs-lookup"><span data-stu-id="8fe5b-116">If users click OK, they may also see an elevation prompt where they must enter their credentials.</span></span> <span data-ttu-id="8fe5b-117">Il componente verrà quindi installato e l'app verrà ripresa.</span><span class="sxs-lookup"><span data-stu-id="8fe5b-117">The component will then be installed and the app will resume.</span></span>

## <a name="mitigation"></a><span data-ttu-id="8fe5b-118">Strategia di riduzione del rischio</span><span class="sxs-lookup"><span data-stu-id="8fe5b-118">Mitigation</span></span>

<span data-ttu-id="8fe5b-119">Per impedire l'apertura dell'interfaccia utente su richiesta delle funzionalità, è possibile pre-installare DirectPlay e NTVDM utilizzando DISM o l'interfaccia utente dei componenti facoltativi.</span><span class="sxs-lookup"><span data-stu-id="8fe5b-119">To keep the Features on Demand UI from opening, you can pre-install DirectPlay and NTVDM using DISM or the Optional Components UI.</span></span>

## <a name="solution"></a><span data-ttu-id="8fe5b-120">Soluzione</span><span class="sxs-lookup"><span data-stu-id="8fe5b-120">Solution</span></span>

<span data-ttu-id="8fe5b-121">Si consiglia di evitare di fare riferimento o chiamare componenti che sono stati elencati come componenti facoltativi legacy in Windows nelle versioni future dell'app.</span><span class="sxs-lookup"><span data-stu-id="8fe5b-121">You are strongly encouraged to avoid referencing or calling components that have been listed as Legacy Optional Components in Windows in future versions of your app.</span></span> <span data-ttu-id="8fe5b-122">I componenti facoltativi legacy includeranno solo componenti meno recenti e meno utilizzati che potrebbero causare problemi di prestazioni e sicurezza per gli utenti.</span><span class="sxs-lookup"><span data-stu-id="8fe5b-122">Legacy Optional Components will only include older, lesser-used components that could potentially cause performance and security issues for users.</span></span>

## <a name="tests"></a><span data-ttu-id="8fe5b-123">Test</span><span class="sxs-lookup"><span data-stu-id="8fe5b-123">Tests</span></span>

<span data-ttu-id="8fe5b-124">Non sono necessarie ulteriori soluzioni di test per la compatibilità.</span><span class="sxs-lookup"><span data-stu-id="8fe5b-124">No additional test accommodations are necessary for compatibility.</span></span> <span data-ttu-id="8fe5b-125">È importante tenere presente che questa finestra di dialogo verrà visualizzata quando il componente facoltativo viene chiamato o a cui viene fatto riferimento e questa installazione richiede l'elevazione dei privilegi.</span><span class="sxs-lookup"><span data-stu-id="8fe5b-125">It is important to be aware that this dialog will appear when the optional component is called or referenced, and this installation requires elevation.</span></span>

 

 




