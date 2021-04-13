---
title: Registrazione multimediale
description: Registrazione multimediale
ms.assetid: e37aaac2-be89-4907-b1a8-f2c64ab2f39e
keywords:
- MCIWndCreate (funzione)
- MCIWndNew (macro)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b6b1793ff7653e87a631ce1a4599345ec78f4015
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104395918"
---
# <a name="multimedia-recording"></a><span data-ttu-id="9155e-105">Registrazione multimediale</span><span class="sxs-lookup"><span data-stu-id="9155e-105">Multimedia Recording</span></span>

<span data-ttu-id="9155e-106">È possibile implementare le funzionalità di registrazione nell'applicazione usando l'interfaccia utente incorporata in MCIWnd.</span><span class="sxs-lookup"><span data-stu-id="9155e-106">You can implement recording capabilities in your application by using the user interface built into MCIWnd.</span></span> <span data-ttu-id="9155e-107">È possibile utilizzare la funzione [**MCIWndCreate**](/windows/desktop/api/Vfw/nf-vfw-mciwndcreatea) e la macro [**MCIWndNew**](/windows/desktop/api/Vfw/nf-vfw-mciwndnew) per fornire controlli per l'avvio e l'arresto della registrazione e per il salvataggio delle informazioni registrate.</span><span class="sxs-lookup"><span data-stu-id="9155e-107">You can use the [**MCIWndCreate**](/windows/desktop/api/Vfw/nf-vfw-mciwndcreatea) function and the [**MCIWndNew**](/windows/desktop/api/Vfw/nf-vfw-mciwndnew) macro to provide controls for starting and stopping recording and for saving the recorded information.</span></span> <span data-ttu-id="9155e-108">Utilizzando **MCIWndCreate**, è possibile specificare gli stili della finestra per visualizzare una finestra di MCIWnd e includere il pulsante **record** sulla barra degli strumenti.</span><span class="sxs-lookup"><span data-stu-id="9155e-108">Using **MCIWndCreate**, you can specify window styles to display an MCIWnd window and to include the **Record** button on the toolbar.</span></span> <span data-ttu-id="9155e-109">Usando **MCIWndNew**, è possibile specificare il tipo di dispositivo da registrare e specificare che le informazioni devono essere acquisite in un nuovo file.</span><span class="sxs-lookup"><span data-stu-id="9155e-109">Using **MCIWndNew**, you can specify the device type that is being recorded and specify that the information is to be captured in a new file.</span></span>

<span data-ttu-id="9155e-110">Se l'applicazione richiede una maggiore complessità, è possibile automatizzare e personalizzare la registrazione usando la macro [**MCIWndRecord**](/windows/desktop/api/Vfw/nf-vfw-mciwndrecord) .</span><span class="sxs-lookup"><span data-stu-id="9155e-110">If your application requires more sophistication, you can automate and customize the recording by using the [**MCIWndRecord**](/windows/desktop/api/Vfw/nf-vfw-mciwndrecord) macro.</span></span> <span data-ttu-id="9155e-111">Per ulteriori informazioni, vedere [personalizzazione del processo di registrazione](customizing-the-recording-process.md).</span><span class="sxs-lookup"><span data-stu-id="9155e-111">For more information, see [Customizing the Recording Process](customizing-the-recording-process.md).</span></span>

> [!Note]  
> <span data-ttu-id="9155e-112">Alcuni dispositivi, ad esempio CD audio e MCIAVI, vengono usati solo per la riproduzione.</span><span class="sxs-lookup"><span data-stu-id="9155e-112">Some devices, such as CD audio and MCIAVI, are used for playback only.</span></span> <span data-ttu-id="9155e-113">Per la registrazione, è possibile usare altri dispositivi, ad esempio dispositivi audio waveform.</span><span class="sxs-lookup"><span data-stu-id="9155e-113">Other devices, such as waveform-audio devices, can be used for recording.</span></span> <span data-ttu-id="9155e-114">Se si specifica un dispositivo che non è in grado di registrare, MCIWnd omette il pulsante **record** dalla barra degli strumenti.</span><span class="sxs-lookup"><span data-stu-id="9155e-114">If you specify a device that cannot record, MCIWnd omits the **Record** button from the toolbar.</span></span>

 

 

 




