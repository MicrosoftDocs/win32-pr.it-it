---
title: Installazione dal Web in linea
description: Installazione dal Web in linea
ms.assetid: 891483b0-6ba4-4ed4-b043-c6c109dc696b
keywords:
- Windows Media Player Online Stores, installazione dal Web in linea
- negozi online, installazione dal Web in linea
- digitare 1 negozi online, installazione dal Web in linea
- digitare 2 archivi online, installazione dal Web in linea
- Windows Media Player Online Stores, installazioni online dal Web
- negozi online, installazioni online dal Web
- digitare 1 negozi online, installazioni online dal Web
- digitare 2 archivi online, installazioni online dal Web
- installazione di archivi online dal Web in linea
- installazioni online di archivi online
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dd342d3fc79cf3012d5bc290561a9b63167e044f
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "106298429"
---
# <a name="installing-from-the-web-while-online"></a>Installazione dal Web in linea

Gli utenti possono installare Windows Media Player come download Web mentre si è connessi a Internet. In questo caso, Microsoft può configurare l'archivio online iniziale specificato.

Per ridistribuire Windows Media Player in questo modo, usare l'URL seguente:

https://go.microsoft.com/fwlink/p/?linkid=32981&SV=*version*&UserLocale =*localizzated*&Service =*Key*

Nell'URL precedente impostare *chiave* sul nome della chiave per l'archivio online e impostare *LocaleID* sull'identificatore delle impostazioni locali in cui l'archivio fornisce il servizio. Impostare la *versione* su 2 per Windows Media Player 11 in Windows XP o 1 per Windows Media Player 10. L'URL installa Windows Media Player e imposta l'archivio attivo iniziale su quello specificato dalla *chiave*.

Nell'esempio seguente viene illustrato un URL che installa Windows Media Player 11 e imposta Proseware come archivio attivo iniziale. Il valore di 409 per *LocaleID* indica che Proseware fornisce il servizio nel Stati Uniti.

https://go.microsoft.com/fwlink/p/?linkid=32981&SV=2&UserLocale=409&Service=Proseware

Se il documento ServiceInfo per l'archivio online include un elemento di installazione, il programma di installazione di Windows Media Player Personalizza il processo di installazione. Utilizzando i valori di attributo, il programma di installazione Visualizza il contratto di licenza con l'utente finale (EULA) e l'informativa sulla privacy, nonché recupera e installa il file CAB nel computer dell'utente. Ad esempio, è possibile usare questa funzionalità per installare la versione più recente di un oggetto COM richiesto dal negozio online.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Informazioni comuni ai negozi online di tipo 1 e di tipo 2**](information-common-to-type-1-and-type-2-online-stores.md)
</dt> <dt>

[**Elemento install**](install-element.md)
</dt> <dt>

[**Documento ServiceInfo**](serviceinfo-document.md)
</dt> <dt>

[**Impostazione dell'archivio online iniziale**](setting-the-initial-online-store.md)
</dt> </dl>

 

 




