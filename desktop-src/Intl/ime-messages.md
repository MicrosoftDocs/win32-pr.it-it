---
description: Il sistema operativo invia messaggi della finestra IME alla routine della finestra di un'applicazione quando si verificano determinati eventi che interessano le finestre IME.
ms.assetid: 7eac1ab7-d04b-4e1b-9e2c-fa9a778756cd
title: Messaggi IME
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f0f30baa01081e0aca1423f3384926938e6fdc07
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104049558"
---
# <a name="ime-messages"></a><span data-ttu-id="07d79-103">Messaggi IME</span><span class="sxs-lookup"><span data-stu-id="07d79-103">IME Messages</span></span>

<span data-ttu-id="07d79-104">Il sistema operativo invia messaggi della finestra IME alla routine della finestra di un'applicazione quando si verificano determinati eventi che interessano le finestre IME.</span><span class="sxs-lookup"><span data-stu-id="07d79-104">The operating system sends IME window messages to the window procedure of an application when certain events occur that affect the IME windows.</span></span> <span data-ttu-id="07d79-105">Ad esempio, il sistema operativo invia il messaggio di [**\_ \_ contesto di WM IME**](wm-ime-setcontext.md) all'applicazione quando una finestra viene attivata.</span><span class="sxs-lookup"><span data-stu-id="07d79-105">For example, the operating system sends the [**WM\_IME\_SETCONTEXT**](wm-ime-setcontext.md) message to the application when a window is activated.</span></span> <span data-ttu-id="07d79-106">Le applicazioni non compatibili con IME passano questi messaggi alla funzione [DefWindowProc](/windows/desktop/api/winuser/nf-winuser-defwindowproca) , che li invia alla finestra IME predefinita corrispondente.</span><span class="sxs-lookup"><span data-stu-id="07d79-106">IME-unaware applications pass these messages to the [DefWindowProc](/windows/desktop/api/winuser/nf-winuser-defwindowproca) function, which sends them to the corresponding default IME window.</span></span> <span data-ttu-id="07d79-107">Le applicazioni in grado di riconoscere gli IME elaborano questi messaggi o le inviano alla propria finestra IME.</span><span class="sxs-lookup"><span data-stu-id="07d79-107">IME-aware applications either process these messages or forward them to their own IME windows.</span></span>

<span data-ttu-id="07d79-108">L'applicazione può indirizzare una finestra IME per eseguire un comando, ad esempio modificare la posizione di una finestra di composizione, usando il messaggio [**di \_ \_ controllo di WM IME**](wm-ime-control.md) .</span><span class="sxs-lookup"><span data-stu-id="07d79-108">Your application can direct an IME window to carry out a command, for example, change the position of a composition window, by using the [**WM\_IME\_CONTROL**](wm-ime-control.md) message.</span></span> <span data-ttu-id="07d79-109">L'IME notifica all'applicazione le modifiche apportate alla stringa di composizione utilizzando il messaggio di [**\_ \_ composizione IME WM**](wm-ime-composition.md) e le modifiche generali apportate allo stato delle finestre IME inviando il messaggio di [**\_ \_ notifica di WM IME**](wm-ime-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="07d79-109">The IME notifies the application about changes to the composition string by using the [**WM\_IME\_COMPOSITION**](wm-ime-composition.md) message, and about general changes to the status of the IME windows by sending the [**WM\_IME\_NOTIFY**](wm-ime-notify.md) message.</span></span>

## <a name="related-topics"></a><span data-ttu-id="07d79-110">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="07d79-110">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="07d79-111">Informazioni su Gestione metodi di input</span><span class="sxs-lookup"><span data-stu-id="07d79-111">About Input Method Manager</span></span>](about-input-method-manager.md)
</dt> </dl>

 

 
