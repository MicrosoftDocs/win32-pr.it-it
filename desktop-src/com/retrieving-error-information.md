---
title: Recupero delle informazioni sugli errori
description: Recupero delle informazioni sugli errori
ms.assetid: 51a0e401-43f2-4738-9799-a96e2580a29f
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8e26844505b7c5de3e39c3199a6087c94f35bed9f64ef11a65d1c6df9a3dd4e9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118309653"
---
# <a name="retrieving-error-information"></a>Recupero delle informazioni sugli errori

Usando le interfacce e le funzioni di gestione degli errori COM, è possibile recuperare le informazioni sugli errori come indicato di seguito:

1.  Controllare se il valore restituito rappresenta un errore che l'oggetto è pronto per gestire.
2.  Chiamare [**QueryInterface**](/windows/desktop/api/Unknwn/nf-unknwn-iunknown-queryinterface(q)) per ottenere un puntatore [**all'interfaccia ISupportErrorInfo.**](/windows/win32/api/oaidl/nn-oaidl-isupporterrorinfo) Chiamare quindi [**ISupportErrorInfo::InterfaceSupportsErrorInfo**](/windows/win32/api/oaidl/nf-oaidl-isupporterrorinfo-interfacesupportserrorinfo) per verificare che l'errore sia stato generato dall'oggetto che lo ha restituito e che l'oggetto errore sia relativo all'errore corrente e non a una chiamata precedente.
3.  Per ottenere un puntatore all'oggetto error, chiamare la [**funzione GetErrorInfo.**](/windows/win32/api/oleauto/nf-oleauto-geterrorinfo)
4.  Per recuperare informazioni dall'oggetto errore, usare i [**metodi IErrorInfo.**](/windows/win32/api/oaidl/nn-oaidl-ierrorinfo)

Se l'oggetto non è pronto per gestire l'errore, ma deve propagare le informazioni sull'errore più avanti nella catena di chiamate, deve semplicemente passare il valore restituito al chiamante. Poiché la [**funzione GetErrorInfo**](/windows/win32/api/oleauto/nf-oleauto-geterrorinfo) cancella le informazioni sull'errore e passa la proprietà dell'oggetto errore al chiamante, la funzione deve essere chiamata solo dall'oggetto che gestisce l'errore.

 

 