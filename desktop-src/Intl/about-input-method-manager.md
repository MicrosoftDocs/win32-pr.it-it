---
description: L'uso della funzionalità IMM nell'applicazione in grado di riconoscere gli IME consente agli utenti di ricordare tutti i possibili valori di caratteri.
ms.assetid: 43b3e561-b844-4688-ab3d-d99f92ed140e
title: Informazioni su Gestione metodi di input
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: af7b96c64eba5ddfb6966c96d88792fd657f94aa
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106314311"
---
# <a name="about-input-method-manager"></a><span data-ttu-id="e139b-103">Informazioni su Gestione metodi di input</span><span class="sxs-lookup"><span data-stu-id="e139b-103">About Input Method Manager</span></span>

<span data-ttu-id="e139b-104">L'uso della funzionalità IMM nell'applicazione in grado di riconoscere gli IME consente agli utenti di ricordare tutti i possibili valori di caratteri.</span><span class="sxs-lookup"><span data-stu-id="e139b-104">Use of the IMM functionality in your IME-aware application relieves users of the need to remember all possible character values.</span></span> <span data-ttu-id="e139b-105">Consente invece di monitorare le sequenze di tasti di un utente, prevedere i caratteri desiderati dall'utente e presentare un elenco di caratteri candidati da cui scegliere.</span><span class="sxs-lookup"><span data-stu-id="e139b-105">Instead, it allows the IME to monitor a user's keystrokes, anticipates the characters the user might want, and presents a list of candidate characters from which to choose.</span></span>

> [!Note]  
> <span data-ttu-id="e139b-106">IMM esegue operazioni simili a quelle del Framework dei [servizi di testo](../tsf/text-services-framework.md), utilizzate da applicazioni che comunicano con i servizi di testo.</span><span class="sxs-lookup"><span data-stu-id="e139b-106">The IMM performs similar operations to those of the [Text Services Framework](../tsf/text-services-framework.md), used by applications that communicate with text services.</span></span>

 

<span data-ttu-id="e139b-107">Per impostazione predefinita, IMM fornisce una finestra IME tramite cui l'utente immette le sequenze di tasti e le visualizzazioni e seleziona i candidati.</span><span class="sxs-lookup"><span data-stu-id="e139b-107">By default, the IMM provides an IME window through which the user enters keystrokes and views and selects candidates.</span></span> <span data-ttu-id="e139b-108">Le applicazioni possono utilizzare le funzioni e i messaggi di IMM per creare e gestire le proprie finestre IME, offrendo un'interfaccia personalizzata utilizzando le funzionalità di conversione dell'IME.</span><span class="sxs-lookup"><span data-stu-id="e139b-108">Applications can use the IMM functions and messages to create and manage their own IME windows, providing a custom interface while using the conversion capabilities of the IME.</span></span>

<span data-ttu-id="e139b-109">IMM è abilitato solo nei sistemi operativi Windows localizzati nell'Asia orientale (cinese, giapponese, coreano).</span><span class="sxs-lookup"><span data-stu-id="e139b-109">The IMM is only enabled on East Asian (Chinese, Japanese, Korean) localized Windows operating systems.</span></span> <span data-ttu-id="e139b-110">In questi sistemi, l'applicazione chiama [GetSystemMetrics](/windows/win32/api/winuser/nf-winuser-getsystemmetrics) con SM \_ DBCSENABLED per determinare se IMM è abilitato.</span><span class="sxs-lookup"><span data-stu-id="e139b-110">On these systems, the application calls [GetSystemMetrics](/windows/win32/api/winuser/nf-winuser-getsystemmetrics) with SM\_DBCSENABLED to determine if the IMM is enabled.</span></span>

<span data-ttu-id="e139b-111">**Windows 2000:** Il supporto di IMM completo è disponibile in tutte le versioni in lingua localizzata.</span><span class="sxs-lookup"><span data-stu-id="e139b-111">**Windows 2000:** Full-featured IMM support is provided in all localized language versions.</span></span> <span data-ttu-id="e139b-112">Tuttavia, l'IMM è abilitato solo quando viene installato un Language Pack asiatico.</span><span class="sxs-lookup"><span data-stu-id="e139b-112">However, the IMM is enabled only when an Asian language pack is installed.</span></span> <span data-ttu-id="e139b-113">Un'applicazione che supporta IME può chiamare [GetSystemMetrics](/windows/win32/api/winuser/nf-winuser-getsystemmetrics) con SM \_ IMMENABLED per determinare se IMM è abilitato.</span><span class="sxs-lookup"><span data-stu-id="e139b-113">An IME-aware application can call [GetSystemMetrics](/windows/win32/api/winuser/nf-winuser-getsystemmetrics) with SM\_IMMENABLED to determine if the IMM is enabled.</span></span>

<span data-ttu-id="e139b-114">In questo argomento sono contenute le sezioni seguenti.</span><span class="sxs-lookup"><span data-stu-id="e139b-114">This topic contains the following sections.</span></span>

-   [<span data-ttu-id="e139b-115">Elenchi candidati</span><span class="sxs-lookup"><span data-stu-id="e139b-115">Candidate Lists</span></span>](candidate-lists.md)
-   [<span data-ttu-id="e139b-116">Stringa di composizione</span><span class="sxs-lookup"><span data-stu-id="e139b-116">Composition String</span></span>](composition-string.md)
-   [<span data-ttu-id="e139b-117">IME HexToUnicode</span><span class="sxs-lookup"><span data-stu-id="e139b-117">HexToUnicode IME</span></span>](hextounicode-ime.md)
-   [<span data-ttu-id="e139b-118">Hot Keys</span><span class="sxs-lookup"><span data-stu-id="e139b-118">Hot Keys</span></span>](hot-keys.md)
-   [<span data-ttu-id="e139b-119">Messaggi IME</span><span class="sxs-lookup"><span data-stu-id="e139b-119">IME Messages</span></span>](ime-messages.md)
-   [<span data-ttu-id="e139b-120">Classe della finestra IME</span><span class="sxs-lookup"><span data-stu-id="e139b-120">IME Window Class</span></span>](ime-window-class.md)
-   [<span data-ttu-id="e139b-121">Contesto di input</span><span class="sxs-lookup"><span data-stu-id="e139b-121">Input Context</span></span>](input-context.md)
-   [<span data-ttu-id="e139b-122">Finestre stato, composizione e candidati</span><span class="sxs-lookup"><span data-stu-id="e139b-122">Status, Composition, and Candidates Windows</span></span>](status--composition--and-candidates-windows.md)

 

 
