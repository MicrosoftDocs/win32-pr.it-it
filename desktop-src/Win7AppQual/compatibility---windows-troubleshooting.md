---
description: .
ms.assetid: fb2c487a-d395-45eb-9010-936a61a414d0
title: Risoluzione dei problemi di Windows
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: eacea2f4f62852da7fbaefd51db5834907a323ae
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104349636"
---
# <a name="windows-troubleshooting"></a><span data-ttu-id="1f2a5-103">Risoluzione dei problemi di Windows</span><span class="sxs-lookup"><span data-stu-id="1f2a5-103">Windows Troubleshooting</span></span>

## <a name="affected-platforms"></a><span data-ttu-id="1f2a5-104">Piattaforme interessate</span><span class="sxs-lookup"><span data-stu-id="1f2a5-104">Affected Platforms</span></span>

<span data-ttu-id="1f2a5-105">**Client** -Windows 7</span><span class="sxs-lookup"><span data-stu-id="1f2a5-105">**Clients** - Windows 7</span></span>  
<span data-ttu-id="1f2a5-106">**Server** -Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="1f2a5-106">**Servers** - Windows Server 2008 R2</span></span>  









## <a name="description"></a><span data-ttu-id="1f2a5-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="1f2a5-107">Description</span></span>

<span data-ttu-id="1f2a5-108">Una nuova funzionalità di Windows 7 Action Center (precedentemente nota come Solutions Center), risoluzione dei problemi di Windows, offre un'esperienza di risoluzione dei problemi sistematica per l'utente.</span><span class="sxs-lookup"><span data-stu-id="1f2a5-108">A new Windows 7 Action Center (formerly known as Solutions Center) feature, Windows Troubleshooting, delivers a systematic troubleshooting experience for the user.</span></span> <span data-ttu-id="1f2a5-109">Il centro operativo è una delle cinque icone aggiunte nel systray.</span><span class="sxs-lookup"><span data-stu-id="1f2a5-109">The Action Center is one of the five icons pinned in the systray.</span></span> <span data-ttu-id="1f2a5-110">Risoluzione dei problemi di Windows consente di sfogliare o cercare i pacchetti di risoluzione dei problemi inclusi nel pacchetto e per la risoluzione dei problemi relativi ai pacchetti archiviati in un server Microsoft su Internet, un'esperienza migliore quando si è connessi (BWC).</span><span class="sxs-lookup"><span data-stu-id="1f2a5-110">Windows Troubleshooting allows you to browse or search for in-box troubleshooting packs and for troubleshooting packs that are stored on a Microsoft server on the Internet – a Better When Connected (BWC) experience.</span></span> <span data-ttu-id="1f2a5-111">È possibile selezionare ed eseguire un pacchetto di risoluzione dei problemi per tentare di risolvere il problema.</span><span class="sxs-lookup"><span data-stu-id="1f2a5-111">You can select and run a troubleshooting pack to attempt to resolve their problem.</span></span> <span data-ttu-id="1f2a5-112">Se non è possibile identificare la risoluzione del problema, è possibile scegliere di cercare la guida, il contenuto della community e gli articoli di supporto o altri pacchetti di risoluzione dei problemi relativi al contenuto correlato.</span><span class="sxs-lookup"><span data-stu-id="1f2a5-112">If you cannot identify a resolution to the problem, you have the option of searching help, community content, and support articles, or other troubleshooting packs for relevant related content.</span></span> <span data-ttu-id="1f2a5-113">Se non si fornisce una risposta al problema, è possibile ripristinare il computer fino a un momento precedente a quando si è verificato il problema oppure ottenere assistenza tramite assistenza remota.</span><span class="sxs-lookup"><span data-stu-id="1f2a5-113">Should that not provide an answer to the problem, you can restore the PC to a time prior to when the problem occurred or get help through remote assistance.</span></span> <span data-ttu-id="1f2a5-114">Lo scopo è quello di consentire all'utente di trovare una soluzione al problema in modo semplice e rapido.</span><span class="sxs-lookup"><span data-stu-id="1f2a5-114">The intent is to allow you to find a solution to the problem easily and quickly.</span></span>

## <a name="usage"></a><span data-ttu-id="1f2a5-115">Utilizzo</span><span class="sxs-lookup"><span data-stu-id="1f2a5-115">Usage</span></span>

<span data-ttu-id="1f2a5-116">Il centro operativo è chiaramente visibile e disponibile da diverse posizioni.</span><span class="sxs-lookup"><span data-stu-id="1f2a5-116">The Action Center is clearly visible and available from several locations.</span></span> <span data-ttu-id="1f2a5-117">È possibile avviarlo dal menu di scelta rapida del centro operativo nel systray, dal pannello di controllo come collegamento di collegamento in sistema e manutenzione, dalla pagina principale del centro operativo e dal contenuto della guida.</span><span class="sxs-lookup"><span data-stu-id="1f2a5-117">You can launch it from the context menu of the Action Center in the systray, from the control panel as a shortcut link under system and maintenance, from the main page of the Action Center, and from Help content.</span></span>

<span data-ttu-id="1f2a5-118">I pacchetti di risoluzione dei problemi sono basati su script di PowerShell.</span><span class="sxs-lookup"><span data-stu-id="1f2a5-118">Troubleshooting packs are based upon powershell scripts.</span></span> <span data-ttu-id="1f2a5-119">Il processo di creazione e pubblicazione di un pacchetto di risoluzione dei problemi verrà reso pubblico per consentire a OEM, IHV, ISV e professionisti IT di sviluppare e distribuire il proprio contenuto per la risoluzione dei problemi.</span><span class="sxs-lookup"><span data-stu-id="1f2a5-119">The process of authoring and publishing a troubleshooting pack will be made public to allow OEMs, IHVs, ISVs, and IT Professionals to develop and ship their own troubleshooting content.</span></span>

<span data-ttu-id="1f2a5-120">Per un'esperienza utente coerente, assicurarsi di seguire le procedure consigliate e le linee guida descritte nel Toolkit per la risoluzione dei problemi di Windows durante la progettazione di pacchetti di risoluzione dei problemi personalizzati.</span><span class="sxs-lookup"><span data-stu-id="1f2a5-120">For a consistent user experience, be sure to follow the best practices and guidelines described in the Windows troubleshooting toolkit when designing your own troubleshooting packs.</span></span>

 

 



