---
title: Aggiunta del pulsante Chiudielement
description: Aggiunta del pulsante Chiudielement
ms.assetid: 18f0ee9d-b0d4-4134-8dd6-6ece480b2818
keywords:
- creazione di interfacce, elemento BUTTONelement
- Windows Media Player Skin, elemento BUTTONelement
- interfacce, elemento BUTTONelement
- file di definizione dell'interfaccia, elemento BUTTONelement
- BUTTONelement (elemento)
- Elements, BUTTONelement
- creazione di interfacce, chiusura di pulsanti
- Interfacce Media Player di Windows, pulsanti Chiudi
- interfacce, pulsanti Chiudi
- file di definizione dell'interfaccia, pulsanti Chiudi
- Chiudi pulsanti
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 40716d4094d23eaf6ab86414f37c0778cc8d89cf
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104221525"
---
# <a name="adding-the-close-buttonelement"></a>Aggiunta del pulsante Chiudielement

Il pulsante Chiudi è concettualmente simile al pulsante Riproduci, ma dispone di codici e colori diversi.

Inserire il codice del **pulsante** di chiusura dopo la parentesi angolare di chiusura del **pulsante** di riproduzione.


```C++
        <BUTTONELEMENT
            mappingColor = "#FF0000"
            upToolTip = "Close"
            onClick="JScript: view.close();" />

```



Gli attributi seguenti vengono usati per definire il **pulsante ButtonElement** per il pulsante Chiudi:

**mappingColor**

Si tratta del valore del colore dell'area nel file di grafica di mapping creato in precedenza. In questo caso si tratta del colore rosso a tinta unita. Questo attributo è obbligatorio per qualsiasi **pulsanteelement**. Definendo questo colore, si indica a Windows Media Player di associare questa area dei colori al codice XML di questo pulsante.

**Descrizione comando**

Definisce il testo che verrà visualizzato quando l'utente passa il puntatore del mouse sul pulsante. Si tratta dello stesso pulsante Riproduci, ad eccezione del fatto che è denominato "close".

**onClick**

Definisce l'evento che si verifica quando si fa clic con il mouse sul pulsante. Il valore di questo attributo evento è denominato gestore eventi e sarà una riga di codice Microsoft JScript o una funzione JScript in un file di testo esterno caricato dall'attributo **loadScript** di una **vista**. In questo caso, il codice JScript chiama il metodo **Close** dell'elemento **View** usando la **visualizzazione** dell'attributo globale, che chiude la visualizzazione e arresta Windows Media Player.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Creazione del file di definizione dell'interfaccia**](creating-the-skin-definition-file.md)
</dt> </dl>

 

 




