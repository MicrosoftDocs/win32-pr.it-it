---
description: Per le costanti di dati scalari estendibili, un fornitore del provider di servizi può definire nuovi valori in un intervallo specificato.
ms.assetid: 62280b71-9bec-4a9d-abd2-d3e1c2cee43f
title: Costanti di dati scalari
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c3187d2064501727614dfcbf0b8e11c136fea13e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103760799"
---
# <a name="scalar-data-constants"></a>Costanti di dati scalari

Per le costanti di dati scalari estendibili, un fornitore del provider di servizi può definire nuovi valori in un intervallo specificato. Poiché la maggior parte delle costanti di dati è **DWORD** s, l'intervallo 0x00000000 tramite 0x7FFFFFFF è in genere riservato per le estensioni future comuni, mentre 0X80000000 tramite 0xFFFFFFFF è disponibile per le estensioni specifiche del fornitore. Si presuppone che un fornitore definisca i valori che sono estensioni naturali dei tipi di databases definiti dall'API.

 

 



