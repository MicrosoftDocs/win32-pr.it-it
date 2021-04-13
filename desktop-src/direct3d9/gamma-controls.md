---
description: I controlli gamma consentono di modificare il modo in cui il sistema Visualizza il contenuto della superficie, senza influire sul contenuto della superficie stessa.
ms.assetid: 74f106be-8f47-4875-9908-32ff35912968
title: Controlli gamma (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6484bcf7e8fa5e07a3bf4bb718cd361330560f8c
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "104568740"
---
# <a name="gamma-controls-direct3d-9"></a>Controlli gamma (Direct3D 9)

I controlli gamma consentono di modificare il modo in cui il sistema Visualizza il contenuto della superficie, senza influire sul contenuto della superficie stessa. Si pensi a questi controlli come filtri molto semplici che Direct3D applica ai dati quando lascia una superficie e prima che venga eseguito il rendering sullo schermo.

I controlli gamma sono una proprietà di una catena di scambio. I controlli gamma consentono di modificare dinamicamente il mapping dei livelli rosso, verde e blu di una superficie ai livelli effettivi visualizzati dal sistema. Impostando i livelli gamma, è possibile fare in modo che lo schermo dell'utente lampeggi i colori rossi quando il carattere dell'utente viene colpito, verde quando il carattere preleva un nuovo elemento e così via, senza copiare nuove immagini nel buffer del frame per ottenere l'effetto. In alternativa, è possibile modificare i livelli di colore per applicare una distorsione dei colori alle immagini nel buffer nascosto.

È sempre presente almeno una catena di scambio (la catena di scambio implicita) per ogni dispositivo, perché Direct3D 9 ha una catena di scambio come proprietà del dispositivo. Poiché la rampa gamma è una proprietà della catena di scambio, la rampa gamma può essere applicata quando la catena di scambio è a finestra. La rampa gamma ha effetto immediato. Non è in attesa di un'operazione di sincronizzazione verticale.

I metodi [**SetGammaRamp**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setgammaramp) e [**GetGammaRamp**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-getgammaramp) consentono di modificare i livelli di rampa che interessano i componenti di colore rosso, verde e blu dei pixel della superficie prima di essere inviati al convertitore da digitale a analogico (DAC) per la visualizzazione.

## <a name="gamma-ramp-levels"></a>Livelli di rampa gamma

In Direct3D il termine gamma gamma descrive un set di valori che eseguono il mapping del livello di un particolare componente colore, rosso, verde, blu, per tutti i pixel nel buffer del frame, ai nuovi livelli ricevuti dall'applicazione livello dati per la visualizzazione. Il mapping viene eseguito tramite tre tabelle di ricerca, una per ogni componente del colore.

Ecco come funziona: Direct3D accetta un pixel dal buffer dei frame e valuta i singoli componenti di colore rosso, verde e blu. Ogni componente è rappresentato da un valore compreso tra 0 e 65535. Direct3D acquisisce il valore originale e lo usa per indicizzare una matrice di 256 elementi (la rampa), in cui ogni elemento contiene un valore che sostituisce quello originale. Direct3D esegue questo processo di ricerca e sostituzione per ogni componente colore di ogni pixel nel buffer dei frame, modificando quindi i colori finali per tutti i pixel sullo schermo.

È utile visualizzare i valori della rampa creando un grafico, come illustrato nei due grafici seguenti. Il grafico a sinistra mostra una rampa che non modifica i colori. Il grafico a destra mostra una rampa che impone una distorsione negativa al componente colore a cui viene applicato.

![grafici dei valori delle rampe gamma](images/gammalv.png)

Gli elementi della matrice per il grafico a sinistra contengono valori identici all'indice 0 nell'elemento in corrispondenza dell'indice 0 e 65535 in corrispondenza dell'indice 255. Questo tipo di rampa è l'impostazione predefinita, in quanto non modifica i valori di input prima che vengano visualizzati. Il grafico a destra offre maggiore variazione; la relativa rampa contiene valori che variano da 0 nel primo elemento a 32768 nell'ultimo elemento, con valori uniformi tra. L'effetto è che il componente colore che usa questa rampa viene disattivato sullo schermo. Non si è limitati all'uso di grafici lineari; Se l'applicazione può assegnare un mapping arbitrario, se necessario. È anche possibile impostare le voci su tutti zeri per rimuovere completamente un componente colore dalla visualizzazione.

## <a name="setting-and-retrieving-gamma-ramp-levels"></a>Impostazione e recupero di livelli di rampa gamma

I livelli di rampa gamma sono le tabelle di ricerca che Direct3D usa per eseguire il mapping dei componenti del colore del buffer del frame ai nuovi livelli che verranno visualizzati. È possibile impostare e recuperare i livelli di rampa per la superficie primaria chiamando i metodi [**SetGammaRamp**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setgammaramp) e [**GetGammaRamp**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-getgammaramp) . **SetGammaRamp** accetta due parametri e **GetGammaRamp** accetta un solo parametro. Per **SetGammaRamp**, il primo parametro è D3DSGR \_ calibrate o D3DSGR \_ No \_ Calibration. Il secondo parametro, pRamp, è un puntatore a una struttura [**D3DGAMMARAMP**](d3dgammaramp.md) . La struttura **D3DGAMMARAMP** contiene matrici di parole di 3 256 elementi, una matrice che contiene le rampe di colore rosso, verde e blu. **GetGammaRamp** dispone di un parametro che accetta un puntatore a un tipo **D3DGAMMARAMP** che verrà riempito con la rampa gamma corrente.

È possibile includere il \_ valore D3DSGR calibrate per il primo parametro di [**SetGammaRamp**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setgammaramp) per richiamare il calibratore quando si impostano nuovi livelli gamma. La calibratura delle rampe gamma comporta un sovraccarico di elaborazione e non deve essere usata di frequente. L'impostazione di una rampa gamma calibrata fornisce un valore gamma coerente e assoluto per l'utente, indipendentemente dalla scheda di visualizzazione e dal monitoraggio.

Non tutti i sistemi supportano la calibrazione gamma. Per determinare se la calibrazione gamma è supportata, chiamare [**GetDeviceCaps**](/windows/desktop/api)ed esaminare il membro Caps2 della struttura [**D3DCAPS9**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9) associata dopo che il metodo restituisce un risultato. Se \_ è presente il flag D3DCAPS2 CANCALIBRATEGAMMA Capability, la calibrazione gamma è supportata.

Quando si impostano nuovi livelli di rampa, tenere presente che i livelli impostati nelle matrici vengono usati solo quando l'applicazione è in modalità esclusiva a schermo intero. Ogni volta che l'applicazione passa alla modalità normale, i livelli di rampa vengono accantonati, che diventano effettivi quando l'applicazione ripristina la modalità a schermo intero.

Se il dispositivo non supporta le rampe gamma nella modalità di presentazione corrente della catena di scambio (a schermo intero o a finestra), non viene restituito alcun valore di errore. Le applicazioni possono controllare i \_ bit della funzionalità D3DCAPS2 FULLSCREENGAMMA e D3DCAPS2 \_ CANCALIBRATEGAMMA nel membro Caps2 del tipo D3DCAPS9 per determinare le funzionalità del dispositivo e se è installato un calibratore.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Superfici Direct3D](direct3d-surfaces.md)
</dt> </dl>

 

 
