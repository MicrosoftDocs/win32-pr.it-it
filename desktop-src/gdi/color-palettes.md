---
description: Una tavolozza dei colori è una matrice che contiene valori di colore che identificano i colori che possono essere attualmente visualizzati o disegnati nel dispositivo di output.
ms.assetid: 260c5924-d082-4ed2-a8ed-b8a3ad1ca1a9
title: Tavolozze dei colori (Windows GDI)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 81079ac94b40de98bc1c53098a8b9d1654f90d0d855397ac38d11311e9741e9e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118761958"
---
# <a name="color-palettes-windows-gdi"></a>Tavolozze dei colori (Windows GDI)

Una tavolozza dei colori è una matrice che contiene valori di colore che identificano i colori che possono essere attualmente visualizzati o disegnati nel dispositivo di output. Le tavolozze dei colori vengono usate da dispositivi in grado di generare molti colori, ma che possono visualizzare o disegnare solo un subset di questi colori in un determinato momento. Per tali dispositivi, il sistema mantiene una tavolozza *di* sistema per tenere traccia e gestire i colori correnti del dispositivo. Le applicazioni non hanno accesso diretto alla tavolozza di sistema. Al contrario, il sistema associa una tavolozza predefinita a ogni contesto di dispositivo. Le applicazioni possono usare i colori nella tavolozza  predefinita o definire i propri colori creando tavolozze logiche e associandole a singoli contesti di dispositivo.

Un'applicazione può determinare se un dispositivo supporta le tavolozze dei colori controllando la presenza del bit RC PALETTE nel valore RASTERCAPS restituito dalla \_ [**funzione GetDeviceCaps.**](/windows/desktop/api/Wingdi/nf-wingdi-getdevicecaps)

 

 



