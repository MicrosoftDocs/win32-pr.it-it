---
description: Le sequenze di escape della stampante fornite da dispositivi a 16 bit Windows'accesso alle funzionalità speciali del dispositivo.
ms.assetid: 4bdd1d47-8cf4-4088-aec8-88193e71a828
title: Escape della stampante
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5dd8bc842e60ca0019fc523b27a4657e66a623cda4802bfdb489213b694fd432
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119711561"
---
# <a name="printer-escapes"></a>Escape della stampante

Le sequenze di escape della stampante fornite da dispositivi a 16 bit Windows'accesso alle funzionalità speciali del dispositivo. La maggior parte di questi caratteri di escape è obsoleta, ma ne vengono forniti alcuni per semplificare la portabilità di applicazioni Windows a 16 bit. GDI supporta un set completo di funzioni di percorso che le applicazioni possono usare al posto delle sequenze di escape per disegnare tracciati in qualsiasi dispositivo. Per un elenco di funzioni che sostituiscono alcuni caratteri di escape, vedere la [**funzione Escape.**](/windows/desktop/api/Wingdi/nf-wingdi-escape)

Delle 64 sequenze di escape della stampante originali, è possibile usare solo **QUERYESCSUPPORT** **e PASSTHROUGH.**

È disponibile anche una funzione di escape estesa denominata [**ExtEscape.**](/windows/desktop/api/Wingdi/nf-wingdi-extescape) Questa funzione consente alle applicazioni di accedere alle funzionalità di un determinato dispositivo non direttamente disponibili tramite GDI.

 

 



