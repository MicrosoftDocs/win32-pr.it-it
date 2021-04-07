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
# <a name="scalar-data-constants"></a><span data-ttu-id="49836-103">Costanti di dati scalari</span><span class="sxs-lookup"><span data-stu-id="49836-103">Scalar Data Constants</span></span>

<span data-ttu-id="49836-104">Per le costanti di dati scalari estendibili, un fornitore del provider di servizi può definire nuovi valori in un intervallo specificato.</span><span class="sxs-lookup"><span data-stu-id="49836-104">For extensible scalar data constants, a service-provider vendor can define new values in a specified range.</span></span> <span data-ttu-id="49836-105">Poiché la maggior parte delle costanti di dati è **DWORD** s, l'intervallo 0x00000000 tramite 0x7FFFFFFF è in genere riservato per le estensioni future comuni, mentre 0X80000000 tramite 0xFFFFFFFF è disponibile per le estensioni specifiche del fornitore.</span><span class="sxs-lookup"><span data-stu-id="49836-105">Because most data constants are **DWORD** s, the range 0x00000000 through 0x7FFFFFFF is typically reserved for common future extensions, while 0x80000000 through 0xFFFFFFFF is available for vendor-specific extensions.</span></span> <span data-ttu-id="49836-106">Si presuppone che un fornitore definisca i valori che sono estensioni naturali dei tipi di databases definiti dall'API.</span><span class="sxs-lookup"><span data-stu-id="49836-106">The assumption is that a vendor would define values that are natural extensions of the datatypes defined by the API.</span></span>

 

 



