---
title: Restituzione di informazioni sull'errore
description: Restituzione di informazioni sull'errore
ms.assetid: 4206f2e5-db01-458c-93cb-10c5cd4a4536
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 303db82dc220d09d4db7f52bf4c04ad1e5ca691f
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/21/2020
ms.locfileid: "104399750"
---
# <a name="returning-error-information"></a>Restituzione di informazioni sull'errore

Utilizzando le interfacce e le funzioni di gestione degli errori COM, è possibile restituire informazioni sugli errori eseguendo i passaggi seguenti:

1.  Implementare l'interfaccia [**ISupportErrorInfo**](/windows/win32/api/oaidl/nn-oaidl-isupporterrorinfo) .
2.  Per creare un'istanza dell'oggetto errore generico, chiamare la funzione [**CreateErrorInfo**](/windows/win32/api/oleauto/nf-oleauto-createerrorinfo) .
3.  Per impostarne il contenuto, usare i metodi [**ICreateErrorInfo**](/windows/win32/api/oaidl/nn-oaidl-icreateerrorinfo) .
4.  Per associare l'oggetto Error al thread logico corrente, chiamare la funzione [**SetErrorInfo**](/windows/win32/api/oleauto/nf-oleauto-seterrorinfo) .

Le interfacce di gestione degli errori creano e gestiscono un oggetto Error, che fornisce informazioni sull'errore. L'oggetto Error non è uguale all'oggetto che ha rilevato l'errore. Si tratta di un oggetto separato associato al thread di esecuzione corrente.

 

 