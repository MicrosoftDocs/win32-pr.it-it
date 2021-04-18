---
description: In questa sezione vengono descritte le proprietà della finestra. Una proprietà della finestra è qualsiasi dato assegnato a una finestra.
ms.assetid: vs|winui|~\winui\windowsuserinterface\windowing\windowproperties.htm
title: Proprietà finestra
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 87a06be9fca67dedeb98afd7a56638622dabc858
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106312473"
---
# <a name="window-properties"></a>Proprietà finestra

Una proprietà della finestra è qualsiasi dato assegnato a una finestra. Una proprietà della finestra è in genere un handle dei dati specifici della finestra, ma può essere qualsiasi valore. Ogni proprietà della finestra è identificata da un nome di stringa.

### <a name="in-this-section"></a>Contenuto della sezione



| Nome                                                       | Descrizione                                                                               |
|------------------------------------------------------------|-------------------------------------------------------------------------------------------|
| [Informazioni sulle proprietà della finestra](about-window-properties.md)     | Vengono illustrate le proprietà della finestra.<br/>                                                   |
| [Uso delle proprietà della finestra](using-window-properties.md)     | Viene illustrato come eseguire le attività seguenti associate alle proprietà della finestra.<br/> |
| [Riferimento alle proprietà della finestra](window-property-reference.md) | Contiene il riferimento all'API.<br/>                                                    |



 

### <a name="window-property-functions"></a>Funzioni di proprietà della finestra



| Nome                                   | Descrizione                                                                                                                                                                                                                                                                                                                                                       |
|----------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**EnumProps**](/windows/win32/api/winuser/nf-winuser-enumpropsa)         | Enumera tutte le voci nell'elenco di proprietà di una finestra passandole, una alla volta, alla funzione di callback specificata. [**EnumProps**](/windows/win32/api/winuser/nf-winuser-enumpropsa) continua fino a quando non viene enumerata l'ultima voce o la funzione di callback restituisce **false**.<br/>                                                                                                        |
| [**EnumPropsEx**](/windows/win32/api/winuser/nf-winuser-enumpropsexa)     | Enumera tutte le voci nell'elenco di proprietà di una finestra passandole, una alla volta, alla funzione di callback specificata. [**EnumPropsEx**](/windows/win32/api/winuser/nf-winuser-enumpropsexa) continua fino a quando non viene enumerata l'ultima voce o la funzione di callback restituisce **false**. <br/>                                                                                                  |
| [**GetProp**](/windows/win32/api/winuser/nf-winuser-getpropa)             | Recupera un handle di dati dall'elenco di proprietà della finestra specificata. La stringa di caratteri identifica l'handle da recuperare. La stringa e l'handle devono essere stati aggiunti all'elenco di proprietà da una chiamata precedente alla funzione [**seprop**](/windows/win32/api/winuser/nf-winuser-setpropa) . <br/>                                                                                    |
| [*PropEnumProc*](/windows/win32/api/winuser/nc-winuser-propenumproca)     | Funzione di callback definita dall'applicazione utilizzata con la funzione [**EnumProps**](/windows/win32/api/winuser/nf-winuser-enumpropsa) . La funzione riceve le voci di proprietà dall'elenco di proprietà di una finestra. Il tipo **PROPENUMPROC** definisce un puntatore a questa funzione di callback. [*PropEnumProc*](/windows/win32/api/winuser/nc-winuser-propenumproca) è un segnaposto per il nome della funzione definita dall'applicazione. <br/>           |
| [*PropEnumProcEx*](/windows/win32/api/winuser/nc-winuser-propenumprocexa) | Funzione di callback definita dall'applicazione utilizzata con la funzione [**EnumPropsEx**](/windows/win32/api/winuser/nf-winuser-enumpropsexa) . La funzione riceve le voci di proprietà dall'elenco di proprietà di una finestra. Il tipo **PROPENUMPROCEX** definisce un puntatore a questa funzione di callback. [*PropEnumProcEx*](/windows/win32/api/winuser/nc-winuser-propenumprocexa) è un segnaposto per il nome della funzione definita dall'applicazione. <br/> |
| [**RemoveProp**](/windows/win32/api/winuser/nf-winuser-removepropa)       | Rimuove una voce dall'elenco di proprietà della finestra specificata. La stringa di caratteri specificata identifica la voce da rimuovere.<br/>                                                                                                                                                                                                                    |
| [**SetProp**](/windows/win32/api/winuser/nf-winuser-setpropa)             | Aggiunge una nuova voce o modifica una voce esistente nell'elenco di proprietà della finestra specificata. La funzione aggiunge una nuova voce all'elenco se la stringa di caratteri specificata non esiste già nell'elenco. La nuova voce contiene la stringa e l'handle. In caso contrario, la funzione sostituisce l'handle corrente della stringa con l'handle specificato. <br/> |



 

 

 
