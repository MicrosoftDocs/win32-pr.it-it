---
description: Per le costanti dati scalari estendibili, un fornitore di provider di servizi può definire nuovi valori in un intervallo specificato.
ms.assetid: 62280b71-9bec-4a9d-abd2-d3e1c2cee43f
title: Costanti per dati scalari
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 815288ca4a22da741e5b98257ae50732f818b466404a95712ee74756785fd699
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119773311"
---
# <a name="scalar-data-constants"></a>Costanti per dati scalari

Per le costanti dati scalari estendibili, un fornitore di provider di servizi può definire nuovi valori in un intervallo specificato. Poiché la maggior parte delle costanti di dati sono **DWORD,** l'intervallo da 0x00000000 a 0x7FFFFFFF è in genere riservato per le estensioni future comuni, mentre 0x80000000 tramite 0xFFFFFFFF è disponibile per estensioni specifiche del fornitore. Si presuppone che un fornitore definirebbe valori che sono estensioni naturali dei tipi di dati definiti dall'API.

 

 



