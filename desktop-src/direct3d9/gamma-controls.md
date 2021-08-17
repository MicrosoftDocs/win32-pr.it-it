---
description: I controlli Gamma consentono di modificare il modo in cui il sistema visualizza il contenuto della superficie, senza influire sul contenuto della superficie stessa.
ms.assetid: 74f106be-8f47-4875-9908-32ff35912968
title: Controlli Gamma (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5074f60199364ba86a0b5ad743fcc03121351cad0ac071d9231beef7c7156f9d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119122205"
---
# <a name="gamma-controls-direct3d-9"></a>Controlli Gamma (Direct3D 9)

I controlli Gamma consentono di modificare il modo in cui il sistema visualizza il contenuto della superficie, senza influire sul contenuto della superficie stessa. Si pensi a questi controlli come a filtri molto semplici che Direct3D applica ai dati quando esce da una superficie e prima che ne venga eseguito il rendering sullo schermo.

I controlli Gamma sono una proprietà di una catena di scambio. I controlli Gamma rendono possibile modificare dinamicamente il mapping dei livelli rosso, verde e blu di una superficie ai livelli effettivi visualizzati dal sistema. Impostando i livelli gamma, è possibile far lampeggiare i colori dello schermo dell'utente, rosso quando viene scattato il carattere dell'utente, verde quando il carattere preleva un nuovo elemento e così via, senza copiare nuove immagini nel buffer dei fotogrammi per ottenere l'effetto. In caso contrario, è possibile regolare i livelli di colore per applicare una distorsione del colore alle immagini nel buffer nascosto.

Esiste sempre almeno una catena di scambio (catena di scambio implicita) per ogni dispositivo perché Direct3D 9 ha una catena di scambio come proprietà del dispositivo. Poiché la rampa gamma è una proprietà della catena di scambio, la rampa gamma può essere applicata quando la catena di scambio è finestrata. La rampa gamma ha effetto immediato. Non è in attesa di un'operazione di sincronizzazione verticale.

I metodi [**SetGammaRamp**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setgammaramp) e [**GetGammaRamp**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-getgammaramp) consentono di modificare i livelli di rampa che influiscono sui componenti di colore rosso, verde e blu dei pixel dalla superficie prima che siano inviati al convertitore da digitale ad analogico (DAC) per la visualizzazione.

## <a name="gamma-ramp-levels"></a>Livelli di rampa gamma

In Direct3D il termine gamma ramp descrive un set di valori che mappano il livello di un particolare componente di colore , rosso, verde, blu, per tutti i pixel nel buffer dei frame ai nuovi livelli ricevuti dall'applicazione livello dati per la visualizzazione. Il remapping viene eseguito tramite tre tabelle di ricerca, una per ogni componente di colore.

Ecco come funziona: Direct3D prende un pixel dal buffer dei fotogrammi e valuta i singoli componenti di colore rosso, verde e blu. Ogni componente è rappresentato da un valore compreso tra 0 e 65535. Direct3D accetta il valore originale e lo usa per indicizzare una matrice di 256 elementi (rampa), in cui ogni elemento contiene un valore che sostituisce quello originale. Direct3D esegue questo processo di ricerca e sostituzione per ogni componente di colore di ogni pixel nel buffer dei frame, modificando in tal modo i colori finali per tutti i pixel sullo schermo.

È utile visualizzare i valori di rampa tramite grafici, come illustrato nei due grafici seguenti. Il grafico a sinistra mostra una rampa che non modifica affatto i colori. Il grafico a destra mostra una rampa che impone una distorsione negativa al componente di colore a cui viene applicato.

![grafici dei valori di rampa gamma](images/gammalv.png)

Gli elementi della matrice per il grafo a sinistra contengono valori identici al relativo indice: 0 nell'elemento in corrispondenza dell'indice 0 e 65535 in corrispondenza dell'indice 255. Questo tipo di rampa è l'impostazione predefinita, in quanto non modifica i valori di input prima che siano visualizzati. Il grafo destro offre più variazione. la relativa rampa contiene valori compresi tra 0 nel primo elemento e 32768 nell'ultimo elemento, con valori compresi in modo uniforme tra. L'effetto è che il componente colore che usa questa rampa appare disattivato sullo schermo. Non si è limitati all'uso di grafici lineari. se l'applicazione può assegnare un mapping arbitrario, se necessario. È anche possibile impostare le voci su tutti gli zeri per rimuovere completamente un componente colore dalla visualizzazione.

## <a name="setting-and-retrieving-gamma-ramp-levels"></a>Impostazione e recupero dei livelli di rampa gamma

I livelli di rampa gamma sono in effetti tabelle di ricerca che Direct3D usa per eseguire il mapping dei componenti di colore del buffer dei frame ai nuovi livelli che verranno visualizzati. È possibile impostare e recuperare i livelli di rampa per la superficie primaria chiamando i [**metodi SetGammaRamp**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setgammaramp) [**e GetGammaRamp.**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-getgammaramp) **SetGammaRamp** accetta due parametri e **GetGammaRamp** accetta un parametro. Per **SetGammaRamp**, il primo parametro è D3DSGR \_ CALIBRATE o D3DSGR \_ NO \_ CALIBRATION. Il secondo parametro, pRamp, è un puntatore a una [**struttura D3DGAMMARAMP.**](d3dgammaramp.md) La **struttura D3DGAMMARAMP** contiene tre matrici di 256 elementi di WORD, una matrice ognuna per contenere le rampe gamma rosse, verdi e blu. **GetGammaRamp** ha un parametro che accetta un puntatore a un **tipo D3DGAMMARAMP** che verrà riempito con la rampa gamma corrente.

È possibile includere il valore D3DSGR CALIBRATE per il primo parametro di \_ [**SetGammaRamp**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setgammaramp) per richiamare il calibratore quando si impostano nuovi livelli gamma. La calibrazione delle rampe gamma comporta un sovraccarico di elaborazione e non deve essere usata di frequente. L'impostazione di una rampa gamma calibrata fornisce un valore gamma coerente e assoluto per l'utente, indipendentemente dalla scheda video e dal monitoraggio.

Non tutti i sistemi supportano la calibrazione gamma. Per determinare se la calibrazione gamma è supportata, chiamare [**GetDeviceCaps**](/windows/desktop/api)ed esaminare il membro Caps2 della struttura [**D3DCAPS9**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9) associata dopo la fine del metodo. Se è presente il flag di funzionalità D3DCAPS2 \_ CANCALIBRATEGAMMA, la calibrazione gamma è supportata.

Quando si impostano nuovi livelli di rampa, tenere presente che i livelli impostati nelle matrici vengono usati solo quando l'applicazione è in modalità esclusiva a schermo intero. Ogni volta che l'applicazione cambia in modalità normale, i livelli di rampa vengono accantonati e vengono nuovamente applicate quando l'applicazione ripristina la modalità schermo intero.

Se il dispositivo non supporta le rampe gamma nella modalità di presentazione corrente della catena di scambio (a schermo intero o con finestra), non viene restituito alcun valore di errore. Le applicazioni possono controllare i bit di funzionalità D3DCAPS2 \_ FULLSCREENGAMMA e D3DCAPS2 \_ CANCALIBRATEGAMMA nel membro Caps2 del tipo D3DCAPS9 per determinare le funzionalità del dispositivo e se è installato un calibratore.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Superfici Direct3D](direct3d-surfaces.md)
</dt> </dl>

 

 
