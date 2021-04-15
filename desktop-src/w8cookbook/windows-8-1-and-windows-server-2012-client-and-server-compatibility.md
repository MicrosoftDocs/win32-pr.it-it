---
title: Compatibilità tra client e server Windows 8.1 e Windows Server 2012 R2
description: Compatibilità tra client e server Windows 8.1 e Windows Server 2012 R2
ms.assetid: 45C37E2D-3513-4708-A562-1426D2B832F0
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1c46647dd9ad0f0baeae1ffb98905740a37f9530
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104515607"
---
# <a name="windows-81-and-windows-server-2012-r2-client-and-server-compatibility"></a><span data-ttu-id="b0f00-103">Compatibilità tra client e server Windows 8.1 e Windows Server 2012 R2</span><span class="sxs-lookup"><span data-stu-id="b0f00-103">Windows 8.1 and Windows Server 2012 R2 client and server compatibility</span></span>

<span data-ttu-id="b0f00-104">In questa sezione vengono descritte le modifiche apportate al sistema operativo a cui è necessario prestare particolare attenzione a causa del potenziale impatto sulle app esistenti e del modo in cui le nuove app devono essere progettate nei client, nei server o nei client e nei server.</span><span class="sxs-lookup"><span data-stu-id="b0f00-104">This section describes changes in the operating system that you should pay special attention to due to the potential impacts on existing apps and how new apps should be designed on clients, on servers, or on both clients and servers.</span></span> <span data-ttu-id="b0f00-105">Di seguito è riportato l'elenco degli argomenti trattati in questa sezione:</span><span class="sxs-lookup"><span data-stu-id="b0f00-105">Following is the list of topics covered in this section:</span></span>

## <a name="in-this-section"></a><span data-ttu-id="b0f00-106">Contenuto della sezione</span><span class="sxs-lookup"><span data-stu-id="b0f00-106">In this section</span></span>



| <span data-ttu-id="b0f00-107">Argomento</span><span class="sxs-lookup"><span data-stu-id="b0f00-107">Topic</span></span>                                                                                                                                                                                                                         | <span data-ttu-id="b0f00-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="b0f00-108">Description</span></span> |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------|
| [<span data-ttu-id="b0f00-109">Modifiche della versione del sistema operativo in Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="b0f00-109">Operating system version changes in Windows 8.1</span></span>](operating-system-version-changes-in-windows-8-1.md)<br/>                                                                                                             |             |
| [<span data-ttu-id="b0f00-110">Componenti di Windows installati su richiesta</span><span class="sxs-lookup"><span data-stu-id="b0f00-110">Windows components installed on demand</span></span>](windows-components-installed-on-demand.md)<br/>                                                                                                                               |             |
| [<span data-ttu-id="b0f00-111">Comportamento del fallback del tipo di carattere HTML</span><span class="sxs-lookup"><span data-stu-id="b0f00-111">HTML font fallback behavior</span></span>](html-font-fallback-behavior.md)<br/>                                                                                                                                                     |             |
| [<span data-ttu-id="b0f00-112">Windows 8.1 consente solo URI https, non URI http</span><span class="sxs-lookup"><span data-stu-id="b0f00-112">Windows 8.1 allows only https URIs, not http URIs</span></span>](windows-8-1-allows-only-https-uris--not-http-uris.md)<br/>                                                                                                         |             |
| [<span data-ttu-id="b0f00-113">Input MouseWheel per Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="b0f00-113">Mousewheel input for Windows 8.1</span></span>](mousewheel-input-for-windows-8-1.md)<br/>                                                                                                                                           |             |
| [<span data-ttu-id="b0f00-114">Dispositivi touchpad di precisione Windows</span><span class="sxs-lookup"><span data-stu-id="b0f00-114">Windows precision touchpad devices</span></span>](windows-precision-touchpad-devices.md)<br/>                                                                                                                                       |             |
| [<span data-ttu-id="b0f00-115">DPI elevato per le app desktop in Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="b0f00-115">High DPI for desktop apps in Windows 8.1</span></span>](high-dpi-for-desktop-apps-in-windows-8-1.md)<br/>                                                                                                                           |             |
| [<span data-ttu-id="b0f00-116">L'interfaccia utente di Edge viene evitata in scenari di inerzia e in uscita</span><span class="sxs-lookup"><span data-stu-id="b0f00-116">Edge UI is suppressed in  in-out-in  and  inertia  scenarios</span></span>](edge-ui-is-suppressed-in--in-out-in--and--inertia--scenarios.md)<br/>                                                                                   |             |
| [<span data-ttu-id="b0f00-117">La chiamata a ImmSetConversionStatus () o ImmGetConversionStatus () dalle app di Windows Store non è supportata</span><span class="sxs-lookup"><span data-stu-id="b0f00-117">Calling ImmSetConversionStatus() or ImmGetConversionStatus() from Windows Store apps is not supported</span></span>](calling-immsetconversionstatus---or-immgetconversionstatus---from-windows-store-apps-is-not-supported.md)<br/> |             |
| [<span data-ttu-id="b0f00-118">Modello in modalità IME modificato da per utente a per thread</span><span class="sxs-lookup"><span data-stu-id="b0f00-118">IME mode model changed from per-user to per-thread</span></span>](ime-mode-model-changed-from-per-user-to-per-thread.md)<br/>                                                                                                       |             |
| [<span data-ttu-id="b0f00-119">Le API di input Method Manager non sono supportate dall'IME cinese semplificato</span><span class="sxs-lookup"><span data-stu-id="b0f00-119">Input Method manager APIs are not supported by Simplified Chinese IME</span></span>](input-method-manager-apis-are-not-supported-by-simplified-chinese-ime.md)<br/>                                                                 |             |
| [<span data-ttu-id="b0f00-120">Alcuni pannelli di input software IME per l'Asia orientale inviano ora vKey</span><span class="sxs-lookup"><span data-stu-id="b0f00-120">Some East Asian IME software input panels now send vKey</span></span>](some-east-asian-ime-software-input-panels-now-send-vkey.md)<br/>                                                                                             |             |



 

 

 





