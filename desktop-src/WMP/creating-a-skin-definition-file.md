---
title: Creazione di un file di definizione dell'interfaccia
description: Creazione di un file di definizione dell'interfaccia
ms.assetid: ea7f8e7c-a505-478d-80c3-cb3a3f67859d
keywords:
- Windows Media Player Skin per dispositivi mobili, file di definizione dell'interfaccia
- skins,file di definizione dell'interfaccia
- file per le skin, definizione dell'interfaccia
- file di definizione dell'interfaccia, creazione
- creazione di skin, informazioni
- creazione di skin, Windows Media Player Mobile
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a0bb18289a8ed124c820e983c37ccc9fff60c5c1c2b0794e4964a8e170c84909
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118341601"
---
# <a name="creating-a-skin-definition-file"></a>Creazione di un file di definizione dell'interfaccia

Un file di definizione dell'interfaccia è un file di testo che definisce un'interfaccia e tutte le relative parti composte. L'estensione del nome file deve essere .skn.

Ogni file di definizione dell'interfaccia deve iniziare con la riga seguente, che specifica il numero di versione del file di interfaccia. La tabella seguente illustra Windows Media Player e la riga di codice che deve essere usata per identificare ognuna in un file di definizione dell'interfaccia. Anche se alcuni numeri nelle righe di codice non sono ciò che ci si aspetterebbe, sono corretti come illustrato nella tabella seguente.



| Windows Media Player versione | Prima riga del file di definizione dell'interfaccia |
|------------------------------|------------------------------------|
| 1.01.1<br/>            | \[Pocket WMP Skin File v1.0\]      |
| 1.2                          | \[File di interfaccia WMP Pocket v1.2\]      |
| 7.0                          | \[File di interfaccia WMP Pocket v2.0\]      |
| 7.1                          | \[Pocket WMP Skin File v8.0\]      |
| Serie 9                     | \[File di interfaccia WMP Pocket v9.0.1\]    |
| Windows 10 Mobile                    | \[File di interfaccia WMP Pocket v9.0.1\]    |
| 10.1 Mobile                  | \[File di interfaccia WMP Pocket v9.0.1\]    |



 

Il numero di versione 9.0.1 è per le skin create specificamente per Windows Media Player serie 9 o successive. Le skin con un numero di versione precedente vengono aperte da Windows Media Player serie 9 o successive come modalità verticale, 96 punti per pollice (DPI).

Il file di definizione dell'interfaccia è costituito da diverse sezioni. Ogni sezione definisce una particolare area dell'interfaccia. Le sezioni devono essere inserite nell'ordine seguente:

1.  Descrizione
2.  Bitmap
3.  Video
4.  Pulsanti
5.  Stato
6.  Testo
7.  Testo scorrevole
8.  Trackbar

Ogni sezione inizia con il nome della sezione tra parentesi quadre, ad esempio:


```C++
[ Bitmaps ]

```



> [!Note]  
> Il file di definizione dell'interfaccia non verrà analizzato correttamente a meno che non si includano spazi tra le parentesi e il nome della sezione.

 

Una o più righe definiscono quindi singole immagini, pulsanti e così via. Ad esempio, una sezione Bitmaps può includere quanto segue:


```C++
    Background  Background.bmp  0,0
    Disabled    Disabled.bmp    0,0
    Pushed      Pushed.bmp      0,0
    Region      Region.bmp      0,0
    Super       Super.bmp       0,0

```



Non è necessario allineare i valori nelle colonne, ma il codice sarà più leggibile. Per altri dettagli su ogni sezione del file di definizione dell'interfaccia, vedere Le informazioni [di riferimento sull'interfaccia](skin-reference.md).

> [!Note]  
> Non usare tabulazioni in un punto qualsiasi del file. usare invece spazi aggiuntivi. Questo è molto importante, perché premendo TAB durante la scrittura o la modifica del file di definizione dell'interfaccia, l'intera interfaccia avrà esito negativo. Ogni riga deve essere completa e non può continuare su una seconda riga. Inoltre, i valori Region e Super sono deprecati per le skin usate con Windows Media Player 10 Mobile o versione successiva.

 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**File di definizione dell'interfaccia**](skin-definition-file-mobile.md)
</dt> </dl>

 

 





