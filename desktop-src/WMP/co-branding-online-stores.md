---
title: Co-Branding online
description: Co-Branding online
ms.assetid: b564845a-a4e0-4fe6-90cb-63ef320c7e52
keywords:
- Windows Media Player online store, co-branding
- online store, co-branding
- tipo 1 punti vendita online, co-personalizzazione
- store online di tipo 2, co-personalizzazione
- co-branding di negozi online
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: db3ca69c377a7aedeb71f05008d707fab955f02bf0e02d7b0ca35861105aade1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118342132"
---
# <a name="co-branding-online-stores"></a>Co-Branding online

Gli OEM di personal computer che non gestiscono un negozio di musica possono creare un co-brand con i provider di store online. Windows Media Player programma di installazione supporta il parametro della riga di comando ServiceExtra per consentire agli OEM hardware di impostare un attributo personalizzato che lo store online può usare per identificare quale OEM ha installato lo store online iniziale.

Ad esempio, se un autore di computer denominato Fabrikam vuole impostare lo store online iniziale su Proseware Music Store, potrebbe usare la riga di comando seguente per installare Windows Media Player 10:


```C++
MP10Setup.exe /q:A /c:"setup_wm.exe /Q /R:N /DefaultService:Proseware /ServiceInfo:c:\Proseware\service_info_local.xml /ServiceExtra:OEM=Fabrikam"
```



Quando Windows Media Player viene installato in questo modo, il lettore aggiunge la stringa ServiceExtra ogni volta che apre il servizio Proseware. L'esempio seguente mostra l'URL che Windows Media Player inviare al servizio Proseware per recuperare il documento ServiceInfo:


```C++
https://www.proseware.com/XML/serviceinfo.asp?OEM=Fabrikam
```



Lo store online Proseware può quindi usare la stringa di query per determinare quale OEM installato Windows Media Player e restituire un documento ServiceInfo generato dinamicamente che punta alla versione con marchio co-branded dello store online.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Informazioni comuni ai negozi online di tipo 1 e di tipo 2**](information-common-to-type-1-and-type-2-online-stores.md)
</dt> <dt>

[**Configurare i parametri della riga di comando per i negozi online**](setup-command-line-parameters-for-online-stores.md)
</dt> </dl>

 

 




