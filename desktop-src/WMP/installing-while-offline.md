---
title: Installazione offline
description: Installazione offline
ms.assetid: 29d80b6b-161d-44a7-b91e-70766b849c55
keywords:
- Windows Media Player online, installazione offline
- online store, installazione offline
- tipo 1 negozi online, installazione offline
- store online di tipo 2, installazione offline
- Windows Media Player online store, installazioni offline
- negozi online, installazioni offline
- tipo 1 negozi online, installazioni offline
- store online di tipo 2, installazioni offline
- installazione di negozi online offline
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b3051aca9634bc2c53950baa783bcf62fc6861c616facd9dc563d70d011c2459
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119135504"
---
# <a name="installing-while-offline"></a>Installazione offline

Gli utenti possono installare Windows Media Player mentre non sono connessi a Internet. In questo caso, Windows Media Player il programma di installazione individua ServiceInfo.xml documento specificato dal parametro della riga di comando *ServiceInfo.* Se **l'attributo Key** corrisponde al parametro della riga di comando *DefaultService,* il programma di installazione applica le informazioni degli elementi seguenti Windows Media Player:

-   Friendlyname. Il nome descrittivo dello store online viene visualizzato nell'Windows Media Player utente.
-   Colore. I colori specificati vengono applicati alla barra delle applicazioni e ai pulsanti.
-   ServiceTask1, ServiceTask2 e ServiceTask3. Gli elementi figlio ButtonText e ButtonTip sono impostati. L'attributo URL non è impostato. L'URL viene impostato quando l'utente si connette a Internet Windows Media Player recupera l'elenco dei negozi online nel modo normale.
-   Immagine. Vengono impostati gli attributi MenuURL e ServiceLargeURL. Questi URL devono puntare alle immagini installate nel disco rigido dell'utente usando il file:// remoto.

Quando l'utente tenta di visualizzare lo store online, Windows Media Player un messaggio che informa l'utente che è necessaria una connessione Internet.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Elemento Color**](color-element.md)
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

[**Impostazione dello Store online iniziale**](setting-the-initial-online-store.md)
</dt> <dt>

[**Configurare i parametri della riga di comando per i negozi online**](setup-command-line-parameters-for-online-stores.md)
</dt> </dl>

 

 




