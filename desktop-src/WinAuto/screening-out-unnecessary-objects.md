---
title: Screening degli oggetti non necessari
description: Se si usa Inspect per esaminare un controllo semplice, ad esempio un pulsante OK, nell'accessorio Microsoft WordPad, è possibile vedere che questi oggetti finestra padre contengono anche diversi oggetti figlio invisibili.
ms.assetid: 30884e11-cc73-4bb8-9d9e-b9f1b53c4193
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2c52dc54f2c32be3aff3e535427668943cf1ee21423636e3be8c018f6e3257b2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117745284"
---
# <a name="screening-out-unnecessary-objects"></a>Screening degli oggetti non necessari

Se si usa [Inspect](inspect-objects.md) per esaminare un controllo semplice, ad esempio un pulsante OK, nell'accessorio Microsoft WordPad, è possibile vedere che anche questi oggetti finestra padre contengono diversi oggetti figlio invisibili. Questi oggetti invisibili hanno lo stesso nome della classe finestra del controllo e hanno la [proprietà State](state-property.md) di STATE [**SYSTEM \_ \_ INVISIBLE**](object-state-constants.md). Nella tabella seguente sono elencati gli oggetti figlio invisibili creati Microsoft Active Accessibility per il controllo .



| Nome          | Ruolo                                                                  | ChildCount |
|---------------|-----------------------------------------------------------------------|------------|
| "System"      | [**BARRA \_ DEI MENU DEL SISTEMA DEI \_ RUOLI**](object-roles.md)     | 0          |
| nessuno          | [**BARRA \_ DEL TITOLO DEL SISTEMA DI \_ RUOLI**](object-roles.md)   | 5          |
| "Applicazione" | [**BARRA \_ DEI MENU DEL SISTEMA DEI \_ RUOLI**](object-roles.md)     | 0          |
| "Verticale"    | [**BARRA \_ DI SCORRIMENTO \_ DEL SISTEMA RUOLO**](object-roles.md) | 5          |
| "Orizzontale"  | [**BARRA \_ DI SCORRIMENTO \_ DEL SISTEMA RUOLO**](object-roles.md) | 5          |
| "Size Box"    | [**CONTROLLO \_ DEL SISTEMA DEI \_ RUOLI**](object-roles.md)           | 0          |



 

Gli sviluppatori client devono identificare e filtrare questi oggetti finestra padre e gli oggetti figlio invisibili perché non forniscono informazioni significative agli utenti finali.

 

 




