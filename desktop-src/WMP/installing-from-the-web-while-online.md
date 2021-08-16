---
title: Installazione dal Web in modalità online
description: Installazione dal Web in modalità online
ms.assetid: 891483b0-6ba4-4ed4-b043-c6c109dc696b
keywords:
- Windows Media Player online, installazione dal Web mentre è online
- online store, installazione dal Web mentre è online
- type 1 online stores,installing from Web while online
- store online di tipo 2, installazione dal Web mentre è online
- Windows Media Player online store, installazioni online dal Web
- online store, installazioni online dal Web
- store online di tipo 1, installazioni online dal Web
- store online di tipo 2, installazioni online dal Web
- installazione di negozi online dal Web mentre è online
- installazioni online di negozi online
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 801dd9fbee8bff2660a39f6b40e8a5a9e703df00f82be54a7b93c0d200d2ccea
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119135554"
---
# <a name="installing-from-the-web-while-online"></a>Installazione dal Web in modalità online

Gli utenti possono Windows Media Player come download Web mentre sono connessi a Internet. In questo caso, Microsoft può configurare lo store online iniziale specificato.

Per ridistribuire Windows Media Player in questo modo, usare l'URL seguente:

https://go.microsoft.com/fwlink/p/?linkid=32981&SV=*version*&UserLocale=*localID*&Service=*key*

Nell'URL precedente impostare *key* sul nome della chiave per il negozio online e *localeID* sull'identificatore delle impostazioni locali in cui il negozio fornisce il servizio. Impostare *la* versione su 2 per Windows Media Player 11 in Windows XP o 1 per Windows Media Player 10. L'URL Windows Media Player e imposta l'archivio attivo iniziale su quello specificato dalla *chiave*.

L'esempio seguente mostra un URL che installa Windows Media Player 11 e imposta Proseware come archivio attivo iniziale. Il valore 409 per *localeID* indica che Proseware fornisce il servizio nel Stati Uniti.

https://go.microsoft.com/fwlink/p/?linkid=32981&SV=2&UserLocale=409&Service=Proseware

Se il documento ServiceInfo per lo store online include un elemento Install, Windows Media Player programma di installazione personalizza il processo di installazione. Usando i valori degli attributi, il programma di installazione visualizza il contratto di licenza con l'utente finale e l'informativa sulla privacy e recupera e installa il file .cab nel computer dell'utente. Ad esempio, è possibile usare questa funzionalità per installare la versione più recente di un oggetto COM richiesto dal negozio online.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Informazioni comuni ai negozi online di tipo 1 e di tipo 2**](information-common-to-type-1-and-type-2-online-stores.md)
</dt> <dt>

[**Elemento Install**](install-element.md)
</dt> <dt>

[**Documento ServiceInfo**](serviceinfo-document.md)
</dt> <dt>

[**Impostazione dello Store online iniziale**](setting-the-initial-online-store.md)
</dt> </dl>

 

 




