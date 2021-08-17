---
description: Per comprendere in modo completo uno shader che implementa PRT, è utile derivare la formula che lo shader usa per calcolare la luminosità dell'uscita.
ms.assetid: 66876e9e-cde1-4d04-9b31-30be1c115e6b
title: Equazioni PRT (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bcd3dc716349ce46d4e678f0e408e5c964eb5f01d633649e3d512db6115c0267
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118798172"
---
# <a name="prt-equations-direct3d-9"></a>Equazioni PRT (Direct3D 9)

Per comprendere in modo completo uno shader che implementa PRT, è utile derivare la formula che lo shader usa per calcolare la luminosità dell'uscita.

Per iniziare, l'equazione seguente è l'equazione generale per calcolare la luminosità dell'uscita risultante dall'illuminazione diretta su un oggetto diffuso con illuminazione arbitraria distante.

![equazione della luminosità di uscita risultante dall'illuminazione diretta su un oggetto diffuso con illuminazione arbitraria distante](images/prt-theory-eq1.png)

dove:



| Parametro     | Descrizione                                                                                             |
|---------------|---------------------------------------------------------------------------------------------------------|
| Rp            | Raggio di uscita al vertice p. Valutato in corrispondenza di ogni vertice della mesh.                                   |
| p<sub>d</sub> | Albedo della superficie.                                                                              |
| pi            | Costante, usata come fattore di normalizzazione della normalizzazione della energia.                                        |
| L(s)          | Ambiente di illuminazione (sorgente).                                                             |
| Vp₍s₎         | Funzione di visibilità binaria per il punto p. È 1 se il punto può vedere la luce, 0 in caso contrario.             |
| Hnp₍s₎        | Termine coseno dalla legge di Lambert. Uguale a max((Np· s), 0) dove Np è la normale della superficie al punto p. |
| s             | Variabile che si integra sulla sfera.                                                           |



 

Usando funzioni di base sferiche, ad esempio sferiche ariche, l'equazione seguente approssima l'ambiente di illuminazione.

![equazione dell'ambiente di illuminazione](images/prt-theory-eq2.png)

dove:



| Parametro        | Descrizione                                              |
|------------------|----------------------------------------------------------|
| L(s)             | Ambiente di illuminazione (sorgente).              |
| i                | Intero che somma il numero di funzioni di base. |
| O                | Ordine delle armonici sferiche.                        |
| l<sub>i</sub>    | Coefficiente.                                           |
| Y<sub>i(s)</sub> | Alcune funzioni di base sulla sfera.                     |



 

La raccolta di questi coefficienti, L', fornisce l'approssimazione ottimale per la funzione L(s) con le funzioni di base Y. La sostituzione e la distribuzione producono l'equazione seguente.

![equazione della radice di uscita dopo la sostituzione di l/e e la distribuzione](images/prt-theory-eq3.png)

L₍ integrale di Y i₍s₎Hnp₍s₎ è un coefficiente di trasferimento t<sub>pi</sub> greco che il simulatore pre-ricalcola per ogni vertice nella mesh.<sub></sub> La sostituzione di questo metodo produce l'equazione seguente.

![equazione della radice di uscita dopo la sostituzione del coefficiente di trasferimento](images/prt-theory-eq4.png)

La modifica della notazione vettoriale produce l'equazione non compressa seguente per calcolare la radice di uscita per ogni canale.

![equazione della radice di uscita dopo il passaggio alla notazione vettoriale](images/prt-theory-eq5.png)

dove:



| Parametro     | Descrizione                                                                                                                                                                         |
|---------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Rp            | Raggio di uscita al vertice p.                                                                                                                                                      |
| p<sub>d</sub> | Albedo della superficie.                                                                                                                                                          |
| L'            | Il vettore di l<sub>i</sub>e è la proiezione della radice di origine nelle funzioni di base sferiche aricali. Si tratta di un vettore di ordinamento dei coefficienti aricali sferici. |
| Tp            | Vettore di trasferimento order più per il vertice p. Il simulatore divide i coefficienti di trasferimento per p.                                                                                       |



 

Entrambi questi vettori sono un vettore di ordinamento dei coefficienti sferici aricali, quindi si noti che si tratta semplicemente di un prodotto punto. A seconda dell'ordine, il punto può essere costoso, quindi è possibile usare la compressione. Un algoritmo denominato Clustered Principal Component Analysis (CPCA) comprime in modo efficiente i dati. Ciò consente l'uso di un'approssimazione sferica sferica di ordine superiore che comporta ombreggiature più nitide.

CPCA fornisce l'equazione seguente per approssimare il vettore di trasferimento.

![equazione del vettore di trasferimento approssimativo](images/prt-theory-eq6.png)

dove:



| Parametro      | Descrizione                                          |
|----------------|------------------------------------------------------|
| Tp             | Vettore di trasferimento per il vertice p.                    |
| Mk             | Media per il cluster k.                              |
| j              | Intero che somma il numero di vettori PCA. |
| N              | Numero di vettori PCA.                           |
| w<sub>pj</sub> | Peso jth PCA per il punto p.                      |
| B<sub>kj</sub> | Vettore di base JTH PCA per il cluster k.              |



 

Un cluster è semplicemente un numero di vertici che condividono lo stesso vettore medio. Di seguito viene descritto come ottenere la media del cluster, i pesi PCA, i vettori di base PCA e gli ID cluster per i vertici.

La sostituzione di queste due equazioni produce:

![equazione della radice di uscita dopo la sostituzione del vettore di trasferimento](images/prt-theory-eq7.png)

La distribuzione del prodotto punto produce quindi l'equazione seguente.

![equazione della radice di uscita dopo la distribuzione del prodotto punto](images/prt-theory-eq8.png)

Poiché entrambi (Mk· L') e (B<sub>kj</sub>· L') sono costanti per vertice, il campione calcola questi valori con la CPU e li passa come costanti nel vertex shader; Poiché w<sub>pj</sub> cambia per ogni vertice, l'esempio archivia i dati per vertice nel buffer dei vertici.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Trasferimento di radiance pre-ricalcolato](precomputed-radiance-transfer.md)
</dt> </dl>

 

 



