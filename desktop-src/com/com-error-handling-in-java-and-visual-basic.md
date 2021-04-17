---
title: Gestione degli errori COM in Java e Visual Basic
description: Gestione degli errori COM in Java e Visual Basic
ms.assetid: 1130a038-3c18-4530-a6d7-9f538352297f
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ea12dc040218e14098ce2394fbb5cd2ebeff1704
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/21/2020
ms.locfileid: "104399774"
---
# <a name="com-error-handling-in-java-and-visual-basic"></a>Gestione degli errori COM in Java e Visual Basic

Sono disponibili tre interfacce e tre funzioni che possono essere utilizzate in COM per fornire la gestione degli errori durante la programmazione in Java o Microsoft Visual Basic. In Java e Visual Basic la chiamata al metodo non restituisce **HRESULT** come valore restituito. Al contrario, questi linguaggi utilizzano le interfacce COM e le funzioni per ottenere i valori **HRESULT** e per gestire gli errori o le eccezioni. (Le eccezioni sono eventi oltre il controllo del programma, ad esempio problemi di file o parametri non validi).

Le tre interfacce che forniscono supporto per **HRESULT** s sono elencate e descritte brevemente nella tabella seguente.



|                                                                          |                                                                                                                      |
|--------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------|
| [**ICreateErrorInfo**](/windows/win32/api/oaidl/nn-oaidl-icreateerrorinfo)<br/>  | Imposta le informazioni sull'errore.<br/>                                                                                   |
| [**IErrorInfo**](/windows/win32/api/oaidl/nn-oaidl-ierrorinfo)<br/>        | Restituisce informazioni da un oggetto Error.<br/>                                                                 |
| [**ISupportErrorInfo**](/windows/win32/api/oaidl/nn-oaidl-isupporterrorinfo)<br/> | Identifica l'oggetto come supporto dell'interfaccia [**IErrorInfo**](/windows/win32/api/oaidl/nn-oaidl-ierrorinfo) .<br/> |



 

Le tre funzioni che forniscono supporto per **HRESULT** s sono elencate e descritte brevemente nella tabella seguente.



|                                                                        |                                                                                                                                                                      |
|------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**CreateErrorInfo**](/windows/win32/api/oleauto/nf-oleauto-createerrorinfo)<br/> | Crea un'istanza di un oggetto errore generico.<br/>                                                                                                            |
| [**GetErrorInfo**](/windows/win32/api/oleauto/nf-oleauto-geterrorinfo)<br/>    | Ottiene il puntatore alle informazioni sull'errore impostato dalla chiamata precedente a [**SetErrorInfo**](/windows/win32/api/oleauto/nf-oleauto-seterrorinfo) nel thread logico corrente.<br/> |
| [**SetErrorInfo**](/windows/win32/api/oleauto/nf-oleauto-seterrorinfo)<br/>    | Imposta l'oggetto informazioni sull'errore per il thread di esecuzione corrente.<br/>                                                                                    |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Gestione degli errori in COM](error-handling-in-com.md)
</dt> </dl>

 

