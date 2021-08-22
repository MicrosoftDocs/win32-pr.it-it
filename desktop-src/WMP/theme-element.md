---
title: Elemento THEME
description: Elemento THEME
ms.assetid: fe7e793e-1774-412c-aed2-721ed2cf1bb3
keywords:
- Windows Media Player, elemento THEME
- skins,theme - elemento
- THEME - elemento
- informazioni di riferimento per le interfaccia, elemento THEME
- elementi, THEME
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0c15091ffa93e3ae64a06979580931c27bdf4c1cd2e26c7acc206d76de8b0fc4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119507391"
---
# <a name="theme-element"></a>Elemento THEME

**L'elemento THEME** è l'elemento a livello padre di un'interfaccia e contiene uno o più elementi **VIEW,** che a loro volta contengono tutti gli altri elementi all'interno di un'interfaccia. All'interno del codice script l'accesso all'elemento **THEME** avviene tramite l'attributo globale del tema anziché tramite un nome specificato da un **attributo id,** che non è supportato dall'elemento **THEME.** 

**L'elemento THEME** supporta gli attributi seguenti.



| Attributo                                | Descrizione                                                                                                                     |
|------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------|
| [Autore](theme-author.md)               | Specifica o recupera il nome dell'autore dell'interfaccia.                                                                      |
| [authorVersion](theme-authorversion.md) | Specifica o recupera il numero di versione dell'interfaccia come assegnato dall'autore.                                                |
| [Copyright](theme-copyright.md)         | Specifica o recupera la stringa di copyright per l'interfaccia.                                                                       |
| [currentViewID](theme-currentviewid.md) | Specifica o recupera l'oggetto **VIEW attualmente visualizzato.**                                                                        |
| [title](theme-title.md)                 | Specifica o recupera il titolo dell'interfaccia.                                                                                   |
| [version](theme-version.md)             | Specifica o recupera il numero Windows Media Player versione per cui è stata modificata l'interfaccia. Può essere impostato solo in fase di progettazione. |



 

**L'elemento THEME** supporta i metodi seguenti.



| Metodo                                         | Descrizione                                                                                                     |
|------------------------------------------------|-----------------------------------------------------------------------------------------------------------------|
| [closeView](theme-closeview.md)               | Chiude un oggetto **VIEW aperto.**                                                                                        |
| [loadPreference](theme-loadpreference.md)     | Carica una preferenza dal Registro di sistema.                                                                           |
| [logString](theme-logstring.md)               | Registra una stringa definita dall'utente nel file degli errori, se la registrazione è abilitata.                                            |
| [openDialog](theme-opendialog.md)             | Apre una finestra di dialogo file.                                                                                        |
| [Openview](theme-openview.md)                 | Apre una **vista** in una nuova finestra.                                                                               |
| [openViewRelative](theme-openviewrelative.md) | Apre un **oggetto VIEW** in una nuova finestra in una posizione iniziale specificata rispetto all'angolo superiore sinistro dell'interfaccia. |
| [Playsound](theme-playsound.md)               | Riproduce il file audio specificato.                                                                                 |
| [savePreference](theme-savepreference.md)     | Salva una preferenza nel Registro di sistema.                                                                             |
| [finestra di dialogo showErrorDialog](theme-showerrordialog.md)   | Visualizza la finestra di dialogo di errore standard.                                                                         |



 

**L'elemento THEME** non supporta i gestori eventi.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Informazioni di riferimento sulla programmazione dell'interfaccia**](skin-programming-reference.md)
</dt> </dl>

 

 




