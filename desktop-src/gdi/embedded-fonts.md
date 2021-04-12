---
description: Incorporare un tipo di carattere è la tecnica di aggregazione di un documento e dei tipi di carattere contenuti in un file per la trasmissione a un altro computer.
ms.assetid: ded409f1-5bd9-411b-b905-fc49c484786a
title: Tipi di carattere incorporati
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 83fb8ab821afa5f44ded05a4a61a53439b8db9fc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104130782"
---
# <a name="embedded-fonts"></a>Tipi di carattere incorporati

Incorporare un tipo di carattere è la tecnica di aggregazione di un documento e dei tipi di carattere contenuti in un file per la trasmissione a un altro computer. Incorporando un tipo di carattere si garantisce che un tipo di carattere specificato in un file trasmesso sia presente nel computer che riceve il file. Tuttavia, non tutti i tipi di carattere possono essere spostati da computer a computer, poiché la maggior parte dei tipi di carattere è concessa in licenza a un solo computer alla volta. È possibile incorporare solo tipi di carattere TrueType e OpenType.

Le applicazioni devono incorporare un tipo di carattere in un documento solo quando richiesto da un utente. Non è possibile distribuire un'applicazione insieme a documenti che contengono tipi di carattere incorporati, né un'applicazione può contenere un tipo di carattere incorporato. Ogni volta che un'applicazione distribuisce un tipo di carattere in qualsiasi formato, i diritti proprietari del proprietario del tipo di carattere devono essere riconosciuti.

Potrebbe trattarsi di una violazione dei diritti proprietari o del contratto di licenza utente di un fornitore di tipi di carattere per incorporare i tipi di carattere in cui l'incorporamento non è consentito o non rispettare le linee guida seguenti per l'incorporamento dei tipi di carattere. Una licenza del tipo di carattere può concedere solo l'autorizzazione di lettura/scrittura per l'installazione e l'utilizzo di un tipo di carattere nel computer di destinazione. In alternativa, la licenza può concedere l'autorizzazione di sola lettura. L'autorizzazione di sola lettura consente a un documento di essere visualizzato e stampato (ma non modificato) dal computer di destinazione. i documenti con tipi di carattere incorporati di sola lettura sono di sola lettura. I tipi di carattere incorporati di sola lettura non possono essere disaggregati dal documento e installati nel computer di destinazione.

Un'applicazione può determinare lo stato della licenza chiamando la funzione [**GetOutlineTextMetrics**](/windows/desktop/api/Wingdi/nf-wingdi-getoutlinetextmetricsa) ed esaminando il membro **OtmfsType** della struttura [**OUTLINETEXTMETRIC**](/windows/desktop/api/Wingdi/ns-wingdi-outlinetextmetrica) . Se viene impostato il bit 1 di **otmfsType** , l'incorporamento non è consentito per il tipo di carattere. Se il bit 1 è chiaro, il tipo di carattere può essere incorporato. Se è impostato il bit 2, l'incorporamento è di sola lettura.

Per incorporare un tipo di carattere TrueType, un'applicazione può utilizzare la funzione [**GetFontData**](/windows/desktop/api/Wingdi/nf-wingdi-getfontdata) per leggere il file del tipo di carattere. L'impostazione dei parametri *dwTable* e *dwOffset* di [**GetFontData**](/windows/win32/api/wingdi/nf-wingdi-getfontdata) su 0L e del parametro *cbData* su 1L garantisce che l'applicazione legga l'intero file del tipo di carattere dall'inizio.

Sono disponibili diverse funzioni per incorporare i tipi di carattere OpenType a seconda della larghezza dei caratteri e della posizione in cui risiedono i dati del tipo di carattere. Per incorporare un tipo di carattere Unicode OpenType che risiede in un contesto di dispositivo, un'applicazione può usare [**TTEmbedFont**](/windows/desktop/api/T2embapi/nf-t2embapi-ttembedfont). Per incorporare un tipo di carattere UCS-4 OpenType che risiede in un contesto di dispositivo, un'applicazione può usare [**TTEmbedFontEx**](/windows/desktop/api/T2embapi/nf-t2embapi-ttembedfontex). Per incorporare un tipo di carattere Unicode OpenType che risiede in un file del tipo di carattere, un'applicazione può usare [**TTEmbedFontFromFile**](/windows/desktop/api/T2embapi/nf-t2embapi-ttembedfontfromfilea). Per ulteriori informazioni sull'incorporamento di tipi di carattere OpenType, vedere il [riferimento all'incorporamento dei tipi di carattere](font-embedding-reference.md).

Dopo che un'applicazione ha recuperato i dati del tipo di carattere, può archiviare i dati con il documento usando qualsiasi formato applicabile. La maggior parte delle applicazioni compila una directory dei tipi di carattere nel documento, elencando i tipi di carattere incorporati e se l'incorporamento è di lettura/scrittura o di sola lettura. Un'applicazione può usare i membri **otmpStyleName** e **OtmFamilyName** della struttura [**OUTLINETEXTMETRIC**](/windows/win32/api/wingdi/ns-wingdi-outlinetextmetrica) per identificare il tipo di carattere.

Se per il tipo di carattere incorporato è impostato il bit di sola lettura, le applicazioni devono crittografare i dati del tipo di carattere prima di archiviarli con il documento. Il metodo di crittografia non deve essere complicato; ad esempio, l'uso dell'operatore XOR per combinare i dati del tipo di carattere con una costante definita dall'applicazione è sufficiente e veloce.

 

 
