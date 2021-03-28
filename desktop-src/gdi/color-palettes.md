---
description: Una tavolozza di colori è una matrice che contiene i valori dei colori che identificano i colori che possono essere visualizzati o disegnati sul dispositivo di output.
ms.assetid: 260c5924-d082-4ed2-a8ed-b8a3ad1ca1a9
title: Tavolozze dei colori (Windows GDI)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: db6da2aab08d2b482eb678e8541ec166156b78f0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104130811"
---
# <a name="color-palettes-windows-gdi"></a>Tavolozze dei colori (Windows GDI)

Una tavolozza di colori è una matrice che contiene i valori dei colori che identificano i colori che possono essere visualizzati o disegnati sul dispositivo di output. Le tavolozze dei colori vengono usate dai dispositivi in grado di generare molti colori ma che possono solo visualizzare o creare un subset di questi in un determinato momento. Per tali dispositivi, il sistema gestisce una *tavolozza di sistema* per tenere traccia e gestire i colori correnti del dispositivo. Le applicazioni non hanno accesso diretto alla tavolozza di sistema. Al contrario, il sistema associa una tavolozza predefinita a ogni contesto di dispositivo. Le applicazioni possono utilizzare i colori della tavolozza predefinita o definire i propri colori creando *tavolozze logiche* e associando loro i singoli contesti di dispositivo.

Un'applicazione può determinare se un dispositivo supporta le tavolozze dei colori controllando il \_ bit della tavolozza RC nel valore RasterCaps restituito dalla funzione [**GetDeviceCaps**](/windows/desktop/api/Wingdi/nf-wingdi-getdevicecaps) .

 

 



