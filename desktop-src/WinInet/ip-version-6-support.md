---
title: Supporto ip versione 6
description: A partire da IE7 e versione superiore, WinINet supporta i valori letterali IPv6 nel nome host e il componente dell'autorità dell'URI.
ms.assetid: cbbb9f93-15b0-4017-ac39-8a396203532e
keywords:
- Supporto ip versione 6
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 67a024c792995780769a078c84b0493b7abba8647189fa2cee835d93dcb83770
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118113631"
---
# <a name="ip-version-6-support"></a>Supporto ip versione 6

A partire da IE7 e versione superiore, WinINet supporta i valori letterali IPv6 nel nome host e il componente dell'autorità dell'URI. WinINet supporta anche l'uso di valori letterali IPv6 in parti pertinenti del protocollo HTTP, ad esempio nell'intestazione Location.

## <a name="hostname-ipv6-literals-and-uri-components"></a>Valori letterali IPv6 del nome host e componenti URI

WinINet implementa i valori letterali IPv6 in base alle specifiche in RFC 3513. Come specificato in questa RFC, i valori letterali IPv6 in un URI devono essere racchiusi tra parentesi quadre. Ad esempio, https:// \[ ::1 / è un URI IPv6 valido. Il formato senza \] parentesi quadre ( non è https://::1/) valido. I valori letterali IPv6 del nome host che non fanno parte dell'URI, tuttavia, non devono essere racchiusi tra parentesi quadre. Entrambi i moduli sono accettabili per WinINet. Ad esempio, sia "::1" che " ::1 " sono forme accettabili di valori letterali \[ \] nome host IPv6. Anche altre API, ad esempio l'API WinSock, accetteranno entrambi i moduli. Le applicazioni devono quindi essere preparate a gestire entrambe le forme di valori letterali nome host IPv6.

## <a name="scope-id"></a>ID ambito

L'indirizzo letterale IPv6 nell'URI può includere un ID ambito. Un ID ambito può essere un ID di interfaccia, ad \[ esempio FE80::1%1. \] Lo standard URI, documentato in RFC 3986, non definisce la sintassi per l'ID ambito e l'URI viene considerato non uniforme quando è presente l'ID ambito. Tuttavia, WinINet accetta un ID ambito nel componente dell'autorità dell'URI e nel valore letterale IPv6 del nome host.

Il carattere percentuale (%) nell'indirizzo letterale IPv6 deve essere preceduto da un carattere di escape percentuale quando è presente nell'URI. Ad esempio, l'ID di ambito FE80::2%3 deve essere visualizzato nell'URI come "https:// \[ FE80::2%253 /", dove %25 è il carattere percentuale con codifica esadecimale \] (%). Se l'applicazione recupera l'URI da un'API Unicode, ad esempio l'API [**Winsock WSAAddressToString,**](/windows/desktop/api/winsock2/nf-winsock2-wsaaddresstostringa) l'applicazione deve aggiungere la versione preceduta da carattere di escape del carattere di percentuale (%) nel nome host dell'URI. Per creare la versione con caratteri di escape dell'URI, le applicazioni chiamano [**InternetCreateUrl**](/windows/desktop/api/Wininet/nf-wininet-internetcreateurla) con il parametro *dwFlags* impostato su **ICU \_ ESCAPE \_ AUTHORITY** e il nome host IPv6 specificato nella struttura dei componenti URL specificata nel parametro *lpUrlComponents.*

Per tutte le operazioni socket, WinINet usa l'ID ambito. Tuttavia, poiché l'ID ambito ha significato solo per l'host locale, non viene inviato come parte delle intestazioni del protocollo HTTP nella richiesta. Ad esempio, la chiamata a [**InternetOpenUrl**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla) viene chiamata con l'URL seguente nel *parametro lpszUrl.*

``` syntax
https://[fec0::2%251]:80/path.htm
```

La parte dell'ID ambito dell'URL viene rimossa da WinINet quando viene inviata la richiesta HTTP per questo URL. La richiesta contiene le intestazioni seguenti:

``` syntax
GET path.htm HTTP/1.1
Host: [fec0::2]
```

> [!Note]  
> WinINet non supporta le implementazioni del server. Inoltre, non deve essere usato da un servizio. Per le implementazioni o i servizi server, [usare Microsoft Windows servizi HTTP (WinHTTP).](/windows/desktop/WinHttp/winhttp-start-page)

 

 

 