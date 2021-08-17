---
title: Considerazioni sulla sicurezza Framework servizi di testo
description: Considerazioni sulla sicurezza Framework servizi di testo
ms.assetid: c1250ca0-3887-4519-888f-2ed436a39917
keywords:
- Framework servizi di testo (TSF), sicurezza
- TSF (Framework servizi di testo),security
- servizi di testo, sicurezza
- applicazioni abilitate per TSF, sicurezza
- sicurezza per TSF
- Framework servizi di testo (TSF), procedure consigliate
- TSF (Framework servizi di testo), procedure consigliate
- Applicazioni abilitate per TSF, procedure consigliate
- servizi di testo, procedure consigliate
- procedure consigliate per TSF
- Framework servizi di testo (TSF), controllo degli errori
- TSF (Framework servizi di testo), controllo degli errori
- applicazioni abilitate per TSF, controllo degli errori
- servizi di testo, controllo degli errori
- controllo degli errori
- Framework servizi di testo (TSF), firme digitali
- TSF (Framework servizi di testo),firme digitali
- servizi di testo, firme digitali
- applicazioni abilitate per TSF, firme digitali
- firme digitali
- Framework servizi di testo (TSF), chiamate LoadLibrary
- TSF (Framework servizi di testo), chiamate LoadLibrary
- servizi di testo, chiamate LoadLibrary
- Applicazioni abilitate per TSF, chiamate LoadLibrary
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 432418fbcb6221082083d6595aa374939bc2f4d5cf5aad145cac87444e75bdc0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118873576"
---
# <a name="security-considerations-text-services-framework"></a>Considerazioni sulla sicurezza: Framework servizi di testo

## <a name="best-practices-for-developing-with-tsf"></a>Procedure consigliate per lo sviluppo con TSF

-   **Firme digitali:** I provider di servizi di testo devono fornire firme digitali con i relativi file eseguibili binari. Un servizio di testo registrato ha accesso ai thread di sistema e potrebbe esporre informazioni altrimenti non accessibili. Per garantire un funzionamento stabile e sicuro, l'utente deve verificare la firma digitale di un servizio di testo prima che sia consentito il caricamento del servizio di testo. Per la procedura appropriata per creare una firma [digitale,](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms537361(v=vs.85)) vedere Introduzione alla firma del codice.
-   **Controllo errori:** Ogni chiamata di metodo o funzione deve essere verificata l'esito positivo. In caso di errore, le chiamate di metodo o di funzione rimanenti devono essere ignorate. La maggior parte degli esempi di codice in questa documentazione ha un controllo degli errori limitato, o nessuno, per evitare di nascondere il punto da illustrare. Non incollare gli esempi dalla documentazione direttamente nel codice di produzione. è invece consigliabile migliorare gli esempi aggiungendo il proprio controllo degli errori.

-   **Chiamate a LoadLibrary:** Per ottenere un puntatore a una qualsiasi [delle funzioni di TSF,](text-services-framework-functions.md)è necessario usare [LoadLibrary](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) e [GetProcAddress](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress). Tuttavia, è importante seguire le procedure per la formattazione del nome del percorso dll, come specificato nella **documentazione di LoadLibrary.**

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Procedure consigliate per la sicurezza](/windows/desktop/SecBP/best-practices-for-the-security-apis)
</dt> <dt>

[Introduzione alla firma del codice](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms537361(v=vs.85))
</dt> <dt>

[Funzioni TSF](text-services-framework-functions.md)
</dt> <dt>

[LoadLibrary](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya)
</dt> <dt>

[GetProcAddress](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress)
</dt> </dl>

 

 