---
title: Acquisto di contenuti multimediali
description: Acquisto di contenuti multimediali
ms.assetid: df4a3152-f9e3-4a97-b021-6d5e8de9c184
keywords:
- Windows Media Player store online, acquisto di contenuti multimediali
- negozi online, acquisto di contenuti multimediali
- tipo 1 negozi online, acquisto di contenuti multimediali
- Windows Media Player store online, acquisti di contenuti multimediali
- negozi online, acquisti di contenuti multimediali
- tipo 1 negozi online, acquisti di contenuti multimediali
- contenuto multimediale, acquisto
- acquisto di contenuti multimediali
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fc830d4b1351b7649343f1f76f347c89da9a8ed9ceffedc3663c3156be6b7ead
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118995641"
---
# <a name="purchasing-media-content"></a>Acquisto di contenuti multimediali

Quando Windows Media Player contenuto musicale nella visualizzazione albero della libreria, l'interfaccia utente include elementi su cui l'utente può fare clic per acquistare il contenuto. Ad esempio, l'utente potrebbe fare clic su un pulsante per acquistare un singolo brano o per acquistare un intero album.

Se lo store online attivo è di tipo 1, Windows Media Player può accedere ai prezzi di traccia, album ed elenco nel catalogo del negozio online. Questi prezzi nel catalogo sono stringhe con un formato riconosciuto solo dallo store online. Windows Media Player non interpreta le stringhe di prezzo; semplicemente li visualizza in elementi dell'interfaccia utente come i pulsanti Acquista.

Quando Windows Media Player un acquisto per un set di elementi multimediali, passa gli ID e i prezzi degli elementi multimediali al plug-in partner di contenuti chiamando [IWMPContentPartner::CanBuySilent.](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartner-canbuysilent) A questo punto, il plug-in può esaminare i prezzi forniti dal lettore. Questi sono i prezzi che l'utente prevede di pagare. cio, i prezzi visualizzati dal lettore all'utente. In base agli ID multimediali e ai prezzi forniti dal lettore, il plug-in calcola un prezzo totale, che restituisce al lettore nel *parametro bstrTotalPrice.* I prezzi che il lettore passa a **CanBuySilent** forniscono al plug-in informazioni, ma non obbligano il plug-in a restituire un determinato prezzo totale. Il plug-in può calcolare il prezzo totale in base alle esigenze.

Oltre a calcolare il prezzo totale di un acquisto, **CanBuySilent** determina se il purchace può procedere in modo invisibile all'utente; senza visualizzare una finestra di dialogo. Se **CanBuySilent** restituisce **True,** Windows Media Player modifica semplicemente il testo nel pulsante Acquista per richiedere all'utente di confermare l'acquisto. Se **CanBuySilent** restituisce **False,** Windows Media Player viene visualizzata una finestra di dialogo che richiede all'utente di confermare l'acquisto. La finestra di dialogo fornisce all'utente informazioni che riepilogano l'acquisto, ad esempio il numero di album, il numero di tracce singole e il prezzo totale (restituito dal plug-in).

Dopo che l'utente ha confermato l'acquisto, il lettore chiama [IWMPContentPartner::Buy.](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartner-buy) Questa chiamata al metodo fornisce al plug-in lo stesso elenco di contenitori di contenuto **di CanBuySilent.** Quando si **chiama Acquista,** Windows Media Player fornisce anche un cookie (semplicemente un **valore DWORD,** univoco per la sessione) che il plug-in può usare per identificare la transazione. Al termine della transazione, il plug-in deve chiamare [IWMPContentPartnerCallback::BuyComplete,](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartnercallback-buycomplete)passando il valore del cookie originale per *il parametro dwBuyCookie,* per notificare al lettore che la transazione è stata completata.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Guida di programmazione per gli store online di tipo 1**](programming-guide-for-type-1-online-stores.md)
</dt> </dl>

 

 




