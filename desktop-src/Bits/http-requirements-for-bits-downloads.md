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
# <a name="http-requirements-for-bits-downloads"></a>Requisiti HTTP per i download BITS

BITS supporta il caricamento e il download HTTP e HTTPS e richiede che il server supporti il protocollo HTTP/1.1. Per i download, il metodo **Head** del server http deve restituire le dimensioni del file e il metodo **Get** deve supportare le intestazioni Content-Range e Content-Length. Di conseguenza, BITS trasferisce solo il contenuto del file statico e genera un errore se si tenta di trasferire il contenuto dinamico, a meno che lo script ASP, ISAPI o CGI non supporti le intestazioni Content-Range e Content-Length.

BITS può usare un server HTTP/1.0 purché soddisfi i requisiti del metodo **Head** e **Get** .

Per supportare il download degli intervalli di un file, il server deve supportare i requisiti seguenti:

-   Consente alle intestazioni MIME di includere le intestazioni Content-Range e Content-Type standard, oltre a un massimo di 180 byte di altre intestazioni.
-   Consente un massimo di due CR/LFs tra le intestazioni HTTP e la prima stringa limite.

 

 




