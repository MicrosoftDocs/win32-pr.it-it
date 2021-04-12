---
title: Flag di notifica
description: Flag di notifica
ms.assetid: ed5dbb0b-ce4d-4bda-8daa-c62cfda717d1
keywords:
- Flag di MCI_NOTIFY
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9093e539becb4ba2f09b48d628a57d8243bd837c
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2020
ms.locfileid: "104398984"
---
# <a name="the-notify-flag"></a><span data-ttu-id="804cf-104">Flag di notifica</span><span class="sxs-lookup"><span data-stu-id="804cf-104">The Notify Flag</span></span>

<span data-ttu-id="804cf-105">Il flag di notifica (MCI \_ Notify) indica al dispositivo di inserire un messaggio [**mm MCINOTIFY**](mm-mcinotify.md) quando il dispositivo completa un'azione.</span><span class="sxs-lookup"><span data-stu-id="804cf-105">The "notify" (MCI\_NOTIFY) flag directs the device to post an [**MM MCINOTIFY**](mm-mcinotify.md) message when the device completes an action.</span></span> <span data-ttu-id="804cf-106">L'applicazione deve disporre di una routine della finestra per elaborare il \_ messaggio MCINOTIFY mm affinché la notifica abbia effetto.</span><span class="sxs-lookup"><span data-stu-id="804cf-106">Your application must have a window procedure to process the MM\_MCINOTIFY message for notification to have any effect.</span></span> <span data-ttu-id="804cf-107">Un \_ messaggio mm MCINOTIFY indica che l'elaborazione di un comando è stata completata, ma non indica se il comando è stato completato correttamente, non è riuscito oppure è stato sostituito o interrotto.</span><span class="sxs-lookup"><span data-stu-id="804cf-107">An MM\_MCINOTIFY message indicates that the processing of a command has completed, but it does not indicate whether the command was completed successfully, failed, or was superseded or aborted.</span></span>

<span data-ttu-id="804cf-108">L'applicazione specifica l'handle per la finestra di destinazione per il messaggio quando emette un comando.</span><span class="sxs-lookup"><span data-stu-id="804cf-108">The application specifies the handle to the destination window for the message when it issues a command.</span></span> <span data-ttu-id="804cf-109">Nell'interfaccia della stringa di comando, questo handle è l'ultimo parametro della funzione [**mciSendString**](/previous-versions//dd757161(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="804cf-109">In the command-string interface, this handle is the last parameter of the [**mciSendString**](/previous-versions//dd757161(v=vs.85)) function.</span></span> <span data-ttu-id="804cf-110">Nell'interfaccia del messaggio di comando, l'handle viene specificato nella parola di ordine inferiore del membro **dwCallBack** della struttura inviata con il messaggio di comando.</span><span class="sxs-lookup"><span data-stu-id="804cf-110">In the command-message interface, the handle is specified in the low-order word of the **dwCallBack** member of the structure sent with the command message.</span></span> <span data-ttu-id="804cf-111">(Ogni struttura associata a un messaggio di comando contiene questo membro).</span><span class="sxs-lookup"><span data-stu-id="804cf-111">(Every structure associated with a command message contains this member.)</span></span>

 

 