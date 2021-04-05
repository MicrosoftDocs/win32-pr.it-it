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
# <a name="bluetooth-and-wsaaddresstostring"></a><span data-ttu-id="91eac-103">Bluetooth e WSAAddressToString</span><span class="sxs-lookup"><span data-stu-id="91eac-103">Bluetooth and WSAAddressToString</span></span>

<span data-ttu-id="91eac-104">La funzione [**WSAAddressToString**](/windows/desktop/api/winsock2/nf-winsock2-wsaaddresstostringa) Windows Sockets viene usata per convertire un indirizzo del dispositivo Bluetooth in una stringa, che a sua volta viene fornita alla funzione [**WSALookupServiceBegin**](/windows/desktop/api/winsock2/nf-winsock2-wsalookupservicebegina) tramite la struttura [**WSAQUERYSET**](/windows/desktop/api/winsock2/ns-winsock2-wsaquerysetw) durante il recupero delle informazioni sul servizio del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="91eac-104">The [**WSAAddressToString**](/windows/desktop/api/winsock2/nf-winsock2-wsaaddresstostringa) Windows Sockets function is used to convert a Bluetooth Device Address to a string, which is in turn provided to the [**WSALookupServiceBegin**](/windows/desktop/api/winsock2/nf-winsock2-wsalookupservicebegina) function via the [**WSAQUERYSET**](/windows/desktop/api/winsock2/ns-winsock2-wsaquerysetw) structure when retrieving device service information.</span></span>

<span data-ttu-id="91eac-105">Mentre un indirizzo del dispositivo Bluetooth rientra in un buffer di 20 caratteri, la funzione [**WSAAddressToString**](/windows/desktop/api/winsock2/nf-winsock2-wsaaddresstostringa) restituisce attualmente **WSAEFAULT** per gli indirizzi del dispositivo Bluetooth, a meno che il buffer e il valore *lpdwAddressStringLength* specificato non siano impostati su una lunghezza di caratteri pari a 40.</span><span class="sxs-lookup"><span data-stu-id="91eac-105">While a Bluetooth Device Address fits within a 20 character buffer, the [**WSAAddressToString**](/windows/desktop/api/winsock2/nf-winsock2-wsaaddresstostringa) function currently returns **WSAEFAULT** for Bluetooth Device Addresses unless the buffer and the specified *lpdwAddressStringLength* value are set to a character length of 40.</span></span>

> [!Note]  
> <span data-ttu-id="91eac-106">Quando **WSAEFAULT** viene restituito da [**WSAAddressToString**](/windows/desktop/api/winsock2/nf-winsock2-wsaaddresstostringa) come risultato di un buffer insufficiente, il parametro *lpdwAddressStringLength* non viene aggiornato con le dimensioni del buffer richieste per l'operazione.</span><span class="sxs-lookup"><span data-stu-id="91eac-106">When **WSAEFAULT** is returned by [**WSAAddressToString**](/windows/desktop/api/winsock2/nf-winsock2-wsaaddresstostringa) as the result of an insufficient buffer, the *lpdwAddressStringLength* parameter is not updated with the buffer size required for the operation.</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="91eac-107">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="91eac-107">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="91eac-108">**WSAAddressToString**</span><span class="sxs-lookup"><span data-stu-id="91eac-108">**WSAAddressToString**</span></span>](/windows/desktop/api/winsock2/nf-winsock2-wsaaddresstostringa)
</dt> <dt>

[<span data-ttu-id="91eac-109">Bluetooth e WSALookupServiceBegin</span><span class="sxs-lookup"><span data-stu-id="91eac-109">Bluetooth and WSALookupServiceBegin</span></span>](bluetooth-and-wsalookupservicebegin.md)
</dt> <dt>

[<span data-ttu-id="91eac-110">Bluetooth e WSAQUERYSET</span><span class="sxs-lookup"><span data-stu-id="91eac-110">Bluetooth and WSAQUERYSET</span></span>](bluetooth-and-wsaqueryset.md)
</dt> </dl>

 

 