---
title: Negoziazione Media-Type
description: Molti protocolli Internet a livello di applicazione sono basati sullo scambio di messaggi in un formato semplice e flessibile denominato Multipurpose Internet Mail Extensions (MIME).
ms.assetid: 7a2c9d8f-639a-4865-a62b-63330175f5f0
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cb145fa3a76da6574172ddd24888f3b5da7ad85e
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/21/2020
ms.locfileid: "104399782"
---
# <a name="media-type-negotiation"></a>Negoziazione Media-Type

Molti protocolli Internet a livello di applicazione sono basati sullo scambio di messaggi in un formato semplice e flessibile denominato Multipurpose Internet Mail Extensions (MIME). Sebbene MIME sia stato originato come standard per lo scambio di messaggi di posta elettronica, viene usato oggi da un'ampia gamma di applicazioni per specificare i formati di dati riconosciuti a vicenda come MIME, o supporti, tipi. Il processo è denominato *negoziazione del tipo di supporto*.

I tipi di supporto sono stringhe semplici che indicano un tipo e un sottotipo (ad esempio "text/plain" o "Text/HTML"). Vengono usati per etichettare i dati o qualificare una richiesta. Un Web browser, ad esempio, come parte di una richiesta HTTP for-data o Request-for-info, specifica che richiede i tipi di supporto "image/gif" o "image/jpeg", a cui un server Web risponde restituendo il tipo di supporto appropriato e, se la chiamata era una richiesta di dati, i dati nel formato richiesto.

La negoziazione del tipo di supporto è spesso simile al modo in cui le applicazioni desktop esistenti negoziano con gli Appunti di sistema per determinare il formato dati da incollare quando un utente sceglie Modifica/Incolla o esegue query per i formati quando riceve un puntatore [**IDataObject**](/windows/desktop/api/ObjIdl/nn-objidl-idataobject) durante un'operazione di trascinamento della selezione. La differenza minima nella negoziazione del tipo di supporto HTTP è che il client non è in grado di stabilire in anticipo quali formati sono disponibili nel server. Pertanto, il client specifica i tipi di supporto supportati, in ordine di fedeltà massima, e il server risponde con il migliore formato disponibile.

I moniker URL supportano la negoziazione del tipo di supporto per i client e i server Internet per accettare i formati da usare durante il download dei dati nelle operazioni [**BindToStorage**](/windows/desktop/api/ObjIdl/nf-objidl-imoniker-bindtostorage) . Per supportare la negoziazione del tipo di supporto, un client implementa l'interfaccia [**IEnumFORMATETC**](/windows/desktop/api/ObjIdl/nn-objidl-ienumformatetc) e chiama la funzione [**RegisterFormatEnumerator**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms775116(v=vs.85)) per registrarla con il contesto di associazione. L'enumeratore di formato elenca i formati che il client può accettare. Un moniker URL converte questi formati in tipi di supporto durante l'associazione agli URL HTTP.

I tipi di supporti possibili richiesti dal client sono rappresentati da moniker URL tramite strutture [**FORMATETC**](/windows/win32/api/objidl/ns-objidl-formatetc) disponibili nell'enumeratore [**IEnumFORMATETC**](/windows/desktop/api/ObjIdl/nn-objidl-ienumformatetc) registrato dal chiamante nel contesto di binding: ogni **FORMATETC** specifica un formato degli appunti che identifica il tipo di supporto. Ad esempio, il frammento di codice seguente specifica che il tipo di supporto è post-script.

``` syntax
FORMATETC fmtetc;
fmtetc.cfFormat = RegisterClipboardFormat(CF_MIME_POSTSCRIPT);
. . .
```

Un client può impostare il formato degli Appunti sul tipo di supporto speciale CF \_ null per indicare che il tipo di supporto predefinito della risorsa a cui fa riferimento l'URL deve essere recuperato. Questo formato è in genere l'ultimo a cui il client è interessato. Quando nessun enumeratore viene registrato con il contesto di binding, un moniker URL funziona come se fosse disponibile un enumeratore contenente un singolo [**FORMATETC**](/windows/win32/api/objidl/ns-objidl-formatetc) con **cfFormat**= CF \_ null, scaricando automaticamente il tipo di supporto predefinito.

Indipendentemente dal tipo di supporto da usare, il client riceve una notifica della scelta per mezzo dell'argomento *pFormatetc* nel metodo [**IBindStatusCallback:: ondataavailable**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms775061(v=vs.85)) . Il callback si verifica nel contesto della chiamata del client a [**BindToStorage**](/windows/desktop/api/ObjIdl/nf-objidl-imoniker-bindtostorage).

> [!Note]  
> Se il contenuto ricevuto è di un tipo di supporto non riconosciuto, il client chiama automaticamente [**RegisterMediaTypes**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms775118(v=vs.85)) per registrare il nuovo tipo.

 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Moniker URL](url-monikers.md)
</dt> </dl>

 

 