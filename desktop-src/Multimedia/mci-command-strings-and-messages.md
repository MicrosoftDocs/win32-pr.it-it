---
title: Messaggi e stringhe di comando MCI
description: Messaggi e stringhe di comando MCI
ms.assetid: eb60c96b-e89e-4673-a8e0-98fabe4af7ca
keywords:
- Stringhe di comando MCI, informazioni
- Messaggi di comando MCI, informazioni
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 107a317442280b8fb4c7afe7832205b1c7128513
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2020
ms.locfileid: "103872529"
---
# <a name="mci-command-strings-and-messages"></a><span data-ttu-id="f394e-105">Messaggi e stringhe di comando MCI</span><span class="sxs-lookup"><span data-stu-id="f394e-105">MCI Command Strings and Messages</span></span>

<span data-ttu-id="f394e-106">MCI supporta le [stringhe di comando](command-strings.md) e [i messaggi di comando](command-messages.md).</span><span class="sxs-lookup"><span data-stu-id="f394e-106">MCI supports [Command Strings](command-strings.md) and [Command Messages](command-messages.md).</span></span> <span data-ttu-id="f394e-107">Nell'applicazione MCI è possibile usare stringhe o messaggi o entrambi.</span><span class="sxs-lookup"><span data-stu-id="f394e-107">You can use either strings or messages, or both, in your MCI application.</span></span>

-   <span data-ttu-id="f394e-108">L' *interfaccia del messaggio di comando* è costituita da costanti e strutture.</span><span class="sxs-lookup"><span data-stu-id="f394e-108">The *command-message interface* consists of constants and structures.</span></span> <span data-ttu-id="f394e-109">Usare la funzione [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) per inviare messaggi a un dispositivo MCI.</span><span class="sxs-lookup"><span data-stu-id="f394e-109">Use the [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) function to send messages to an MCI device.</span></span>
-   <span data-ttu-id="f394e-110">L' *interfaccia della stringa di comando* fornisce una versione testuale dei messaggi di comando.</span><span class="sxs-lookup"><span data-stu-id="f394e-110">The *command-string interface* provides a textual version of the command messages.</span></span> <span data-ttu-id="f394e-111">Usare la funzione [**mciSendString**](/previous-versions//dd757161(v=vs.85)) per inviare stringhe a un dispositivo MCI.</span><span class="sxs-lookup"><span data-stu-id="f394e-111">Use the [**mciSendString**](/previous-versions//dd757161(v=vs.85)) function to send strings to an MCI device.</span></span> <span data-ttu-id="f394e-112">Le stringhe di comando duplicano la funzionalità dei messaggi di comando.</span><span class="sxs-lookup"><span data-stu-id="f394e-112">Command strings duplicate the functionality of the command messages.</span></span> <span data-ttu-id="f394e-113">Il sistema operativo converte le stringhe di comando in messaggi di comando prima di inviarli al driver MCI per l'elaborazione.</span><span class="sxs-lookup"><span data-stu-id="f394e-113">The operating system converts the command strings to command messages before sending them to the MCI driver for processing.</span></span>

<span data-ttu-id="f394e-114">I messaggi di comando che recuperano informazioni consentono di eseguire questa operazione sotto forma di strutture, che risultano facili da interpretare in un'applicazione C.</span><span class="sxs-lookup"><span data-stu-id="f394e-114">The command messages that retrieve information do so in the form of structures, which are easy to interpret in a C application.</span></span> <span data-ttu-id="f394e-115">Queste strutture possono contenere informazioni su molti aspetti diversi di un dispositivo.</span><span class="sxs-lookup"><span data-stu-id="f394e-115">These structures can contain information on many different aspects of a device.</span></span> <span data-ttu-id="f394e-116">Le stringhe di comando che recuperano le informazioni vengono eseguite sotto forma di stringhe e possono recuperare una sola stringa alla volta.</span><span class="sxs-lookup"><span data-stu-id="f394e-116">The command strings that retrieve information do so in the form of strings, and can only retrieve one string at a time.</span></span> <span data-ttu-id="f394e-117">L'applicazione deve analizzare o testare ogni stringa per interpretarla.</span><span class="sxs-lookup"><span data-stu-id="f394e-117">Your application must parse or test each string to interpret it.</span></span> <span data-ttu-id="f394e-118">È possibile che i messaggi di comando siano più facili da utilizzare rispetto alle stringhe di comando in alcuni casi, ma le stringhe di comando sono facili da ricordare e implementare.</span><span class="sxs-lookup"><span data-stu-id="f394e-118">You might find that the command messages are easier to use than the command strings in some cases, but the command strings are easy to remember and implement.</span></span> <span data-ttu-id="f394e-119">Alcune applicazioni MCI usano stringhe di comando quando il valore restituito non verrà usato (ad eccezione di per verificare l'esito positivo) e i messaggi di comando durante il recupero delle informazioni dal dispositivo.</span><span class="sxs-lookup"><span data-stu-id="f394e-119">Some MCI applications use command strings when the return value will not be used (other than to verify success) and command messages when retrieving information from the device.</span></span>

<span data-ttu-id="f394e-120">Quando vengono discussi i comandi, in questa panoramica viene usato il formato stringa del comando seguito dal form del messaggio tra parentesi.</span><span class="sxs-lookup"><span data-stu-id="f394e-120">When commands are discussed, this overview uses the string form of the command followed by the message form in parentheses.</span></span>

 

 