---
title: Linee di porting
description: Il porting di codice IRIS GL che disegna linee è piuttosto semplice, anche se è opportuno notare le differenze nel modo in cui OpenGL stipples. La tabella seguente elenca le funzioni di IRIS GL per le linee di disegno e le relative funzioni OpenGL equivalenti.
ms.assetid: de5fd544-5a64-44b5-8976-b96867e4006d
keywords:
- Porting di IRIS GL, righe
- porting da IRIS GL, righe
- porting in OpenGL da IRIS GL, righe
- Porting OpenGL da IRIS GL, righe
- disegno di funzioni, righe
- lines
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8c9c97593d0230d6830cf3d3ce8fa2c13466e21e
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104221821"
---
# <a name="porting-lines"></a>Linee di porting

Il porting di codice IRIS GL che disegna linee è piuttosto semplice, anche se è opportuno notare le differenze nel modo in cui OpenGL stipples. La tabella seguente elenca le funzioni di IRIS GL per le linee di disegno e le relative funzioni OpenGL equivalenti.



| Funzione IRIS GL                               | OpenGL (funzione)                                                                                         | Significato                                                                                                                                      |
|------------------------------------------------|---------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| **bgnclosedline**,**endclosedline**<br/> | [**glBegin**](glbegin.md) ( \_ ciclo linea GL \_ )[**glEnd**](glend.md)<br/>                          | Disegna una linea chiusa.                                                                                                                         |
| **bgnline**                                    | [**glBegin**](glbegin.md) ( \_ striscia di riga GL \_ )                                                          | Disegna segmenti di linea.                                                                                                                         |
| **LineWidth**                                  | [**glLineWidth**](gllinewidth.md)                                                                      | Imposta la lunghezza riga.                                                                                                                             |
| **getlwidth**                                  | [**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) ( \_ lunghezza riga GL \_ )            | Restituisce la lunghezza della riga corrente.                                                                                                                  |
| **deflinestyle**,**setlinestyle**<br/>   | [**glLineStipple**](gllinestipple.md)                                                                  | Specifica un modello di stipple di linea.                                                                                                            |
| **lsrepeat**                                   | argomento factor di **glLineStipple**                                                                    | Imposta un fattore di ripetizione per lo stile di linea.                                                                                                     |
| **getlstyle**                                  | [**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) ( \_ modello di \_ stipple linea GL \_ ) | Restituisce il pattern stipple della riga.                                                                                                                |
| **getlsrepeat**                                | [**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) ( \_ riga GL \_ stipple \_ ripetizione)  | Restituisce il fattore di ripetizione.                                                                                                                       |
| **linesmooth**, **a linee smussate**                 | [**glEnable**](glenable.md) ( \_ linea GL \_ smussata)                                                       | Attiva l'anti-aliasing della riga. per ulteriori informazioni sull'anti-aliasing, vedere [porting anti-aliasing Functions](porting-antialiasing-functions.md). |



 

OpenGL non usa le tabelle per la riga stipples; mantiene solo un modello line-stipple. È possibile usare [**glPushAttrib**](glpushattrib.md) e [**glPopAttrib**](glpopattrib.md) per passare da un modello di stipple all'altro.

Le funzioni di stile linea IRIS GL precedenti (ad esempio, **Disegna**, **lsbackup**, **getlsbackup** e così via) non sono supportate da OpenGL.

Per informazioni sul disegno di linee con antialias, vedere [porting anti-aliasing Functions](porting-antialiasing-functions.md).

??

 

 





