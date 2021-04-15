---
description: Segmenti busta
ms.assetid: 1b59cd1c-7c37-4c70-a36c-2ee1f42b42c5
title: Segmenti busta
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1bac997667f52ef9bbf14760584889fa16cbbd04
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "104521634"
---
# <a name="envelope-segments"></a>Segmenti busta

Una curva di parametro è costituita da uno o più segmenti di busta, definiti mediante la struttura del [**\_ \_ segmento della busta MP**](/previous-versions/windows/desktop/api/Medparam/ns-medparam-mp_envelope_segment) . Questa struttura contiene le informazioni seguenti:

-   Ora di inizio e di fine.
-   Valori di inizio e di fine.
-   Tipo di curva (lineare, quadrato e così via).
-   Flag facoltativi, descritti a breve.

Il client aggiunge segmenti di busta a un parametro chiamando il metodo [**IMediaParams:: AddEnvelope**](/previous-versions/windows/desktop/api/Medparam/nf-medparam-imediaparams-addenvelope) e passando una matrice di strutture **del \_ \_ segmento della busta MP** . Il client deve ordinare i segmenti in ordine di tempo crescente prima di chiamare il metodo. Quando DMO elabora i dati, è possibile immaginare il parametro in viaggio su ogni segmento della busta, ad esempio un'auto che conduce a una serie di colline. Il metodo [**IMediaParams:: Getparat**](/previous-versions/windows/desktop/api/Medparam/nf-medparam-imediaparams-getparam) restituisce il valore più recente.

Due segmenti adiacenti possono avere un gap tra di essi. Durante i gap, il parametro mantiene il valore precedente, come indicato di seguito:

-   Prima del primo segmento, il valore è il valore neutro.
-   Tra i segmenti, il valore è il valore finale del segmento precedente.
-   Dopo l'ultimo segmento, il valore rimane in corrispondenza del valore finale di tale segmento.
-   Se il client Scarica DMO, il valore viene ripristinato sul valore neutro.

È possibile modificare un segmento impostando uno dei flag seguenti:

-   ENVLP di MPF \_ \_ Avvia \_ CURRENTVAL. DMO usa il valore più recente del parametro come valore iniziale per il segmento. Potrebbe trattarsi del valore neutro o del valore finale del segmento precedente. DMO ignora il membro **valStart** della struttura del **segmento della \_ busta \_ MP** .
-   ENVLP di MPF \_ \_ Avvia \_ NEUTRALVAL. DMO usa il valore neutro del parametro come valore iniziale per il segmento. Ignora **valStart**.

È possibile considerare questi flag come il punto iniziale del segmento e spostarli verso l'alto o verso il basso, mentre il valore finale rimane fisso. Il segmento si estenderà di conseguenza.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Parametri dei supporti](media-parameters.md)
</dt> </dl>

 

 



