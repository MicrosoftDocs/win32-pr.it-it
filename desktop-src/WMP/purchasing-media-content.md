---
title: Acquisto di contenuti multimediali
description: Acquisto di contenuti multimediali
ms.assetid: df4a3152-f9e3-4a97-b021-6d5e8de9c184
keywords:
- Windows Media Player Online Stores, acquisto di contenuti multimediali
- negozi online, acquisto di contenuti multimediali
- digitare 1 negozi online, acquistare contenuti multimediali
- Windows Media Player Online Store, acquisti di contenuti multimediali
- negozi online, acquisti di contenuti multimediali
- digitare 1 negozi online, acquisti di contenuti multimediali
- contenuti multimediali, acquisti
- acquisto di contenuti multimediali
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e420f1dce607e1c596c48490d10bbe8a2a5a5f61
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/19/2020
ms.locfileid: "103956171"
---
# <a name="purchasing-media-content"></a>Acquisto di contenuti multimediali

Quando Windows Media Player Visualizza contenuto musicale nella visualizzazione albero della libreria, l'interfaccia utente include gli elementi su cui l'utente può fare clic per acquistare il contenuto. Ad esempio, l'utente può fare clic su un pulsante per acquistare un singolo brano o acquistare un intero album.

Se lo Store online attivo è di tipo 1, Windows Media Player ha accesso ai prezzi Track, album ed List nel catalogo del negozio online. I prezzi nel catalogo sono stringhe con un formato riconosciuto solo dal negozio online. Windows Media Player non interpreta le stringhe dei prezzi; vengono semplicemente visualizzate negli elementi dell'interfaccia utente come i pulsanti Acquista.

Quando Windows Media Player imposta un acquisto per un set di elementi multimediali, passa gli ID e i prezzi degli elementi multimediali al plug-in del partner di contenuti chiamando [IWMPContentPartner:: CanBuySilent](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartner-canbuysilent). A questo punto, il plug-in può ispezionare i prezzi forniti dal lettore. Si tratta dei prezzi che l'utente prevede di pagare; ovvero i prezzi visualizzati dall'utente. In base agli ID dei supporti e ai prezzi forniti dal lettore, il plug-in calcola il prezzo totale restituito al lettore nel parametro *bstrTotalPrice* . I prezzi che il giocatore passa a **CanBuySilent** forniscono il plug-in con le informazioni, ma non obbligano il plug-in a restituire un determinato prezzo totale. Il plug-in è in grado di calcolare il prezzo totale che ritiene appropriato.

Oltre a calcolare il prezzo totale di un acquisto, **CanBuySilent** determina se il purchace può procedere in modo invisibile all'utente; ovvero senza visualizzare una finestra di dialogo. Se **CanBuySilent** restituisce **True**, Windows Media Player semplicemente modifica il testo del pulsante Acquista per richiedere all'utente di confermare l'acquisto. Se **CanBuySilent** restituisce **False**, Windows Media Player visualizza una finestra di dialogo in cui viene richiesto all'utente di confermare l'acquisto. La finestra di dialogo fornisce all'utente informazioni che riepilogano l'acquisto, ad esempio il numero di album, il numero di singole tracce e il prezzo totale (restituito dal plug-in).

Dopo che l'utente ha confermato l'acquisto, il lettore chiama [IWMPContentPartner:: Buy](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartner-buy). Questa chiamata al metodo fornisce il plug-in con lo stesso elenco di contenitori di contenuto di **CanBuySilent**. Quando si chiama **Acquista**, Windows Media Player fornisce anche un cookie (semplicemente un valore **DWORD** , univoco per la sessione) che il plug-in può usare per identificare la transazione. Al termine della transazione, il plug-in deve chiamare [IWMPContentPartnerCallback:: BuyComplete](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartnercallback-buycomplete), passando il valore del cookie originale per il parametro *dwBuyCookie* , per notificare al lettore che la transazione è stata completata.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Guida per programmatori per i negozi di tipo 1 online**](programming-guide-for-type-1-online-stores.md)
</dt> </dl>

 

 




