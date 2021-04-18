---
title: Animazione (DirectComposition)
description: Questo argomento descrive le nozioni di base di Microsoft DirectComposition Animation.
ms.assetid: 65DA3971-97C0-4B59-BC67-287AAEAAE340
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5f7462a10fd83b45c1b90450fdde806ef306a2f6
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/10/2020
ms.locfileid: "106300800"
---
# <a name="animation-directcomposition"></a>Animazione (DirectComposition)

> [!NOTE]
> Per le app in Windows 10, è consigliabile usare le API Windows. UI. Composition anziché DirectComposition. Per altre informazioni, vedere [modernizzare l'app desktop usando il livello visivo](/windows/uwp/composition/visual-layer-in-desktop-apps).

Questo argomento descrive le nozioni di base di Microsoft DirectComposition Animation. Questa lezione contiene i seguenti argomenti:

-   [Che cos'è un'animazione?](#what-is-an-animation)
-   [Proprietà che possono essere animate](#properties-that-can-be-animated)
-   [Funzioni di animazione](#animation-functions)
-   [Segmenti di animazione](#animation-segments)
    -   [Segmento cubico](#cubic-segment)
    -   [Segmento sinusoidale](#sinusoidal-segment)
    -   [Ripeti segmento](#repeat-segment)
    -   [Segmento finale](#end-segment)
-   [Compatibilità con gestione animazioni Windows](#compatibility-with-windows-animation-manager)
-   [Argomenti correlati](#related-topics)

## <a name="what-is-an-animation"></a>Che cos'è un'animazione?

L' *animazione* è un'illusione ottica creata rendendo rapidamente le modifiche incrementali apportate a un oggetto visivo in un periodo di tempo durante il ridisegno dell'oggetto visivo dopo ogni modifica apportata. Poiché i ridisegni si verificano rapidamente, il cervello percepisce le modifiche incrementali come una singola scena modificabile, così come in un film o video di un'azione live.

Nella tabella seguente vengono descritte alcune delle modalità tipiche di utilizzo dell'animazione.

| Animazione                 | Descrizione                                                                                                                                                                                                                                          |
|---------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Scorrimento                 | Usare l'animazione per aggiungere funzionalità, ad esempio il momento dell'emulazione fisica, a un controllo elenco a scorrimento.                                                                                                                                                           |
| Transizioni di scena         | Usare l'animazione per creare transizioni di scene di spostamento che forniscono continuità tra le attività in un flusso di lavoro. Le transizioni della scena di spostamento forniscono il contesto che mostra l'utente in cui si trovavano, dove si trovano e dove devono andare avanti. |
| Interazioni tra finestre | Animare gli elementi dell'interfaccia utente di diverse applicazioni in modo da dare la percezione della continuità uniforme tra di essi per consentire all'utente di completare le attività che comportano il passaggio da un'applicazione a un'altra.                                         |



 

## <a name="properties-that-can-be-animated"></a>Proprietà che possono essere animate

In DirectComposition è possibile animare un oggetto visivo applicando un'animazione alle singole proprietà degli oggetti che definiscono l'oggetto visivo. Se, ad esempio, si desidera spostare un oggetto visivo orizzontalmente sullo schermo, applicare l'animazione alla proprietà OffsetX dell'oggetto visivo. Analogamente, se si desidera eseguire una semplice rotazione 2D animata di un oggetto visivo, applicare l'animazione alla proprietà Angle di un oggetto Transform 2D, quindi applicare l'oggetto Transform 2D alla proprietà Transform dell'oggetto visivo.

DirectComposition consente di applicare l'animazione a qualsiasi proprietà dell'oggetto che accetta un valore scalare. È possibile applicare animazioni simultanee a più proprietà e a più oggetti.

DirectComposition esegue animazioni in un thread separato. È possibile avviare un'animazione o un set di animazioni, quindi eseguire altre operazioni sui thread dell'applicazione o persino mettere i thread in sospensione, mentre il motore di composizione esegue le animazioni alla frequenza dei fotogrammi appropriata.

## <a name="animation-functions"></a>Funzioni di animazione

DirectComposition aggiunge un'animazione a una proprietà dell'oggetto in base a una funzione di animazione definita dall'utente. Una *funzione di animazione* è un costrutto che specifica la modalità di modifica del valore di una proprietà dell'oggetto in un determinato periodo di tempo. Ad esempio, è possibile definire una funzione di animazione che modifica il valore di una proprietà da 1 a 360 nel corso di 4 secondi. Quindi, se si applica la funzione di animazione alla proprietà Angle di un oggetto Transform 2D rotate, quindi si applica l'oggetto Transform alla proprietà Transform di un oggetto visivo, la funzione di animazione ruota l'oggetto visivo in un cerchio completo nel corso di 4 secondi.

Una funzione di animazione viene rappresentata da un *oggetto di animazione* creato da una chiamata al metodo [**IDCompositionDevice:: CreateAnimation**](/windows/win32/api/dcomp/nf-dcomp-idcompositiondevice-createanimation) . Per creare una funzione di animazione, è possibile usare i metodi dell'interfaccia [**IDCompositionAnimation**](/windows/desktop/api/DcompAnimation/nn-dcompanimation-idcompositionanimation) di un oggetto animazione per aggiungere i *segmenti di animazione*, uno alla volta, alla matrice che definisce la funzione di animazione. Quando si aggiunge un segmento, si specifica un offset in base zero che contrassegna l'ora di inizio del segmento rispetto all'inizio della funzione di animazione. I segmenti di animazione devono essere accodati in ordine crescente per gli orari di inizio. Il tentativo di accodare un segmento di animazione la cui ora di inizio è precedente o uguale a un segmento precedente avrà esito negativo. Una funzione di animazione può avere un'ora di fine specificata, che indica quando la funzione deve terminare.

Se non diversamente specificato, una funzione di animazione viene avviata quando il Gestione finestre desktop (DWM) riceve il comando per eseguire l'animazione. Ogni segmento viene eseguito fino a quando non viene raggiunta l'ora di inizio del segmento successivo. Eventuali modifiche discontinue che si verificano nel valore della proprietà animata tra segmenti sono considerate modifiche discrete.

Per applicare una funzione di animazione a una proprietà, impostare il valore della proprietà sul puntatore [**IDCompositionAnimation**](/windows/desktop/api/DcompAnimation/nn-dcompanimation-idcompositionanimation) dell'oggetto animazione che rappresenta la funzione di animazione. Lo stesso oggetto di animazione può essere applicato a più proprietà dello stesso oggetto, oltre che alle proprietà di altri oggetti creati dallo stesso dispositivo.

## <a name="animation-segments"></a>Segmenti di animazione

I segmenti di animazione sono le definizioni di intervallo fondamentali di una funzione di animazione; sono le primitive da cui vengono compilate funzioni di animazione più complesse e di livello superiore. Un segmento di animazione viene costruito da una serie di parametri che descrivono la funzione e l'ora in cui inizia il segmento, relativo all'inizio della funzione di animazione. Per ogni segmento, Time (*t*) avanza lungo l'asse orizzontale e inizia a *t* = 0.

### <a name="cubic-segment"></a>Segmento cubico

La tempistica di un segmento cubico è definita da un polinomio cubico. Per un dato tempo di input (*t*), il valore di output viene fornito dall'equazione seguente:

*x*(*t*) = *in*³ + *BT*² + *CT*  +  *d*

Nel diagramma seguente viene illustrata una funzione di animazione che contiene due segmenti cubici. Il primo segmento esegue la transizione di un valore da 0 a 16 in 4 secondi e il secondo modifica il valore in modo lineare da 16 a 0 nei successivi 4 secondi. La prima transizione si verifica lungo questo polinomio cubico:

*x*(*t*) = *t*³-6 *t*² + 12 *t*

e la seconda transizione si verifica lungo questo:

*x*(*t*) =-4 *t* + 16

![diagramma di una funzione di animazione con due segmenti cubici](images/cubicsegment.png)

Si aggiunge un segmento cubico a una funzione di animazione usando il metodo [**IDCompositionAnimation:: AddCubic**](/windows/desktop/api/DcompAnimation/nf-dcompanimation-idcompositionanimation-addcubic) .

### <a name="sinusoidal-segment"></a>Segmento sinusoidale

L'intervallo di tempo di un segmento sinusoidale è definito dall'equazione seguente:

*x*(*t*) = *distorsione* di disparità  +   \* sin (*t* \* *Frequency* \* 2 \* pi + *fase* \* pi/180.0)

Si aggiunge un segmento sinusoidale a una funzione di animazione usando il metodo [**IDCompositionAnimation:: AddSinusoidal**](/windows/desktop/api/DcompAnimation/nf-dcompanimation-idcompositionanimation-addsinusoidal) .

### <a name="repeat-segment"></a>Ripeti segmento

Un segmento di ripetizione ripete una parte precedente specificata di una funzione di animazione. Un segmento di ripetizione determina il ciclo illimitato della parte specificata della funzione di animazione fino a quando non viene rilevato il segmento successivo o viene raggiunta la fine dell'animazione specificata. La parte precedente di un'animazione è costituita da altri segmenti, inclusi altri segmenti ripetuti. Non è possibile usare un segmento di ripetizione come primo segmento di una funzione di animazione.

Il diagramma seguente illustra una funzione di animazione costituita da due segmenti cubi di durata di 4 secondi, seguiti da un segmento di ripetizione che dura 12 secondi. Il segmento di ripetizione inizia 8 secondi nell'animazione e ripete i 6 secondi precedenti dell'animazione due volte finché non viene raggiunto il segmento finale a 20 secondi.

![diagramma di una funzione di animazione che contiene due segmenti cubici e un segmento di ripetizione](images/repeatsegment.png)

Per aggiungere un segmento di ripetizione a una funzione di animazione, usare il metodo [**IDCompositionAnimation:: AddRepeat**](/windows/desktop/api/DcompAnimation/nf-dcompanimation-idcompositionanimation-addrepeat) .

### <a name="end-segment"></a>Segmento finale

Dopo la costruzione di una funzione di animazione dai segmenti, è possibile aggiungere un segmento finale per fare in modo che la funzione di animazione termini in un determinato momento. Se non si aggiunge un segmento finale, il segmento finale della funzione di animazione viene eseguito a tempo indefinito.

Si aggiunge un segmento finale chiamando il metodo [**IDCompositionAnimation:: end**](/windows/desktop/api/DcompAnimation/nf-dcompanimation-idcompositionanimation-end) , specificando un offset dall'inizio della funzione di animazione che indica il punto finale della funzione. L'offset deve essere maggiore dell'offset iniziale del segmento precedente. Non è inoltre possibile utilizzare un segmento finale come prima primitiva in una funzione di animazione.

Quando si chiama [**end**](/windows/desktop/api/DcompAnimation/nf-dcompanimation-idcompositionanimation-end), si specifica anche un valore finale per la proprietà a cui si sta aggiungendo un'animazione. La proprietà viene impostata sul valore finale specificato nel momento in cui viene raggiunto il punto finale della funzione di animazione.

Dopo l'aggiunta di un segmento finale, non è possibile aggiungere altri segmenti alla funzione di animazione. Ovvero, tutte le chiamate al metodo sull'oggetto Animation hanno esito negativo, ad eccezione di [**IDCompositionAnimation:: Reset**](/windows/desktop/api/DcompAnimation/nf-dcompanimation-idcompositionanimation-reset). La chiamata di **Reset** restituisce l'oggetto animazione per pulire lo stato in cui la funzione di animazione non contiene segmenti. a questo punto è possibile aggiungere di nuovo segmenti.

## <a name="compatibility-with-windows-animation-manager"></a>Compatibilità con gestione animazioni Windows

Gestione animazioni Windows (animazione Windows) genera le primitive di animazione in un formato compatibile con l'API DirectComposition. Ciò significa che DirectComposition può creare animazioni basate sulle primitive di animazione create dall'animazione di Windows.

Per ulteriori informazioni, vedere [Gestione animazioni Windows](/windows/desktop/UIAnimation/-main-portal), il metodo [**IUIAnimationVariable2:: getcurve**](/windows/desktop/api/uianimation/nf-uianimation-iuianimationvariable2-getcurve) e [gestione dell'animazione DirectComposition con Windows Animation Manager v2](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/DirectCompositionWindowsAnimationManager).

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Concetti di DirectComposition](directcomposition-concepts.md)
</dt> </dl>

 

 
