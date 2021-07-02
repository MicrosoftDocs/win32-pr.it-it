---
description: Questo argomento identifica le costanti utilizzate da WinHTTP.
ms.assetid: 460f1463-57a8-47eb-9957-17976757bd7f
title: Costanti WinHTTP
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7e37b0e4de7aa3df5e155933bea2be25386c1637
ms.sourcegitcommit: 8e3d8594fa073a9c43eb5dcc7babea03ea30f10f
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 07/01/2021
ms.locfileid: "113174999"
---
# <a name="winhttp-constants"></a>Costanti WinHTTP

WinHTTP usa le costanti seguenti:

<dl>

<dt>

[**messaggi di errore**](error-messages.md)
</dt> <dd>

Messaggi di errore specifici delle funzioni WinHTTP. Queste funzioni restituiscono anche Windows di errore quando appropriato. Il valore che corrisponde a ogni costante è il valore della costante per le funzioni API (Application Programming Interface) e i 16 bit inferiori del numero di errore per [**l'oggetto WinHttpRequest.**](winhttprequest.md)

</dd> <dt>

[**Codici di stato HTTP**](http-status-codes.md)
</dt> <dd>

Costanti e valori corrispondenti che indicano i codici di stato HTTP restituiti dai server su Internet.

</dd> <dt>

[**Flag di opzione**](option-flags.md)
</dt> <dd>

Flag di opzione supportati [**da WinHttpQueryOption**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpqueryoption) e [**WinHttpSetOption.**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsetoption) Tutti i flag di opzione validi hanno un valore maggiore o uguale a WINHTTP FIRST OPTION e minore o \_ \_ uguale a WINHTTP LAST \_ \_ OPTION.

</dd> <dt>

[**PORTA \_ INTERNET**](internet-port.md)
</dt> <dd>

Valore WORD che indica la porta.

</dd> <dt>

[**SCHEMA \_ INTERNET**](internet-scheme.md)
</dt> <dd>

Schemi Internet supportati da WinHTTP.

</dd>

<dt>

[**Flag di informazioni sulle query**](query-info-flags.md)
</dt>
<dd>

Attributi e modificatori usati da [**WinHttpQueryHeaders.**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpqueryheaders)
</dd>

<dt>

**WINHTTP_EXTENDED_HEADER_FLAG_UNICODE**
</dt>
<dd>

Ha un valore di 0x00000001. Indica a [WinHttpAddRequestHeadersEx](/windows/win32/api/winhttp/nf-winhttp-winhttpaddrequestheadersex) che le stringhe passate sono stringhe Unicode.
</dd>

<dt>

**WINHTTP_READ_DATA_EX_FLAG_FILL_BUFFER**
</dt>
<dd>

Ha un valore pari a 0x0000000000000001ull. Indica a [WinHttpReadDataEx](/windows/win32/api/winhttp/nf-winhttp-winhttpreaddataex) di non completare la chiamata fino a quando il buffer di dati specificato non è stato riempito o la risposta non è stata completata. Il passaggio di questo flag rende il **comportamento di WinHttpReadDataEx** equivalente a quello di [WinHttpReadData.](/windows/win32/api/winhttp/nf-winhttp-winhttpreaddata)
</dd>

</dl>
