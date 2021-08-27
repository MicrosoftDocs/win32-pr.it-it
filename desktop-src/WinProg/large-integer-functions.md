---
title: Funzioni Large Integer
description: Le funzioni seguenti vengono usate con numeri interi di grandi dimensioni.
ms.assetid: f34932f4-b126-4d6c-a2f0-3ad706fd5629
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7878d817e7647f46da52105cea264f6332303de2ca1d7b440697defc656cd0b2
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120071631"
---
# <a name="large-integer-functions"></a>Funzioni Large Integer

Le funzioni seguenti vengono usate con numeri interi di grandi dimensioni.

## <a name="in-this-section"></a>Contenuto della sezione



| Funzione                                                                    | Descrizione                                                                                                                                                                                                   |
|-----------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Int32x32To64**](/windows/desktop/api/Winnt/nf-winnt-int32x32to64)<br/>                             | Moltiplica due interi a 32 bit con segno, che restituiscono un risultato intero a 64 bit con segno.<br/>                                                                                                                   |
| [**Int64ShllMod32**](/windows/desktop/api/Winnt/nf-winnt-int64shllmod32)<br/>                         | Esegue un'operazione di spostamento logico a sinistra su un valore integer a 64 bit senza segno. La funzione fornisce codice di spostamento migliorato per i turni logici a sinistra in cui il numero di turni è compreso nell'intervallo 0-31.<br/>      |
| [**Int64ShraMod32**](/windows/desktop/api/Winnt/nf-winnt-int64shramod32)<br/>                         | Esegue un'operazione di spostamento aritmetico a destra su un valore integer a 64 bit con segno. La funzione fornisce codice di spostamento migliorato per gli turni aritmetici a destra in cui il numero di turni è compreso nell'intervallo 0-31.<br/> |
| [**Int64ShrlMod32**](/windows/desktop/api/Winnt/nf-winnt-int64shrlmod32)<br/>                         | Esegue un'operazione di spostamento logico a destra su un valore integer a 64 bit senza segno. La funzione fornisce codice di spostamento migliorato per i turni logici a destra in cui il numero di turni è compreso nell'intervallo 0-31.<br/>    |
| [**MulDiv**](/windows/desktop/api/Winbase/nf-winbase-muldiv)<br/>                                         | Moltiplica due valori a 32 bit e quindi divide il risultato a 64 bit per un terzo valore a 32 bit.<br/>                                                                                                           |
| [**Moltiplicare128**](/windows/desktop/api/Winnt/nf-winnt-multiply128)<br/>                               | Moltiplica due interi a 64 bit per produrre un intero a 128 bit.<br/>                                                                                                                                       |
| [**MultiplyExtract128**](/windows/desktop/api/Winnt/nf-winnt-multiplyextract128)<br/>                 | Moltiplica due interi a 64 bit per produrre un intero a 128 bit, sposta il prodotto verso destra per il numero specificato di bit e restituisce i 64 bit bassi del risultato.<br/>                           |
| [**MultiplyHigh**](/windows/desktop/api/Winnt/nf-winnt-multiplyhigh)<br/>                             | Moltiplica due interi a 64 bit per produrre un intero a 128 bit e ottiene i 64 bit alti.<br/>                                                                                                             |
| [**PopulationCount64**](/windows/desktop/api/Winnt/nf-winnt-populationcount64)<br/>                   | Conta il numero di un bit (numero di popolamento) in un intero senza segno a 64 bit.<br/>                                                                                                                     |
| [**MAIUSCLeft128**](/windows/desktop/api/winnt/nf-winnt-shiftleft128)<br/>                             | Sposta a sinistra di 128 bit.<br/>                                                                                                                                                                               |
| [**MaiuscRight128**](/windows/desktop/api/winnt/nf-winnt-shiftright128)<br/>                           | Sposta a destra a 128 bit.<br/>                                                                                                                                                                              |
| [**UInt32x32To64**](/windows/desktop/api/Winnt/nf-winnt-uint32x32to64)<br/>                           | Moltiplica due interi senza segno a 32 bit, che restituiscono un risultato intero senza segno a 64 bit.<br/>                                                                                                              |
| [**UnsignedMultiply128**](/windows/desktop/api/Winnt/nf-winnt-unsignedmultiply128)<br/>               | Moltiplica due interi senza segno a 64 bit per produrre un intero senza segno a 128 bit.<br/>                                                                                                                    |
| [**UnsignedMultiplyExtract128**](/windows/desktop/api/Winnt/nf-winnt-unsignedmultiplyextract128)<br/> | Moltiplica due interi senza segno a 64 bit per produrre un intero senza segno a 128 bit, sposta il prodotto a destra per il numero di bit specificato e restituisce i 64 bit bassi del risultato.<br/>        |
| [**UnsignedMulitplyHigh**](/windows/desktop/api/Winnt/nf-winnt-unsignedmultiplyhigh)<br/>             | Moltiplica due interi a 64 bit per produrre un intero a 128 bit e ottiene i 64 bit senza segno alti.<br/>                                                                                                    |



 

 

 





