---
title: Considerazioni sulla sicurezza Framework servizi di testo
description: Considerazioni sulla sicurezza Framework servizi di testo
ms.assetid: c1250ca0-3887-4519-888f-2ed436a39917
keywords:
- Framework servizi di testo (TSF), sicurezza
- TSF (Framework di servizi di testo), sicurezza
- Servizi di testo, sicurezza
- Applicazioni abilitate per TSF, sicurezza
- sicurezza per TSF
- Framework servizi di testo (TSF), procedure consigliate
- TSF (Framework di servizi di testo), procedure consigliate
- Applicazioni abilitate per TSF, procedure consigliate
- Servizi di testo, procedure consigliate
- procedure consigliate per TSF
- Framework servizi di testo (TSF), controllo degli errori
- TSF (Framework dei servizi di testo), controllo degli errori
- Applicazioni abilitate per TSF, controllo degli errori
- Servizi di testo, controllo degli errori
- controllo degli errori
- Framework servizi di testo (TSF), firme digitali
- TSF (Text Services Framework), firme digitali
- Servizi di testo, firme digitali
- Applicazioni abilitate per TSF, firme digitali
- firme digitali
- Framework servizi di testo (TSF), chiamate LoadLibrary
- TSF (Framework di servizi di testo), chiamate LoadLibrary
- Servizi di testo, chiamate LoadLibrary
- Applicazioni abilitate per TSF, chiamate LoadLibrary
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0d71966106cde0f59d39442f7e2bf9b2a216cd94
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "106299866"
---
# <a name="security-considerations-text-services-framework"></a>Considerazioni sulla sicurezza: Framework dei servizi di testo

## <a name="best-practices-for-developing-with-tsf"></a>Procedure consigliate per lo sviluppo con TSF

-   **Firme digitali:** I provider di servizi di testo devono fornire firme digitali con i rispettivi file eseguibili binari. Un servizio di testo registrato può accedere ai thread di sistema e potrebbe esporre informazioni che altrimenti non sarebbero accessibili. Per garantire un'operazione stabile e sicura, l'utente deve verificare la firma digitale di un servizio di testo prima che il servizio di testo possa essere caricato. Per la procedura appropriata per la creazione di una firma digitale, vedere [Introduzione alla firma del codice](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms537361(v=vs.85)) .
-   **Controllo errori:** Ogni metodo o chiamata di funzione deve essere verificata in caso di esito positivo. In caso di errore, le chiamate al metodo o alla funzione rimanenti devono essere ignorate. La maggior parte degli esempi di codice in questa documentazione ha un controllo degli errori limitato o nessuno, per evitare di nascondere il punto da illustrare. Non è consigliabile incollare esempi dalla documentazione direttamente nel codice di produzione; è invece consigliabile migliorare gli esempi aggiungendo il controllo degli errori.

-   **Chiamate LoadLibrary:** Per ottenere un puntatore a una qualsiasi delle [funzioni TSF](text-services-framework-functions.md), è necessario usare [LoadLibrary](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) e [GetProcAddress](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress). Tuttavia, è importante attenersi alle procedure per formattare il nome del percorso della DLL, come indicato nella documentazione di **LoadLibrary** .

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Procedure di sicurezza consigliate](/windows/desktop/SecBP/best-practices-for-the-security-apis)
</dt> <dt>

[Introduzione alla firma del codice](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms537361(v=vs.85))
</dt> <dt>

[Funzioni TSF](text-services-framework-functions.md)
</dt> <dt>

[LoadLibrary](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya)
</dt> <dt>

[GetProcAddress](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress)
</dt> </dl>

 

 