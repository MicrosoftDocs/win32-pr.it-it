---
title: Requisiti HTTP per i download BITS
description: BITS supporta i download e i caricamenti HTTP e HTTPS e richiede che il server supporti il protocollo HTTP/1.1.
ms.assetid: 35af422b-62e4-41fd-8890-579ccf016c83
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cd9bd997bb5ef7f2125cfe7c3dc6850c0f44e81a8c3138f7f130952e31202a1c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118010876"
---
# <a name="http-requirements-for-bits-downloads"></a>Requisiti HTTP per i download BITS

BITS supporta i download e i caricamenti HTTP e HTTPS e richiede che il server supporti il protocollo HTTP/1.1. Per i download, il metodo **Head** del server HTTP deve restituire le dimensioni del file e il metodo **Get** deve supportare le intestazioni Content-Range e Content-Length. Di conseguenza, BITS trasferisce solo il contenuto dei file statici e genera un errore se si tenta di trasferire il contenuto dinamico, a meno che lo script ASP, ISAPI o CGI non supporti le intestazioni Content-Range e Content-Length.

BITS può usare un server HTTP/1.0 purché soddisfi i requisiti dei metodi **Head** e **Get.**

Per supportare il download di intervalli di un file, il server deve supportare i requisiti seguenti:

-   Consente alle intestazioni MIME di includere le intestazioni Standard Content-Range e Content-Type, oltre a un massimo di 180 byte di altre intestazioni.
-   Consentire un massimo di due CR/LFs tra le intestazioni HTTP e la prima stringa limite.

 

 




