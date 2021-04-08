---
title: Funzioni Integer di grandi dimensioni
description: Le funzioni seguenti vengono utilizzate con Integer di grandi dimensioni.
ms.assetid: f34932f4-b126-4d6c-a2f0-3ad706fd5629
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0aebb5bd8c3edc35098dcf1bb232d858a9c6638d
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104044857"
---
# <a name="large-integer-functions"></a>Funzioni Integer di grandi dimensioni

Le funzioni seguenti vengono utilizzate con Integer di grandi dimensioni.

## <a name="in-this-section"></a>Contenuto della sezione



| Funzione                                                                    | Descrizione                                                                                                                                                                                                   |
|-----------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Int32x32To64**](/windows/desktop/api/Winnt/nf-winnt-int32x32to64)<br/>                             | Moltiplica due interi con segno a 32 bit, restituendo un risultato Integer a 64 bit con segno.<br/>                                                                                                                   |
| [**Int64ShllMod32**](/windows/desktop/api/Winnt/nf-winnt-int64shllmod32)<br/>                         | Esegue un'operazione di spostamento logico a sinistra su un valore intero senza segno a 64 bit. La funzione fornisce codice di spostamento migliorato per i turni logici sinistri in cui il conteggio dello spostamento è compreso nell'intervallo 0-31.<br/>      |
| [**Int64ShraMod32**](/windows/desktop/api/Winnt/nf-winnt-int64shramod32)<br/>                         | Esegue un'operazione di spostamento aritmetica a destra su un valore intero con segno a 64 bit. La funzione fornisce un codice di spostamento migliorato per i turni aritmetici corretti in cui il conteggio dello spostamento è compreso nell'intervallo 0-31.<br/> |
| [**Int64ShrlMod32**](/windows/desktop/api/Winnt/nf-winnt-int64shrlmod32)<br/>                         | Esegue un'operazione di spostamento logico a destra su un valore intero senza segno a 64 bit. La funzione fornisce un codice di spostamento migliorato per i turni logici corretti in cui il conteggio dello spostamento è compreso nell'intervallo 0-31.<br/>    |
| [**MulDiv**](/windows/desktop/api/Winbase/nf-winbase-muldiv)<br/>                                         | Moltiplica i valori a 2 32 bit e quindi divide il risultato di 64 bit per un terzo valore a 32 bit.<br/>                                                                                                           |
| [**Multiply128**](/windows/desktop/api/Winnt/nf-winnt-multiply128)<br/>                               | Moltiplica gli Integer a 2 64 bit per produrre un intero a 128 bit.<br/>                                                                                                                                       |
| [**MultiplyExtract128**](/windows/desktop/api/Winnt/nf-winnt-multiplyextract128)<br/>                 | Moltiplica gli Integer a 2 64 bit per produrre un valore integer a 128 bit, sposta il prodotto a destra del numero di bit specificato e restituisce i 64 bit bassi del risultato.<br/>                           |
| [**MultiplyHigh**](/windows/desktop/api/Winnt/nf-winnt-multiplyhigh)<br/>                             | Moltiplica gli Integer a 2 64 bit per produrre un valore integer a 128 bit e ottiene i bit 64 alti.<br/>                                                                                                             |
| [**PopulationCount64**](/windows/desktop/api/Winnt/nf-winnt-populationcount64)<br/>                   | Conta il numero di un bit (conteggio popolazione) in una Unsigned Integer a 64 bit.<br/>                                                                                                                     |
| [**ShiftLeft128**](/windows/desktop/api/winnt/nf-winnt-shiftleft128)<br/>                             | Sposta a sinistra di 128 bit.<br/>                                                                                                                                                                               |
| [**ShiftRight128**](/windows/desktop/api/winnt/nf-winnt-shiftright128)<br/>                           | Sposta a destra di 128 bit.<br/>                                                                                                                                                                              |
| [**UInt32x32To64**](/windows/desktop/api/Winnt/nf-winnt-uint32x32to64)<br/>                           | Moltiplica due interi senza segno a 32 bit, restituendo un risultato Integer a 64 bit senza segno.<br/>                                                                                                              |
| [**UnsignedMultiply128**](/windows/desktop/api/Winnt/nf-winnt-unsignedmultiply128)<br/>               | Moltiplica due interi senza segno a 64 bit per produrre un intero senza segno a 128 bit.<br/>                                                                                                                    |
| [**UnsignedMultiplyExtract128**](/windows/desktop/api/Winnt/nf-winnt-unsignedmultiplyextract128)<br/> | Moltiplica due interi senza segno a 64 bit per produrre un intero senza segno a 128 bit, sposta il prodotto a destra del numero di bit specificato e restituisce i 64 bit inferiori del risultato.<br/>        |
| [**UnsignedMulitplyHigh**](/windows/desktop/api/Winnt/nf-winnt-unsignedmultiplyhigh)<br/>             | Moltiplica gli Integer a 2 64 bit per produrre un valore integer a 128 bit e ottiene i bit 64 non firmati elevati.<br/>                                                                                                    |



 

 

 





