---
title: Per gli elementi DragPattern/DragDropPattern è necessario il nome
description: Per gli elementi DragPattern/DragDropPattern è necessario il nome
ms.assetid: DEF58FB2-5830-4162-87D0-40DEC1237529
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9ecc60eeca59f4754f9c160696cdfa2556c36a5e
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "106297613"
---
# <a name="dragpatterndragdroppattern-elements-requires-name"></a>Per gli elementi DragPattern/DragDropPattern è necessario il nome

## <a name="text"></a>Testo

Gli elementi che supportano il trascinamento della selezione devono avere un set ' name ' valido

## <a name="type"></a>Tipo

Errore

## <a name="description"></a>Descrizione

L'elemento supporta [**IUIAutomationDragPattern**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationdragpattern) o [**IUIAutomationDropTargetPattern**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationdroptargetpattern), ma non è impostato un nome valido.

Questo problema causa problemi per gli utenti che si affidano a un lettore di schermate. L'utente non sarà in grado di stabilire quale sia l'oggetto perché la lettura dello schermo non consente di leggere un nome valido per distinguere l'elemento durante il trascinamento.

## <a name="possible-causes"></a>Possibili cause

-   All'elemento o al relativo padre è assegnato un nome o un'etichetta non correttamente assegnati.
-   Uno sviluppatore non è A conoscenza dello schermo che legge i nomi e i tipi di controllo.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**IAccessible:: Get \_ accName**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accname)
</dt> <dt>

[Proprietà Name](name-property.md)
</dt> <dt>

[**\_NAMEPROPERTYID UIA**](uiauto-automation-element-propids.md)
</dt> <dt>

[**IUIAutomationElement:: currentname**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-get_currentname)
</dt> </dl>

 

 




