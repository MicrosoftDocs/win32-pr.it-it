---
title: Hit testing tocco
description: Negli argomenti di questa sezione viene fornita una panoramica del supporto per l'hit testing di tocco in Windows 8.
ms.assetid: bdd7630c-b2d8-4080-a149-efec018f697d
keywords:
- interazione dell'utente
- input
- indicatore di misura
- tocco
ms.topic: article
ms.date: 02/07/2020
ms.openlocfilehash: 8cf6d28badb47a176a6feccf166344003faf1de8
ms.sourcegitcommit: 9e389b8e39616dcef8f7ff4bc53d945179401478
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/07/2020
ms.locfileid: "103857969"
---
# <a name="touch-hit-testing"></a>Hit testing tocco

## <a name="purpose"></a>Scopo

Negli argomenti di questa sezione viene fornita una panoramica del supporto per l'hit testing di tocco in Windows. L'hit testing tocco consente di identificare una destinazione di input a seconda che l'area di contenuto di un elemento dell'interfaccia utente rientri nell'area di contatto o includa il punto di contatto.

L'hit testing tocco usa la geometria di contatto complessa per l'intera area di tocco anziché una singola coordinata x-y interpolata. L'uso dell'intera geometria dei contatti migliora notevolmente la precisione e l'accuratezza quando si identifica la destinazione più probabile dell'input tocco.

## <a name="in-this-section"></a>Contenuto della sezione

| Argomento | Descrizione |
| --- | --- |
| [Riferimento all'hit testing tocco](touchhittest-reference.md)<br/> | Negli argomenti di questa sezione vengono fornite le specifiche di riferimento per gli [hit test di tocco](touch-hit-testing-portal.md).<br/> |

## <a name="developer-audience"></a>Sviluppatori

Le API di hit testing touch sono progettate per gli sviluppatori che compilano Framework dell'interfaccia utente che forniscono un'esperienza utente ottimizzata per il tocco per le applicazioni desktop.

## <a name="related-topics"></a>Argomenti correlati

[Interazione dell'utente](../user-interaction.md)
