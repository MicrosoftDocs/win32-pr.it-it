---
description: Conversione automatica da MTS
ms.assetid: 0848639a-26ce-47ad-8384-8969a7c3bcde
title: Conversione automatica da MTS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d424a443995c9fff9073878a43543d4c029a2445
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104127166"
---
# <a name="automatic-conversion-from-mts"></a><span data-ttu-id="ac343-103">Conversione automatica da MTS</span><span class="sxs-lookup"><span data-stu-id="ac343-103">Automatic Conversion from MTS</span></span>

<span data-ttu-id="ac343-104">La conversione automatica viene eseguita in due passaggi, come indicato di seguito:</span><span class="sxs-lookup"><span data-stu-id="ac343-104">Automatic conversion occurs in two steps, as follows:</span></span>

1.  <span data-ttu-id="ac343-105">Durante l'installazione di Windows.</span><span class="sxs-lookup"><span data-stu-id="ac343-105">During Windows setup.</span></span> <span data-ttu-id="ac343-106">La conversione viene gestita dal processo di installazione di Windows tramite l'utilità MTSTOCOM.</span><span class="sxs-lookup"><span data-stu-id="ac343-106">The conversion is handled by the Windows setup process through the MTSTOCOM utility.</span></span>
    > [!Note]  
    > <span data-ttu-id="ac343-107">Se il passaggio 1 ha esito negativo, è possibile che alcuni o tutti i pacchetti MTS siano stati effettivamente convertiti, ma che alcune proprietà siano mancanti.</span><span class="sxs-lookup"><span data-stu-id="ac343-107">If step 1 fails, some or all of the MTS packages may actually have been converted but may be missing certain properties.</span></span> <span data-ttu-id="ac343-108">In questo caso, utilizzare lo strumento di amministrazione Servizi componenti per verificare tutti gli attributi.</span><span class="sxs-lookup"><span data-stu-id="ac343-108">In this case, use the Component Services administrative tool to verify all attributes.</span></span> <span data-ttu-id="ac343-109">Gli attributi MTS saranno ancora presenti nel computer (nel registro di sistema nel computer locale HKEY \_ \_ \\ Microsoft \\ Transaction Server) ma saranno accessibili solo tramite l'utilità regedit.exe.</span><span class="sxs-lookup"><span data-stu-id="ac343-109">The MTS attributes will still be present on the computer (in the system registry at HKEY\_LOCAL\_MACHINE\\Microsoft\\Transaction Server) but will be accessible only through the regedit.exe utility.</span></span>

     

2.  <span data-ttu-id="ac343-110">Dopo l'ultimo riavvio prima della visualizzazione della finestra di dialogo di accesso di Windows.</span><span class="sxs-lookup"><span data-stu-id="ac343-110">After the last reboot before the Windows logon dialog box is displayed.</span></span> <span data-ttu-id="ac343-111">Il passaggio 2 gestisce le azioni di conversione che richiedono l'accesso alla rete (principalmente la creazione di membri del ruolo).</span><span class="sxs-lookup"><span data-stu-id="ac343-111">Step 2 handles those conversion actions that require network access (primarily role member creation).</span></span>
    > [!Note]  
    > <span data-ttu-id="ac343-112">Se il passaggio 2 ha esito negativo (a causa di errori di rete o del controller di dominio temporanei), è possibile eseguire di nuovo l'utilità di conversione MTSTOCOM per un numero qualsiasi di volte.</span><span class="sxs-lookup"><span data-stu-id="ac343-112">If step 2 fails (due to temporary network or domain controller failures), it is possible to rerun the MTSTOCOM conversion utility any number of times.</span></span> <span data-ttu-id="ac343-113">A tale scopo, al prompt dei comandi o dopo aver selezionato **Esegui** dal menu **Start** , digitare quanto segue: **% windir% \\ system32 \\mtstocom.exe**.</span><span class="sxs-lookup"><span data-stu-id="ac343-113">To do this, at the command prompt or after selecting **Run** from the **Start** menu, type the following: **%windir%\\system32\\mtstocom.exe**.</span></span>

     

## <a name="mtstocom-log-file"></a><span data-ttu-id="ac343-114">File di log MTSTOCOM</span><span class="sxs-lookup"><span data-stu-id="ac343-114">MTSTOCOM Log File</span></span>

<span data-ttu-id="ac343-115">L'utilità MTSTOCOM genera un file di log (Mtstocom. log) nella directory Windows.</span><span class="sxs-lookup"><span data-stu-id="ac343-115">The MTSTOCOM utility generates a log file (Mtstocom.log) in the Windows directory.</span></span> <span data-ttu-id="ac343-116">Questo file di log mantiene un record della conversione da pacchetti MTS a applicazioni COM+.</span><span class="sxs-lookup"><span data-stu-id="ac343-116">This log file keeps a record of the conversion from MTS packages to COM+ applications.</span></span> <span data-ttu-id="ac343-117">Se si sono verificati errori durante il processo di conversione, è sempre consigliabile controllare il file di log per ulteriori informazioni.</span><span class="sxs-lookup"><span data-stu-id="ac343-117">If there were any errors during the conversion process, it is always a good idea to check the log file for further information.</span></span> <span data-ttu-id="ac343-118">Il file di log rileva i problemi comuni, ad esempio l'utente o la password non valida.</span><span class="sxs-lookup"><span data-stu-id="ac343-118">The log file catches common problems, such as invalid user or password.</span></span>

## <a name="related-topics"></a><span data-ttu-id="ac343-119">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="ac343-119">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ac343-120">Risultati e problemi di conversione COM+</span><span class="sxs-lookup"><span data-stu-id="ac343-120">COM+ Conversion Results and Issues</span></span>](com--conversion-results-and-issues.md)
</dt> <dt>

[<span data-ttu-id="ac343-121">Conversione manuale da MTS</span><span class="sxs-lookup"><span data-stu-id="ac343-121">Manual Conversion from MTS</span></span>](manual-conversion-from-mts.md)
</dt> <dt>

[<span data-ttu-id="ac343-122">Libreria di amministrazione MTS</span><span class="sxs-lookup"><span data-stu-id="ac343-122">MTS Administration Library</span></span>](mts-administration-library.md)
</dt> </dl>

 

 



