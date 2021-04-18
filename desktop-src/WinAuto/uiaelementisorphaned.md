---
title: UiaElementIsOrphaned
description: UiaElementIsOrphaned
ms.assetid: F85F08E7-5A9C-4F08-B680-8B251D51168A
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f0ec0861a586fd5275a674d9ef8ba6a0e72364b2
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "106298383"
---
# <a name="uiaelementisorphaned"></a>UiaElementIsOrphaned

## <a name="text"></a>Testo

L'elemento è un oggetto AutomationElement orfano nell'albero

## <a name="type"></a>Tipo

Errore

## <a name="description"></a>Descrizione

L'indirizzo dell'interfaccia [**IUIAutomationElement**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationelement) dell'oggetto ottenuto per le coordinate specificate è un riferimento a un elemento orfano nell'albero degli elementi.

Questo problema rappresenta un problema per gli utenti che si affidano a un lettore di schermate e a una tastiera per la navigazione perché gli elementi verranno considerati invisibili e non verranno annunciati all'utente.

## <a name="possible-causes"></a>Possibili cause

-   Interazione dell'utente durante la verifica, ad esempio lo spostare lo stato attivo su un HWND non di destinazione, interferisce con il processo di verifica.
-   Implementazione di automazione interfaccia utente non corretta o non valida.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**IUIAutomationElement.ElementFromPoint**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomation-elementfrompoint)
</dt> </dl>

 

 




