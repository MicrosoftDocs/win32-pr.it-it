---
description: Delle sei modalità di mapping predefinite, una è dipendente dal dispositivo ( \_ testo mm) e i restanti cinque (mm \_ HIENGLISH, mm \_ LOENGLISH, MM \_ HIMETRIC, mm \_ LOMETRIC e mm \_ twip) sono indipendenti dal dispositivo.
ms.assetid: 722df020-edf2-4763-b58c-3e29fa7007db
title: Modalità di mapping predefinite
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f252f587e98a739306a84450a1d9669ed21873cf
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104978383"
---
# <a name="predefined-mapping-modes"></a>Modalità di mapping predefinite

Delle sei modalità di mapping predefinite, una è dipendente dal dispositivo ( \_ testo mm) e i restanti cinque (mm \_ HIENGLISH, mm \_ LOENGLISH, MM \_ HIMETRIC, mm \_ LOMETRIC e mm \_ twip) sono indipendenti dal dispositivo.

La modalità di mapping predefinita è il \_ testo mm. Un'unità logica equivale a un pixel. X positivo è a destra e y positivo è inattivo. Questa modalità è mappata direttamente al sistema di coordinate del dispositivo. Il mapping logico a fisico prevede solo un offset in x e y definito dalle origini della finestra controllata dall'applicazione e dal viewport. Gli extent del viewport e della finestra sono tutti impostati su 1, creando un mapping uno-a-uno.

Le applicazioni che visualizzano forme geometriche (cerchi, quadrati, poligoni e così via) usano una delle modalità di mapping indipendenti dal dispositivo. Se, ad esempio, si scrive un'applicazione per fornire funzionalità di creazione di grafici per un programma di foglio di calcolo e si desidera garantire che il diametro di ogni grafico a torta sia di 2 centimetri, utilizzare la \_ modalità di mapping mm LOENGLISH e chiamare le funzioni appropriate per creare e riempire il grafico. \_Se si specifica mm LOENGLISH, il diametro del grafico sarà coerente in qualsiasi visualizzazione o stampante. Se \_ si usa il testo mm anziché mm \_ LOENGLISH, un grafico visualizzato circolare su una visualizzazione VGA sembrerebbe ellittico in una visualizzazione EGA e apparirebbe molto piccolo in una stampante laser con 300 dpi (punti per pollice).

 

 



