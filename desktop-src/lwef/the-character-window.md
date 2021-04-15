---
title: Finestra dei caratteri
description: Finestra dei caratteri
ms.assetid: 92b6111f-b52d-4720-8bd9-59585d826bf5
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 67a386dc769e2b5fe7313b768d1b2debfe4a1131
ms.sourcegitcommit: a716ca2a6a22a400f02c6b31699cf4da83ee3619
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 11/04/2020
ms.locfileid: "104399971"
---
# <a name="the-character-window"></a><span data-ttu-id="a5f17-103">Finestra dei caratteri</span><span class="sxs-lookup"><span data-stu-id="a5f17-103">The Character Window</span></span>

<span data-ttu-id="a5f17-104">\[Microsoft Agent è stato deprecato a partire da Windows 7 e potrebbe non essere disponibile nelle versioni successive di Windows.\]</span><span class="sxs-lookup"><span data-stu-id="a5f17-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

<span data-ttu-id="a5f17-105">Microsoft Agent Visualizza i caratteri animati nelle rispettive finestre che vengono sempre visualizzate nella parte superiore della finestra z-order (ovvero always on top).</span><span class="sxs-lookup"><span data-stu-id="a5f17-105">Microsoft Agent displays animated characters in their own windows that always appear at the top of the window z-order (that is, always on top).</span></span> <span data-ttu-id="a5f17-106">Un utente può spostare la finestra di un carattere trascinando il carattere con il pulsante sinistro del mouse.</span><span class="sxs-lookup"><span data-stu-id="a5f17-106">A user can move a character's window by dragging the character with the left mouse button.</span></span> <span data-ttu-id="a5f17-107">L'immagine del carattere viene spostata con il puntatore.</span><span class="sxs-lookup"><span data-stu-id="a5f17-107">The character image moves with the pointer.</span></span> <span data-ttu-id="a5f17-108">Inoltre, un'applicazione può spostare un carattere utilizzando il metodo [**MoveTo**](moveto-method.md) .</span><span class="sxs-lookup"><span data-stu-id="a5f17-108">In addition, an application can move a character using the [**MoveTo**](moveto-method.md) method.</span></span>

<span data-ttu-id="a5f17-109">Quando l'utente fa clic con il pulsante destro del mouse su un carattere, viene visualizzato un menu popup che Visualizza i comandi seguenti:</span><span class="sxs-lookup"><span data-stu-id="a5f17-109">When the user right-clicks a character, a pop-up menu appears that displays the following commands:</span></span>

<span data-ttu-id="a5f17-110">Apre \| la <span class="underline"></span>finestra comandi OICE di chiusura</span><span class="sxs-lookup"><span data-stu-id="a5f17-110">Open \| Close <span class="underline">V</span>oice Commands Window</span></span>

<span data-ttu-id="a5f17-111">IDE <span class="underline">H</span></span><span class="sxs-lookup"><span data-stu-id="a5f17-111"><span class="underline">H</span>ide</span></span>

<span data-ttu-id="a5f17-112">----------------------------…</span><span class="sxs-lookup"><span data-stu-id="a5f17-112">----------------------------…</span></span>

<span data-ttu-id="a5f17-113">Comando\*</span><span class="sxs-lookup"><span data-stu-id="a5f17-113">Command\*</span></span>


<span data-ttu-id="a5f17-114">*OtherHostingApplicationCaption\*\**</span><span class="sxs-lookup"><span data-stu-id="a5f17-114">*OtherHostingApplicationCaption\*\**</span></span>

<span data-ttu-id="a5f17-115">\*I comandi elencati sono basati sul client attivo per l'input.</span><span class="sxs-lookup"><span data-stu-id="a5f17-115">\*Commands listed are based on the input-active client.</span></span> <span data-ttu-id="a5f17-116">Per ulteriori informazioni sulla definizione dei comandi visualizzati nel menu a comparsa, vedere la panoramica dell'interfaccia di programmazione Microsoft Agent.</span><span class="sxs-lookup"><span data-stu-id="a5f17-116">For more information on defining commands that appear in the pop-up menu, see The Microsoft Agent Programming Interface Overview.</span></span>

<span data-ttu-id="a5f17-117">\*\*Le voci elencate sono tutte le altre applicazioni che attualmente ospitano il carattere.</span><span class="sxs-lookup"><span data-stu-id="a5f17-117">\*\*Entries listed are all other applications currently hosting the character.</span></span> <span data-ttu-id="a5f17-118">Per ulteriori informazioni sulla definizione di questa voce, vedere Cenni preliminari sull'interfaccia di programmazione Microsoft Agent.</span><span class="sxs-lookup"><span data-stu-id="a5f17-118">For more information on defining this entry, see The Microsoft Agent Programming Interface Overview.</span></span>

<span data-ttu-id="a5f17-119">Il \| comando Apri Chiudi voce comandi finestra Controlla la visualizzazione della finestra comandi del carattere attivo corrente.</span><span class="sxs-lookup"><span data-stu-id="a5f17-119">The Open \| Close Voice Commands Window command controls the display of the Commands Window of the current active character.</span></span> <span data-ttu-id="a5f17-120">Se i servizi di riconoscimento vocale sono disabilitati, questo comando è disabilitato.</span><span class="sxs-lookup"><span data-stu-id="a5f17-120">If speech recognition services are disabled, this command is disabled.</span></span> <span data-ttu-id="a5f17-121">Se servizi di riconoscimento vocale non è installato, questo comando non viene visualizzato.</span><span class="sxs-lookup"><span data-stu-id="a5f17-121">If speech recognition services are not installed, this command does not appear.</span></span>

<span data-ttu-id="a5f17-122">Il comando Hide nasconde il carattere.</span><span class="sxs-lookup"><span data-stu-id="a5f17-122">The Hide command hides the character.</span></span> <span data-ttu-id="a5f17-123">L'animazione assegnata allo stato di **Nascondi** del carattere viene riprodotta e nasconde il carattere.</span><span class="sxs-lookup"><span data-stu-id="a5f17-123">The animation assigned to the character's **Hiding** state plays and hides the character.</span></span> <span data-ttu-id="a5f17-124">La lettera "H" in Hide è la chiave di accesso del comando (mnemonico).</span><span class="sxs-lookup"><span data-stu-id="a5f17-124">The letter "H" in hide is the command's access key (mnemonic).</span></span>

<span data-ttu-id="a5f17-125">I comandi per le applicazioni che attualmente ospitano il carattere seguono il comando Hide, preceduto da un separatore.</span><span class="sxs-lookup"><span data-stu-id="a5f17-125">The commands for the application(s) currently hosting the character follow the Hide command, preceded by a separator.</span></span> <span data-ttu-id="a5f17-126">Vengono quindi visualizzati i nomi di altre applicazioni che utilizzano il carattere, preceduti anche da un separatore.</span><span class="sxs-lookup"><span data-stu-id="a5f17-126">Then the names of other applications using the character appear, also preceded by a separator.</span></span>

 

 




