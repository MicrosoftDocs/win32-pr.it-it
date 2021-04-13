---
title: Dispositivi touchpad di precisione Windows
description: Dispositivi touchpad di precisione Windows
ms.assetid: 026F9940-C985-4F3A-BDBB-2977B14EAB1F
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 07107c1d9532c4a4663a667a8e3db64124f23e5d
ms.sourcegitcommit: 40dd8501397fc79a643deb528c6c57ac2e9726ce
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/24/2020
ms.locfileid: "104398437"
---
# <a name="windows-precision-touchpad-devices"></a><span data-ttu-id="88617-103">Dispositivi touchpad di precisione Windows</span><span class="sxs-lookup"><span data-stu-id="88617-103">Windows precision touchpad devices</span></span>

## <a name="platforms"></a><span data-ttu-id="88617-104">Piattaforme</span><span class="sxs-lookup"><span data-stu-id="88617-104">Platforms</span></span>

<dl> <span data-ttu-id="88617-105">Client-Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="88617-105">Clients - Windows 8.1</span></span>  
</dl>

## <a name="description"></a><span data-ttu-id="88617-106">Descrizione</span><span class="sxs-lookup"><span data-stu-id="88617-106">Description</span></span>

<span data-ttu-id="88617-107">Windows Precision touchpad è una nuova classe di dispositivi di input che fornisce funzionalità di input e movimento del puntatore a precisione elevata.</span><span class="sxs-lookup"><span data-stu-id="88617-107">The Windows Precision Touchpad is a new class of input devices that provide high precision pointer input and gesture functionality.</span></span> <span data-ttu-id="88617-108">Per impostazione predefinita, questi dispositivi generano messaggi della rotellina di scorrimento con precisione elevata per l'utilizzo delle applicazioni desktop.</span><span class="sxs-lookup"><span data-stu-id="88617-108">By default, these devices generate ultra-high precision scroll wheel messages for desktop application consumption.</span></span>

## <a name="manifestations"></a><span data-ttu-id="88617-109">Manifestazioni</span><span class="sxs-lookup"><span data-stu-id="88617-109">Manifestations</span></span>

<span data-ttu-id="88617-110">Le applicazioni che non sono progettate per gestire i messaggi della rotellina di scorrimento con precisione ultra-alta possono scorrere in modo non corretto.</span><span class="sxs-lookup"><span data-stu-id="88617-110">Applications that are not designed to handle ultra-high precision scroll wheel messages may either over-scroll or not scroll correctly.</span></span>

## <a name="mitigation"></a><span data-ttu-id="88617-111">Strategia di riduzione del rischio</span><span class="sxs-lookup"><span data-stu-id="88617-111">Mitigation</span></span>

<span data-ttu-id="88617-112">Gli sviluppatori di applicazioni devono esaminare il Delta di scorrimento nei messaggi della rotellina di scorrimento del mouse e modificare le proprie app di conseguenza. Tuttavia, nel frattempo un'applicazione può rifiutare esplicitamente i messaggi della rotellina di scorrimento con precisione elevatissima (Delta = 1) e scegliere di ricevere messaggi della rotellina di scorrimento ad alta precisione (Delta = 40) o messaggi della rotellina di scorrimento standard (Delta = 120).</span><span class="sxs-lookup"><span data-stu-id="88617-112">Application developers should look at the scroll delta in mouse scroll wheel messages and modify their apps accordingly; however, in the interim an application may opt-out of ultra-high precision scroll wheel messages (delta = 1)and elect to receive high precision scroll wheel messages (delta = 40) or standard scroll wheel messages (delta = 120).</span></span>

## <a name="solution"></a><span data-ttu-id="88617-113">Soluzione</span><span class="sxs-lookup"><span data-stu-id="88617-113">Solution</span></span>

<span data-ttu-id="88617-114">Se l'applicazione è in grado di gestire i messaggi della rotellina di scorrimento con precisione elevatissima, non è necessario eseguire alcuna operazione perché questo è il messaggio predefinito inviato da touchpad di precisione di Windows.</span><span class="sxs-lookup"><span data-stu-id="88617-114">If the application is capable of handling ultra-high precision scroll wheel messages, nothing needs to be done as this is the default message sent by Windows Precision Touchpads.</span></span>

<span data-ttu-id="88617-115">Se l'applicazione è in grado di gestire i messaggi della rotellina di scorrimento a precisione elevata, ma non i messaggi della rotellina con precisione elevata, aggiungere quanto segue al manifesto dell'applicazione:</span><span class="sxs-lookup"><span data-stu-id="88617-115">If the application is capable of handling high precision scroll wheel messages, but not ultra-high precision wheel messages, add the following to the application manifest:</span></span>


```
<application xmlns="urn:schemas-microsoft-com:asm.v3">  
    <windowsSettings>  
      <highResolutionScrollingAware xmlns="http://schemas.microsoft.com/SMI/2013/WindowsSettings">true</highResolutionScrollingAware>  
  </windowsSettings>  
</application>  
```



<span data-ttu-id="88617-116">Se l'applicazione non è in grado di gestire i messaggi della rotellina di scorrimento a precisione elevata o i messaggi della rotellina con precisione elevata, aggiungere il codice seguente al manifesto dell'applicazione per indicare che si desiderano i messaggi della rotellina di scorrimento standard:</span><span class="sxs-lookup"><span data-stu-id="88617-116">If the application is not capable of handling either high precision scroll wheel messages or ultra-high precision wheel messages, add the following to the application manifest to indicate that standard scroll wheel messages are desired:</span></span>


```
<application xmlns="urn:schemas-microsoft-com:asm.v3">  
    <windowsSettings>  
      <ultraHighResolutionScrollingAware xmlns="http://schemas.microsoft.com/SMI/2013/WindowsSettings">false</ultraHighResolutionScrollingAware >  
  </windowsSettings>  
</application>  
```



 

 




