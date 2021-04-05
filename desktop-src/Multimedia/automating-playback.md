---
title: Automazione della riproduzione
description: Automazione della riproduzione
ms.assetid: 3aa05a54-58d7-4d14-93ee-459aa860b20e
keywords:
- MCIWndCreate (macro)
- MCIWndPlay (macro)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6097d38b3d468b6de68ee7e11f98f530aff00d2b
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103714074"
---
# <a name="automating-playback"></a><span data-ttu-id="fc99e-105">Automazione della riproduzione</span><span class="sxs-lookup"><span data-stu-id="fc99e-105">Automating Playback</span></span>

<span data-ttu-id="fc99e-106">È possibile automatizzare la riproduzione nell'applicazione usando [**MCIWndCreate**](/windows/desktop/api/Vfw/nf-vfw-mciwndcreatea) e la macro [**MCIWndPlay**](/windows/desktop/api/Vfw/nf-vfw-mciwndplay) , insieme alla macro [**MCIWndDestroy**](/windows/desktop/api/Vfw/nf-vfw-mciwnddestroy) o [**MCIWndClose**](/windows/desktop/api/Vfw/nf-vfw-mciwndclose) .</span><span class="sxs-lookup"><span data-stu-id="fc99e-106">You can automate playback in your application by using [**MCIWndCreate**](/windows/desktop/api/Vfw/nf-vfw-mciwndcreatea) and the [**MCIWndPlay**](/windows/desktop/api/Vfw/nf-vfw-mciwndplay) macro, along with either the [**MCIWndDestroy**](/windows/desktop/api/Vfw/nf-vfw-mciwnddestroy) or the [**MCIWndClose**](/windows/desktop/api/Vfw/nf-vfw-mciwndclose) macro.</span></span> <span data-ttu-id="fc99e-107">Per automatizzare la riproduzione, specificare gli \_ stili MCIWNDF NOPLAYBAR e MCIWNDF \_ NOTIFYMODE nel parametro \**MCIWndCreate \* \* \* dwStyle* .</span><span class="sxs-lookup"><span data-stu-id="fc99e-107">To automate playback, specify the MCIWNDF\_NOPLAYBAR and MCIWNDF\_NOTIFYMODE styles in the \**MCIWndCreate\*\*\*dwStyle* parameter.</span></span> <span data-ttu-id="fc99e-108">Specificare lo \_ stile di NOPLAYBAR MCIWNDF per nascondere la barra degli strumenti e lo \_ stile di NOTIFYMODE MCIWNDF per emettere un messaggio di notifica appropriato quando il dispositivo smette di riprodursi.</span><span class="sxs-lookup"><span data-stu-id="fc99e-108">Specify the MCIWNDF\_NOPLAYBAR style to hide the toolbar, and the MCIWNDF\_NOTIFYMODE style to issue an appropriate notification message when the device stops playing.</span></span>

<span data-ttu-id="fc99e-109">È possibile riprodurre il dispositivo o il file specificato in **MCIWndCreate** usando **MCIWndPlay**.</span><span class="sxs-lookup"><span data-stu-id="fc99e-109">You can play the device or file specified in **MCIWndCreate** by using **MCIWndPlay**.</span></span> <span data-ttu-id="fc99e-110">La macro MCIWndPlay inizia a riprodurre il contenuto dalla posizione di riproduzione corrente e continua fino alla fine.</span><span class="sxs-lookup"><span data-stu-id="fc99e-110">The MCIWndPlay macro starts playing the content from its current playback position and continues to its end.</span></span>

<span data-ttu-id="fc99e-111">È possibile eliminare o chiudere una finestra MCIWnd usando la macro [**MCIWndDestroy**](/windows/desktop/api/Vfw/nf-vfw-mciwnddestroy) o [**MCIWndClose**](/windows/desktop/api/Vfw/nf-vfw-mciwndclose) .</span><span class="sxs-lookup"><span data-stu-id="fc99e-111">You can destroy or close an MCIWnd window by using the [**MCIWndDestroy**](/windows/desktop/api/Vfw/nf-vfw-mciwnddestroy) or [**MCIWndClose**](/windows/desktop/api/Vfw/nf-vfw-mciwndclose) macro.</span></span> <span data-ttu-id="fc99e-112">La macro **MCIWndDestroy** chiude il dispositivo o il file ed elimina la finestra MCIWnd invalidando il relativo handle.</span><span class="sxs-lookup"><span data-stu-id="fc99e-112">The **MCIWndDestroy** macro closes the device or file and destroys the MCIWnd window by invalidating its handle.</span></span> <span data-ttu-id="fc99e-113">Se l'applicazione può riutilizzare la finestra MCIWnd, utilizzare **MCIWndClose** per chiudere il dispositivo senza eliminare definitivamente la finestra.</span><span class="sxs-lookup"><span data-stu-id="fc99e-113">If your application can reuse the MCIWnd window, use **MCIWndClose** to close the device without destroying the window.</span></span>

<span data-ttu-id="fc99e-114">L'applicazione può rilevare quando il dispositivo smette di essere riprodotto e chiude automaticamente la finestra.</span><span class="sxs-lookup"><span data-stu-id="fc99e-114">Your application can detect when the device stops playing and automatically close the window.</span></span> <span data-ttu-id="fc99e-115">A tale scopo, specificare lo \_ stile NOTIFYMODE MCIWNDF per il parametro *DwStyle* di [**MCIWndCreate**](/windows/desktop/api/Vfw/nf-vfw-mciwndcreatea).</span><span class="sxs-lookup"><span data-stu-id="fc99e-115">To do this, specify the MCIWNDF\_NOTIFYMODE style for the *dwStyle* parameter of [**MCIWndCreate**](/windows/desktop/api/Vfw/nf-vfw-mciwndcreatea).</span></span> <span data-ttu-id="fc99e-116">In questo modo, il dispositivo invia un messaggio [**MCIWNDM \_ NOTIFYMODE**](mciwndm-notifymode.md) ogni volta che modifica le modalità.</span><span class="sxs-lookup"><span data-stu-id="fc99e-116">This causes the device to send a [**MCIWNDM\_NOTIFYMODE**](mciwndm-notifymode.md) message whenever it changes modes.</span></span> <span data-ttu-id="fc99e-117">L'applicazione può intercettare questo messaggio per determinare se la riproduzione del dispositivo è stata interrotta.</span><span class="sxs-lookup"><span data-stu-id="fc99e-117">Your application can trap this message to determine whether the device has stopped playing.</span></span> <span data-ttu-id="fc99e-118">Quando il dispositivo smette di rigiocare, l'applicazione chiude la finestra.</span><span class="sxs-lookup"><span data-stu-id="fc99e-118">When the device stops playing, the application closes the window.</span></span>

 

 




