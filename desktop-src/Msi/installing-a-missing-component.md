---
description: È possibile usare il Windows installer per rilevare i componenti o i file mancanti e quindi reinstallare le funzionalità che contengono i componenti mancanti.
ms.assetid: b197c9d0-fcc2-4ca7-a870-e1af82343455
title: Installazione di un componente mancante
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2e788cad738d46d35a7ac0948be2e2e2d6ede4347eec424fb24cf17571e3a59f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119828791"
---
# <a name="installing-a-missing-component"></a>Installazione di un componente mancante

È possibile usare il Windows installer per rilevare i componenti o i file mancanti e quindi reinstallare le funzionalità che contengono i componenti mancanti. Poiché il programma di installazione installa le funzionalità e non i componenti, deve prima risolvere il componente a cui appartiene un file mancante e quindi installare la funzionalità che contiene il componente. Se al componente sono collegate più funzionalità, il programma di installazione installa la funzionalità che richiede meno spazio su disco.

Se si chiama [**MsiGetComponentPath,**](/windows/desktop/api/Msi/nf-msi-msigetcomponentpatha)è possibile verificare che il file di chiave di un componente sia presente. Tuttavia, è comunque possibile che altri file appartenenti al componente siano mancanti. In questo scenario, chiamare [**MsiInstallMissingFile**](/windows/desktop/api/Msi/nf-msi-msiinstallmissingfilea). Il programma di installazione risolve quindi il componente a cui appartiene il file e installa la funzionalità collegata al componente che richiede meno spazio su disco.

Se la [**funzione MsiGetComponentPath**](/windows/desktop/api/Msi/nf-msi-msigetcomponentpatha) ha esito negativo in modo imprevisto, è necessario installare i componenti mancanti.

La procedura seguente illustra come installare i componenti mancanti.

**Per rilevare e installare un componente mancante**

1.  Chiamare [**MsiGetComponentPath**](/windows/desktop/api/Msi/nf-msi-msigetcomponentpatha) per verificare che il file di chiave di un componente sia presente. Tuttavia, anche se il file di chiave del componente è presente, è comunque possibile che altri file appartenenti al componente siano mancanti.
2.  Chiamare la [**funzione MsiInstallMissingComponent**](/windows/desktop/api/Msi/nf-msi-msiinstallmissingcomponenta) se la funzionalità associata al componente è sconosciuta.
3.  Chiamare la [**funzione MsiConfigureFeature**](/windows/desktop/api/Msi/nf-msi-msiconfigurefeaturea) o [**MsiProvideComponent**](/windows/desktop/api/Msi/nf-msi-msiprovidecomponenta) se la funzionalità associata al componente è nota.
4.  Chiamare [**MsiInstallMissingFile**](/windows/desktop/api/Msi/nf-msi-msiinstallmissingfilea) se un'applicazione non è in grado di aprire un file.

 

 



