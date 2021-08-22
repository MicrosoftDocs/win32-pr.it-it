---
description: La tabella seguente specifica le metriche dei tipi di carattere più importanti per le applicazioni che richiedono documenti portabili e le funzioni che consentono a un'applicazione di recuperarli.
ms.assetid: 61f6d244-7397-42af-af58-0ab9d07bf19e
title: Metriche per i documenti portabili
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3762846e6d8280c2680f47f3cb32cd847ea4e664dab47a8a0995f5505c393da3
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119558501"
---
# <a name="metrics-for-portable-documents"></a>Metriche per i documenti portabili

La tabella seguente specifica le metriche dei tipi di carattere più importanti per le applicazioni che richiedono documenti portabili e le funzioni che consentono a un'applicazione di recuperarli.



| Funzione                                               | Metrica                | Uso                                                                                                          |
|--------------------------------------------------------|-----------------------|--------------------------------------------------------------------------------------------------------------|
| [**EnumFontFamilies**](/windows/desktop/api/Wingdi/nf-wingdi-enumfontfamiliesa)           | **ntmSizeEM**         | Recupero delle metriche di progettazione; conversione in metriche del dispositivo.                                                   |
| [**GetCharABCWidths**](/windows/desktop/api/Wingdi/nf-wingdi-getcharabcwidthsa)           | **ABCWidths**         | Posizionamento accurato dei caratteri all'inizio e alla fine dei margini, dei limiti dell'immagine e di altre interruzioni di testo. |
| [**GetCharWidth32**](/windows/desktop/api/Wingdi/nf-wingdi-getcharwidth32a)               | **Proprietà AdvanceWidths**     | Posizione dei caratteri in una riga.                                                                           |
| [**GetOutlineTextMetrics**](/windows/desktop/api/Wingdi/nf-wingdi-getoutlinetextmetricsa) | **otmfsType**         | Bit di incorporamento del tipo di carattere.                                                                                         |
|                                                        | **otmsCharSlopeRise** | Componente Y per l'inclinazione del cursore per i tipi di carattere corsivo.                                                            |
|                                                        | **otmsCharSlopeRun**  | Componente X per l'inclinazione del cursore per i tipi di carattere corsivo.                                                            |
|                                                        | **otmAscent**         | Interlinea.                                                                                                |
|                                                        | **otmDescent**        | Interlinea.                                                                                                |
|                                                        | **otmLineGap**        | Interlinea.                                                                                                |
|                                                        | **otmpFamilyName**    | Identificazione del tipo di carattere.                                                                                         |
|                                                        | **otmpStyleName**     | Identificazione del tipo di carattere.                                                                                         |
|                                                        | **otmpFullName**      | Identificazione del tipo di carattere (in genere, famiglia e nome dello stile).                                                      |



 

I membri **otmsCharSlopeRise**, **otmsCharSlopeRun**, **otmAscent**, **otmDescent** e **otmLineGap** della struttura [OUTLINETEXTMETRIC](/windows/desktop/api/Wingdi/ns-wingdi-outlinetextmetrica) vengono ridimensionati o trasformati in modo da corrispondere alla modalità del dispositivo corrente e all'altezza fisica (come specificato nel membro **tmHeight** della [struttura NEWTEXTMETRIC).](/windows/win32/api/wingdi/ns-wingdi-newtextmetrica)

L'identificazione del carattere è importante in questi casi quando un'applicazione deve selezionare lo stesso tipo di carattere, ad esempio quando un documento viene riaperto o spostato in un sistema operativo diverso. Il mapper dei tipi di carattere seleziona sempre il tipo di carattere corretto quando un'applicazione richiede un tipo di carattere in base al nome completo. I nomi di famiglia e stile forniscono l'input per la finestra di dialogo tipo di carattere standard, che garantisce che le barre di selezione siano posizionate correttamente.

I **valori otmsCharSlopeRise** e **otmsCharSlopeRun** vengono usati per produrre un'approssimazione vicina dell'angolo corsivo principale del tipo di carattere. Per i tipi di carattere romani tipici, **otmsCharSlopeRise** è 1 e **otmsCharSlopeRun** è 0. Per i tipi di carattere corsivo, i valori tentano di approssimare il seno e il coseno dell'angolo corsivo principale del tipo di carattere (in gradi in senso antiorario dopo l'verticale); Si noti che l'angolo corsivo per i tipi di carattere in verticale è 0. Poiché questi valori non sono espressi in unità di progettazione, non devono essere convertiti in unità di dispositivo.

Le metriche relative al posizionamento dei caratteri e all'interlinea consentono a un'applicazione di calcolare interruzioni di riga indipendenti dal dispositivo portabili su schermi, stampanti, tipi e persino piattaforme.

**Per eseguire il layout di pagina indipendente dal dispositivo**

1.  Normalizzare tutte le metriche di progettazione a un valore comune di ultra-alta risoluzione (UHR), ad esempio 65.536 DPI; In questo modo si evitano errori di arrotondamento.
2.  Calcolare le interruzioni di riga in base alle metriche UHR e alla larghezza fisica della pagina; in modo da ottenere un punto iniziale e un punto finale di una riga all'interno del flusso di testo.
3.  Calcolare la larghezza della pagina del dispositivo in unità di dispositivo (ad esempio pixel).
4.  Adattare ogni riga di testo alla larghezza della pagina del dispositivo, usando le interruzioni di riga calcolate nel passaggio 2.
5.  Calcolare le interruzioni di pagina usando le metriche UHR e la lunghezza fisica della pagina; In questo modo viene prodotto il numero di righe per pagina.
6.  Calcolare l'altezza della linea in unità di dispositivo.
7.  Adattare le righe di testo alla pagina, usando le righe per pagina del passaggio 5 e le altezze delle righe del passaggio 6.

Se tutte le applicazioni adottano queste tecniche, gli sviluppatori possono praticamente garantire che i documenti spostati da un'applicazione a un'altra manterranno l'aspetto e il formato originali.

 

 



