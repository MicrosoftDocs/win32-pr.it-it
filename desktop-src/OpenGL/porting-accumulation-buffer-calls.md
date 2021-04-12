---
title: Porting di chiamate del buffer di accumulo
description: È necessario allocare il buffer di accumulo richiedendo il formato pixel appropriato con la funzione OpenGL auxInitDisplayMode o ChoosePixelFormat.
ms.assetid: 523728ce-4aae-4247-a3dc-23864231cad1
keywords:
- Porting di IRIS GL, buffer di accumulo
- porting da IRIS GL, buffer di accumulo
- porting in OpenGL da IRIS GL, buffer di accumulo
- Porting OpenGL da IRIS GL, buffer di accumulo
- buffer di accumulo OpenGL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 91ca91cb3ba35535ba2470297070dffc932a1c33
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104222082"
---
# <a name="porting-accumulation-buffer-calls"></a>Porting di chiamate del buffer di accumulo

È necessario allocare il buffer di accumulo richiedendo il formato pixel appropriato con la funzione OpenGL **auxInitDisplayMode** o [**ChoosePixelFormat**](/windows/desktop/api/wingdi/nf-wingdi-choosepixelformat) . La tabella seguente elenca le funzioni di IRIS GL che interessano il buffer di accumulo e le relative funzioni OpenGL equivalenti.



| Funzione IRIS GL       | OpenGL (funzione)                                       | Significato                                                                       |
|------------------------|-------------------------------------------------------|-------------------------------------------------------------------------------|
| **acsize**             | **auxInitDisplayMode** o **ChoosePixelFormat**       | Specifica il numero di bitplane per ogni componente colore nel buffer di accumulo. |
| **acbuf**              | [**glAccum**](glaccum.md)                            | Opera sul buffer di accumulo.                                          |
|                        | [**glClearAccum**](glclearaccum.md)                  | Imposta i valori cancellati per il buffer di accumulo.                                    |
| **acbuf**( \_ Clear AC) | [**glClear**](glclear.md) ( \_ bit del buffer di accut GL \_ \_ ) | Cancella il buffer di accumulo.                                               |



 

La tabella seguente elenca i parametri **acbuf** di Iris GL insieme ai parametri [**glAccum**](glaccum.md) OpenGL equivalenti.



| Parametro di IRIS GL     | Parametro OpenGL |
|-----------------------|------------------|
| \_accumulo AC        | \_Accue GL        |
| \_ \_ accumulo Clear AC | \_carico GL         |
| \_ritorno AC            | \_return GL       |
| \_mult AC              | \_mult         |
| \_aggiunta CA               | Aggiunta di GL \_          |



 

 

 




