---
description: È possibile utilizzare il Windows Installer per rilevare i componenti o i file mancanti, quindi reinstallare le funzionalità che contengono i componenti mancanti.
ms.assetid: b197c9d0-fcc2-4ca7-a870-e1af82343455
title: Installazione di un componente mancante
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c9bbfd38517e850a7f4e83c9c84075d92fea2290
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106310972"
---
# <a name="installing-a-missing-component"></a>Installazione di un componente mancante

È possibile utilizzare il Windows Installer per rilevare i componenti o i file mancanti, quindi reinstallare le funzionalità che contengono i componenti mancanti. Poiché il programma di installazione installa le funzionalità e non i componenti, è necessario innanzitutto risolvere il componente a cui appartiene un file mancante, quindi installare la funzionalità che contiene il componente. Se più di una funzionalità è collegata al componente, il programma di installazione installa la funzionalità che richiede lo spazio su disco minimo.

Se si chiama [**MsiGetComponentPath**](/windows/desktop/api/Msi/nf-msi-msigetcomponentpatha), è possibile verificare che il file di chiave di un componente sia presente. Tuttavia, è comunque possibile che altri file appartenenti al componente siano mancanti. In questo scenario, chiamare [**MsiInstallMissingFile**](/windows/desktop/api/Msi/nf-msi-msiinstallmissingfilea). Il programma di installazione risolve quindi il componente a cui appartiene il file e installa la funzionalità collegata al componente che richiede lo spazio minimo su disco.

Se la funzione [**MsiGetComponentPath**](/windows/desktop/api/Msi/nf-msi-msigetcomponentpatha) non riesce in modo imprevisto, è necessario installare tutti i componenti mancanti.

Nella procedura seguente viene illustrato come installare i componenti mancanti.

**Per rilevare e installare un componente mancante**

1.  Chiamare [**MsiGetComponentPath**](/windows/desktop/api/Msi/nf-msi-msigetcomponentpatha) per verificare che il file di chiave di un componente sia presente. Tuttavia, anche se il file di chiave del componente è presente, è comunque possibile che altri file appartenenti al componente siano mancanti.
2.  Chiamare la funzione [**MsiInstallMissingComponent**](/windows/desktop/api/Msi/nf-msi-msiinstallmissingcomponenta) se la funzionalità associata al componente è sconosciuta.
3.  Chiamare la funzione [**MsiConfigureFeature**](/windows/desktop/api/Msi/nf-msi-msiconfigurefeaturea) o [**MsiProvideComponent**](/windows/desktop/api/Msi/nf-msi-msiprovidecomponenta) se la funzionalità associata al componente è nota.
4.  Chiamare [**MsiInstallMissingFile**](/windows/desktop/api/Msi/nf-msi-msiinstallmissingfilea) se un'applicazione non è in grado di aprire un file.

 

 



