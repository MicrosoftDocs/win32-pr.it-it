---
title: Supporto IP versione 6
description: A partire da IE7 e versioni successive, WinINet supporta i valori letterali IPv6 nel nome host e il componente Authority dell'URI.
ms.assetid: cbbb9f93-15b0-4017-ac39-8a396203532e
keywords:
- Supporto IP versione 6
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f5ed0857d9a0968bcd3e6c18e54623fb0c7d86cb
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104399530"
---
# <a name="ip-version-6-support"></a>Supporto IP versione 6

A partire da IE7 e versioni successive, WinINet supporta i valori letterali IPv6 nel nome host e il componente Authority dell'URI. WinINet supporta inoltre l'utilizzo di valori letterali IPv6 in parti rilevanti del protocollo HTTP, ad esempio nell'intestazione Location.

## <a name="hostname-ipv6-literals-and-uri-components"></a>Valori letterali IPv6 hostname e componenti URI

WinINet implementa i valori letterali IPv6 secondo le specifiche in RFC 3513. Come specificato in questa RFC, i valori letterali IPv6 in un URI devono essere racchiusi tra parentesi quadre. Ad esempio, https:// \[ :: 1 \] /è un URI IPv6 valido, il form senza parentesi quadre ( https://::1/) non è valido. I valori letterali IPv6 hostname che non fanno parte dell'URI, tuttavia, non devono essere racchiusi tra parentesi quadre. ogni form è accettabile per WinINet. Ad esempio, ":: 1" e " \[ :: 1 \] " sono formati accettabili di valori letterali hostname IPv6. Altre API, ad esempio l'API WinSock, accetteranno anche entrambi i moduli. Pertanto, le applicazioni devono essere preparate a gestire entrambe le forme di valori letterali del nome host IPv6.

## <a name="scope-id"></a>ID ambito

L'indirizzo letterale IPv6 nell'URI può includere un ID ambito. Un ID ambito può essere un ID di interfaccia, ad esempio \[ FE80:: 1% 1 \] . Lo standard URI, documentato in RFC 3986, non definisce la sintassi per l'ID ambito e l'URI viene considerato non uniforme quando è presente l'ID ambito. Tuttavia, WinINet accetta un ID ambito nel componente Authority dell'URI e nel valore letterale IPv6 del nome host.

Il carattere di percentuale (%) nell'indirizzo letterale IPv6 deve essere preceduto da un carattere di escape percentuale se presente nell'URI. L'ID ambito FE80:: 2% 3, ad esempio, deve essere visualizzato nell'URI come "https:// \[ FE80:: 2% 253 \] /", dove %25 è il carattere di percentuale con codifica esadecimale (%). Se l'applicazione recupera l'URI da un'API Unicode, ad esempio l'API Winsock [**WSAAddressToString**](/windows/desktop/api/winsock2/nf-winsock2-wsaaddresstostringa) , l'applicazione deve aggiungere la versione di escape del carattere di percentuale (%) nel nome host dell'URI. Per creare la versione di escape dell'URI, le applicazioni chiamano [**InternetCreateUrl**](/windows/desktop/api/Wininet/nf-wininet-internetcreateurla) con il parametro *dwFlags* impostato sull' **\_ \_ autorità di escape ICU** e il nome host IPv6 specificato nella struttura dei componenti URL specificata nel parametro *lpUrlComponents* .

Per tutte le operazioni sui socket, WinINet usa l'ID ambito. Tuttavia, poiché l'ID ambito ha solo l'importanza dell'host locale, non viene inviato come parte delle intestazioni del protocollo HTTP nella richiesta. Ad esempio, la chiamata a [**InternetOpenUrl**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla) viene chiamata con l'URL seguente nel parametro *lpszURL* .

``` syntax
https://[fec0::2%251]:80/path.htm
```

La parte relativa all'ID ambito dell'URL viene rimossa da WinINet quando viene inviata la richiesta HTTP per questo URL. La richiesta contiene le intestazioni seguenti:

``` syntax
GET path.htm HTTP/1.1
Host: [fec0::2]
```

> [!Note]  
> WinINet non supporta le implementazioni del server. Inoltre, non deve essere utilizzato da un servizio. Per le implementazioni o i servizi del server, usare i [Servizi http di Microsoft Windows (WinHTTP)](/windows/desktop/WinHttp/winhttp-start-page).

 

 

 