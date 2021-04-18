---
title: Riproduzione e posizionamento
description: Riproduzione e posizionamento
ms.assetid: fbf9294e-c644-45c7-ab60-dd903409a44f
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1efbd6256fbd0d258f5d5c9d3da9b01c72a203dd
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "106298095"
---
# <a name="playback-and-positioning"></a><span data-ttu-id="ceba0-103">Riproduzione e posizionamento</span><span class="sxs-lookup"><span data-stu-id="ceba0-103">Playback and Positioning</span></span>

<span data-ttu-id="ceba0-104">Una serie di comandi MCI, ad esempio [**Play**](play.md) ([**MCI \_ Play**](mci-play.md)), [**Stop**](stop.md) ([**MCI \_ Stop**](mci-stop.md)), [**pause**](pause.md) ([**MCI \_ pause**](mci-pause.md)), [**Resume**](resume.md) ([**MCI \_ Resume**](mci-resume.md)) e [**Seek**](seek.md) ([**MCI \_ Seek**](mci-seek.md)), influiscono sulla riproduzione o sul posizionamento di un file multimediale.</span><span class="sxs-lookup"><span data-stu-id="ceba0-104">A number of MCI commands, such as [**play**](play.md) ([**MCI\_PLAY**](mci-play.md)), [**stop**](stop.md) ([**MCI\_STOP**](mci-stop.md)), [**pause**](pause.md) ([**MCI\_PAUSE**](mci-pause.md)), [**resume**](resume.md) ([**MCI\_RESUME**](mci-resume.md)), and [**seek**](seek.md) ([**MCI\_SEEK**](mci-seek.md)), affect the playback or positioning of a multimedia file.</span></span> <span data-ttu-id="ceba0-105">Se un dispositivo MCI riceve un comando di riproduzione mentre è in corso un altro comando di riproduzione, accetta il comando e arresta o sostituisce il comando precedente.</span><span class="sxs-lookup"><span data-stu-id="ceba0-105">If an MCI device receives a playback command while another playback command is in progress, it accepts the command and either stops or supersedes the previous command.</span></span>

<span data-ttu-id="ceba0-106">Molti comandi MCI, ad esempio [**set**](set.md) ([**MCI \_ set**](mci-set.md)), non influiscono sulla riproduzione.</span><span class="sxs-lookup"><span data-stu-id="ceba0-106">Many MCI commands, such as [**set**](set.md) ([**MCI\_SET**](mci-set.md)), do not affect playback.</span></span> <span data-ttu-id="ceba0-107">Una notifica da uno di questi comandi non interferisce con i comandi di riproduzione o posizione in sospeso, purché le notifiche non vengano eseguite dalla stessa istanza del driver.</span><span class="sxs-lookup"><span data-stu-id="ceba0-107">A notification from one of these commands does not interfere with pending playback or position commands as long as the notifications are not performed from the same instance of the driver.</span></span> <span data-ttu-id="ceba0-108">È ad esempio possibile emettere un comando **set** o [**status**](status.md) ([**\_ stato MCI**](mci-status.md)) mentre un dispositivo esegue un comando **Seek** senza arrestare o sostituire il comando **Seek** .</span><span class="sxs-lookup"><span data-stu-id="ceba0-108">For example, you can issue a **set** or [**status**](status.md) ([**MCI\_STATUS**](mci-status.md)) command while a device is performing a **seek** command without stopping or superseding the **seek** command.</span></span>

<span data-ttu-id="ceba0-109">Tuttavia, può essere presente una sola notifica in sospeso.</span><span class="sxs-lookup"><span data-stu-id="ceba0-109">However, there can be only one pending notification.</span></span> <span data-ttu-id="ceba0-110">Se, ad esempio, un'applicazione richiede una notifica per la **riproduzione** e segue la richiesta con **stato** "inizio posizione notifica", la notifica di **riproduzione** restituirà "sostituito" e la notifica del comando di stato restituirà al termine.</span><span class="sxs-lookup"><span data-stu-id="ceba0-110">For example, if an application requests a notification for **play** and follows that request with **status** "start position notify," the **play** notification will return "superseded" and the notification for the status command will return when it is finished.</span></span> <span data-ttu-id="ceba0-111">In questo caso, tuttavia, il comando **Play** avrà esito positivo anche se l'applicazione non ha ricevuto la notifica.</span><span class="sxs-lookup"><span data-stu-id="ceba0-111">In this case, however, the **play** command will still succeed, even though the application did not receive the notification.</span></span>

 

 




