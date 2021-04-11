---
title: Gestione degli errori degli oggetti servizio
description: Quando si verifica un errore in un oggetto servizio, il valore restituito per la chiamata IDispatch Invoke deve essere DISP \_ E \_ Exception e il puntatore al parametro pExceptInfo a una struttura EXCEPTINFO in deve essere compilato.
ms.assetid: 1b08c404-69f2-4b0d-9231-c2bd242e124d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8fd39d08dc7ca5152ca412df1a6fb67d6df524f2
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104117910"
---
# <a name="service-object-error-handling"></a>Gestione degli errori degli oggetti servizio

Quando si verifica un errore in un oggetto servizio, il valore restituito per la chiamata [**IDispatch:: Invoke**](/windows/win32/api/oaidl/nf-oaidl-idispatch-invoke) deve essere disp \_ e \_ l'eccezione e il puntatore al parametro *pExceptInfo* a una struttura [**EXCEPTINFO**](/windows/win32/api/oaidl/ns-oaidl-excepinfo) in devono essere compilati.

In particolare, i membri **bstrSource** e **BstrDescription** della struttura [**EXCEPTINFO**](/windows/win32/api/oaidl/ns-oaidl-excepinfo) vengono utilizzati dall'host del dispositivo con la tecnologia UPnP per creare una risposta di errore UPnP. **bstrSource** è il codice di errore e **bstrDescription** è la descrizione dell'errore.

 

 