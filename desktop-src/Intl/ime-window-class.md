---
description: La classe della finestra IME è una classe globale di sistema predefinita che definisce l'aspetto e il comportamento delle finestre IME standard.
ms.assetid: 0fa01d84-1304-4235-a148-ea5e8dd5d0b3
title: Classe della finestra IME
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: faae7fd0135ec894186b4e10df9bc02da66bb933
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103882145"
---
# <a name="ime-window-class"></a><span data-ttu-id="2e207-103">Classe della finestra IME</span><span class="sxs-lookup"><span data-stu-id="2e207-103">IME Window Class</span></span>

<span data-ttu-id="2e207-104">La classe della finestra IME è una classe globale di sistema predefinita che definisce l'aspetto e il comportamento delle finestre IME standard.</span><span class="sxs-lookup"><span data-stu-id="2e207-104">The IME window class is a predefined system global class that defines the appearance and behavior of the standard IME windows.</span></span> <span data-ttu-id="2e207-105">La classe è simile alle classi di controlli comuni in quanto l'applicazione crea una finestra di questa classe tramite la funzione [**CreateWindowEx**](/windows/win32/api/winuser/nf-winuser-createwindowexa) .</span><span class="sxs-lookup"><span data-stu-id="2e207-105">The class is similar to common control classes in that the application creates a window of this class by using the [**CreateWindowEx**](/windows/win32/api/winuser/nf-winuser-createwindowexa) function.</span></span> <span data-ttu-id="2e207-106">Analogamente ai controlli statici, una finestra IME non risponde all'input dell'utente.</span><span class="sxs-lookup"><span data-stu-id="2e207-106">Like static controls, an IME window does not respond to user input by itself.</span></span> <span data-ttu-id="2e207-107">Al contrario, notifica all'IME le azioni di input dell'utente ed elabora i messaggi di controllo inviati dall'IME o dalle applicazioni per eseguire una risposta all'azione dell'utente.</span><span class="sxs-lookup"><span data-stu-id="2e207-107">Instead, it notifies the IME of user input actions and processes control messages sent to it by the IME or applications to carry out a response to the user action.</span></span>

<span data-ttu-id="2e207-108">Le applicazioni compatibili con IME talvolta creano finestre IME personalizzate utilizzando la classe della finestra IME.</span><span class="sxs-lookup"><span data-stu-id="2e207-108">IME-aware applications sometimes create customized IME windows using the IME window class.</span></span> <span data-ttu-id="2e207-109">L'utilizzo della personalizzazione della finestra consente all'applicazione di sfruttare i vantaggi dell'elaborazione predefinita della finestra IME con il controllo del posizionamento della finestra.</span><span class="sxs-lookup"><span data-stu-id="2e207-109">Use of window customization allows the application to take advantage of the default processing of the IME window while having control of window positioning.</span></span>

## <a name="related-topics"></a><span data-ttu-id="2e207-110">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="2e207-110">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="2e207-111">Informazioni su Gestione metodi di input</span><span class="sxs-lookup"><span data-stu-id="2e207-111">About Input Method Manager</span></span>](about-input-method-manager.md)
</dt> </dl>

 

 
