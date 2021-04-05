---
title: Collegamenti ai comandi e varianti
description: Collegamenti ai comandi e varianti
ms.assetid: 4f854c78-435c-4a10-8938-645ad605fff3
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a82ce41aaa9cc5744a2f199a7f7761111734e848
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103712529"
---
# <a name="command-shortcuts-and-variations"></a><span data-ttu-id="18bbd-103">Collegamenti ai comandi e varianti</span><span class="sxs-lookup"><span data-stu-id="18bbd-103">Command Shortcuts and Variations</span></span>

<span data-ttu-id="18bbd-104">Quando si utilizzano i comandi MCI è possibile utilizzare diversi tasti di scelta rapida.</span><span class="sxs-lookup"><span data-stu-id="18bbd-104">You can use several shortcuts when working with MCI commands.</span></span> <span data-ttu-id="18bbd-105">Questi tasti di scelta rapida consentono di usare un singolo identificatore per fare riferimento a tutti i dispositivi aperti dall'applicazione o di aprire un dispositivo senza emettere esplicitamente un comando [**Open**](open.md) ([**MCI \_ Open**](mci-open.md)).</span><span class="sxs-lookup"><span data-stu-id="18bbd-105">These shortcuts enable you to use a single identifier to refer to all the devices your application has opened, or to open a device without explicitly issuing an [**open**](open.md) ([**MCI\_OPEN**](mci-open.md)) command.</span></span>

<span data-ttu-id="18bbd-106">È possibile specificare "All" (MCI \_ All \_ Device \_ ID) come identificatore di dispositivo per qualsiasi comando che non restituisce informazioni.</span><span class="sxs-lookup"><span data-stu-id="18bbd-106">You can specify "all" (MCI\_ALL\_DEVICE\_ID) as a device identifier for any command that does not return information.</span></span> <span data-ttu-id="18bbd-107">Quando si specifica "All", MCI invia il comando in sequenza a tutti i dispositivi aperti dall'applicazione corrente.</span><span class="sxs-lookup"><span data-stu-id="18bbd-107">When you specify "all", MCI sends the command sequentially to all devices opened by the current application.</span></span>

<span data-ttu-id="18bbd-108">Il comando [**Chiudi**](close.md) "tutti", ad esempio, chiude tutti i dispositivi aperti e il comando [**Play**](play.md) "All" avvia la riproduzione di tutti i dispositivi aperti dall'applicazione.</span><span class="sxs-lookup"><span data-stu-id="18bbd-108">For example, the [**close**](close.md) "all" command closes all open devices and the [**play**](play.md) "all" command starts playing all devices opened by the application.</span></span> <span data-ttu-id="18bbd-109">Poiché MCI invia in modo sequenziale i comandi ai dispositivi MCI, esiste un intervallo tra la ricezione del comando da parte del primo e dell'ultimo dispositivo.</span><span class="sxs-lookup"><span data-stu-id="18bbd-109">Because MCI sequentially sends the commands to the MCI devices, there is an interval between when the first and last devices receive the command.</span></span>

<span data-ttu-id="18bbd-110">L'uso di "All" è un modo pratico per trasmettere un comando a tutti i dispositivi, ma non è consigliabile fare affidamento su di esso per sincronizzare i dispositivi. l'intervallo tra i messaggi può variare.</span><span class="sxs-lookup"><span data-stu-id="18bbd-110">Using "all" is a convenient way to broadcast a command to all your devices, but you should not rely on it to synchronize devices; the timing between messages can vary.</span></span>

<span data-ttu-id="18bbd-111">Quando si emette un comando e si specifica un dispositivo che non è aperto, MCI tenta di aprire il dispositivo prima di implementare il comando.</span><span class="sxs-lookup"><span data-stu-id="18bbd-111">When you issue a command and specify a device that is not open, MCI tries to open the device before implementing the command.</span></span> <span data-ttu-id="18bbd-112">Per l'apertura automatica dei dispositivi sono valide le regole seguenti:</span><span class="sxs-lookup"><span data-stu-id="18bbd-112">The following rules apply to automatically opening devices:</span></span>

-   <span data-ttu-id="18bbd-113">La funzionalità di apertura automatica funziona solo con l'interfaccia della stringa di comando.</span><span class="sxs-lookup"><span data-stu-id="18bbd-113">The automatic open feature works only with the command-string interface.</span></span>
-   <span data-ttu-id="18bbd-114">La funzionalità di apertura automatica non riesce per i comandi specifici dei driver di dispositivo personalizzati.</span><span class="sxs-lookup"><span data-stu-id="18bbd-114">The automatic open feature fails for commands that are specific to custom device drivers.</span></span>
-   <span data-ttu-id="18bbd-115">I dispositivi aperti automaticamente non rispondono ai comandi che usano "All" come nome del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="18bbd-115">Automatically opened devices do not respond to commands that use "all" as a device name.</span></span>
-   <span data-ttu-id="18bbd-116">La funzionalità di apertura automatica non consente all'applicazione di specificare il flag "Type".</span><span class="sxs-lookup"><span data-stu-id="18bbd-116">The automatic open feature does not let your application specify the "type" flag.</span></span> <span data-ttu-id="18bbd-117">Senza il nome del dispositivo, MCI determina il nome del dispositivo dalle voci nel registro di sistema.</span><span class="sxs-lookup"><span data-stu-id="18bbd-117">Without the device name, MCI determines the device name from the entries in the registry.</span></span> <span data-ttu-id="18bbd-118">Per usare un dispositivo specifico, è possibile combinare il nome del dispositivo con il nome del file usando il punto esclamativo, come descritto nel materiale di riferimento per il comando [**Apri**](open.md) .</span><span class="sxs-lookup"><span data-stu-id="18bbd-118">To use a specific device, you can combine the device name with the filename by using the exclamation point, as described in the reference material for the [**open**](open.md) command.</span></span>

<span data-ttu-id="18bbd-119">Se un'applicazione usa la funzionalità di apertura automatica per aprire un dispositivo, l'applicazione deve controllare il valore restituito di ogni comando aperto successivo per verificare che il dispositivo sia ancora aperto.</span><span class="sxs-lookup"><span data-stu-id="18bbd-119">If an application uses the automatic open feature to open a device, the application should check the return value of every subsequent open command to verify that the device is still open.</span></span> <span data-ttu-id="18bbd-120">MCI chiude automaticamente anche tutti i dispositivi che vengono aperti automaticamente.</span><span class="sxs-lookup"><span data-stu-id="18bbd-120">MCI also automatically closes any device that it automatically opens.</span></span> <span data-ttu-id="18bbd-121">MCI in genere chiude un dispositivo nelle situazioni seguenti:</span><span class="sxs-lookup"><span data-stu-id="18bbd-121">MCI typically closes a device in the following situations:</span></span>

-   <span data-ttu-id="18bbd-122">Il comando è stato completato.</span><span class="sxs-lookup"><span data-stu-id="18bbd-122">The command is completed.</span></span>
-   <span data-ttu-id="18bbd-123">Si interrompe il comando.</span><span class="sxs-lookup"><span data-stu-id="18bbd-123">You abort the command.</span></span>
-   <span data-ttu-id="18bbd-124">Viene richiesta una notifica in un comando successivo.</span><span class="sxs-lookup"><span data-stu-id="18bbd-124">You request notification in a subsequent command.</span></span>
-   <span data-ttu-id="18bbd-125">MCI rileva un errore.</span><span class="sxs-lookup"><span data-stu-id="18bbd-125">MCI detects a failure.</span></span>

 

 




