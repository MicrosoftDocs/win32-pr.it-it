---
title: Gestione degli errori degli oggetti servizio
description: Quando si verifica un errore in un oggetto servizio, il valore restituito per la chiamata IDispatch Invoke deve essere DISP E EXCEPTION e il puntatore al parametro \_ pExceptInfo a una struttura EXCEPTINFO in deve \_ essere compilato.
ms.assetid: 1b08c404-69f2-4b0d-9231-c2bd242e124d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 17c98db4ffdb3c4625ec4c0dfbe3d497ab1cbe4b5152b172c34422c1630ce581
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118999521"
---
# <a name="service-object-error-handling"></a>Gestione degli errori degli oggetti servizio

Quando si verifica un errore in un oggetto servizio, il valore restituito per la chiamata [**IDispatch::Invoke**](/windows/win32/api/oaidl/nf-oaidl-idispatch-invoke) deve essere DISP E EXCEPTION e il puntatore al parametro \_ \_ *pExceptInfo* a una struttura [**EXCEPTINFO**](/windows/win32/api/oaidl/ns-oaidl-excepinfo) in deve essere compilato.

In particolare, i **membri bstrSource** e **bstrDescription** della struttura [**EXCEPTINFO**](/windows/win32/api/oaidl/ns-oaidl-excepinfo) vengono usati dall'host del dispositivo con la tecnologia UPnP per creare una risposta di errore UPnP. **bstrSource è** il codice di errore e **bstrDescription** è la descrizione dell'errore.

 

 