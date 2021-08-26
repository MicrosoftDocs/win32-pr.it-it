---
description: L'impostazione di questi criteri di sistema per utente specifica l'ordine in cui il programma di installazione esegue la ricerca in tre tipi di origini.
ms.assetid: c16a5cbb-d530-4932-944b-af68d0a4018c
title: SearchOrder
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cfaab6ff8d4b40b966b5ab1785ddd5fd473316732833fc32be7102acaa7c4877
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120041041"
---
# <a name="searchorder"></a>SearchOrder

L'impostazione di questi criteri di [sistema per utente](system-policy.md) specifica l'ordine in cui il programma di installazione esegue la ricerca in tre tipi di origini. I tipi di origini sono:

"n": rete

"m": supporto (CD-ROM o DVD)

"u": Uniform Resource Locator (URL)

Ad esempio, per cercare prima le origini di rete, le origini multimediali per seconda e le origini URL, impostare questi criteri sul valore "nmu". Per omettere la ricerca di un particolare tipo di origine, omettere la lettera corrispondente dal valore.

Se SearchOrder non è impostato, l'ordine di ricerca predefinito è network, media e quindi URL.

## <a name="registry-key"></a>Chiave del Registro di sistema

**HKEY \_ CURRENT \_ USER** \\ **Software** \\ **Policies** \\ **Microsoft** \\ **Windows** \\ **Installer**

## <a name="data-type"></a>Tipo di dati

**REG \_ SZ**

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Resilienza di origine](source-resiliency.md)
</dt> </dl>

 

 



