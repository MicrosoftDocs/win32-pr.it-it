---
title: Bluetooth e WSAAddressToString
description: La funzione WSAAddressToString Windows Sockets viene usata per convertire un indirizzo del dispositivo Bluetooth in una stringa, che a sua volta viene fornita alla funzione WSALookupServiceBegin tramite la struttura WSAQUERYSET durante il recupero delle informazioni sul servizio del dispositivo.
ms.assetid: 3489d29a-2b64-4051-b579-57878efc0c73
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a78e8a9ae3ea6a0f853619a3f3610a64204ad3c3
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104046824"
---
# <a name="bluetooth-and-wsaaddresstostring"></a>Bluetooth e WSAAddressToString

La funzione [**WSAAddressToString**](/windows/desktop/api/winsock2/nf-winsock2-wsaaddresstostringa) Windows Sockets viene usata per convertire un indirizzo del dispositivo Bluetooth in una stringa, che a sua volta viene fornita alla funzione [**WSALookupServiceBegin**](/windows/desktop/api/winsock2/nf-winsock2-wsalookupservicebegina) tramite la struttura [**WSAQUERYSET**](/windows/desktop/api/winsock2/ns-winsock2-wsaquerysetw) durante il recupero delle informazioni sul servizio del dispositivo.

Mentre un indirizzo del dispositivo Bluetooth rientra in un buffer di 20 caratteri, la funzione [**WSAAddressToString**](/windows/desktop/api/winsock2/nf-winsock2-wsaaddresstostringa) restituisce attualmente **WSAEFAULT** per gli indirizzi del dispositivo Bluetooth, a meno che il buffer e il valore *lpdwAddressStringLength* specificato non siano impostati su una lunghezza di caratteri pari a 40.

> [!Note]  
> Quando **WSAEFAULT** viene restituito da [**WSAAddressToString**](/windows/desktop/api/winsock2/nf-winsock2-wsaaddresstostringa) come risultato di un buffer insufficiente, il parametro *lpdwAddressStringLength* non viene aggiornato con le dimensioni del buffer richieste per l'operazione.

 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**WSAAddressToString**](/windows/desktop/api/winsock2/nf-winsock2-wsaaddresstostringa)
</dt> <dt>

[Bluetooth e WSALookupServiceBegin](bluetooth-and-wsalookupservicebegin.md)
</dt> <dt>

[Bluetooth e WSAQUERYSET](bluetooth-and-wsaqueryset.md)
</dt> </dl>

 

 