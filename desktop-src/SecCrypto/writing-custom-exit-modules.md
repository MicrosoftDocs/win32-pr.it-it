---
description: I moduli di uscita personalizzati devono implementare l'interfaccia ICertExit, chiamata dal motore del server.
ms.assetid: 509e7945-b656-4c4c-b5eb-45fbe80377c7
title: Scrittura di moduli di uscita personalizzati
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 81798996059e878ef11dbcdf290298094d0849cb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106316647"
---
# <a name="writing-custom-exit-modules"></a><span data-ttu-id="3429c-103">Scrittura di moduli di uscita personalizzati</span><span class="sxs-lookup"><span data-stu-id="3429c-103">Writing Custom Exit Modules</span></span>

<span data-ttu-id="3429c-104">I moduli di uscita personalizzati devono implementare l'interfaccia [**ICertExit**](/windows/desktop/api/Certexit/nn-certexit-icertexit) , chiamata dal motore del server.</span><span class="sxs-lookup"><span data-stu-id="3429c-104">Custom exit modules must implement the [**ICertExit**](/windows/desktop/api/Certexit/nn-certexit-icertexit) interface, which is called by the server engine.</span></span> <span data-ttu-id="3429c-105">Il metodo [**ICertExit:: Initialize**](/windows/desktop/api/Certexit/nf-certexit-icertexit-initialize) viene chiamato dal motore del server quando viene caricato il modulo di uscita.</span><span class="sxs-lookup"><span data-stu-id="3429c-105">The [**ICertExit::Initialize**](/windows/desktop/api/Certexit/nf-certexit-icertexit-initialize) method is called by the server engine when the exit module is loaded.</span></span> <span data-ttu-id="3429c-106">Consente al modulo Exit di eseguire l'inizializzazione e restituisce un valore che informa il motore del server dei tipi di eventi per i quali si desidera la notifica.</span><span class="sxs-lookup"><span data-stu-id="3429c-106">It allows the exit module to perform initialization and returns a value that informs the server engine of the kinds of events for which it wants notification.</span></span> <span data-ttu-id="3429c-107">Il metodo [**ICertExit:: GetDescription**](/windows/desktop/api/Certexit/nf-certexit-icertexit-getdescription) deve restituire una stringa di descrizione quando viene richiesta dal motore Server.</span><span class="sxs-lookup"><span data-stu-id="3429c-107">The [**ICertExit::GetDescription**](/windows/desktop/api/Certexit/nf-certexit-icertexit-getdescription) method must return a description string when the server engine requests it.</span></span> <span data-ttu-id="3429c-108">Il metodo [**ICertExit:: Notify**](/windows/desktop/api/Certexit/nf-certexit-icertexit-notify) viene chiamato dal motore del server per notificare al modulo di uscita che si è verificato un evento.</span><span class="sxs-lookup"><span data-stu-id="3429c-108">The [**ICertExit::Notify**](/windows/desktop/api/Certexit/nf-certexit-icertexit-notify) method is called by the server engine to notify the exit module that an event has occurred.</span></span>

<span data-ttu-id="3429c-109">I moduli di uscita possono chiamare l'interfaccia [**ICertServerExit**](/windows/desktop/api/Certif/nn-certif-icertserverexit) , che supporta molti degli stessi metodi dell'interfaccia [**ICertServerPolicy**](/windows/desktop/api/Certif/nn-certif-icertserverpolicy) , ad eccezione dei metodi [**SetCertificateExtension**](/windows/desktop/api/Certif/nf-certif-icertserverpolicy-setcertificateextension) e [**SetCertificateProperty**](/windows/desktop/api/Certif/nf-certif-icertserverpolicy-setcertificateproperty) .</span><span class="sxs-lookup"><span data-stu-id="3429c-109">Exit modules can call the [**ICertServerExit**](/windows/desktop/api/Certif/nn-certif-icertserverexit) interface, which supports many of the same methods as the [**ICertServerPolicy**](/windows/desktop/api/Certif/nn-certif-icertserverpolicy) interface, with the exception of the [**SetCertificateExtension**](/windows/desktop/api/Certif/nf-certif-icertserverpolicy-setcertificateextension) and [**SetCertificateProperty**](/windows/desktop/api/Certif/nf-certif-icertserverpolicy-setcertificateproperty) methods.</span></span>

<span data-ttu-id="3429c-110">Per informazioni sulla rimozione del modulo di uscita esistente e sull'installazione di uno nuovo, vedere l'argomento relativo alla personalizzazione del modulo di uscita nella Guida di.</span><span class="sxs-lookup"><span data-stu-id="3429c-110">For information about removing the existing exit module and installing a new one, see the Exit Module Customization topic in Help.</span></span>

 

 



