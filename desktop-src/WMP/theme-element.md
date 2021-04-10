---
title: Elemento THEME
description: Elemento THEME
ms.assetid: fe7e793e-1774-412c-aed2-721ed2cf1bb3
keywords:
- Windows Media Player Skin, elemento THEME
- Skin, elemento THEME
- Elemento THEME
- riferimento per le interfacce, elemento del tema
- elementi, tema
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b8cd0d40b4b020cf5416569417401af9e4f3a33b
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103855761"
---
# <a name="theme-element"></a>Elemento THEME

L'elemento **Theme** è l'elemento a livello padre di un'interfaccia e contiene uno o più elementi **View** , che a loro volta contengono tutti gli altri elementi all'interno di un'interfaccia. All'interno del codice di script, l'accesso all'elemento del **tema** viene effettuato tramite l'attributo globale del **tema** anziché tramite un nome specificato da un attributo **ID** , che non è supportato dall'elemento **theme** .

L'elemento **Theme** supporta gli attributi seguenti.



| Attributo                                | Descrizione                                                                                                                     |
|------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------|
| [autore](theme-author.md)               | Specifica o Recupera il nome dell'autore dell'interfaccia.                                                                      |
| [authorVersion](theme-authorversion.md) | Specifica o Recupera il numero di versione dell'interfaccia in base a quanto assegnato dall'autore.                                                |
| [Copyright](theme-copyright.md)         | Specifica o recupera la stringa del copyright per l'interfaccia.                                                                       |
| [currentViewID](theme-currentviewid.md) | Specifica o recupera la **visualizzazione** attualmente visualizzata.                                                                        |
| [title](theme-title.md)                 | Specifica o Recupera il titolo dell'interfaccia.                                                                                   |
| [version](theme-version.md)             | Specifica o Recupera il numero di versione di Windows Media Player per cui è stata creata l'interfaccia. Può essere impostato solo in fase di progettazione. |



 

L'elemento **Theme** supporta i metodi seguenti.



| Metodo                                         | Descrizione                                                                                                     |
|------------------------------------------------|-----------------------------------------------------------------------------------------------------------------|
| [closeView](theme-closeview.md)               | Chiude una **visualizzazione** aperta.                                                                                        |
| [loadPreference](theme-loadpreference.md)     | Carica una preferenza dal registro di sistema.                                                                           |
| [logString](theme-logstring.md)               | Registra una stringa definita dall'utente nel file degli errori, se la registrazione è abilitata.                                            |
| [openDialog](theme-opendialog.md)             | Apre una finestra di dialogo file.                                                                                        |
| [openView](theme-openview.md)                 | Apre una **vista** in una nuova finestra.                                                                               |
| [openViewRelative](theme-openviewrelative.md) | Apre una **vista** in una nuova finestra in corrispondenza della posizione iniziale specificata rispetto all'angolo superiore sinistro dell'interfaccia. |
| [playSound](theme-playsound.md)               | Riproduce il file audio specificato.                                                                                 |
| [savePreference](theme-savepreference.md)     | Salva una preferenza nel registro di sistema.                                                                             |
| [showErrorDialog](theme-showerrordialog.md)   | Consente di visualizzare la finestra di dialogo errore standard.                                                                         |



 

L'elemento **Theme** non supporta i gestori eventi.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Informazioni di riferimento sulla programmazione dell'interfaccia**](skin-programming-reference.md)
</dt> </dl>

 

 




