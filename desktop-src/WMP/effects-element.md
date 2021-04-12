---
title: EFFECTs-elemento
description: EFFECTs-elemento
ms.assetid: ada3c452-1bc6-4700-8048-1a4b2ee00aeb
keywords:
- Windows Media Player Skin, elemento EFFECTs
- interfacce, elemento EFFECTs
- EFFECTs-elemento
- riferimento per interfacce, elemento EFFECTs
- elementi, effetti
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9e4b6fdcde74288b0dd4215732d1e5b6a281154f
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104395335"
---
# <a name="effects-element"></a>EFFECTs-elemento

L'elemento **Effects** consente di organizzare e modificare le visualizzazioni utilizzando i seguenti attributi e metodi. Viene inoltre fornito un elemento **Effects** predefinito per praticità.

L'elemento **Effects** supporta gli attributi seguenti.



| Attributo                                                        | Descrizione                                                                                                                                                                                                                                          |
|------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [allowAll](effects-allowall.md)                                 | Specifica o recupera un valore che indica se includere tutte le visualizzazioni nel registro di sistema.                                                                                                                                                 |
| [currentEffect](effects-currenteffect.md)                       | Specifica o recupera la visualizzazione corrente.                                                                                                                                                                                                    |
| [currentEffectPresetCount](effects-currenteffectpresetcount.md) | Recupera il numero di set di impostazioni disponibili per la visualizzazione corrente.                                                                                                                                                                                 |
| [currentEffectTitle](effects-currenteffecttitle.md)             | Recupera il titolo visualizzato della visualizzazione corrente.                                                                                                                                                                                            |
| [currentEffectType](effects-currenteffecttype.md)               | Recupera il nome del registro di sistema della visualizzazione corrente.                                                                                                                                                                                            |
| [currentPreset](effects-currentpreset.md)                       | Specifica o Recupera il set di impostazioni corrente della visualizzazione corrente.                                                                                                                                                                              |
| [currentPresetTitle](effects-currentpresettitle.md)             | Recupera il titolo del set di impostazioni corrente della visualizzazione corrente.                                                                                                                                                                              |
| [effectCanGoFullScreen](effects-effectcangofullscreen.md)       | Recupera un valore che indica se la visualizzazione corrente può essere visualizzata a schermo intero.                                                                                                                                                         |
| [effectCount](effects-effectcount.md)                           | Recupera il numero di visualizzazioni disponibili.                                                                                                                                                                                                    |
| [effectHasPropertyPage](effects-effecthaspropertypage.md)       | Recupera un valore che indica se la visualizzazione corrente include una pagina delle proprietà.                                                                                                                                                                  |
| [Schermo intero](effects-fullscreen.md)                             | Specifica o recupera un valore che indica se la visualizzazione corrente è visualizzata a schermo intero. Può essere impostato solo in fase di esecuzione.                                                                                                                   |
| [finestra](effects-windowed.md)                                 | Specifica o recupera un valore che indica se la visualizzazione sarà finestra o senza finestra, ovvero se l'intero rettangolo del controllo sarà visibile in qualsiasi momento o se può essere ritagliato. Può essere impostato solo in fase di progettazione. |



 

L'elemento **Effects** supporta i metodi seguenti.



| Metodo                                       | Descrizione                                                                                                       |
|----------------------------------------------|-------------------------------------------------------------------------------------------------------------------|
| [effectTitle](effects-effecttitle.md)       | Recupera il nome descrittivo della visualizzazione con l'indice del registro di sistema specificato.                               |
| [effectType](effects-effecttype.md)         | Recupera il nome del registro di sistema della visualizzazione con l'indice del registro di sistema specificato.                               |
| [avanti](effects-next.md)                     | Visualizza il set di impostazioni di visualizzazione successivo, se necessario, andando alla visualizzazione successiva.                            |
| [nextEffect](effects-nexteffect.md)         | Visualizza il primo set di impostazioni della visualizzazione successiva, ignorando le impostazioni predefinite.                                |
| [nextPreset](effects-nextpreset.md)         | Visualizza il set di impostazioni successivo della visualizzazione corrente.                                                            |
| [previous](effects-previous.md)             | Visualizza il set di impostazioni di visualizzazione precedente, se necessario, fino all'ultimo set di impostazioni della visualizzazione precedente. |
| [previousEffect](effects-previouseffect.md) | Visualizza la visualizzazione precedente, ignorando i set di impostazioni.                                                            |
| [previousPreset](effects-previouspreset.md) | Visualizza il set di impostazioni precedente della visualizzazione corrente.                                                        |
| [impostazioni](effects-settings.md)             | Visualizza la pagina attributo per la visualizzazione corrente, se presente.                                            |



 

L'elemento **Effects** supporta gli attributi di ambiente e può implementare i gestori eventi di ambiente. Per altre informazioni, vedere [attributi di ambiente](ambient-attributes.md) e [gestori di eventi di ambiente](ambient-event-handlers.md).

Gli effetti predefiniti sono elementi **effettivi** normali con diverse impostazioni degli attributi comuni specificati per impostazione predefinita. Sono disponibili gli effetti predefiniti seguenti.



| EFFETTI predefiniti           | Descrizione                                                         |
|------------------------------|---------------------------------------------------------------------|
| [WMPEFFECTS](wmpeffects.md) | Elemento **Effects** che consente di scorrere gli effetti disponibili. |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Informazioni di riferimento sulla programmazione dell'interfaccia**](skin-programming-reference.md)
</dt> </dl>

 

 




