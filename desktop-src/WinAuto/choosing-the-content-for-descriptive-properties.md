---
title: Scelta del contenuto per le proprietà descrittive
description: Mentre il contenuto di alcune proprietà è specifico, il contenuto per altre proprietà è costituito da testo descrittivo che viene fornito dallo sviluppatore del server.
ms.assetid: 3f399451-e9c5-4901-9b6e-198aa0c2deab
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5215a6592d11272223654184340c4df8b299b88edb5b5f4addbd2c8d4712ab74
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120071851"
---
# <a name="choosing-the-content-for-descriptive-properties"></a>Scelta del contenuto per le proprietà descrittive

Mentre il contenuto di alcune proprietà è specifico, il contenuto per altre proprietà è costituito da testo descrittivo che viene fornito dallo sviluppatore del server. Inoltre, il tipo di informazioni per ogni proprietà varia a seconda dell'oggetto. Nella tabella seguente vengono forniti suggerimenti per la scelta del contenuto di queste proprietà descrittive.



| Proprietà                                        | Suggerimento del contenuto                                                                                                                                                                                                                                                    |
|-------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Nome**](name-property.md)                   | Etichetta che descrive e identifica brevemente l'oggetto all'interno del relativo contenitore, ad esempio il testo in un pulsante di comando, il nome di una voce di menu o un'etichetta visualizzata accanto a un controllo di modifica.                                                                              |
| [**Defaultaction**](defaultaction-property.md) | Interazione predefinita con l'oggetto . La stringa restituita da questa proprietà è un singolo verbo, ad esempio "Press" per un pulsante della barra degli strumenti, o una breve frase che inizia con un verbo.                                                                               |
| [**Valore**](value-property.md)                 | Informazioni contenute nell'oggetto , ad esempio il testo in un controllo di modifica o il nome file di un collegamento HTML. Il contenuto della [**proprietà Value**](value-property.md) può cambiare, mentre il contenuto della [**proprietà Name**](name-property.md) non cambia. |
| [**Descrizione**](description-property.md)     | Descrive l'aspetto dell'oggetto.                                                                                                                                                                                                                                    |
| [**Help**](help-property.md)                   | Informazioni sullo stile della descrizione comando o del fumetto usate per descrivere le funzionalità dell'oggetto o come usarlo.                                                                                                                                                                   |
| [**Argomento della Guida**](helptopic-property.md)         | Identificatore di contesto di un [argomento WinHelp](/windows/win32/api/winuser/nf-winuser-winhelpa) che documenta l'oggetto .                                                                                                                                                 |



 

Usare uno dei valori predefiniti del ruolo [oggetto](object-roles.md) per [**Role**](role-property.md) e la combinazione appropriata di costanti di stato [dell'oggetto](object-state-constants.md) per [**State.**](state-property.md)

Il contenuto delle proprietà per i controlli personalizzati deve corrispondere al contenuto delle proprietà per i controlli forniti dal sistema emulati dai controlli personalizzati. Per informazioni sulle proprietà supportate dai controlli forniti dal sistema, vedere [Appendix A: Supported Interfaccia utente Elements Reference](appendix-a--supported-user-interface-elements-reference.md).

 

 