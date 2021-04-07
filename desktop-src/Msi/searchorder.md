---
description: L'impostazione di questo criterio di sistema per utente specifica l'ordine in cui il programma di installazione esegue la ricerca di tre tipi di origini.
ms.assetid: c16a5cbb-d530-4932-944b-af68d0a4018c
title: SearchOrder
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c8f486ee58eebd1a1bd1174f18e413785e5e3129
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103885690"
---
# <a name="searchorder"></a>SearchOrder

L'impostazione di questo [criterio di sistema](system-policy.md) per utente specifica l'ordine in cui il programma di installazione esegue la ricerca di tre tipi di origini. I tipi di origini sono:

"n"-rete

"m"-supporto (CD-ROM o DVD)

"u"-Uniform Resource Locator (URL)

Ad esempio, per cercare prima origini di rete, origini multimediali secondo e origini URL, impostare questo criterio su un valore "NMU". Per omettere la ricerca di un particolare tipo di origine, lasciare la lettera corrispondente dal valore.

Se SearchOrder non è impostato, l'ordine di ricerca predefinito è rete, supporto e URL.

## <a name="registry-key"></a>Chiave del Registro di sistema

**HKEY \_ Criteri \_ software utente correnti** \\  \\  \\ **Microsoft** \\ **Windows** \\ **Installer**

## <a name="data-type"></a>Tipo di dati

**REG \_ SZ**

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Resilienza di origine](source-resiliency.md)
</dt> </dl>

 

 



