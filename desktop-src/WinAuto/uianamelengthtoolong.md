---
title: UiaNameLengthTooLong
description: UiaNameLengthTooLong
ms.assetid: 01AF3F1E-9A3F-48B4-8219-6E80BAFC82EE
keywords:
- Identificatore UIA_NamePropertyId AutomationElement. proprietà NameProperty
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6ab786b7167dab4a25384ce3abe2509babcf1f82
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104396670"
---
# <a name="uianamelengthtoolong"></a>UiaNameLengthTooLong

## <a name="text"></a>Testo

Il nome dell'elemento non deve restituire una stringa più lunga di un {0} carattere

## <a name="type"></a>Tipo

Errore

## <a name="description"></a>Descrizione

Il nome di un elemento contiene troppi caratteri. Ad esempio, il metodo [**IUIAutomationElement:: currentname**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-get_currentname) usato per recuperare il nome dell'elemento UIA di un elemento restituisce una stringa superiore al limite.

Questo problema causa problemi per gli utenti che si affidano a un lettore di schermate e a una tastiera per la navigazione, perché un elemento potrebbe avere un nome non pronunciabile e non intuitivo.

## <a name="possible-causes"></a>Possibili cause

All'elemento o al relativo padre è assegnato un nome o un'etichetta non corretta.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**\_NAMEPROPERTYID UIA**](uiauto-automation-element-propids.md)
</dt> <dt>

[**IUIAutomationElement:: currentname**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-get_currentname)
</dt> </dl>

 

 




