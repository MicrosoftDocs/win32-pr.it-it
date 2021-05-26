---
title: Gestione degli errori COM in Java e Visual Basic
description: Gestione degli errori COM in Java e Visual Basic
ms.assetid: 1130a038-3c18-4530-a6d7-9f538352297f
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 11c55c1c2414c69ff9398845858baadebd58cbf9
ms.sourcegitcommit: 0f7a8198bacd5493ab1e78a9583c7a3578794765
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 05/25/2021
ms.locfileid: "110424011"
---
# <a name="com-error-handling-in-java-and-visual-basic"></a>Gestione degli errori COM in Java e Visual Basic

Esistono tre interfacce e tre funzioni che possono essere usate in COM per fornire la gestione degli errori durante la programmazione in Java o Microsoft Visual Basic. In Java e Visual Basic, la chiamata al metodo non restituisce **un HRESULT** come valore restituito. Questi linguaggi usano invece le interfacce e le funzioni COM per ottenere **valori HRESULT** e per gestire errori o eccezioni. Le eccezioni sono eventi oltre il controllo del programma, ad esempio problemi di file o parametri non validi.

Le tre interfacce che forniscono supporto per **HRESULT** sono elencate e descritte brevemente nella tabella seguente.



|  Interfaccia                                                                        |  Descrizione                                                                                                                    |
|--------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------|
| [**ICreateErrorInfo**](/windows/win32/api/oaidl/nn-oaidl-icreateerrorinfo)<br/>  | Imposta le informazioni sull'errore.<br/>                                                                                   |
| [**IErrorInfo**](/windows/win32/api/oaidl/nn-oaidl-ierrorinfo)<br/>        | Restituisce informazioni da un oggetto errore.<br/>                                                                 |
| [**ISupportErrorInfo**](/windows/win32/api/oaidl/nn-oaidl-isupporterrorinfo)<br/> | Identifica l'oggetto come supporto [**dell'interfaccia IErrorInfo.**](/windows/win32/api/oaidl/nn-oaidl-ierrorinfo)<br/> |



 

Le tre funzioni che forniscono supporto per **HRESULT** sono elencate e descritte brevemente nella tabella seguente.



|    Interfaccia       |       Descrizione       |
|------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**CreateErrorInfo**](/windows/win32/api/oleauto/nf-oleauto-createerrorinfo)<br/> | Crea un'istanza di un oggetto errore generico.<br/>                                                                                                            |
| [**GetErrorInfo**](/windows/win32/api/oleauto/nf-oleauto-geterrorinfo)<br/>    | Ottiene il puntatore alle informazioni sull'errore impostato dalla chiamata precedente [**a SetErrorInfo**](/windows/win32/api/oleauto/nf-oleauto-seterrorinfo) nel thread logico corrente.<br/> |
| [**Seterrorinfo**](/windows/win32/api/oleauto/nf-oleauto-seterrorinfo)<br/>    | Imposta l'oggetto informazioni sull'errore per il thread di esecuzione corrente.<br/>                                                                                    |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Gestione degli errori in COM](error-handling-in-com.md)
</dt> </dl>

 

