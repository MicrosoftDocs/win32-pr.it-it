---
description: Un set di continuità specifica i protocolli che seguono un protocollo. Il parser utilizza un set di continuità solo quando il parser è in grado di identificare il protocollo successivo tra i dati in un'istanza del protocollo.
ms.assetid: d1f44646-98ee-4e3a-a81a-83d6c87c23f4
title: Specifica di un set di continuità
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e9acb421963bea3ffaa70b6165c6ffceee138e38
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106308157"
---
# <a name="specifying-a-handoff-set"></a>Specifica di un set di continuità

Un set di continuità specifica i protocolli che seguono un protocollo. Il parser utilizza un set di continuità solo quando il parser è in grado di identificare il protocollo successivo tra i dati in un'istanza del protocollo.

Il protocollo TCP, ad esempio, dispone di una proprietà Port che identifica il protocollo che segue il protocollo TCP. Il valore della proprietà 20 indica che il protocollo successivo è FTP. Il valore della proprietà 53 indica che il protocollo successivo è DNS. Poiché la proprietà Port identifica il protocollo che segue, il parser TCP può usare il set di continuità seguente per ottenere un handle per il protocollo specificato dalla proprietà Port.

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

I set di continuità vengono archiviati nel file INI del parser. Il set di continuità TCP precedente, ad esempio, si trova nel file tcpip.ini. Si noti che se una DLL del parser supporta più protocolli, ogni parser che usa un set di continuità ha il proprio percorso nel file INI.

Le informazioni sui set di continuità vengono specificate durante l'implementazione della funzione [**ParserAutoInstallInfo**](parserautoinstallinfo.md) . Il parser può specificare i protocolli che precedono il protocollo del parser e i protocolli che seguono il protocollo del parser. Network Monitor accetta tutti i protocolli che precedono e aggiunge il protocollo del parser alle sezioni seguenti set del file INI del parser, per ogni protocollo precedente. Network Monitor archivia l'elenco dei protocolli seguiti nella sezione set di continuità del file INI del parser.

Network Monitor archivia le informazioni sul set di continuità nel file INI del parser, ma il parser non accede direttamente ai file INI. Per usare le informazioni nel set di continuità, il parser chiama la funzione [**CreateHandoffTable**](createhandofftable.md) per creare una tabella con continuità. In genere, la tabella di continuità viene creata quando il parser registra il protocollo. Dopo che il protocollo è stato registrato, Network Monitor crea una tabella set uniforme che può essere utilizzata dal parser.

Il parser usa il set di continuità quando riconoscono i dati. Prima di tutto il parser legge il valore della proprietà che identifica il protocollo successivo. Il parser chiama quindi [**GetProtocolFromTable**](getprotocolfromtable.md) per ottenere un handle per il protocollo successivo. Infine, il parser restituisce un puntatore all'handle nel parametro *phNextProtocol* di [**RecognizeFrame**](recognizeframe.md).

 

 



