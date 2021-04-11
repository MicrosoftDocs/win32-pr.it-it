---
title: Recupero delle informazioni sugli errori
description: Recupero delle informazioni sugli errori
ms.assetid: 51a0e401-43f2-4738-9799-a96e2580a29f
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b6a5918ee7338d1b8428079da20ecb43c7b4b4ef
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/21/2020
ms.locfileid: "104047391"
---
# <a name="retrieving-error-information"></a>Recupero delle informazioni sugli errori

Utilizzando le interfacce e le funzioni di gestione degli errori COM, è possibile recuperare le informazioni sugli errori nel modo seguente:

1.  Controllare se il valore restituito rappresenta un errore che l'oggetto è pronto a gestire.
2.  Chiamare [**QueryInterface**](/windows/desktop/api/Unknwn/nf-unknwn-iunknown-queryinterface(q)) per ottenere un puntatore all'interfaccia [**ISupportErrorInfo**](/windows/win32/api/oaidl/nn-oaidl-isupporterrorinfo) . Chiamare quindi [**ISupportErrorInfo:: InterfaceSupportsErrorInfo**](/windows/win32/api/oaidl/nf-oaidl-isupporterrorinfo-interfacesupportserrorinfo) per verificare che l'errore sia stato generato dall'oggetto che lo ha restituito e che l'oggetto Error sia relativo all'errore corrente e non a una chiamata precedente.
3.  Per ottenere un puntatore all'oggetto Error, chiamare la funzione [**GetErrorInfo**](/windows/win32/api/oleauto/nf-oleauto-geterrorinfo) .
4.  Per recuperare informazioni dall'oggetto Error, usare i metodi [**IErrorInfo**](/windows/win32/api/oaidl/nn-oaidl-ierrorinfo) .

Se l'oggetto non è pronto per gestire l'errore, ma è necessario propagare le informazioni sugli errori ulteriormente nella catena di chiamate, è sufficiente passare il valore restituito al chiamante. Poiché la funzione [**GetErrorInfo**](/windows/win32/api/oleauto/nf-oleauto-geterrorinfo) Cancella le informazioni sull'errore e passa la proprietà dell'oggetto Error al chiamante, la funzione deve essere chiamata solo dall'oggetto che gestisce l'errore.

 

 