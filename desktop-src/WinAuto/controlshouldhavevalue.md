---
title: ControlShouldHaveValue
description: ControlShouldHaveValue
ms.assetid: 90C37CC5-21D2-4D26-B6D9-2C95C52127BF
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8b078712319ffcfde386df519837ba467ca2fcf4
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104221593"
---
# <a name="controlshouldhavevalue"></a>ControlShouldHaveValue

## <a name="text"></a>Testo

Un controllo con ruolo {0} deve avere un valore ma Get \_ accValue non è implementato

## <a name="type"></a>Tipo

Errore

## <a name="description"></a>Descrizione

Un elemento non fornisce un valore come previsto in base al ruolo MSAA assegnato, a indicare che l'elemento non ha implementato il metodo [**get \_ accValue**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accvalue) . I ruoli MSAA seguenti, ad esempio, devono fornire un valore.

-   \_ \_ casella combinata sistema ruolo
-   \_IPAddress sistema \_ ruolo
-   \_collegamento del sistema ruolo \_
-   \_OUTLINEITEM di sistema ruolo \_
-   \_PROGRESSBAR del sistema di ruolo \_
-   \_dispositivo di \_ scorrimento sistema ruolo
-   \_SPINBUTTON di sistema ruolo \_
-   \_barra di \_ scorrimento sistema ruolo
-   \_testo del sistema ruolo \_

Questo problema rappresenta un problema per gli utenti che si affidano a un lettore di schermate e a una tastiera per la navigazione, perché un elemento con un valore intrinseco deve essere in grado di segnalare tale valore a un utente.

## <a name="possible-causes"></a>Possibili cause

Per l'elemento o per il relativo padre è impostato un ruolo MSAA in modo non appropriato.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**IAccessible:: Get \_ accRole**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accrole)
</dt> <dt>

[**Ruoli oggetto**](object-roles.md)
</dt> </dl>

 

 




