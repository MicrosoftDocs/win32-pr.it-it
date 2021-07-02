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
# <a name="winhttp-constants"></a><span data-ttu-id="f86cb-103">Costanti WinHTTP</span><span class="sxs-lookup"><span data-stu-id="f86cb-103">WinHTTP Constants</span></span>

<span data-ttu-id="f86cb-104">WinHTTP usa le costanti seguenti:</span><span class="sxs-lookup"><span data-stu-id="f86cb-104">WinHTTP uses the following constants:</span></span>

<dl>

<dt>

[<span data-ttu-id="f86cb-105">**messaggi di errore**</span><span class="sxs-lookup"><span data-stu-id="f86cb-105">**Error Messages**</span></span>](error-messages.md)
</dt> <dd>

<span data-ttu-id="f86cb-106">Messaggi di errore specifici delle funzioni WinHTTP.</span><span class="sxs-lookup"><span data-stu-id="f86cb-106">Error messages specific to the WinHTTP functions.</span></span> <span data-ttu-id="f86cb-107">Queste funzioni restituiscono anche Windows di errore quando appropriato.</span><span class="sxs-lookup"><span data-stu-id="f86cb-107">These functions also return Windows error messages where appropriate.</span></span> <span data-ttu-id="f86cb-108">Il valore che corrisponde a ogni costante è il valore della costante per le funzioni API (Application Programming Interface) e i 16 bit inferiori del numero di errore per [**l'oggetto WinHttpRequest.**](winhttprequest.md)</span><span class="sxs-lookup"><span data-stu-id="f86cb-108">The value that corresponds to each constant is the value of the constant for the application programming interface (API) functions and the lower 16 bits of the error number for the [**WinHttpRequest**](winhttprequest.md) object.</span></span>

</dd> <dt>

[<span data-ttu-id="f86cb-109">**Codici di stato HTTP**</span><span class="sxs-lookup"><span data-stu-id="f86cb-109">**HTTP Status Codes**</span></span>](http-status-codes.md)
</dt> <dd>

<span data-ttu-id="f86cb-110">Costanti e valori corrispondenti che indicano i codici di stato HTTP restituiti dai server su Internet.</span><span class="sxs-lookup"><span data-stu-id="f86cb-110">Constants and corresponding values that indicate HTTP status codes returned by servers on the Internet.</span></span>

</dd> <dt>

[<span data-ttu-id="f86cb-111">**Flag di opzione**</span><span class="sxs-lookup"><span data-stu-id="f86cb-111">**Option Flags**</span></span>](option-flags.md)
</dt> <dd>

<span data-ttu-id="f86cb-112">Flag di opzione supportati [**da WinHttpQueryOption**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpqueryoption) e [**WinHttpSetOption.**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsetoption)</span><span class="sxs-lookup"><span data-stu-id="f86cb-112">Option flags supported by [**WinHttpQueryOption**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpqueryoption) and [**WinHttpSetOption**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsetoption).</span></span> <span data-ttu-id="f86cb-113">Tutti i flag di opzione validi hanno un valore maggiore o uguale a WINHTTP FIRST OPTION e minore o \_ \_ uguale a WINHTTP LAST \_ \_ OPTION.</span><span class="sxs-lookup"><span data-stu-id="f86cb-113">All valid option flags have a value greater than or equal to WINHTTP\_FIRST\_OPTION and less than or equal to WINHTTP\_LAST\_OPTION.</span></span>

</dd> <dt>

[<span data-ttu-id="f86cb-114">**PORTA \_ INTERNET**</span><span class="sxs-lookup"><span data-stu-id="f86cb-114">**INTERNET\_PORT**</span></span>](internet-port.md)
</dt> <dd>

<span data-ttu-id="f86cb-115">Valore WORD che indica la porta.</span><span class="sxs-lookup"><span data-stu-id="f86cb-115">A WORD value indicating the port.</span></span>

</dd> <dt>

[<span data-ttu-id="f86cb-116">**SCHEMA \_ INTERNET**</span><span class="sxs-lookup"><span data-stu-id="f86cb-116">**INTERNET\_SCHEME**</span></span>](internet-scheme.md)
</dt> <dd>

<span data-ttu-id="f86cb-117">Schemi Internet supportati da WinHTTP.</span><span class="sxs-lookup"><span data-stu-id="f86cb-117">Internet schemes supported by WinHTTP.</span></span>

</dd>

<dt>

[<span data-ttu-id="f86cb-118">**Flag di informazioni sulle query**</span><span class="sxs-lookup"><span data-stu-id="f86cb-118">**Query Info Flags**</span></span>](query-info-flags.md)
</dt>
<dd>

<span data-ttu-id="f86cb-119">Attributi e modificatori usati da [**WinHttpQueryHeaders.**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpqueryheaders)</span><span class="sxs-lookup"><span data-stu-id="f86cb-119">Attributes and modifiers used by [**WinHttpQueryHeaders**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpqueryheaders).</span></span>
</dd>

<dt>

<span data-ttu-id="f86cb-120">**WINHTTP_EXTENDED_HEADER_FLAG_UNICODE**</span><span class="sxs-lookup"><span data-stu-id="f86cb-120">**WINHTTP_EXTENDED_HEADER_FLAG_UNICODE**</span></span>
</dt>
<dd>

<span data-ttu-id="f86cb-121">Ha un valore di 0x00000001.</span><span class="sxs-lookup"><span data-stu-id="f86cb-121">Has a value of 0x00000001.</span></span> <span data-ttu-id="f86cb-122">Indica a [WinHttpAddRequestHeadersEx](/windows/win32/api/winhttp/nf-winhttp-winhttpaddrequestheadersex) che le stringhe passate sono stringhe Unicode.</span><span class="sxs-lookup"><span data-stu-id="f86cb-122">Indicates to [WinHttpAddRequestHeadersEx](/windows/win32/api/winhttp/nf-winhttp-winhttpaddrequestheadersex) that the strings passed in are Unicode strings.</span></span>
</dd>

<dt>

<span data-ttu-id="f86cb-123">**WINHTTP_READ_DATA_EX_FLAG_FILL_BUFFER**</span><span class="sxs-lookup"><span data-stu-id="f86cb-123">**WINHTTP_READ_DATA_EX_FLAG_FILL_BUFFER**</span></span>
</dt>
<dd>

<span data-ttu-id="f86cb-124">Ha un valore pari a 0x0000000000000001ull.</span><span class="sxs-lookup"><span data-stu-id="f86cb-124">Has a value of 0x0000000000000001ull.</span></span> <span data-ttu-id="f86cb-125">Indica a [WinHttpReadDataEx](/windows/win32/api/winhttp/nf-winhttp-winhttpreaddataex) di non completare la chiamata fino a quando il buffer di dati specificato non è stato riempito o la risposta non è stata completata.</span><span class="sxs-lookup"><span data-stu-id="f86cb-125">Instructs [WinHttpReadDataEx](/windows/win32/api/winhttp/nf-winhttp-winhttpreaddataex) not to complete the call until the provided data buffer has been filled, or the response is complete.</span></span> <span data-ttu-id="f86cb-126">Il passaggio di questo flag rende il **comportamento di WinHttpReadDataEx** equivalente a quello di [WinHttpReadData.](/windows/win32/api/winhttp/nf-winhttp-winhttpreaddata)</span><span class="sxs-lookup"><span data-stu-id="f86cb-126">Passing this flag makes the behavior of **WinHttpReadDataEx** equivalent to that of [WinHttpReadData](/windows/win32/api/winhttp/nf-winhttp-winhttpreaddata).</span></span>
</dd>

</dl>
