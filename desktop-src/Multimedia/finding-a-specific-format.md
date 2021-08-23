---
title: Ricerca di un formato specifico
description: Ricerca di un formato specifico
ms.assetid: 0c892758-d409-4ed7-8f38-a24eee646b65
keywords:
- gestione compressione audio,ricerca di formati
- ACM (Audio Compression Manager),ricerca di formati
- Esempi di ACM, ricerca di formati
- ricerca di formati
- Funzione acmFormatEnum
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ecc291a6dff0c6b2befec6afd001a32735a54e95fd65a464378adb690a95019c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119691531"
---
# <a name="finding-a-specific-format"></a>Ricerca di un formato specifico

Un'applicazione potrebbe avere solo una specifica parziale per un formato quando è richiesta la specifica completa. Ad esempio, la specifica potrebbe prescrivere un formato ADPCM mono a 11 kHz a 4 bit, ma non i byte medi al secondo. L'applicazione può ottenere il formato completo senza l'intervento dell'utente usando la [**funzione acmFormatEnum**](/windows/desktop/api/Msacm/nf-msacm-acmformatenum) e specificando i flag nel *parametro fdwEnum.*

 

 




