---
description: La tabella seguente specifica le metriche dei caratteri più importanti per le applicazioni che richiedono documenti portabili e le funzioni che consentono a un'applicazione di recuperarle.
ms.assetid: 61f6d244-7397-42af-af58-0ab9d07bf19e
title: Metriche per documenti portatili
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9c840b1b8e8014086b97098a44890f170a6bd11d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104978554"
---
# <a name="metrics-for-portable-documents"></a>Metriche per documenti portatili

La tabella seguente specifica le metriche dei caratteri più importanti per le applicazioni che richiedono documenti portabili e le funzioni che consentono a un'applicazione di recuperarle.



| Funzione                                               | Metrica                | Uso                                                                                                          |
|--------------------------------------------------------|-----------------------|--------------------------------------------------------------------------------------------------------------|
| [**EnumFontFamilies**](/windows/desktop/api/Wingdi/nf-wingdi-enumfontfamiliesa)           | **ntmSizeEM**         | Recupero di metriche di progettazione; conversione in metriche del dispositivo.                                                   |
| [**GetCharABCWidths**](/windows/desktop/api/Wingdi/nf-wingdi-getcharabcwidthsa)           | **ABCWidths**         | Posizionamento accurato dei caratteri all'inizio e alla fine dei margini, ai limiti dell'immagine e ad altre interruzioni di testo. |
| [**GetCharWidth32**](/windows/desktop/api/Wingdi/nf-wingdi-getcharwidth32a)               | **AdvanceWidths**     | Posizione dei caratteri su una riga.                                                                           |
| [**GetOutlineTextMetrics**](/windows/desktop/api/Wingdi/nf-wingdi-getoutlinetextmetricsa) | **otmfsType**         | Bit di incorporamento dei tipi di carattere.                                                                                         |
|                                                        | **otmsCharSlopeRise** | Componente Y per la pendenza del cursore per i tipi di carattere corsivo.                                                            |
|                                                        | **otmsCharSlopeRun**  | Componente X per la pendenza del cursore per i tipi di carattere corsivo.                                                            |
|                                                        | **otmAscent**         | Interlinea.                                                                                                |
|                                                        | **otmDescent**        | Interlinea.                                                                                                |
|                                                        | **otmLineGap**        | Interlinea.                                                                                                |
|                                                        | **otmpFamilyName**    | Identificazione del tipo di carattere.                                                                                         |
|                                                        | **otmpStyleName**     | Identificazione del tipo di carattere.                                                                                         |
|                                                        | **otmpFullName**      | Identificazione del tipo di carattere, in genere il nome della famiglia e dello stile.                                                      |



 

I membri **otmsCharSlopeRise**, **otmsCharSlopeRun**, **otmAscent**, **otmDescent** e **otmLineGap** della struttura [OUTLINETEXTMETRIC](/windows/desktop/api/Wingdi/ns-wingdi-outlinetextmetrica) vengono ridimensionati o trasformati in modo che corrispondano alla modalità del dispositivo corrente e all'altezza fisica (come specificato nel membro **tmHeight** della struttura [NEWTEXTMETRIC](/windows/win32/api/wingdi/ns-wingdi-newtextmetrica) ).

L'identificazione dei tipi di carattere è importante nelle istanze in cui un'applicazione deve selezionare lo stesso tipo di carattere, ad esempio quando un documento viene riaperto o spostato in un sistema operativo diverso. Il mapper dei tipi di carattere seleziona sempre il tipo di carattere corretto quando un'applicazione richiede un tipo di carattere per nome completo. I nomi della famiglia e dello stile forniscono input alla finestra di dialogo tipo di carattere standard, che garantisce che le barre di selezione siano posizionate correttamente.

I valori **otmsCharSlopeRise** e **otmsCharSlopeRun** vengono usati per produrre un'approssimazione ravvicinata dell'angolo corsivo principale del tipo di carattere. Per i tipi di carattere Roman tipici, **otmsCharSlopeRise** è 1 e **otmsCharSlopeRun** è 0. Per i tipi di carattere corsivo, i valori tentano di approssimare il seno e il coseno dell'angolo corsivo principale del tipo di carattere (in senso antiorario oltre il verticale); Si noti che l'angolo corsivo per i tipi di carattere verticali è 0. Poiché questi valori non sono espressi in unità di progettazione, non devono essere convertiti in unità di dispositivo.

Le metriche relative alla posizione dei caratteri e all'interlinea consentono a un'applicazione di calcolare interruzioni di riga indipendenti dal dispositivo portabili su schermate, stampanti, tipista e persino piattaforme.

**Per eseguire il layout di pagina indipendente dal dispositivo**

1.  Normalizzare tutte le metriche di progettazione in un valore Ultra-High Resolution (Fossil) comune (ad esempio, 65.536 DPI); in questo modo si evitano gli errori di arrotondamento.
2.  Calcolo di interruzioni di riga in base alle metriche delle unità di misura e alla larghezza della pagina fisica; in questo modo si ottiene un punto iniziale e un punto finale di una riga all'interno del flusso di testo.
3.  Calcolare la larghezza della pagina del dispositivo in unità di dispositivo (ad esempio, pixel).
4.  Inserire ogni riga di testo nella larghezza della pagina del dispositivo, usando le interruzioni di riga calcolate nel passaggio 2.
5.  Le interruzioni di pagina di calcolo usando le metriche di Fossil e la lunghezza fisica della pagina; viene restituito il numero di righe per pagina.
6.  Calcola l'altezza delle righe in unità dispositivo.
7.  Inserire le righe di testo nella pagina usando le righe per pagina del passaggio 5 e le altezze di riga del passaggio 6.

Se tutte le applicazioni adottano queste tecniche, gli sviluppatori possono garantire virtualmente che i documenti spostati da un'applicazione a un'altra manterranno l'aspetto e il formato originali.

 

 



