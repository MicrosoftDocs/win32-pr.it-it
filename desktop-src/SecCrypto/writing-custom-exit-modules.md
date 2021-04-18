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
# <a name="writing-custom-exit-modules"></a>Scrittura di moduli di uscita personalizzati

I moduli di uscita personalizzati devono implementare l'interfaccia [**ICertExit**](/windows/desktop/api/Certexit/nn-certexit-icertexit) , chiamata dal motore del server. Il metodo [**ICertExit:: Initialize**](/windows/desktop/api/Certexit/nf-certexit-icertexit-initialize) viene chiamato dal motore del server quando viene caricato il modulo di uscita. Consente al modulo Exit di eseguire l'inizializzazione e restituisce un valore che informa il motore del server dei tipi di eventi per i quali si desidera la notifica. Il metodo [**ICertExit:: GetDescription**](/windows/desktop/api/Certexit/nf-certexit-icertexit-getdescription) deve restituire una stringa di descrizione quando viene richiesta dal motore Server. Il metodo [**ICertExit:: Notify**](/windows/desktop/api/Certexit/nf-certexit-icertexit-notify) viene chiamato dal motore del server per notificare al modulo di uscita che si è verificato un evento.

I moduli di uscita possono chiamare l'interfaccia [**ICertServerExit**](/windows/desktop/api/Certif/nn-certif-icertserverexit) , che supporta molti degli stessi metodi dell'interfaccia [**ICertServerPolicy**](/windows/desktop/api/Certif/nn-certif-icertserverpolicy) , ad eccezione dei metodi [**SetCertificateExtension**](/windows/desktop/api/Certif/nf-certif-icertserverpolicy-setcertificateextension) e [**SetCertificateProperty**](/windows/desktop/api/Certif/nf-certif-icertserverpolicy-setcertificateproperty) .

Per informazioni sulla rimozione del modulo di uscita esistente e sull'installazione di uno nuovo, vedere l'argomento relativo alla personalizzazione del modulo di uscita nella Guida di.

 

 



