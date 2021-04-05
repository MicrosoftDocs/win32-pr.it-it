---
title: Creazione di un file di definizione dell'interfaccia personalizzata
description: Creazione di un file di definizione dell'interfaccia personalizzata
ms.assetid: ea7f8e7c-a505-478d-80c3-cb3a3f67859d
keywords:
- Interfacce di Windows Media Player Mobile, file di definizione dell'interfaccia
- interfacce, file di definizione dell'interfaccia
- file per le interfacce, definizione dell'interfaccia
- file di definizione dell'interfaccia, creazione
- creazione di interfacce, informazioni
- creazione di interfacce, Windows Media Player Mobile
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8b8a2920a08a3f57f740ff5ed3ca6e291ffd1bde
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103711722"
---
# <a name="creating-a-skin-definition-file"></a>Creazione di un file di definizione dell'interfaccia personalizzata

Un file di definizione dell'interfaccia è un file di testo che definisce un'interfaccia e tutte le relative parti composite. L'estensione del nome file deve essere. skn.

Ogni file di definizione dell'interfaccia deve iniziare con la riga seguente, che specifica il numero di versione del file di interfaccia. La tabella seguente illustra le versioni di Windows Media Player e la riga di codice che devono essere usate per identificare ogni in un file di definizione dell'interfaccia. Sebbene alcuni dei numeri nelle righe di codice non siano quelli previsti, sono corretti, come illustrato nella tabella seguente.



| Versione di Windows Media Player | Prima riga del file di definizione dell'interfaccia personalizzata |
|------------------------------|------------------------------------|
| 1.01.1<br/>            | \[File skin di Pocket WMP v 1.0\]      |
| 1.2                          | \[File skin di Pocket WMP v 1.2\]      |
| 7.0                          | \[File skin di Pocket WMP v 2.0\]      |
| 7.1                          | \[File skin di Pocket WMP v 8.0\]      |
| serie 9                     | \[File skin di Pocket WMP v 9.0.1\]    |
| Windows 10 Mobile                    | \[File skin di Pocket WMP v 9.0.1\]    |
| 10,1 Mobile                  | \[File skin di Pocket WMP v 9.0.1\]    |



 

Il numero di versione 9.0.1 è per le interfacce create appositamente per Windows Media Player 9 serie o versioni successive. Le interfacce con un numero di versione precedente vengono aperte da Windows Media Player 9 serie o successive come modalità verticale, 96 punti per pollice (DPI).

Il file di definizione dell'interfaccia è costituito da diverse sezioni. Ogni sezione definisce un'area specifica dell'interfaccia. Le sezioni devono essere inserite nell'ordine seguente:

1.  Descrizione
2.  Bitmap
3.  Video
4.  Pulsanti
5.  Stato
6.  Testo
7.  Testo scorrevole
8.  TrackBar

Ogni sezione inizia con il nome della sezione tra parentesi quadre, ad esempio:


```C++
[ Bitmaps ]

```



> [!Note]  
> Il file di definizione dell'interfaccia personalizzata non verrà analizzato correttamente a meno che non si includano spazi tra le parentesi quadre e il nome della sezione.

 

Quindi, una o più righe definiscono singole immagini, pulsanti e così via. Ad esempio, una sezione bitmap potrebbe includere quanto segue:


```C++
    Background  Background.bmp  0,0
    Disabled    Disabled.bmp    0,0
    Pushed      Pushed.bmp      0,0
    Region      Region.bmp      0,0
    Super       Super.bmp       0,0

```



Non è necessario allineare i valori nelle colonne, ma consentirà al codice di essere più leggibile. Per altri dettagli su ogni sezione del file di definizione dell'interfaccia, vedere informazioni di [riferimento sull'interfaccia](skin-reference.md).

> [!Note]  
> Non usare le schede in un punto qualsiasi del file; usare invece spazi aggiuntivi. Questo è molto importante, perché premendo il tasto TAB durante la scrittura o la modifica del file di definizione della pelle si verificherà un errore dell'intera interfaccia. Ogni riga deve essere completata e non può proseguire su una seconda riga. Inoltre, l'area e i valori Super sono deprecati per le interfacce usate con Windows Media Player 10 mobile o versione successiva.

 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**File di definizione dell'interfaccia**](skin-definition-file-mobile.md)
</dt> </dl>

 

 





