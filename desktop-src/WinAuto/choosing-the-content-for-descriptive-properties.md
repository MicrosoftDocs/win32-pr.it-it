---
title: Scelta del contenuto per le proprietà descrittive
description: Sebbene il contenuto di alcune proprietà sia specifico, il contenuto di altre proprietà è costituito da un testo descrittivo che rimane disponibile allo sviluppatore del server.
ms.assetid: 3f399451-e9c5-4901-9b6e-198aa0c2deab
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8b77860eaefeb4e371c69fdf6acd205c77d763c3
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "103729962"
---
# <a name="choosing-the-content-for-descriptive-properties"></a>Scelta del contenuto per le proprietà descrittive

Sebbene il contenuto di alcune proprietà sia specifico, il contenuto di altre proprietà è costituito da un testo descrittivo che rimane disponibile allo sviluppatore del server. Inoltre, il tipo di informazioni per ogni proprietà varia a seconda dell'oggetto. Nella tabella seguente vengono forniti suggerimenti per la scelta del contenuto di queste proprietà descrittive.



| Proprietà                                        | Suggerimenti sul contenuto                                                                                                                                                                                                                                                    |
|-------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Nome**](name-property.md)                   | Etichetta che descrive brevemente e identifica l'oggetto all'interno del contenitore, ad esempio il testo in un pulsante di push, il nome di una voce di menu o un'etichetta visualizzata accanto a un controllo di modifica.                                                                              |
| [**DefaultAction**](defaultaction-property.md) | Interazione predefinita con l'oggetto. La stringa restituita da questa proprietà è un singolo verbo, ad esempio "premere" per un pulsante della barra degli strumenti o una breve frase che inizia con un verbo.                                                                               |
| [**Valore**](value-property.md)                 | Informazioni contenute nell'oggetto, ad esempio il testo in un controllo di modifica o il nome file di un collegamento HTML. Il contenuto della proprietà [**value**](value-property.md) può essere modificato, mentre il contenuto della proprietà [**Name**](name-property.md) non viene modificato. |
| [**Descrizione**](description-property.md)     | Descrive l'aspetto dell'oggetto.                                                                                                                                                                                                                                    |
| [**Help**](help-property.md)                   | Descrizione comando o informazioni di tipo Balloon utilizzate per descrivere le operazioni svolte dall'oggetto o come utilizzarlo.                                                                                                                                                                   |
| [**HelpTopic**](helptopic-property.md)         | Identificatore di contesto di un argomento [WinHelp](/windows/win32/api/winuser/nf-winuser-winhelpa) che documenta l'oggetto.                                                                                                                                                 |



 

Usare uno dei valori predefiniti del [ruolo oggetto](object-roles.md) per il [**ruolo**](role-property.md) e la combinazione appropriata di [costanti di stato dell'oggetto](object-state-constants.md) per lo [**stato**](state-property.md).

Il contenuto delle proprietà dei controlli personalizzati deve corrispondere al contenuto delle proprietà dei controlli forniti dal sistema che i controlli personalizzati emulano. Per informazioni sulle proprietà supportate dai controlli forniti dal sistema, vedere [Appendice A: riferimenti agli elementi dell'interfaccia utente supportati](appendix-a--supported-user-interface-elements-reference.md).

 

 