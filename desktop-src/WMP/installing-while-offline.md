---
title: Installazione offline
description: Installazione offline
ms.assetid: 29d80b6b-161d-44a7-b91e-70766b849c55
keywords:
- Windows Media Player Online Stores, installazione offline
- negozi online, installazione offline
- digitare 1 negozi online, installazione offline
- digitare 2 archivi online, installazione offline
- Windows Media Player Online Stores, installazioni offline
- archivi online, installazioni offline
- digitare 1 archivi online, installazioni offline
- digitare 2 archivi online, installazioni offline
- installazione di archivi online offline
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cad7048926f218ea7be74a2522eb32c58241a017
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103856365"
---
# <a name="installing-while-offline"></a>Installazione offline

Gli utenti possono installare Windows Media Player mentre non sono connessi a Internet. In tal caso, il programma di installazione di Windows Media Player individua il documento ServiceInfo.xml specificato dal parametro della riga di comando *ServiceInfo* . Se l'attributo **chiave** corrisponde al parametro della riga di comando *DefaultService* , il programma di installazione applica le informazioni dei seguenti elementi a Windows Media Player:

-   FriendlyName. Il nome descrittivo dello Store online viene visualizzato nell'interfaccia utente di Windows Media Player.
-   Colore. I colori specificati vengono applicati alla barra delle applicazioni e ai pulsanti.
-   ServiceTask1, ServiceTask2 e ServiceTask3. Gli elementi figlio ButtonText e ButtonTip sono impostati. L'attributo URL non è impostato. L'URL viene impostato quando l'utente si connette a Internet e Windows Media Player recupera l'elenco dei negozi online in modo normale.
-   Immagine. Gli attributi MenuURL e ServiceLargeURL sono impostati. Questi URL devono puntare alle immagini installate sul disco rigido dell'utente usando il protocollo file://.

Quando l'utente tenta di visualizzare lo Store online, Windows Media Player visualizza un messaggio che informa l'utente che è necessaria una connessione Internet.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Elemento color**](color-element.md)
</dt> <dt>

[**Elemento FriendlyName**](friendlyname-element.md)
</dt> <dt>

[**Elemento immagine**](image-element.md)
</dt> <dt>

[**Informazioni comuni ai negozi online di tipo 1 e di tipo 2**](information-common-to-type-1-and-type-2-online-stores.md)
</dt> <dt>

[**Elemento ServiceInfo**](serviceinfo-element.md)
</dt> <dt>

[**Elemento ServiceTask1**](servicetask1-element.md)
</dt> <dt>

[**Elemento ServiceTask2**](servicetask2-element.md)
</dt> <dt>

[**Elemento ServiceTask3**](servicetask3-element.md)
</dt> <dt>

[**Impostazione dell'archivio online iniziale**](setting-the-initial-online-store.md)
</dt> <dt>

[**Configurare i parametri della riga di comando per i negozi online**](setup-command-line-parameters-for-online-stores.md)
</dt> </dl>

 

 




