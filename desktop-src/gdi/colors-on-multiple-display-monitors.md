---
description: Ogni monitoraggio può avere una profondità di colore specifica.
ms.assetid: 8d1ba8d2-b43d-498d-be5a-100fe9fc0f61
title: Colori su più monitor di visualizzazione
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 50410631cf0ea3ac0a1b9967f1116809be0a4851
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103967064"
---
# <a name="colors-on-multiple-display-monitors"></a>Colori su più monitor di visualizzazione

Ogni monitoraggio può avere una profondità di colore specifica. Il sistema regola automaticamente i colori durante lo spostamento di Windows tra i monitoraggi con profondità dei colori differenti. In generale, questo produce risultati soddisfacenti. Tuttavia, questo non è sempre ottimale. Per sfruttare i vantaggi delle funzionalità relative ai colori dei diversi monitoraggi, vedere la sezione [disegno su più monitor di visualizzazione](painting-on-multiple-display-monitors.md) riportata di seguito.

Per determinare se tutti i monitoraggi hanno lo stesso formato di colore, chiamare [**GetSystemMetrics**](/windows/win32/api/winuser/nf-winuser-getsystemmetrics) con SM \_ SAMEDISPLAYFORMAT.

Se il monitoraggio primario è pallettizzati, [**SelectPalette**](/windows/desktop/api/Wingdi/nf-wingdi-selectpalette) e [**RealizePalette**](/windows/desktop/api/Wingdi/nf-wingdi-realizepalette) funzionano come prima, ma in tutti i monitoraggi. Inoltre, le tavolozze di tutti i dispositivi pallettizzati sono sincronizzate. Se il monitoraggio primario non è pallettizzati, **SelectPalette** e **RealizePalette** selezioneranno la tavolozza in background e i dispositivi pallettizzati non verranno sincronizzati.

 

 
