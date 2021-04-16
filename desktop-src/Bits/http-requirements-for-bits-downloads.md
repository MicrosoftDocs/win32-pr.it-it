---
title: Requisiti HTTP per i download BITS
description: BITS supporta il caricamento e il download HTTP e HTTPS e richiede che il server supporti il protocollo HTTP/1.1.
ms.assetid: 35af422b-62e4-41fd-8890-579ccf016c83
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d130ab3e527b62f34f48e6df4695bf75f63dcd2d
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104470966"
---
# <a name="http-requirements-for-bits-downloads"></a><span data-ttu-id="529a9-103">Requisiti HTTP per i download BITS</span><span class="sxs-lookup"><span data-stu-id="529a9-103">HTTP Requirements for BITS Downloads</span></span>

<span data-ttu-id="529a9-104">BITS supporta il caricamento e il download HTTP e HTTPS e richiede che il server supporti il protocollo HTTP/1.1.</span><span class="sxs-lookup"><span data-stu-id="529a9-104">BITS supports HTTP and HTTPS downloads and uploads and requires that the server supports the HTTP/1.1 protocol.</span></span> <span data-ttu-id="529a9-105">Per i download, il metodo **Head** del server http deve restituire le dimensioni del file e il metodo **Get** deve supportare le intestazioni Content-Range e Content-Length.</span><span class="sxs-lookup"><span data-stu-id="529a9-105">For downloads, the HTTP server's **Head** method must return the file size and its **Get** method must support the Content-Range and Content-Length headers.</span></span> <span data-ttu-id="529a9-106">Di conseguenza, BITS trasferisce solo il contenuto del file statico e genera un errore se si tenta di trasferire il contenuto dinamico, a meno che lo script ASP, ISAPI o CGI non supporti le intestazioni Content-Range e Content-Length.</span><span class="sxs-lookup"><span data-stu-id="529a9-106">As a result, BITS only transfers static file content and generates an error if you try to transfer dynamic content, unless the ASP, ISAPI, or CGI script supports the Content-Range and Content-Length headers.</span></span>

<span data-ttu-id="529a9-107">BITS può usare un server HTTP/1.0 purché soddisfi i requisiti del metodo **Head** e **Get** .</span><span class="sxs-lookup"><span data-stu-id="529a9-107">BITS can use an HTTP/1.0 server as long as it meets the **Head** and **Get** method requirements.</span></span>

<span data-ttu-id="529a9-108">Per supportare il download degli intervalli di un file, il server deve supportare i requisiti seguenti:</span><span class="sxs-lookup"><span data-stu-id="529a9-108">To support downloading ranges of a file, the server must support the following requirements:</span></span>

-   <span data-ttu-id="529a9-109">Consente alle intestazioni MIME di includere le intestazioni Content-Range e Content-Type standard, oltre a un massimo di 180 byte di altre intestazioni.</span><span class="sxs-lookup"><span data-stu-id="529a9-109">Allow MIME headers to include the standard Content-Range and Content-Type headers, plus a maximum of 180 bytes of other headers.</span></span>
-   <span data-ttu-id="529a9-110">Consente un massimo di due CR/LFs tra le intestazioni HTTP e la prima stringa limite.</span><span class="sxs-lookup"><span data-stu-id="529a9-110">Allow a maximum of two CR/LFs between the HTTP headers and the first boundary string.</span></span>

 

 




