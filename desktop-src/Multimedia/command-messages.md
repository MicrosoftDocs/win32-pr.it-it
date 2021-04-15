---
title: Messaggi di comando
description: Messaggi di comando
ms.assetid: 29b40f35-d390-49c3-99bd-c648c7c50504
keywords:
- Messaggi di comando MCI, informazioni
- Messaggi di comando MCI, sintassi
- mciSendCommand (funzione)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2cc92b960e646ee1e452c7a356d0291c080d0162
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2020
ms.locfileid: "104516714"
---
# <a name="command-messages"></a><span data-ttu-id="acaf8-106">Messaggi di comando</span><span class="sxs-lookup"><span data-stu-id="acaf8-106">Command Messages</span></span>

<span data-ttu-id="acaf8-107">L'interfaccia del messaggio di comando è progettata per essere utilizzata dalle applicazioni che richiedono un'interfaccia del linguaggio C per il controllo dei dispositivi multimediali.</span><span class="sxs-lookup"><span data-stu-id="acaf8-107">The command-message interface is designed to be used by applications requiring a C-language interface to control multimedia devices.</span></span> <span data-ttu-id="acaf8-108">Usa un paradigma di passaggio dei messaggi per comunicare con i dispositivi MCI.</span><span class="sxs-lookup"><span data-stu-id="acaf8-108">It uses a message-passing paradigm to communicate with MCI devices.</span></span> <span data-ttu-id="acaf8-109">È possibile inviare un comando tramite la funzione [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="acaf8-109">You can send a command by using the [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) function.</span></span>

<span data-ttu-id="acaf8-110">La funzione **mciSendCommand** restituisce zero in caso di esito positivo.</span><span class="sxs-lookup"><span data-stu-id="acaf8-110">The **mciSendCommand** function returns zero if successful.</span></span> <span data-ttu-id="acaf8-111">Se la funzione ha esito negativo, la parola di ordine inferiore del valore restituito contiene un codice di errore.</span><span class="sxs-lookup"><span data-stu-id="acaf8-111">If the function fails, the low-order word of the return value contains an error code.</span></span> <span data-ttu-id="acaf8-112">È possibile passare questo codice di errore alla funzione [**mciGetErrorString**](/previous-versions//dd757158(v=vs.85)) per ottenere una descrizione di testo dell'errore.</span><span class="sxs-lookup"><span data-stu-id="acaf8-112">You can pass this error code to the [**mciGetErrorString**](/previous-versions//dd757158(v=vs.85)) function to get a text description of the error.</span></span>

## <a name="syntax-of-command-messages"></a><span data-ttu-id="acaf8-113">Sintassi dei messaggi di comando</span><span class="sxs-lookup"><span data-stu-id="acaf8-113">Syntax of Command Messages</span></span>

<span data-ttu-id="acaf8-114">I messaggi di comando MCI sono costituiti dagli elementi seguenti:</span><span class="sxs-lookup"><span data-stu-id="acaf8-114">MCI command messages consist of the following elements:</span></span>

-   <span data-ttu-id="acaf8-115">Valore costante del messaggio</span><span class="sxs-lookup"><span data-stu-id="acaf8-115">A constant message value</span></span>
-   <span data-ttu-id="acaf8-116">Struttura che contiene i parametri per il comando.</span><span class="sxs-lookup"><span data-stu-id="acaf8-116">A structure containing parameters for the command</span></span>
-   <span data-ttu-id="acaf8-117">Set di flag che specificano le opzioni per il comando e i campi di convalida nel blocco di parametri</span><span class="sxs-lookup"><span data-stu-id="acaf8-117">A set of flags specifying options for the command and validating fields in the parameter block</span></span>

<span data-ttu-id="acaf8-118">Nell'esempio seguente viene usata la funzione [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) per inviare il comando [**MCI \_ Play**](mci-play.md) al dispositivo identificato da un identificatore di dispositivo.</span><span class="sxs-lookup"><span data-stu-id="acaf8-118">The following example uses the [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) function to send the [**MCI\_ PLAY**](mci-play.md) command to the device identified by a device identifier.</span></span>


```C++
mciSendCommand(wDeviceID,            // device identifier 
    MCI_PLAY,                        // command message 
    0,                               // flags 
    (DWORD)(LPVOID) &mciPlayParms);  // parameter block 
```



<span data-ttu-id="acaf8-119">L'identificatore del dispositivo specificato nel primo parametro viene recuperato quando il dispositivo viene aperto usando il comando [**MCI \_ Open**](mci-open.md) .</span><span class="sxs-lookup"><span data-stu-id="acaf8-119">The device identifier given in the first parameter is retrieved when the device is opened using the [**MCI\_ OPEN**](mci-open.md) command.</span></span> <span data-ttu-id="acaf8-120">L'ultimo parametro è l'indirizzo di una [**struttura \_ \_ parametri di MCI Play**](mci-play-parms.md) , che può contenere informazioni sul punto in cui iniziare e terminare la riproduzione.</span><span class="sxs-lookup"><span data-stu-id="acaf8-120">The last parameter is the address of an [**MCI\_ PLAY\_ PARMS**](mci-play-parms.md) structure, which might contain information about where to begin and end playback.</span></span> <span data-ttu-id="acaf8-121">Molti messaggi di comando MCI usano una struttura per contenere parametri di questo tipo.</span><span class="sxs-lookup"><span data-stu-id="acaf8-121">Many MCI command messages use a structure to contain parameters of this kind.</span></span> <span data-ttu-id="acaf8-122">Il primo membro di ognuna di queste strutture identifica la finestra che riceve un [**messaggio \_ MCINOTIFY mm**](mm-mcinotify.md) al termine dell'operazione.</span><span class="sxs-lookup"><span data-stu-id="acaf8-122">The first member of each of these structures identifies the window that receives an [**MM\_ MCINOTIFY**](mm-mcinotify.md) message when the operation finishes.</span></span>

 

 