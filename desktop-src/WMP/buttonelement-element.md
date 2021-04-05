---
title: BUTTONelement (elemento)
description: BUTTONelement (elemento)
ms.assetid: 2c1bac51-8aea-4c73-b9b4-4ddbf1e4231b
keywords:
- Windows Media Player Skin, elemento BUTTONelement
- interfacce, elemento BUTTONelement
- BUTTONelement (elemento)
- riferimento per le interfacce, elemento BUTTONelement
- Elements, BUTTONelement
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0d4cc69154821981874f0072f6282f708cc4826d
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103711926"
---
# <a name="buttonelement-element"></a>BUTTONelement (elemento)

L'elemento **ButtonElement** definisce un singolo pulsante all'interno di un elemento **ButtonGroup** padre. Supporta i seguenti attributi. Sono disponibili anche elementi **ButtonElement** predefiniti per praticità.

L'elemento **ButtonElement** supporta gli attributi seguenti.



| Attributo                                      | Descrizione                                                                                                                                                                                                      |
|------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [cursor](buttonelement-cursor.md)             | Specifica o Recupera il valore del cursore **ButtonElement** visualizzato quando il mouse è posizionato sul **pulsante**.                                                                                      |
| [giù](buttonelement-down.md)                 | Specifica o Recupera il valore su o giù del **pulsanteelement**.                                                                                                                                            |
| [downToolTip](buttonelement-downtooltip.md)   | Specifica o Recupera il testo della descrizione comando visualizzato quando il mouse si trova sull'oggetto **ButtonElement** e il **pulsante** è nello stato di inattività.                                                                |
| [index](buttonelement-index.md)               | Recupera l'indice di **ButtonElement** all'interno di **ButtonGroup**.                                                                                                                                         |
| [mappingColor](buttonelement-mappingcolor.md) | Specifica o recupera la chiave di colore che identifica questo **ButtonElement** nel gruppo **ButtonElement** .                                                                                                      |
| [permanenti](buttonelement-sticky.md)             | Specifica o recupera un valore che indica se il **pulsante** è appiccicoso. Quando è appiccicoso, un **pulsante ButtonElement** cambierà gli Stati dopo che è stato fatto clic e rimarrà nel nuovo stato fino a quando non si fa clic di nuovo su. |
| [Descrizione comando](buttonelement-uptooltip.md)       | Specifica o Recupera il testo della descrizione comando visualizzato quando il mouse è posizionato su **ButtonElement** e il **pulsante** è nello stato attivo o attivo.                                                        |



 

L'elemento **ButtonElement** supporta il seguente metodo.



| Metodo                           | Descrizione                                                            |
|----------------------------------|------------------------------------------------------------------------|
| [Clicca](buttonelement-click.md) | Chiama il gestore dell'evento **OnClick** definito per il **pulsante**. |



 

L'elemento **ButtonElement** può implementare i gestori eventi di ambiente. Per altre informazioni, vedere [gestori eventi di ambiente](ambient-event-handlers.md).

L'elemento **ButtonElement** supporta gli attributi di ambiente seguenti: [Enabled](ambientattributes-enabled.md) e [TabStop](ambientattributes-tabstop.md).

Gli effetti predefiniti sono elementi **effettivi** normali con diverse impostazioni degli attributi comuni specificati per impostazione predefinita. Sono disponibili gli elementi **ButtonElement** predefiniti seguenti.



| BUTTONelement predefinito         | Descrizione                                                                                               |
|----------------------------------|-----------------------------------------------------------------------------------------------------------|
| [FFWDELEMENT](ffwdelement.md)   | Un oggetto **ButtonElement** con un gestore eventi **OnClick** incorporato che chiama **Player. Controls. fastForward**. |
| [NEXTELEMENT](nextelement.md)   | Un oggetto **ButtonElement** con un gestore eventi **OnClick** incorporato che chiama **Player. Controls. Next**.        |
| [SOSPENDi](pauseelement.md) | Un oggetto **ButtonElement** con un gestore eventi **OnClick** incorporato che chiama **Player. Controls. pause**.       |
| [PLAYelement](playerelement.md) | **ButtonElement** con un gestore dell'evento **OnClick** incorporato che chiama **Player. Controls. Play**.        |
| [PREC.](prevelement.md)   | Un oggetto **ButtonElement** con un gestore eventi **OnClick** incorporato che chiama **Player. Controls. Previous**.    |
| [REWELEMENT](rewelement.md)     | **ButtonElement** con un gestore dell'evento **OnClick** incorporato che chiama **Player. Controls. Rewind**.      |
| [STOPelement](stopelement.md)   | Un oggetto **ButtonElement** con un gestore eventi **OnClick** incorporato che chiama **Player. Controls. Stop**.        |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Informazioni di riferimento sulla programmazione dell'interfaccia**](skin-programming-reference.md)
</dt> </dl>

 

 




