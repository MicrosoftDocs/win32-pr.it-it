---
description: Un set di handoff specifica i protocolli che seguono un protocollo. Il parser usa un set di handoff solo quando il parser può identificare il protocollo successivo dai dati in un'istanza del protocollo.
ms.assetid: d1f44646-98ee-4e3a-a81a-83d6c87c23f4
title: Specifica di un set di handoff
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3c2f3f7d559c83e3c56bc6ea202b3a0e339dbc1b76d93fc2af1b73f5a2c60c4e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119778351"
---
# <a name="specifying-a-handoff-set"></a>Specifica di un set di handoff

Un set di handoff specifica i protocolli che seguono un protocollo. Il parser usa un set di handoff solo quando il parser può identificare il protocollo successivo dai dati in un'istanza del protocollo.

Ad esempio, il protocollo TCP ha una proprietà di porta che identifica il protocollo che segue il protocollo TCP. Il valore della proprietà 20 indica che il protocollo successivo è FTP. Il valore della proprietà 53 indica che il protocollo successivo è DNS. Poiché la proprietà port identifica il protocollo seguente, il parser TCP può usare il set di handoff seguente per ottenere un handle per il protocollo specificato dalla proprietà port.

``` syntax
[TCP_HandoffSet]
  20    = FTP
  21    = FTP
  23    = TELNET
  25    = SMTP
  53    = DNS
  79    = FINGER
  80    = HTTP
  102   = ISO
  111   = RPC
  119   = NNTP
  137   = NBT, 1000
  138   = NBT, 1002
  139   = NBT, 1001
  389   = LDAP
  445   = NBT, 1001
  515   = LPR
  612   = HMMP
  613   = HMMP
  1024  = NBT, 1001
  1047  = NBT, 1001
  1362  = TDS
  1433  = TDS
  1723  = PPTP
  3020  = NBT, 1001
  3268  = LDAP
  5678  = PPTP
```

I set di handoff vengono archiviati nel file INI del parser. Ad esempio, il set di handoff TCP precedente si trova in tcpip.ini file. Si noti che se una DLL del parser supporta più protocolli, ogni parser che usa un set di handoff ha la propria posizione nel file INI.

Le informazioni sul set di handoff vengono specificate durante l'implementazione della [**funzione ParserAutoInstallInfo.**](parserautoinstallinfo.md) Il parser può specificare i protocolli che precedono il protocollo del parser e i protocolli che seguono il protocollo del parser. Network Monitor accetta tutti i protocolli che precedono e aggiunge il protocollo del parser alle sezioni del set di passaggi seguenti del file INI del parser, per ogni protocollo precedente. Network Monitor l'elenco dei protocolli che seguono nella sezione handoff set del file INI del parser.

Network Monitor le informazioni sul set di handoff nel file INI del parser, ma il parser non accede direttamente ai file INI. Per usare le informazioni nel set handoff, il parser chiama la [**funzione CreateHandoffTable**](createhandofftable.md) per creare una tabella handoff. In genere, la tabella handoff viene creata quando il parser registra il protocollo. Dopo la registrazione del protocollo, Network Monitor una tabella del set di handoff che può essere utilizzata dal parser.

Il parser usa il set di handoff per il riconoscimento dei dati. Prima di tutto il parser legge il valore della proprietà che identifica il protocollo successivo. Il parser chiama quindi [**GetProtocolFromTable**](getprotocolfromtable.md) per ottenere un handle per il protocollo successivo. Infine, il parser restituisce un puntatore all'handle nel *parametro phNextProtocol* di [**RecognizeFrame.**](recognizeframe.md)

 

 



