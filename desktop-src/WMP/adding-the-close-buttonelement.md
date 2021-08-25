---
title: Aggiunta di BUTTONELEMENT di chiusura
description: Aggiunta di BUTTONELEMENT di chiusura
ms.assetid: 18f0ee9d-b0d4-4134-8dd6-6ece480b2818
keywords:
- creazione di skin, elemento BUTTONELEMENT
- Windows Media Player skin, elemento BUTTONELEMENT
- skins,ELEMENTO BUTTONELEMENT
- File di definizione dell'interfaccia, elemento BUTTONELEMENT
- Elemento BUTTONELEMENT
- elementi,BUTTONELEMENT
- creazione di skin, pulsanti Chiudi
- Windows Media Player skin, pulsanti Chiudi
- skins,pulsanti Chiudi
- file di definizione dell'interfaccia, pulsanti Chiudi
- Pulsanti di chiusura
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bf5d2a85e43ae4a664504c213d182b396707ff9cfa663187e7f153fa4cc154e8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119765477"
---
# <a name="adding-the-close-buttonelement"></a>Aggiunta di BUTTONELEMENT di chiusura

Il pulsante Chiudi è simile nel concetto al pulsante Riproduci, ma ha codici e colori diversi.

Inserire il codice **CLOSE BUTTONELEMENT** dopo la parentesi uncinata di chiusura di **Play BUTTONELEMENT**.


```C++
        <BUTTONELEMENT
            mappingColor = "#FF0000"
            upToolTip = "Close"
            onClick="JScript: view.close();" />

```



Gli attributi seguenti vengono usati per definire **BUTTONELEMENT** per il pulsante Chiudi:

**mappingColor**

Si tratta del valore del colore dell'area nel file di mapping creato in precedenza. In questo caso è il colore rosso a tinta unita. Questo attributo è obbligatorio per **qualsiasi ELEMENTO BUTTONELEMENT.** Definendo questo colore, si indica Windows Media Player di associare questa area colori al codice XML di questo pulsante.

**upToolTip**

Definisce il testo che verrà visualizzato quando l'utente passa il mouse sul pulsante. È uguale al pulsante Riproduci, ad eccezione del fatto che è contrassegnato con l'etichetta "Chiudi".

**Onclick**

Definisce l'evento che si verifica quando il mouse fa clic sul pulsante. Il valore di questo attributo dell'evento viene chiamato gestore eventi e sarà una riga di codice Microsoft JScript o una funzione JScript in un file di testo esterno caricato dall'attributo **loadScript** di un **oggetto VIEW.** In questo caso, il JScript chiama il metodo **close** dell'elemento **VIEW** usando la visualizzazione degli attributi globale **,** che chiude la visualizzazione e arresta Windows Media Player.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Creazione del file di definizione dell'interfaccia**](creating-the-skin-definition-file.md)
</dt> </dl>

 

 




