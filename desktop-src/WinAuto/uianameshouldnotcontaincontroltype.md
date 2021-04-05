---
title: UiaNameShouldNotContainControlType
description: UiaNameShouldNotContainControlType
ms.assetid: 96F7A5FC-1879-4706-9E67-5B43D57F7281
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d6178ca4cd4c4b2ed0deb0070116b597ba3bd1bc
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103855838"
---
# <a name="uianameshouldnotcontaincontroltype"></a>UiaNameShouldNotContainControlType

## <a name="text"></a>Testo

Il nome dell'elemento ( {0} ) non deve contenere il testo di ControlType ( {1} )

## <a name="type"></a>Tipo

Avviso

## <a name="description"></a>Descrizione

Il nome di un elemento incorpora il tipo di controllo UIA. Questo avviso può verificarsi, ad esempio, se la proprietà nome dell'interfaccia utente per un elemento con il tipo di controllo Button è impostata su "My Button".

Questo problema causa problemi per gli utenti che si affidano a un lettore di schermate e a una tastiera per la navigazione, perché il tipo di controllo verrà letto due volte o potrebbe non essere pronunciabile o non intuitivo per gli utenti.

## <a name="possible-causes"></a>Possibili cause

-   All'elemento o al relativo padre è assegnato un nome o un'etichetta non corretta.
-   L'elemento o il relativo padre ha un nome predefinito che non è stato modificato in un nome descrittivo. Ad esempio, button1.
-   Uno sviluppatore non è A conoscenza dello schermo che legge i nomi e i tipi di controllo.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**\_NAMEPROPERTYID UIA**](uiauto-automation-element-propids.md)
</dt> <dt>

[**IUIAutomationElement:: currentname**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-get_currentname)
</dt> </dl>

 

 




