---
title: Linee di portabilità
description: La portabilità del codice IRIS GL che disegna linee è piuttosto semplice, anche se è necessario notare le differenze nel modo in cui OpenGL si infiamma. La tabella seguente elenca le funzioni IRIS GL per il disegno di linee e le funzioni OpenGL equivalenti.
ms.assetid: de5fd544-5a64-44b5-8976-b96867e4006d
keywords:
- Portabilità IRIS GL, righe
- porting from IRIS GL,lines
- porting to OpenGL from IRIS GL,lines
- Portabilità OpenGL da IRIS GL, righe
- funzioni di disegno, linee
- lines
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a8b0dd0e254380e65171acef1a536038532a370da85ffaa361e8555f77457424
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119776961"
---
# <a name="porting-lines"></a>Linee di portabilità

La portabilità del codice IRIS GL che disegna linee è piuttosto semplice, anche se è necessario notare le differenze nel modo in cui OpenGL si infiamma. La tabella seguente elenca le funzioni IRIS GL per il disegno di linee e le funzioni OpenGL equivalenti.



| Funzione GL IRIS                               | Funzione OpenGL                                                                                         | Significato                                                                                                                                      |
|------------------------------------------------|---------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| **bgnclosedline**,**endclosedline**<br/> | [**glBegin**](glbegin.md) ( GL \_ LINE LOOP ) \_ [**glEnd**](glend.md)<br/>                          | Disegna una linea chiusa.                                                                                                                         |
| **bgnline**                                    | [**glBegin**](glbegin.md) ( GL \_ LINE \_ STRIP )                                                          | Disegna segmenti di linea.                                                                                                                         |
| **linewidth**                                  | [**glLineWidth**](gllinewidth.md)                                                                      | Imposta lo spessore della linea.                                                                                                                             |
| **getlwidth**                                  | [**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) ( GL \_ LINE \_ WIDTH )            | Restituisce lo spessore della riga corrente.                                                                                                                  |
| **deflinestyle**,**setlinestyle**<br/>   | [**glLineStipple**](gllinestipple.md)                                                                  | Specifica un modello di stipple di riga.                                                                                                            |
| **lsrepeat**                                   | argomento factor di **glLineStipple**                                                                    | Imposta un fattore di ripetizione per lo stile della linea.                                                                                                     |
| **getlstyle**                                  | [**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) ( GL \_ LINE \_ STIPPLE \_ PATTERN ) | Restituisce il modello a stipple di riga.                                                                                                                |
| **getlsrepeat**                                | [**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) ( GL \_ LINE \_ STIPPLE \_ REPEAT )  | Restituisce il fattore di ripetizione.                                                                                                                       |
| **linesmooth**, **smoothline**                 | [**glEnable**](glenable.md) ( GL \_ LINE \_ SMOOTH )                                                       | Attiva l'antialiasing di riga. Per altre informazioni sull'antialiasing, vedere [Porting Antialiasing Functions (Porting di funzioni di antialiasing).](porting-antialiasing-functions.md) |



 

OpenGL non usa le tabelle per gli stipple di riga. mantiene un solo modello a punta di riga. È possibile usare [**glPushAttrib**](glpushattrib.md) e [**glPopAttrib**](glpopattrib.md) per passare da uno schema all'altro.

Le funzioni precedenti di stile linea IRIS GL (ad esempio **draw,** **lsbackup,** **getlsbackup** e così via) non sono supportate da OpenGL.

Per informazioni sul disegno di linee con antialias, vedere [Porting Antialiasing Functions](porting-antialiasing-functions.md).

??

 

 





