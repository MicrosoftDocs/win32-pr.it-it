---
title: Documento ServiceInfo per uno Store online di tipo 1
description: Documento ServiceInfo per uno Store online di tipo 1
ms.assetid: 9ca424a1-c29a-4078-8d56-9d0fea52f150
keywords:
- Windows Media Player store online, documento ServiceInfo
- negozi online, documento ServiceInfo
- tipo 1 negozi online, documento ServiceInfo
- Documento ServiceInfo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 893cb3c849e062147d0f6bc80f3f9c1bd56a3457b60dfe30ce837820091e9710
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118995441"
---
# <a name="serviceinfo-document-for-a-type-1-online-store"></a>Documento ServiceInfo per uno Store online di tipo 1

I negozi online di tipo 1 devono fornire a Microsoft l'URL di un documento XML che descrive lo store online. Windows Media Player 11 usa questo documento per determinare come configurare l'interfaccia utente per ospitare lo store online.

Il documento ServiceInfo per un archivio di tipo 1 fornisce le informazioni seguenti per Windows Media Player:

-   Informazioni usate per configurare il **pulsante Punti vendita online** (detto anche scheda), ad esempio il testo del pulsante, il colore del pulsante e la descrizione comando per il pulsante.
-   URL per le immagini Windows Media Player per identificare lo store online.
-   URL delle pagine Web, fornite dallo store online, che Windows Media Player host nell'interfaccia utente.
-   URL in Windows Media Player possibile recuperare il plug-in dello store online in modo che il plug-in possa essere installato nel computer dell'utente.

Quando Windows Media Player recupera il documento ServiceInfo dal Web, aggiunge una stringa di query all'URL. La stringa di query contiene parametri che forniscono informazioni sulle impostazioni locali e sulla posizione geografica dell'utente e sulla versione di Windows Media Player.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Informazioni sui negozi online di tipo 1**](about-type-1-online-stores.md)
</dt> <dt>

[**Creazione dinamica del documento ServiceInfo**](creating-the-serviceinfo-document-dynamically.md)
</dt> <dt>

[**Documento ServiceInfo di esempio per un negozio online di tipo 1**](example-serviceinfo-document-for-a-type-1-online-store.md)
</dt> <dt>

[**Documento ServiceInfo**](serviceinfo-document.md)
</dt> </dl>

 

 




