---
title: Restituzione di informazioni sugli errori
description: Restituzione di informazioni sugli errori
ms.assetid: 4206f2e5-db01-458c-93cb-10c5cd4a4536
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 545c697be7da64362ecce0f5b4c45272832ad682d8b4dd0eb5234620b993e5f3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118309643"
---
# <a name="returning-error-information"></a>Restituzione di informazioni sugli errori

Usando le interfacce e le funzioni di gestione degli errori COM, è possibile restituire informazioni sugli errori eseguendo la procedura seguente:

1.  Implementare [**l'interfaccia ISupportErrorInfo.**](/windows/win32/api/oaidl/nn-oaidl-isupporterrorinfo)
2.  Per creare un'istanza dell'oggetto errore generico, chiamare la [**funzione CreateErrorInfo.**](/windows/win32/api/oleauto/nf-oleauto-createerrorinfo)
3.  Per impostarne il contenuto, usare i [**metodi ICreateErrorInfo.**](/windows/win32/api/oaidl/nn-oaidl-icreateerrorinfo)
4.  Per associare l'oggetto errore al thread logico corrente, chiamare la [**funzione SetErrorInfo.**](/windows/win32/api/oleauto/nf-oleauto-seterrorinfo)

Le interfacce di gestione degli errori creano e gestiscono un oggetto errore, che fornisce informazioni sull'errore. L'oggetto errore non corrisponde all'oggetto che ha rilevato l'errore. Si tratta di un oggetto separato associato al thread di esecuzione corrente.

 

 