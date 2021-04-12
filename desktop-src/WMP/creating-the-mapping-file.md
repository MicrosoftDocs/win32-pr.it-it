---
title: Creazione del file di mapping
description: Creazione del file di mapping
ms.assetid: d882cd5b-1404-4dfd-8b51-a61e1505fae1
keywords:
- creazione di interfacce, mapping di file
- Interfacce di Media Player di Windows, file di immagine
- interfacce, file di immagine
- file per Skins, Art
- file di grafica per interfacce, mapping di immagini
- Interfacce di Media Player di Windows, mapping di immagini
- interfacce, mapping di immagini
- mapping di immagini in interfacce
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e49b71682f48ecdba098f76a9e27f656b27d5fe8
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104395339"
---
# <a name="creating-the-mapping-file"></a>Creazione del file di mapping

Una volta creati i componenti del file dell'immagine principale, è relativamente semplice creare un file di mapping. Il nuovo file di mapping viene creato combinando l'arte dei livelli di due pulsanti già creati.

1.  Sarà necessario eseguire i due pulsanti creati per il file di immagine principale e copiarli in un nuovo livello. Usare i passaggi seguenti: copiare il livello del pulsante Chiudi, rimuovere gli effetti dei livelli e rinominarlo "Chiudi mappa". L'arte dovrebbe apparire piatta senza smussature.
2.  Usare la selezione colori per creare un colore di primo piano di rosso puro. Verificare che il valore del numero di colore sia " \# FF0000". Usare quindi lo strumento Secchiello per riempire l'interno del cerchio del livello di chiusura della mappa.
3.  Copiare il livello del pulsante Play, rimuovere gli effetti dei livelli e rinominarlo "Play map". Anche in questo caso, l'arte dovrebbe apparire piatta. Non si desiderano effetti nel livello di mapping poiché si definiscono solo le aree della bitmap che Windows Media Player utilizzerà per determinare il punto in cui il mouse esegue un'azione e l'operazione che si desidera eseguire.
4.  Usare la selezione colori per creare un colore di primo piano di verde puro. Verificare che il valore del numero di colore sia " \# 00FF00". Usare quindi lo strumento Secchiello per riempire l'interno del cerchio del livello mappa di riproduzione.

A questo punto è possibile creare il file di grafica di mapping. Nascondi tutti i livelli, quindi Mostra solo i livelli seguenti, in questo ordine (dall'alto verso il basso):

Esegui mapping

Chiudi mappa

Salvare in un nuovo file usando il comando Salva copia dal menu file. Selezionare l'opzione BMP nella parte Salva come della finestra di dialogo Salva copia e digitare il nome di un file a cui si fa riferimento in un secondo momento nel file di definizione dell'interfaccia personalizzata. Idealmente deve trovarsi nella stessa directory del file di definizione dell'interfaccia personalizzata. Ad esempio, è possibile chiamare questo file map.bmp. Scegliere le impostazioni predefinite e salvare il file.

Il file di mapping dovrebbe avere un aspetto simile a quello illustrato nella figura seguente.

![mapping file](images/g01map.png)

Come si può intuire, l'area verde verrà utilizzata per determinare quando creare Media Player Windows e l'area rossa indica che l'arresto. È possibile utilizzare due colori qualsiasi, purché vengano utilizzati i numeri di colore quando si configura il file di definizione dell'interfaccia. Assicurarsi che i colori della mappa siano colori puri per l'area che si vuole usare e che abbiano bordi distinti. Un colore puro è uno in cui ogni singolo pixel nell'area ha lo stesso valore di colore. L'uso di un effetto può offuscare o falsare il bordo, modificando leggermente i colori di alcuni pixel. Il file di mapping viene visualizzato solo dal mouse, non da un utente, quindi non infastidirlo e rimuovere gli effetti dei livelli che potrebbero essere stati trasferiti dagli altri livelli.

Quando si salva il file, il nome file scelto verrà usato in un secondo momento come valore per l'attributo **mappingImage** dell'elemento **ButtonGroup** nel file di definizione dell'interfaccia personalizzata.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Creazione della prima interfaccia**](building-your-first-skin.md)
</dt> </dl>

 

 




