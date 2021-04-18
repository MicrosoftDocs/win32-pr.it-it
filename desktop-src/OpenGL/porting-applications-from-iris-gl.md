---
title: Porting di applicazioni da IRIS GL
description: Porting di applicazioni da IRIS GL
ms.assetid: d410b516-76a1-4cab-a843-801aa6215db5
keywords:
- OpenGL per Windows, porting di IRIS GL
- porting in OpenGL, IRIS GL
- Porting OpenGL, IRIS GL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7c9e739b40f63bb2fd00bb62b4e5ec5566df3c82
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "106298887"
---
# <a name="porting-applications-from-iris-gl"></a>Porting di applicazioni da IRIS GL

Questa sezione elenca le differenze importanti tra IRIS GL e OpenGL e descrive i passaggi di base per il porting del codice da IRIS GL a OpenGL. Per un elenco completo delle differenze tra IRIS GL e Open GL, vedere le [differenze tra IRIS GL e OpenGL](iris-gl-and-opengl-differences.md).

Il porting di programmi IRIS GL a OpenGL per Windows richiede molto più lavoro rispetto alla conversione di programmi OpenGL dal sistema X Window. Sebbene i programmi IRIS GL siano progettati per essere eseguiti con hardware e software specifici, OpenGL è stato progettato per la portabilità tra diversi sistemi.

La tabella seguente elenca alcune delle differenze principali tra i programmi OpenGL e IRIS GL.



| Codice OpenGL                                                                                                                                              | Codice IRIS GL                                                                                                                          |
|----------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| Indipendente dal sistema operativo; non contiene funzioni per windowing, gestione degli eventi, allocazione/gestione del buffer e così via.                              | Dipendente dal sistema operativo; Windowing: le funzioni di sistema sono combinate con le funzioni di rendering. Nessun gestore di Windows in IRIS GL. |
| Usa una convenzione di denominazione comune standard. Le funzioni OpenGL e i tipi definiti iniziano con un prefisso "GL" per evitare conflitti con altre librerie.        | Non utilizza una convenzione di denominazione comune per le funzioni e i tipi definiti.                                                              |
| Gestisce le variabili di stato (ad esempio colore, nebbia, trama, illuminazione e così via) direttamente e in modo coerente. Non usa tabelle per caricare i valori delle variabili di stato. | Utilizza le tabelle per gestire le variabili di stato e deve associare le variabili ai valori della tabella.                                                        |
| Impossibile modificare gli elenchi di visualizzazione.                                                                                                                          | È possibile modificare gli elenchi di visualizzazione.                                                                                                          |
| Non fornisce un formato di file per i tipi di carattere.                                                                                                                | Fornisce funzioni per gestire tipi di carattere e stringhe di testo e un formato di file per i tipi di carattere.                                                      |
| Include una libreria di utilità GL (GLU) che contiene funzioni e routine aggiuntive, ad esempio routine di rendering NURBS e quadratica.                    | Non supporta la libreria GLU.                                                                                                     |



 

**Usare la procedura generale seguente per trasferire i programmi IRIS GL a OpenGL**

1.  Riscrivere il codice che effettua chiamate a un gestore di finestre, una configurazione di finestra, un dispositivo o un evento o la posizione in cui si carica una mappa colori in un codice di Windows equivalente. La riscrittura di un'applicazione da un sistema operativo a un altro può essere complessa e difficile. Questo argomento esula dall'ambito di questa sezione.
2.  Individuare il codice che usa le funzioni e le routine di IRIS GL. Tradurre queste funzioni nelle funzioni OpenGL equivalenti. Per un elenco completo delle funzioni e delle routine di IRIS GL e delle relative controparti OpenGL equivalenti, vedere [funzioni OpenGL e rispettivi equivalenti di Iris GL](opengl-functions-and-their-iris-gl-equivalents.md).
3.  Modificare il codice di IRIS GL come descritto in [speciali problemi di porting di Iris GL](special-iris-gl-porting-issues.md).

<!-- -->

1.  Riscrivere il codice che effettua chiamate a un gestore di finestre, una configurazione di finestra, un dispositivo o un evento o la posizione in cui si carica una mappa colori in un codice di Windows equivalente. La riscrittura di un'applicazione da un sistema operativo a un altro può essere complessa e difficile. Questo argomento esula dall'ambito di questa sezione.
2.  Individuare il codice che usa le funzioni e le routine di IRIS GL. Tradurre queste funzioni nelle funzioni OpenGL equivalenti. Per un elenco completo delle funzioni e delle routine di IRIS GL e delle relative controparti OpenGL equivalenti, vedere [funzioni OpenGL e rispettivi equivalenti di Iris GL](opengl-functions-and-their-iris-gl-equivalents.md).
3.  Modificare il codice di IRIS GL come descritto in [speciali problemi di porting di Iris GL](special-iris-gl-porting-issues.md).

 

 




