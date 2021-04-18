---
title: Backup e ripristino di Windows 7 deprecato
description: Backup e ripristino di Windows 7 deprecato
ms.assetid: 89FB9C1B-FEE8-4508-9501-EA139F3706F7
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dcc20fa7ada55ada1f3c2f70c54955cec3d51666
ms.sourcegitcommit: ea4baf9953a78d2d6bd530b680601e39f3884541
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/01/2020
ms.locfileid: "106300564"
---
# <a name="windows-7-backup-and-restore-deprecated"></a><span data-ttu-id="3666a-103">Backup e ripristino di Windows 7 deprecato</span><span class="sxs-lookup"><span data-stu-id="3666a-103">Windows 7 Backup and Restore deprecated</span></span>

## <a name="platform"></a><span data-ttu-id="3666a-104">Piattaforma</span><span class="sxs-lookup"><span data-stu-id="3666a-104">Platform</span></span>

<span data-ttu-id="3666a-105">**Client** -Windows 8</span><span class="sxs-lookup"><span data-stu-id="3666a-105">**Clients** – Windows 8</span></span> 


## <a name="description"></a><span data-ttu-id="3666a-106">Descrizione</span><span class="sxs-lookup"><span data-stu-id="3666a-106">Description</span></span>

<span data-ttu-id="3666a-107">Sebbene non esistano modifiche comportamentali al backup e al ripristino, questa funzione è deprecata e non verrà aggiornata.</span><span class="sxs-lookup"><span data-stu-id="3666a-107">While there is no behavioral change to Backup and Restore, this function is being deprecated and will not be updated.</span></span> <span data-ttu-id="3666a-108">È stato usato raramente e la relativa funzionalità è stata sostituita dalla nuova funzionalità di cronologia file.</span><span class="sxs-lookup"><span data-stu-id="3666a-108">It was rarely used and its functionality has been replaced by the new File History feature.</span></span> <span data-ttu-id="3666a-109">Verrà fornito in Windows 8 e gli appassionati che hanno eseguito l'aggiornamento da Windows 7 a Windows 8 o dipendono da backup e ripristino oppure il backup delle immagini del disco sarà ancora in grado di usarlo.</span><span class="sxs-lookup"><span data-stu-id="3666a-109">It will ship in Windows 8 and enthusiasts who upgraded from Windows 7 to Windows 8 or depend on Backup and Restore or disk image backup will be still able to use it.</span></span> <span data-ttu-id="3666a-110">Tuttavia, tutti i punti di accesso per il backup e il ripristino, ad eccezione del pannello di controllo, sono stati rimossi.</span><span class="sxs-lookup"><span data-stu-id="3666a-110">However, all access points to Backup and Restore, with the exception of the Control Panel, have been removed.</span></span> <span data-ttu-id="3666a-111">L'applet del pannello di controllo utilizzata da backup e ripristino è stata rinominata ripristino file di Windows 7.</span><span class="sxs-lookup"><span data-stu-id="3666a-111">The Control Panel applet used by Backup and Restore was renamed to Windows 7 File Recovery.</span></span>

<span data-ttu-id="3666a-112">Non sarà più necessario che gli OEM che impostavano la chiave del registro di sistema per disabilitare la notifica di backup nelle relative immagini.</span><span class="sxs-lookup"><span data-stu-id="3666a-112">OEMs that were setting the registry key to disable backup notification in their images will no longer need to do that.</span></span>

<span data-ttu-id="3666a-113">Non è consigliabile usare entrambe le funzionalità nello stesso momento.</span><span class="sxs-lookup"><span data-stu-id="3666a-113">We do not recommend using both features at the same time.</span></span> <span data-ttu-id="3666a-114">Cronologia file controlla se la pianificazione del backup esiste ed è attiva e se ne trova una, non consente agli utenti di attivarla.</span><span class="sxs-lookup"><span data-stu-id="3666a-114">File History checks if Backup schedule exists and is active and if it finds one, it will not let users to turn it on.</span></span> <span data-ttu-id="3666a-115">In questo caso, gli utenti che desiderano utilizzare la cronologia file dovranno eliminare la pianificazione di backup di Windows.</span><span class="sxs-lookup"><span data-stu-id="3666a-115">In this case, users who want to use File History will have to delete the Windows Backup schedule.</span></span>

## <a name="manifestation"></a><span data-ttu-id="3666a-116">Manifestazione</span><span class="sxs-lookup"><span data-stu-id="3666a-116">Manifestation</span></span>

<span data-ttu-id="3666a-117">I flussi di lavoro possono essere interrotti e la documentazione che fa riferimento al metodo precedente per accedere alla funzionalità di backup e ripristino di Windows deve essere aggiornata per riflettere queste modifiche.</span><span class="sxs-lookup"><span data-stu-id="3666a-117">Workflows may be interrupted and documentation that refers to the previous method for accessing the Windows Backup and Restore feature will need to be updated to reflect these changes.</span></span>

## <a name="mitigation"></a><span data-ttu-id="3666a-118">Strategia di riduzione del rischio</span><span class="sxs-lookup"><span data-stu-id="3666a-118">Mitigation</span></span>

<span data-ttu-id="3666a-119">Le app che potrebbero attivare il backup e il ripristino devono essere riscritte per verificare se la cronologia file è attiva e consentire agli utenti di scegliere il metodo preferito.</span><span class="sxs-lookup"><span data-stu-id="3666a-119">Apps that might trigger Backup and Restore should be rewritten to check if File History is on and let users choose their preferred method.</span></span>

 

 




