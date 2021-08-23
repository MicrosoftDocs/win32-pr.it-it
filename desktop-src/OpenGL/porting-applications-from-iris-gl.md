---
title: Porting Applications from IRIS GL
description: Porting Applications from IRIS GL
ms.assetid: d410b516-76a1-4cab-a843-801aa6215db5
keywords:
- OpenGL on Windows,IRIS GL porting
- porting to OpenGL,IRIS GL
- Portabilità OpenGL, IRIS GL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a68e218e5b6f57039e364ab4e6ebc29fb1f2b2fad2e8a679b35c1368367f5f2b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119777231"
---
# <a name="porting-applications-from-iris-gl"></a>Porting Applications from IRIS GL

Questa sezione elenca importanti differenze tra IRIS GL e OpenGL e descrive i passaggi di base per la portabilità del codice da IRIS GL a OpenGL. Per un elenco completo delle differenze tra IRIS GL e Open GL, vedere [Differenze tra IRIS GL e OpenGL.](iris-gl-and-opengl-differences.md)

La conversione dei programmi IRIS GL in OpenGL Windows richiede molto più lavoro rispetto alla conversione di programmi OpenGL dal sistema X Window. Anche se i programmi IRIS GL sono progettati per l'esecuzione con hardware e software specifici, OpenGL è stato progettato per la portabilità tra vari sistemi.

La tabella seguente elenca alcune delle differenze principali tra i programmi OpenGL e IRIS GL.



| Codice OpenGL                                                                                                                                              | Codice GL IRIS                                                                                                                          |
|----------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| Indipendente dal sistema operativo; non contiene funzioni per il windowing, la gestione degli eventi, l'allocazione/gestione del buffer e così via.                              | Dipendente dal sistema operativo; Le funzioni windowing-system sono miste alle funzioni di rendering. Non esiste alcun gestore windows in IRIS GL. |
| Usa una convenzione di denominazione standard e comune. Le funzioni OpenGL e i tipi definiti iniziano con un prefisso "gl" per evitare conflitti con altre librerie.        | Non usa una convenzione di denominazione comune per le funzioni e i tipi definiti.                                                              |
| Gestisce le variabili di stato (ad esempio colore, colore, trama, illuminazione e così via) in modo diretto e coerente. Non usa le tabelle per caricare i valori delle variabili di stato. | Usa le tabelle per gestire le variabili di stato e deve associare le variabili ai valori di tabella.                                                        |
| Gli elenchi visualizzati non possono essere modificati.                                                                                                                          | Gli elenchi visualizzati possono essere modificati.                                                                                                          |
| Non fornisce un formato di file per i tipi di carattere.                                                                                                                | Fornisce funzioni per gestire tipi di carattere e stringhe di testo e un formato di file per i tipi di carattere.                                                      |
| Include una libreria DELL'utilità GL (GLU) che contiene funzioni e routine aggiuntive, ad esempio NURBS e routine di rendering quadratico.                    | Non supporta la libreria GLU.                                                                                                     |



 

**Usare la procedura generale seguente per eseguire il port dei programmi IRIS GL in OpenGL**

1.  Riscrivere il codice che effettua chiamate a un gestore di finestre, una configurazione della finestra, un dispositivo o un evento o in cui si carica una mappa colori in un codice Windows codice. La riscrittura di un'applicazione da un sistema operativo a un altro può essere complessa e difficile. Questo argomento non è in ambito di questa sezione.
2.  Individuare il codice che usa routine e funzioni IRIS GL. Convertire queste funzioni nelle funzioni OpenGL equivalenti. Per un elenco completo delle funzioni e delle routine IRIS GL e delle relative controparti OpenGL equivalenti, vedere Funzioni OpenGL e equivalenti [IRIS GL.](opengl-functions-and-their-iris-gl-equivalents.md)
3.  Modificare il codice GL IRIS come descritto in Special IRIS GL Porting Issues (Problemi speciali [di portabilità di IRIS GL).](special-iris-gl-porting-issues.md)

<!-- -->

1.  Riscrivere il codice che effettua chiamate a un gestore di finestre, una configurazione della finestra, un dispositivo o un evento o in cui si carica una mappa colori in un codice Windows codice. La riscrittura di un'applicazione da un sistema operativo a un altro può essere complessa e difficile. Questo argomento non è in ambito di questa sezione.
2.  Individuare il codice che usa routine e funzioni IRIS GL. Convertire queste funzioni nelle funzioni OpenGL equivalenti. Per un elenco completo delle funzioni e delle routine IRIS GL e delle relative controparti OpenGL equivalenti, vedere Funzioni OpenGL e equivalenti [IRIS GL.](opengl-functions-and-their-iris-gl-equivalents.md)
3.  Modificare il codice GL IRIS come descritto in Special IRIS GL Porting Issues (Problemi speciali [di portabilità di IRIS GL).](special-iris-gl-porting-issues.md)

 

 




