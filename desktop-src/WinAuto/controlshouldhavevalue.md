---
title: ControlShouldHaveValue
description: ControlShouldHaveValue
ms.assetid: 90C37CC5-21D2-4D26-B6D9-2C95C52127BF
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1c6ced460fac38552e0b82396e6bbbcf92e90c341e40b289e332a3f188c7e4ce
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119998741"
---
# <a name="controlshouldhavevalue"></a>ControlShouldHaveValue

## <a name="text"></a>Testo

Un controllo con ruolo di {0} deve avere un valore, ma get \_ accValue non è implementato

## <a name="type"></a>Tipo

Errore

## <a name="description"></a>Descrizione

Un elemento non fornisce un valore come previsto in base al ruolo MSAA assegnato, implicando che per l'elemento non è implementato il metodo [**\_ get accValue.**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accvalue) Ad esempio, i ruoli MSAA seguenti devono fornire tutti un valore.

-   CASELLA \_ COMBINATA SISTEMA \_ RUOLO
-   INDIRIZZO \_ IP DEL SISTEMA DEL \_ RUOLO
-   COLLEGAMENTO \_ AL SISTEMA DEL \_ RUOLO
-   ROLE \_ SYSTEM \_ OUTLINEITEM
-   BARRA DI \_ STATO DEL SISTEMA DEL \_ RUOLO
-   DISPOSITIVO DI \_ SCORRIMENTO DEL SISTEMA \_ RUOLO
-   SPINBUTTON \_ DEL \_ SISTEMA DI RUOLI
-   BARRA \_ DI SCORRIMENTO \_ DEL SISTEMA RUOLO
-   TESTO \_ DEL SISTEMA DEL \_ RUOLO

Questo problema è un problema per gli utenti che si affidano a un'utilità per la lettura dello schermo e a una tastiera per la navigazione perché un elemento con un valore intrinseco deve essere in grado di segnalare tale valore a un utente.

## <a name="possible-causes"></a>Possibili cause

L'elemento o il relativo elemento padre ha un ruolo MSAA impostato in modo non appropriato.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**IAccessible::get \_ accRole**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accrole)
</dt> <dt>

[**Ruoli degli oggetti**](object-roles.md)
</dt> </dl>

 

 




