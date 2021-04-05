---
description: Per comprendere completamente uno shader che implementa PRT, è utile derivare la formula utilizzata dallo shader per calcolare l'uscita.
ms.assetid: 66876e9e-cde1-4d04-9b31-30be1c115e6b
title: Equazioni PRT (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a65559fada82fda7f7eed1c7d05543883a06a19e
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "104124818"
---
# <a name="prt-equations-direct3d-9"></a>Equazioni PRT (Direct3D 9)

Per comprendere completamente uno shader che implementa PRT, è utile derivare la formula utilizzata dallo shader per calcolare l'uscita.

Per iniziare, l'equazione seguente è l'equazione generale per calcolare l'uscita radiante risultante dall'illuminazione diretta su un oggetto diffuso con illuminazione distante arbitraria.

![equazione della luminosità di uscita risultante dall'illuminazione diretta su un oggetto diffuso con illuminazione distante arbitraria](images/prt-theory-eq1.png)

dove:



| Parametro     | Descrizione                                                                                             |
|---------------|---------------------------------------------------------------------------------------------------------|
| RP            | Radiance di uscita in corrispondenza del vertice p. Valutato a ogni vertice sulla rete.                                   |
| p<sub>d</sub> | Albedo della superficie.                                                                              |
| pi            | Costante utilizzata come fattore di normalizzazione per la conservazione dell'energia.                                        |
| L (s)          | Ambiente di illuminazione (Radiance di origine).                                                             |
| ₎ VP ₍ s         | Funzione di visibilità binaria per il punto p. È 1 se il punto può visualizzare la luce, 0 in caso contrario.             |
| HNP ₍ s ₎        | Termine del coseno dalla legge di Lambert. Uguale a Max ((NP · s), 0) dove NP è la normale della superficie al punto p. |
| s             | Variabile che si integra sulla sfera.                                                           |



 

Con le funzioni di base sferica, ad esempio le armoniche sferiche, l'equazione seguente si avvicina all'ambiente di illuminazione.

![equazione dell'ambiente di illuminazione](images/prt-theory-eq2.png)

dove:



| Parametro        | Descrizione                                              |
|------------------|----------------------------------------------------------|
| L (s)             | Ambiente di illuminazione (Radiance di origine).              |
| i                | Intero che somma il numero di funzioni di base. |
| O                | Ordine delle armoniche sferiche.                        |
| l<sub>i</sub>    | Coefficiente.                                           |
| <sub>I/o</sub> | Una funzione di base sulla sfera.                     |



 

La raccolta di questi coefficienti, L', fornisce l'approssimazione ottimale per la funzione L (s) con le funzioni di base Y. La sostituzione e la distribuzione producono la seguente equazione.

![equazione della luminosità di uscita dopo la sostituzione di l (s) e della distribuzione](images/prt-theory-eq3.png)

L'integrale di Y<sub>i (s)</sub>VP ₍ s ₎ HNP ₍ s ₎ è un coefficiente di trasferimento t<sub>pi</sub> utilizzato dal simulatore per ogni vertice sulla rete. Se si sostituisce questa operazione, viene restituita l'equazione seguente.

![equazione della luminosità di uscita dopo la sostituzione del coefficiente di trasferimento](images/prt-theory-eq4.png)

Se si modifica questa notazione Vector, viene restituita l'equazione non compressa seguente per calcolare l'uscita Radiance per ogni canale.

![equazione della luminosità di uscita dopo la modifica alla notazione vettoriale](images/prt-theory-eq5.png)

dove:



| Parametro     | Descrizione                                                                                                                                                                         |
|---------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| RP            | Radiance di uscita in corrispondenza del vertice p.                                                                                                                                                      |
| p<sub>d</sub> | Albedo della superficie.                                                                                                                                                          |
| L            | Il vettore di l<sub>i</sub>e rappresenta la proiezione della luminosità di origine nelle funzioni di base armonica sferica. Si tratta di un vettore Order ² dei coefficienti armonici sferici. |
| TP            | Vettore di trasferimento Order ² per il vertice p. Il simulatore divide i coefficienti di trasferimento di p.                                                                                       |



 

Entrambi questi vettori sono un vettore di ordine ² di coefficienti sferici sferici, quindi si noti che si tratta semplicemente di un prodotto a virgola. A seconda dell'ordine, il punto può essere dispendioso, quindi è possibile usare la compressione. Un algoritmo denominato AP (Clustered Principal Component Analysis) comprime i dati in modo efficiente. Questo consente l'uso di un'approssimazione armonica sferica di ordine superiore che produce ombre più nitide.

AP fornisce l'equazione seguente per approssimare il vettore di trasferimento.

![equazione del vettore di trasferimento approssimato](images/prt-theory-eq6.png)

dove:



| Parametro      | Descrizione                                          |
|----------------|------------------------------------------------------|
| TP             | Vettore di trasferimento per il vertice p.                    |
| MK             | Media per il cluster k.                              |
| j              | Intero che somma il numero di vettori PCA. |
| N              | Numero di vettori PCA.                           |
| w<sub>PJ</sub> | Peso PCA JTH per il punto p.                      |
| B<sub>kJ</sub> | Vettore di base di JTH PCA per il cluster k.              |



 

Un cluster è semplicemente un numero di vertici che condividono lo stesso vettore medio. Come ottenere la media del cluster, i pesi PCA, i vettori di base PCA e gli ID cluster per i vertici vengono descritti di seguito.

La sostituzione di queste due equazioni produce:

![equazione della luminosità di uscita dopo la sostituzione del vettore di trasferimento](images/prt-theory-eq7.png)

La distribuzione del prodotto punto produce quindi l'equazione seguente.

![equazione della luminosità di uscita dopo la distribuzione del prodotto del punto](images/prt-theory-eq8.png)

Poiché entrambe (MK · L') e (B<sub>kJ</sub>· L') sono costanti per vertice, l'esempio calcola questi valori con la CPU e li passa come costanti nel vertex shader; Poiché w<sub>PJ</sub> cambia per ogni vertice, l'esempio archivia i dati per vertice nel buffer dei vertici.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Trasferimento Radiance pre-calcolato](precomputed-radiance-transfer.md)
</dt> </dl>

 

 



