---
title: Elemento EFFECTS
description: Elemento EFFECTS
ms.assetid: ada3c452-1bc6-4700-8048-1a4b2ee00aeb
keywords:
- Windows Media Player, elemento EFFECTS
- skins,EFFECTS - elemento
- EFFECTS - elemento
- informazioni di riferimento per le interfaccia, elemento EFFECTS
- elementi, EFFETTI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a859414ffae934cafaa0c35b6b364eb42a5795bbeeef637857a0d81f47623379
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119651141"
---
# <a name="effects-element"></a>Elemento EFFECTS

**L'elemento EFFECTS** consente di organizzare e modificare le visualizzazioni usando gli attributi e i metodi seguenti. Per praticità **viene fornito** anche un elemento EFFECTS predefinito.

**L'elemento EFFECTS** supporta gli attributi seguenti.



| Attributo                                                        | Descrizione                                                                                                                                                                                                                                          |
|------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [allowAll](effects-allowall.md)                                 | Specifica o recupera un valore che indica se includere tutte le visualizzazioni nel registro.                                                                                                                                                 |
| [currentEffect](effects-currenteffect.md)                       | Specifica o recupera la visualizzazione corrente.                                                                                                                                                                                                    |
| [currentEffectPresetCount](effects-currenteffectpresetcount.md) | Recupera il numero di set di impostazioni disponibili per la visualizzazione corrente.                                                                                                                                                                                 |
| [currentEffectTitle](effects-currenteffecttitle.md)             | Recupera il titolo visualizzato della visualizzazione corrente.                                                                                                                                                                                            |
| [currentEffectType](effects-currenteffecttype.md)               | Recupera il nome del registro della visualizzazione corrente.                                                                                                                                                                                            |
| [currentPreset](effects-currentpreset.md)                       | Specifica o recupera il set di impostazioni corrente della visualizzazione corrente.                                                                                                                                                                              |
| [currentPresetTitle](effects-currentpresettitle.md)             | Recupera il titolo del set di impostazioni corrente della visualizzazione corrente.                                                                                                                                                                              |
| [effectCanGoFullScreen](effects-effectcangofullscreen.md)       | Recupera un valore che indica se la visualizzazione corrente può essere visualizzata a schermo intero.                                                                                                                                                         |
| [effectCount](effects-effectcount.md)                           | Recupera il numero di visualizzazioni disponibili.                                                                                                                                                                                                    |
| [effectHasPropertyPage](effects-effecthaspropertypage.md)       | Recupera un valore che indica se la visualizzazione corrente dispone di una pagina delle proprietà.                                                                                                                                                                  |
| [Fullscreen](effects-fullscreen.md)                             | Specifica o recupera un valore che indica se la visualizzazione corrente viene visualizzata a schermo intero. Può essere impostato solo in fase di esecuzione.                                                                                                                   |
| [Finestra](effects-windowed.md)                                 | Specifica o recupera un valore che indica se la visualizzazione sarà finestra o senza finestra, ad esempio se l'intero rettangolo del controllo sarà sempre visibile o se può essere ritagliato. Può essere impostato solo in fase di progettazione. |



 

**L'elemento EFFECTS** supporta i metodi seguenti.



| Metodo                                       | Descrizione                                                                                                       |
|----------------------------------------------|-------------------------------------------------------------------------------------------------------------------|
| [effectTitle](effects-effecttitle.md)       | Recupera il nome descrittivo della visualizzazione con l'indice del Registro di sistema specificato.                               |
| [effectType](effects-effecttype.md)         | Recupera il nome del registro della visualizzazione con l'indice del Registro di sistema specificato.                               |
| [avanti](effects-next.md)                     | Visualizza il set di impostazioni di visualizzazione successivo, passando alla visualizzazione successiva, se necessario.                            |
| [nextEffect](effects-nexteffect.md)         | Visualizza il primo set di impostazioni della visualizzazione successiva, ignorando i set di impostazioni.                                |
| [nextPreset](effects-nextpreset.md)         | Visualizza il set di impostazioni successivo della visualizzazione corrente.                                                            |
| [previous](effects-previous.md)             | Visualizza il set di impostazioni di visualizzazione precedente, passando all'ultimo set di impostazioni della visualizzazione precedente, se necessario. |
| [previousEffect](effects-previouseffect.md) | Visualizza la visualizzazione precedente, ignorando i set di impostazioni.                                                            |
| [previousPreset](effects-previouspreset.md) | Visualizza il set di impostazioni precedente della visualizzazione corrente.                                                        |
| [impostazioni](effects-settings.md)             | Visualizza la pagina degli attributi per la visualizzazione corrente, se presente.                                            |



 

**L'elemento EFFECTS** supporta gli attributi di ambiente e può implementare i gestori eventi di ambiente. Per altre informazioni, vedere [Attributi di ambiente e](ambient-attributes.md) Gestori eventi di [ambiente.](ambient-event-handlers.md)

Gli effetti predefiniti sono elementi **EFFECTS** normali con diverse impostazioni di attributi comuni specificate per impostazione predefinita. Sono disponibili gli effetti predefiniti seguenti.



| Effetti predefiniti           | Descrizione                                                         |
|------------------------------|---------------------------------------------------------------------|
| [WMPEFFECTS](wmpeffects.md) | Elemento **EFFECTS** che scorre gli effetti disponibili. |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Informazioni di riferimento sulla programmazione dell'interfaccia**](skin-programming-reference.md)
</dt> </dl>

 

 




