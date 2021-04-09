---
description: Il database del prodotto contiene informazioni su un prodotto. Per ulteriori informazioni su come ottenere informazioni sui prodotti con funzioni di enumerazione, vedere Inizializzazione di un'applicazione.
ms.assetid: 528c915c-296c-4620-8105-0b5d543e56a5
title: Recupero delle informazioni sull'applicazione
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f2dce842f057efb65b6d0db3ad0407a19bf08435
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103967021"
---
# <a name="getting-application-information"></a>Recupero delle informazioni sull'applicazione

Il database del prodotto contiene informazioni su un prodotto. Per ulteriori informazioni su come ottenere informazioni sui prodotti con funzioni di enumerazione, vedere [inizializzazione di un'applicazione](initializing-an-application.md).

**Per ottenere informazioni sul prodotto**

1.  Verificare che un prodotto sia installato chiamando la funzione [**MsiQueryProductState**](/windows/desktop/api/Msi/nf-msi-msiqueryproductstatea) .
2.  Aprire il database e ottenere un handle per esso chiamando la funzione [**MsiOpenProduct**](/windows/desktop/api/Msi/nf-msi-msiopenproducta) .

    Se il database è incluso in un pacchetto di installazione, chiamare la funzione [**MsiOpenPackage**](/windows/desktop/api/Msi/nf-msi-msiopenpackagea) .

3.  Utilizzare l'handle aperto per ottenere le proprietà del prodotto con la funzione [**MsiGetProductProperty**](/windows/desktop/api/Msi/nf-msi-msigetproductpropertya) e per ottenere informazioni descrittive sulle funzionalità con la funzione [**MsiGetFeatureInfo**](/windows/desktop/api/Msi/nf-msi-msigetfeatureinfoa) .

    Se si desidera ottenere informazioni sul prodotto utilizzando il codice del prodotto, anziché utilizzare l'handle di database aperto, chiamare la funzione [**MsiGetProductInfo**](/windows/desktop/api/Msi/nf-msi-msigetproductinfoa) anziché [**MsiGetProductProperty**](/windows/desktop/api/Msi/nf-msi-msigetproductpropertya).

4.  Chiudere un handle di installazione aperto chiamando la funzione [**MsiCloseHandle**](/windows/desktop/api/Msi/nf-msi-msiclosehandle) .

    La funzione [**MsiCloseAllHandles**](/windows/desktop/api/Msi/nf-msi-msicloseallhandles) è una funzione di diagnostica e non deve essere usata per chiudere gli handle che si sa essere aperti. È accettabile chiamare la funzione **MsiCloseAllHandles** quando l'applicazione viene chiusa per assicurarsi che tutti gli handle siano stati chiusi.

 

 



