---
description: È possibile installare interi prodotti con funzioni Windows Installer. Nei passaggi seguenti viene descritto come installare un prodotto.
ms.assetid: 03cc7abc-63bd-4a01-a05c-9f7928de8827
title: Installazione di un'applicazione
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8cf312e7394c4fcbca699f6e032e315a42356c1f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106317129"
---
# <a name="installing-an-application"></a>Installazione di un'applicazione

È possibile installare interi prodotti con funzioni Windows Installer. Nei passaggi seguenti viene descritto come installare un prodotto.

**Per installare un prodotto**

1.  Eseguire un prodotto tramite la sequenza di installazione o disinstallazione chiamando la funzione [**MsiInstallProduct**](/windows/desktop/api/Msi/nf-msi-msiinstallproducta) .
2.  Specificare il livello di installazione chiamando la funzione [**MsiConfigureProduct**](/windows/desktop/api/Msi/nf-msi-msiconfigureproducta) .

    Per impostare lo stato di installazione, è possibile usare i parametri della funzione [**MsiConfigureProduct**](/windows/desktop/api/Msi/nf-msi-msiconfigureproducta) . Ad esempio, è possibile impostare lo stato su Installa localmente o per eseguire l'installazione dall'origine. È possibile impostare l'intervallo di funzionalità del prodotto da includere impostando il livello.

Per ulteriori informazioni sull'installazione di un'applicazione, vedere la pagina relativa al meccanismo di [resilienza](resiliency.md) e [installazione](installation-mechanism.md).

 

 



