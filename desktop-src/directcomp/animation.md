---
title: Animazione (DirectComposition)
description: Questo argomento illustra le nozioni di base dell'animazione Microsoft DirectComposition.
ms.assetid: 65DA3971-97C0-4B59-BC67-287AAEAAE340
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 75b1f021d5a11fac70f47d5fe87f9389d2ad3e3108d224835fb295a8c3216354
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119119136"
---
# <a name="animation-directcomposition"></a>Animazione (DirectComposition)

> [!NOTE]
> Per le app Windows 10, è consigliabile usare le API Windows.UI.Composition anziché DirectComposition. Per altre informazioni, vedere [Modernizzare l'app desktop usando il livello Visivo.](/windows/uwp/composition/visual-layer-in-desktop-apps)

Questo argomento illustra le nozioni di base dell'animazione Microsoft DirectComposition. Questa lezione contiene i seguenti argomenti:

-   [Che cos'è un'animazione?](#what-is-an-animation)
-   [Proprietà che possono essere animate](#properties-that-can-be-animated)
-   [Funzioni di animazione](#animation-functions)
-   [Segmenti di animazione](#animation-segments)
    -   [Segmento cubico](#cubic-segment)
    -   [Segmento sinusoidale](#sinusoidal-segment)
    -   [Ripeti segmento](#repeat-segment)
    -   [Segmento finale](#end-segment)
-   [Compatibilità con Windows Animation Manager](#compatibility-with-windows-animation-manager)
-   [Argomenti correlati](#related-topics)

## <a name="what-is-an-animation"></a>Che cos'è un'animazione?

*L'animazione* è un'illusione ottica creata apportando rapidamente modifiche incrementali a un oggetto visivo in un periodo di tempo durante il ridisegno dell'oggetto visivo dopo ogni modifica. Poiché i ridisegni si verificano rapidamente, il cervello percepirà le modifiche incrementali come una singola scena che cambia, proprio come in un film o in un video di live action.

La tabella seguente descrive alcuni dei modi tipici di usare l'animazione.

| Animazione                 | Descrizione                                                                                                                                                                                                                                          |
|---------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Scorrimento                 | Usare l'animazione per aggiungere funzionalità come l'emulazione fisica del momento a un controllo elenco a scorrimento.                                                                                                                                                           |
| Transizioni di scena         | Usare l'animazione per creare transizioni di scena di navigazione che forniscono continuità tra le attività in un flusso di lavoro. Le transizioni della scena di navigazione forniscono un contesto che mostra all'utente dove si trova, dove si trova e dove deve andare successivamente. |
| Interazioni tra finestre | Animare gli elementi dell'interfaccia utente di applicazioni diverse in modo da dare la percezione di una continuità trasparente tra di esse per aiutare l'utente a completare le attività che comportano il passaggio da un'applicazione a un'altra.                                         |



 

## <a name="properties-that-can-be-animated"></a>Proprietà che possono essere animate

In DirectComposition si aggiunge un'animazione a un oggetto visivo applicando l'animazione alle singole proprietà degli oggetti che definiscono l'oggetto visivo. Ad esempio, se si vuole spostare un oggetto visivo orizzontalmente sullo schermo, si applica l'animazione alla proprietà OffsetX dell'oggetto visivo. Analogamente, se si vuole eseguire una semplice rotazione 2D animata di un oggetto visivo, si applica l'animazione alla proprietà Angle di un oggetto di trasformazione 2D e quindi si applica l'oggetto di trasformazione 2D alla proprietà Transform dell'oggetto visivo.

DirectComposition consente di applicare l'animazione a qualsiasi proprietà dell'oggetto che accetta un valore scalare. È possibile applicare animazioni simultanee a più proprietà e più oggetti.

DirectComposition esegue animazioni in un thread separato. È possibile avviare un'animazione o un set di animazioni e quindi eseguire altre operazioni sui thread dell'applicazione o persino mettere i thread in sospensione, mentre il motore di composizione esegue le animazioni alla frequenza di fotogrammi appropriata.

## <a name="animation-functions"></a>Funzioni di animazione

DirectComposition aggiunge un'animazione a una proprietà dell'oggetto in base a una funzione di animazione definita dall'utente. Una *funzione di animazione* è un costrutto che specifica come cambia il valore della proprietà di un oggetto in un periodo di tempo. Ad esempio, è possibile definire una funzione di animazione che modifica il valore di una proprietà da 1 a 360 nel corso di 4 secondi. Quindi, se si applica la funzione di animazione alla proprietà Angle di un oggetto di trasformazione di rotazione 2D e quindi si applica l'oggetto di trasformazione alla proprietà Transform di un oggetto visivo, la funzione di animazione ruota l'oggetto visivo in un cerchio completo nel corso di 4 secondi.

Una funzione di animazione è rappresentata da un oggetto *di* animazione creato da una chiamata al [**metodo IDCompositionDevice::CreateAnimation.**](/windows/win32/api/dcomp/nf-dcomp-idcompositiondevice-createanimation) È possibile creare una funzione di animazione usando i metodi dell'interfaccia [**IDCompositionAnimation**](/windows/desktop/api/DcompAnimation/nn-dcompanimation-idcompositionanimation) di un oggetto di animazione per aggiungere segmenti di *animazione,* uno alla volta, alla matrice che definisce la funzione di animazione. Quando si aggiunge un segmento, si specifica un offset in base zero che contrassegna l'ora di inizio del segmento, rispetto all'inizio della funzione di animazione. I segmenti di animazione devono essere aggiunti in ordine crescente di orari di inizio. Il tentativo di aggiungere un segmento di animazione la cui ora di inizio è precedente o uguale a un segmento precedente avrà esito negativo. Una funzione di animazione può avere un'ora di fine specificata, che indica quando la funzione deve essere conclusa.

Se non diversamente specificato, una funzione di animazione viene avviata quando Gestione finestre desktop (DWM) riceve il comando per eseguire l'animazione. Ogni segmento viene eseguito fino a quando non viene raggiunta l'ora di inizio del segmento successivo. Eventuali modifiche discontinue che si verificano nel valore della proprietà animata tra segmenti vengono considerate modifiche discrete.

È possibile applicare una funzione di animazione a una proprietà impostando il valore della proprietà sul [**puntatore IDCompositionAnimation dell'oggetto**](/windows/desktop/api/DcompAnimation/nn-dcompanimation-idcompositionanimation) di animazione che rappresenta la funzione di animazione. Lo stesso oggetto di animazione può essere applicato a più proprietà dello stesso oggetto, nonché alle proprietà di altri oggetti creati dallo stesso dispositivo.

## <a name="animation-segments"></a>Segmenti di animazione

I segmenti di animazione sono le definizioni di temporizzazione fondamentali di una funzione di animazione. sono le primitive da cui vengono compilate funzioni di animazione più complesse e di livello superiore. Un segmento di animazione viene costruito da una serie di parametri che descrivono la funzione e l'ora di inizio del segmento, rispetto all'inizio della funzione di animazione. Per ogni segmento, il tempo (*t*) avanza lungo l'asse orizzontale e inizia *da t* = 0.

### <a name="cubic-segment"></a>Segmento cubico

La tempistica di un segmento cubico è definita da un polinomio cubico. Per un input di tempo specifico (*t*), il valore di output è dato dall'equazione seguente:

*x*(*t*) = *at* rsi + *bt*² + *ct*  +  *d*

Il diagramma seguente illustra una funzione di animazione che contiene due segmenti cubici. Il primo segmento esegue la transizione di un valore da 0 a 16 in 4 secondi e il secondo modifica il valore in modo lineare da 16 a 0 nei 4 secondi successivi. La prima transizione si verifica lungo questo polinomio cubico:

*x*(*t*) = *t*² - 6 *t*² + 12 *t*

e la seconda transizione si verifica in questa:

*x*(*t*) = - 4 *t* + 16

![Diagramma di una funzione di animazione con due segmenti cubici](images/cubicsegment.png)

Per aggiungere un segmento cubico a una funzione di animazione, usare il [**metodo IDCompositionAnimation::AddCubic.**](/windows/desktop/api/DcompAnimation/nf-dcompanimation-idcompositionanimation-addcubic)

### <a name="sinusoidal-segment"></a>Segmento sinusoidale

La tempistica di un segmento sinusoidale è definita dall'equazione seguente:

*x*(*t*) = *Bias*  +  *Amplitude* \* sin(*t* \* *Frequency* \* 2 PI + \* *Phase* \* PI/180.0)

Per aggiungere un segmento sinusoidale a una funzione di animazione, usare il [**metodo IDCompositionAnimation::AddSinusoidal.**](/windows/desktop/api/DcompAnimation/nf-dcompanimation-idcompositionanimation-addsinusoidal)

### <a name="repeat-segment"></a>Ripeti segmento

Un segmento di ripetizione ripete una parte precedente specificata di una funzione di animazione. Un segmento di ripetizione fa sì che la parte specificata della funzione di animazione ciclo illimitato fino a quando non viene rilevato il segmento successivo o viene raggiunta la fine specificata dell'animazione. La parte precedente di un'animazione è costituito da altri segmenti, inclusi altri segmenti di ripetizione. Un segmento di ripetizione non può essere usato come primo segmento in una funzione di animazione.

Il diagramma seguente illustra una funzione di animazione costituita da due segmenti cubici di durata di 4 secondi ciascuno, seguiti da un segmento di ripetizione che dura 12 secondi. Il segmento di ripetizione inizia 8 secondi nell'animazione e ripete i 6 secondi precedenti dell'animazione due volte fino a raggiungere il segmento finale a 20 secondi.

![Diagramma di una funzione di animazione che contiene due segmenti cubici e un segmento di ripetizione](images/repeatsegment.png)

Per aggiungere un segmento di ripetizione a una funzione di animazione, usare il [**metodo IDCompositionAnimation::AddRepeat.**](/windows/desktop/api/DcompAnimation/nf-dcompanimation-idcompositionanimation-addrepeat)

### <a name="end-segment"></a>Segmento finale

Dopo aver costruito una funzione di animazione dai segmenti, è possibile aggiungere un segmento finale per terminare la funzione di animazione in un determinato momento. Se non si aggiunge un segmento finale, il segmento finale della funzione di animazione viene eseguito a tempo indeterminato.

Accodare un segmento finale chiamando il [**metodo IDCompositionAnimation::End,**](/windows/desktop/api/DcompAnimation/nf-dcompanimation-idcompositionanimation-end) specificando un offset dall'inizio della funzione di animazione che indica il punto finale della funzione. L'offset deve essere maggiore dell'offset iniziale del segmento precedente. Inoltre, un segmento finale non può essere usato come prima primitiva in una funzione di animazione.

Quando si chiama [**End**](/windows/desktop/api/DcompAnimation/nf-dcompanimation-idcompositionanimation-end), si specifica anche un valore finale per la proprietà da animare. La proprietà viene impostata sul valore finale specificato nel momento in cui viene raggiunto il punto finale della funzione di animazione.

Dopo aver aggiunto un segmento finale, non è possibile aggiungere altri segmenti alla funzione di animazione. In altre informazioni, tutte le chiamate al metodo sull'oggetto di animazione hanno esito negativo, ad eccezione [**di IDCompositionAnimation::Reset**](/windows/desktop/api/DcompAnimation/nf-dcompanimation-idcompositionanimation-reset). La **chiamata a Reset** restituisce lo stato pulito dell'oggetto di animazione in cui la funzione di animazione non contiene segmenti. A questo punto è possibile aggiungere nuovamente segmenti.

## <a name="compatibility-with-windows-animation-manager"></a>Compatibilità con Windows Animation Manager

Windows Gestione animazioni (Windows Animation) restituisce primitive di animazione in un formato compatibile con l'API DirectComposition. Ciò significa che DirectComposition può creare animazioni basate sulle primitive di animazione create da Windows Animation.

Per altre informazioni, vedere [Windows Animation Manager](/windows/desktop/UIAnimation/-main-portal), il metodo [**IUIAnimationVariable2::GetCurve**](/windows/desktop/api/uianimation/nf-uianimation-iuianimationvariable2-getcurve) e [Managing DirectComposition Animation with Windows Animation Manager v2](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/DirectCompositionWindowsAnimationManager).

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Concetti relativi a DirectComposition](directcomposition-concepts.md)
</dt> </dl>

 

 
